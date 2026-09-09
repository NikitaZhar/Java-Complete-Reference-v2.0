# Повторный независимый аудит Chapter 4 и сравнение с первым аудитом

Дата: 2026-08-28  
Репозиторий: `Java-Complete-Reference-v2.0`  
Проверенный commit: `5fda6bb`  
Цель проекта: Java SE 25

## 1. Как обеспечивалась независимость прохода

Второй аудит не использовал список выводов первого отчёта как checklist.

Сначала заново построены четыре независимые карты:

1. normative obligations из JLS SE 25 §§4.1–4.12 и связанных §§15.1–15.3;
2. declared ownership из Working Contract и Матрицы владения темами;
3. фактическое содержание 33 файлов Ch4;
4. практический материал Boyarsky/Mughal 1Z0-829/830.

Дополнительно механически просмотрены 273 категоричных утверждения с маркерами «всегда», «никогда», «только», «любой», «ровно», «heap/stack», «тип/значение/подтип». После фиксации независимых findings они сравнены с первым отчётом `Точный аудит Chapter 4.md`.

Среда проверки: OpenJDK 21.0.11. Примеры, зависящие от Java SE 25 grammar/type rules, оценивались по JLS SE 25, а не по JDK 21.

## 2. Независимый итог без учёта первого отчёта

### 2.1 Что глава действительно покрывает хорошо

- восемь primitive types, ranges и default values;
- two's-complement intuition и silent overflow;
- basic numeric promotion consequences;
- `char` как UTF-16 code unit;
- основные NaN/infinity/signed-zero traps;
- primitive/reference distinction на уровне aliasing;
- static versus runtime type и dynamic dispatch;
- pass-by-value;
- null/default local-variable traps;
- final reference versus object mutability;
- basic local variable type inference;
- базовая nominal class/interface hierarchy и array covariance.

### 2.2 Независимо найденные P0/P1-проблемы

#### A. Ошибочная модель результата expression

`4.1.2` дважды утверждает, что каждое expression имеет тип и значение либо бросает exception. JLS §15.1 определяет три результата evaluation: variable, value или nothing. Вызов `void`-метода может normally complete и produce no value.

Это самая фундаментальная ошибка главы, потому что находится в определении value/expression.

#### B. Смешаны expression type, value compatibility и runtime class

Утверждение «значение всегда принадлежит ровно одному типу» не является аккуратной моделью Java. Нормативно:

- expression, которое denotes variable/value, имеет один compile-time type;
- stored/result value должно быть assignment-compatible с этим type, кроме heap pollution;
- reference value может denote объект более конкретного runtime class;
- один и тот же объект может наблюдаться через expressions разных static types.

Следовательно, уникальность следует приписывать compile-time type конкретного expression, а не «значению вообще».

#### C. Неверная taxonomy values

Class literal values выделены отдельной категорией рядом с primitive/reference/null. Но `String.class` и `int.class` производят reference values типа `Class<...>`. Отдельной категорией values они не являются.

Таблица «участие values в generics» тоже категориально неаккуратна: в type arguments участвуют types, а не values. Практический смысл строки понятен, но заголовок таблицы и формулировка смешивают уровни.

#### D. Language semantics смешана с предполагаемым memory layout

Файлы многократно обещают physical heap/stack/direct storage, machine-word alignment и lifetime «пока есть ссылки». Это не contract Java language.

Безопасная учебная модель:

- variable stores a primitive value либо reference value;
- assignment/call copies that value;
- copying reference value does not copy object;
- multiple references can denote the same object;
- physical placement/layout, scalar replacement, compressed references и GC roots принадлежат JVM implementation chapters.

Особенно проблемны утверждения:

- отдельный `short` field «обычно выравнивается до машинного слова»;
- `boolean` field/local «обычно занимает как int»;
- объект «живёт, пока на него есть ссылки»;
- тип определяет физическую форму runtime storage.

#### E. Subtyping section не соответствует собственному статусу owner

Раздел объявлен домом subtyping, но:

- сводит происхождение subtype к explicit `extends`/`implements`;
- не знает primitive subtyping;
- не определяет direct/proper/reflexive/transitive relations;
- почти не покрывает parameterized/raw/wildcard supertypes;
- не покрывает type variables/intersections;
- не даёт полных array supertypes;
- не упоминает LUB/type projections.

Фраза «Java nominal, subtype возникает только из extends/implements» допустима лишь с ограничителем «для class/interface declarations в базовом случае».

#### F. Variable taxonomy фактически неверна

Текст говорит «семь видов», перечисляет восемь и затем ставит pattern variables отдельно. JLS: восемь kinds; pattern variable — local variable declared by a pattern.

#### G. Type contexts раскрыты как список примеров, не как модель

`Where Types Are Used` пропускает большую часть правил JLS §4.11:

- wildcard restrictions;
- reifiable-only contexts;
- generic exception-type prohibitions;
- explicit type argument contexts;
- type annotations at different array dimensions;
- intersection of type/declaration contexts.

#### H. Generic forms слишком сильно «вырезаны» из Ch4

Полная generics theory справедливо принадлежит Ch20, но Ch4 использует и обязан определить boundary notions:

- type variable;
- parameterized type;
- erasure;
- reifiable type;
- raw type;
- intersection type.

Без них классификация reference types, type identity, type contexts и subtyping остаются логически незамкнутыми.

#### I. Variables/final/initialization/var покрыты только базово

Не хватает:

- primitive/reference variable runtime compatibility и heap pollution boundary;
- accurate creation/lifetime of eight variable kinds;
- blank final;
- constant variable versus merely final;
- final parameters/exception parameters;
- definite unassignment boundary;
- полного набора `var` restrictions.

### 2.3 Новые находки второго прохода

Эти пункты отсутствовали либо были недостаточно явно отмечены в первом отчёте.

#### N1. Неверное «only read» для `? extends`

Комментарий:

```java
List<? extends Object> ok = ls; // ковариантный wildcard, только чтение
```

— полезная мнемоника, но не точное правило. В такой list можно добавить `null`; также объект, полученный чтением, может быть mutable, а сама list может поддерживать remove/clear и другие structural operations, не требующие значения неизвестного element type.

Точная формула: нельзя safely add non-null value определённого типа, потому что captured element type неизвестен. «Только чтение» допустимо лишь как явно помеченное упрощение PECS.

#### N2. «Проверять NaN только через isNaN» слишком сильно

JLS прямо указывает, что `x != x` true iff `x` is NaN. `Double.isNaN`/`Float.isNaN` — наиболее читаемый API, но не единственный корректный способ. Слово «только» нужно заменить рекомендацией, а не запретом.

#### N3. Primitive `==` описано как «почти всегда ошибка»

Exact floating comparison имеет законные применения: проверка exact sentinels, zero, infinities, результаты операций с гарантированным exactness. Ошибка — ожидать математическое/decimal equality после inexact computation. Это уже не просто стилистика заголовка `Never compare`; формулировка повторяется в operations overview и float file.

#### N4. Универсальный epsilon объявлен «правильным» сравнением

`Math.abs(a-b) < 1e-9` не является универсально правильным:

- threshold зависит от масштаба/domain;
- subtraction может overflow;
- infinities дают NaN difference;
- NaN требует отдельной политики;
- рядом с нулём нужна absolute tolerance, вдали — relative/ULP-aware.

Нужна taxonomy strategies, а не один рецепт.

#### N5. Мотивация integer semantics выдана как установленный факт

Текст утверждает, что silent overflow выбран из-за цены проверки каждой операции и «скорости системного кода», а small-type promotion существует именно из-за JVM opcodes. Это правдоподобная engineering intuition, но не нормативный факт, подтверждённый приведёнными источниками.

Надо разделить:

- language rule;
- JVM mapping;
- возможную historical/design motivation, только с источником.

#### N6. `short`/`byte` memory advice слишком категоричен

Совет «экономия только в больших arrays» игнорирует implementation-dependent object layout, field packing, serialization/native formats и data-oriented layouts. Практический default `int` разумен, но обоснование нельзя строить на безусловном machine-word alignment.

#### N7. `var` typo подтверждена как реальная смысловая ошибка

`ArrayList<String>` позволяет добавлять `String`; текст говорит обратное. Вероятно, пропущено слово «не-String», но при статусе `done` это всё равно factual defect.

#### N8. `char` example не показывает обещанный Unicode escape

Строка:

```java
Unicode-escape 'A'
```

не демонстрирует escape syntax. Это не semantic error результата, но учебный пример не выполняет заявленную функцию. Журнал предыдущего аудита уже замечал это как косметику; статус `done` был оставлен без исправления.

#### N9. `int`/`short` performance claims требуют источника или удаления

Фразы «32-bit arithmetic не медленнее», «short field обычно machine word», «тип уже int физически из-за operand stack» зависят от target JVM/hardware/JIT. Part I может дать practical recommendation, но не универсальную performance guarantee.

#### N10. Helpful NPE представлен как гарантированно называющий local variable

Формулировка «прямо называют, какая именно ссылка была null» слишком широкая. Helpful NPE message зависит от bytecode/source expression и может описать access path, но не обязана всегда восстановить исходное local-variable name. Лучше: «часто указывает null-producing часть expression».

#### N11. Wrapper section — фиктивная structural node

`4.2.13` состоит из 13 строк и фактически является redirect в Ch5/Ch49. Отдельный numbered subsection создаёт ожидание собственного материала и искусственно раздувает structure. Pair mapping достаточно включить в primitive overview, а затем дать ссылки.

#### N12. Common pitfalls размножены на трёх уровнях

Есть Common Mistakes почти в каждом leaf file, `4.1.8 Common Pitfalls`, `4.2.15 ... Pitfalls` и `4.6 Common Mistakes`. Это приводит не только к повторению, но и к расхождениям формулировок (`NaN`, floating equality, wrappers). Нужна одна итоговая diagnostic layer плюс локальные ошибки только там, где они раскрывают новую границу.

## 3. Повторно сгенерированная структура

Структура построена после независимого findings list, до сравнения с первым отчётом.

### Chapter 4. Types, Values, Expressions, and Variables

**4.1 Type-System Guarantees and Their Boundaries**

- static/strong typing;
- type correctness versus runtime safety;
- unsafe/checked boundaries.

**4.2 Types, Values, Variables, Expressions, and Results**

- precise vocabulary;
- expression denotes variable/value/nothing;
- normal/abrupt completion;
- compile-time type, target type pointer to Ch5, runtime class;
- class literals as reference-valued expressions.

**4.3 Primitive Types and Values**

- one complete table;
- integral types/ranges/operations;
- floating formats/operations;
- boolean;
- practical selection;
- links to Ch3 literals, Ch5 conversions, Ch15 operators.

Внутри допустимы 4.3.1 Integral, 4.3.2 Floating-Point, 4.3.3 boolean; отдельный файл на каждый keyword не нужен.

**4.4 Reference Types, Objects, References, and null**

- class/interface/array/type-variable types;
- object definition;
- reference value and aliasing;
- Object/String boundary;
- null type/reference;
- equality boundary;
- GC/layout non-guarantees.

**4.5 Generic-Related Type Forms — Boundary Overview**

- type variables, parameterized, erased, reifiable, raw, intersection;
- why Ch4 needs the terms;
- all operational theory delegated Ch20.

**4.6 Type Identity, Static Type, and Runtime Class**

- compile-time sameness;
- runtime class-loader identity;
- arrays recursively;
- dispatch/getClass/class literals/erasure boundary.

**4.7 Subtyping and Supertypes**

- formal relations;
- primitive;
- classes/interfaces;
- parameterized/raw/wildcard boundary;
- arrays;
- type variables/intersections/null;
- LUB/type projections overview.

**4.8 Type Contexts**

- complete JLS §4.11 map;
- wildcard/reifiable/exception restrictions;
- type/declaration annotations and contexts.

**4.9 Variables, Stored Values, and Pass-by-Value**

- primitive/reference variables;
- compatibility and heap pollution boundary;
- copying values;
- aliasing, mutate/reassign;
- no mandatory stack/heap diagram.

**4.10 The Eight Kinds of Variables**

- exact JLS classification;
- creation/initialization/effective lifetime;
- pattern variable as local variable;
- links to scope, patterns, arrays/classes.

**4.11 Initial Values and Definite Assignment Boundary**

- class/instance/array defaults;
- parameter initialization;
- locals;
- declaration/initialization/assignment;
- link Ch16.

**4.12 final, Blank Final, Constant, and Effectively Final Variables**

- precise categories;
- reference/object immutability;
- parameters/catch;
- JMM link.

**4.13 Local Variable Type Inference**

- `var` grammar and inference;
- complete valid/invalid matrix;
- arrays/null/poly expressions/multiple declarators/self-reference;
- lambda parameter `var` distinction.

**4.14 Diagnostic Guide and Pitfalls**

- one non-duplicating final checklist.

Итог второго проектирования: 14 top-level sections. В сравнении с 33 нынешними files это всё равно существенное укрупнение, но variables/init/final/var не следует объединять в один файл: это четыре разных normative concerns.

## 4. Сравнение со структурой первого аудита

Первый аудит предложил 13 разделов. Второй независимо пришёл почти к той же macro-architecture, что является сильным подтверждением результата.

| Область | Первый аудит | Второй аудит | Итог |
|---|---|---|---|
| Mental model | 4.1 | 4.1–4.2 | Второй точнее отделяет guarantees от vocabulary/result model |
| Primitive types | Единый 4.3 | Единый 4.3 | Полное совпадение |
| Reference/object/null | 4.4 | 4.4 | Полное совпадение |
| Generic boundary | 4.5 | 4.5 | Полное совпадение |
| Type identity/static/runtime | 4.6 | 4.6 | Полное совпадение |
| Subtyping | 4.7 | 4.7 | Полное совпадение |
| Type contexts | 4.8 | 4.8 | Полное совпадение |
| Variables/pass-by-value | 4.9 | 4.9 | Полное совпадение |
| Eight kinds | 4.10 | 4.10 | Полное совпадение |
| final | 4.11 | 4.12 | Тема подтверждена, нумерация сдвинута |
| Defaults + var | Объединены в 4.12 | Разделены 4.11 и 4.13 | Второй вариант лучше: unrelated rules не следует смешивать |
| Pitfalls | 4.13 | 4.14 | Полное смысловое совпадение |

## 5. Сравнение findings двух аудитов

### 5.1 Полностью подтверждены вторым аудитом

- expression can produce no result;
- unique-type-of-value wording is defective;
- class literals are reference values, not a separate category;
- physical heap/stack claims are not language guarantees;
- variable count/classification is wrong;
- primitive and advanced reference subtyping are missing;
- type contexts are incomplete;
- generic boundary map is needed;
- floating equality section is too categorical;
- boolean storage claims are implementation-specific;
- `var` typo and missing restrictions;
- final/variables coverage is incomplete;
- current structure is overfragmented.

### 5.2 Уточнены, но не отменены

#### «Value belongs to exactly one type»

Первый аудит называл это прямой ошибкой. Второй формулирует точнее: это недопустимое смешение уровней. Для literal expression `5` тип `int` действительно однозначен; неверно обобщение на «value вообще».

#### Heap/stack model

Первый аудит предлагал убрать её. Второй уточняет: её можно оставить как явно маркированную implementation intuition, но не как JLS guarantee и не в разделе с названием Runtime Representation без JVM source.

#### Source tags

Первый аудит слишком уверенно говорил о несогласованности. Второй не считает её доказанной по textual similarity. Корректный finding: требуется provenance audit каждого file; до него нельзя ни массово добавить, ни снять теги.

#### Floating theory completeness

Первый аудит перечислил весь формальный IEEE слой. Второй подтверждает behavioral gaps, но не требует переносить математические формулы JLS: для практического учебника достаточно normal/subnormal, precision/range, rounding, overflow/underflow, signed zero и comparison policies.

### 5.3 Новые находки, отсутствовавшие в первом аудите

- `? extends` ошибочно сведён к «только чтение»;
- `x != x` — корректная NaN test, поэтому «только isNaN» неверно;
- universal epsilon recipe не является универсально правильным;
- performance/design motivation выдана без источника;
- short/byte memory claims чрезмерно категоричны;
- helpful NPE guarantee слишком сильна;
- wrapper subsection является structural redirect;
- ошибки дублируются на трёх уровнях;
- class-literal/value table дополнительно смешивает types и values в generics row.

### 5.4 Ложные тревоги первого аудита

Полностью ложных основных findings не обнаружено. Но два утверждения первого отчёта нельзя оставлять как доказанные факты:

1. source-tag mismatch — пока только кандидат на provenance recheck;
2. «одно значение — один тип» — требует точной замены модели, а не простого объявления всякой связи value/type ложной.

## 6. Консолидированный вердикт

Два независимых прохода сходятся в главном:

- Ch4 имеет хороший практический фундамент;
- текущий статус `done` не оправдан;
- макроструктуру следует укрупнить;
- важнейшие исправления находятся не в добавлении ещё примеров `byte/int`, а в expression/result model, subtyping, type contexts и variables;
- physical JVM assumptions нужно отделить от language semantics;
- полную generics theory дублировать не нужно, но boundary forms обязаны присутствовать.

Уверенность в консолидированном выводе выше, чем после первого аудита: основная архитектура воспроизвелась независимо, а второй проход не опроверг ключевых замечаний, только уточнил два из них и добавил новые дефекты.

Рекомендуемая итоговая структура — 14 разделов из §3 этого отчёта.
