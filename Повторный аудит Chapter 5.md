# Повторный аудит Chapter 5: Conversions and Contexts

Дата проверки: 2026-08-28  
Проверенный commit: `5fda6bb`  
Целевая платформа проекта: Java SE 25

## 1. Метод проверки

Этот аудит выполнен заново, без принятия выводов первого аудита за исходные данные.

Сопоставлены четыре слоя:

1. нормативная структура и правила JLS SE 25, Chapter 5;
2. фактическая структура всех 14 файлов `Notes/Ch05`;
3. материал четырёх книг в `Sources` — Mughal и Boyarsky для 1Z0-829 и 1Z0-830;
4. требования `Working Contract` и матрица владения темами.

Проверялось не совпадение оглавлений, а наличие у читателя полной рабочей модели: определение, разрешённые цепочки преобразований, compile-time границы, runtime-поведение, примеры и ошибки.

## 2. Нормативная карта JLS SE 25

JLS SE 25 определяет 12 numbered kinds в §5.1:

1. Identity Conversion
2. Widening Primitive Conversion
3. Narrowing Primitive Conversion
4. Widening and Narrowing Primitive Conversion
5. Widening Reference Conversion
6. Narrowing Reference Conversion
7. Boxing Conversion
8. Unboxing Conversion
9. Unchecked Conversion
10. Capture Conversion
11. String Conversion
12. Forbidden Conversions

Это не означает 12 равноправных «операций»: forbidden conversion — правило замыкания каталога, а `byte → char` вынесено в отдельный комбинированный вид. Value Set Conversion в JLS SE 25 отсутствует; оно было §5.1.13 в JLS SE 16 и было удалено из Chapter 5 начиная с always-strict floating-point semantics Java 17.

JLS перечисляет семь kinds of conversion contexts, если strict и loose invocation считать отдельно:

1. Assignment
2. Strict Invocation
3. Loose Invocation
4. String
5. Casting
6. Numeric
7. Testing

Но структурно JLS объединяет strict и loose invocation в одном §5.3. Поэтому для учебника корректно говорить: «шесть крупных семейств контекстов, invocation имеет два режима» либо «семь видов по счёту JLS». Фраза «пять контекстов» для Java SE 25 неполна.

## 3. Что в текущей структуре сделано правильно

Двухосевая организация «вид преобразования × контекст» удачна и должна быть сохранена. Она удобнее буквального копирования JLS и соответствует Working Contract.

Сильные разделы:

- widening primitive: цепочки и потеря точности;
- narrowing primitive: отбрасывание битов, `char`, `NaN`, infinity, saturation;
- boxing/unboxing: `null`, запрещённое widening-then-boxing, unboxing-then-widening;
- базовые assignment и invocation examples;
- базовое unary/binary numeric promotion;
- практические примеры из Boyarsky и Mughal действительно использованы.

Таким образом, глава не является пустым конспектом. Проблема — не слабость базовых объяснений, а систематические пробелы на границах современной модели Java SE 25.

## 4. Матрица покрытия текущей главы

| Нормативная/учебная тема | Текущее покрытие | Оценка | Что отсутствует или требует исправления |
|---|---|---:|---|
| Target type и poly expressions | Почти отсутствует | Критический пробел | Нельзя объяснить, что контекст сначала может определить тип poly expression, а conversion применяется уже после этого |
| Identity conversion | Объединено с widening | Достаточно для практики | Нужны последствия: redundant cast и универсальность identity |
| Widening primitive | Отдельный хороший раздел | Хорошо | Нужна полная точная таблица и связь с numeric contexts |
| Narrowing primitive | Хороший раздел | Хорошо | Не показано отдельно `double → float`; тезис «почти всегда нужен cast» надо связать с assignment и numeric choice exceptions |
| Widening-and-narrowing primitive | Спрятано внутри `char` | Неполно | `byte → char` отсутствует как самостоятельный элемент каталога и casting matrix |
| Widening reference | Только простая иерархия | Частично | Массивы, type variables и intersection types почти отсутствуют |
| Narrowing reference | Упрощено до downcast | Существенно неполно | Interface/class, arrays, sealed disjointness, provably distinct generics, checked/unchecked, partial/complete runtime checks |
| Boxing | Хорошая практика | Частично | Не показаны boxing null type, точная identity guarantee, `OutOfMemoryError`; performance-тезисы слишком категоричны |
| Unboxing | Хорошая практика | Частично | Не показано unboxing через widening reference chains и полный список разрешённых цепочек |
| Unchecked conversion | Одно упоминание | Пробел | Нет определения raw-to-parameterized conversion, границ warning и примера |
| Capture conversion | Одно упоминание | Пробел | Нет даже wildcard-helper example; полное доказательство можно оставить Ch20 |
| String conversion | Отдельный раздел | Частично и местами неточно | Подмена нормативной семантики на `String.valueOf`; не рассмотрен случай `toString()` возвращает `null` |
| Forbidden conversions | Одно упоминание | Недостаточно | Нет системной границы boolean/numeric/reference и таблицы невозможных цепочек |
| Assignment context | Отдельный раздел | Частично | Нет полных conversion chains, unchecked tail, исключений вследствие boxing/unboxing/heap pollution/array store; ошибочный «аргумент по умолчанию» |
| Strict/loose invocation | Слиты | Частично | Три фазы названы, но строгий и свободный режимы не определены как контексты; нет unchecked/raw chains и ambiguity cases из Mughal |
| String context | Вид conversion есть, контекста нет | Пробел структуры | В overview-таблице String row везде `—`, хотя string context должен быть отдельной колонкой |
| Casting context | Базовый раздел | Существенно неполно | Нет нормативной таблицы compound conversions: reference narrowing + unboxing, boxing + widening reference и др. |
| Numeric contexts | Старая unary/binary модель | Критический пробел | Нет arithmetic/array/choice contexts, general numeric promotion, conditional и standalone switch expressions, constant narrowing в choice context |
| Testing context | Отсутствует | Критический пробел | Нет conversion model для `instanceof` patterns и pattern switch; различия с casting context не объяснены |
| Ошибки и ловушки | Большой сводный раздел | Полезно, но нужен аудит | Есть ошибки формулировок и материал, принадлежащий Ch4/Ch15/Ch49 |
| История value sets | Представлена как текущий conversion kind | Ошибка классификации | Оставить исторической заметкой, но убрать из актуального каталога Java SE 25 |

## 5. Подтверждённые фактические ошибки и неточности

### 5.1 Устаревший каталог

`5.1` включает Value Set Conversion как действующий род и не включает `Widening and Narrowing Primitive Conversion`. Для Java SE 25 это обратная картина: `byte → char` есть в §5.1.4, value set conversion в Chapter 5 уже нет.

### 5.2 Неполный счёт контекстов

`5.1`, `5.8` и opener говорят о пяти контекстах. Пропущен Testing Context; strict и loose invocation не различены. Отдельно отсутствует колонка String Context, хотя текст называет string одним из пяти.

### 5.3 Ошибка в таблице Numeric Context

В `5.8` для Narrowing Primitive × Numeric стоит `нет`. В JLS SE 25 numeric choice context допускает narrowing constant `int` expressions до `byte`, `short` или `char` при выполнении условий. Поэтому клетка должна различать arithmetic/array и choice contexts.

### 5.4 Устаревшая модель numeric promotion

`5.12` утверждает, что promotion бывает unary и binary. В SE 25 есть также general numeric promotion для numeric choice contexts. Не раскрыты result expressions standalone `switch` и numeric conditional expressions.

### 5.5 String conversion описано не строго эквивалентно JLS

Текст сводит conversion ссылки к `String.valueOf(x)`. JLS задаёт другую наблюдаемую границу: для non-null вызывается `toString()`, но если сам `toString()` вернул `null`, результатом conversion должна стать строка `"null"`. Простая модель через `String.valueOf(Object)` этого специального случая не выражает.

### 5.6 Слишком общий тезис о runtime checking downcast

Не всякое narrowing reference conversion полностью проверяется JVM: JLS различает checked, partially unchecked и completely unchecked conversions. Completely unchecked conversion не требует runtime validity check. Текущая формула годится только для обычного nongeneric downcast.

### 5.7 Casting context сведен к одиночным conversions

Фраза «каст добавляет два сужающих рода» скрывает разрешённые составные цепочки. Например, casting context может выполнить narrowing reference conversion, затем unboxing:

```java
Object x = Integer.valueOf(10);
int n = (int) x;
```

Следовательно, безопасно говорить «primitive-to-primitive narrowing не бросает исключения», но нельзя переносить это на всякий cast expression с primitive target: цепочка может бросить `ClassCastException` или `NullPointerException` до получения примитива.

### 5.8 Ошибка/артефакт в Assignment Contexts

«Аргумент по умолчанию» не является конструкцией Java и должен быть удалён или заменён точным названием реально подразумеваемого места.

Ссылка на constant expressions дана как §15.28; в JLS SE 25 это §15.29.

### 5.9 Некорректная формулировка про `NaN`

В `5.13` сказано, что сравнения с `NaN` через `==`/`!=` «всегда дают ложный результат», но непосредственно ниже показано `x != x // true`. Правильно: relational comparisons и `==` с NaN дают `false`, а `!=` даёт `true`.

Фраза «NaN ломает `equals`-контракты» также вводит в заблуждение: `Double.equals` канонизирует NaN для своей семантики равенства. Это отдельная тема Ch49, а не вывод из primitive comparison.

### 5.10 `Integer == Integer` вне cache range

Безусловный комментарий `1000 == 1000 // false` описывает обычное поведение стандартной реализации, но учебный вывод должен быть нормативным: для значений вне гарантированного диапазона идентичность ссылок спецификацией языка не гарантируется. Главный вывод — никогда не использовать wrapper `==` для сравнения значений.

### 5.11 Границы главы размыты

В `5.13` повторяются темы, владельцами которых матрица назначает другие главы: IEEE 754 и деньги, полная семантика compound assignment, wrapper equality/cache. В Ch5 они допустимы как короткие conversion-related pitfalls со ссылкой, но не должны заменять недостающие собственные темы Ch5: testing contexts, generic conversions, casting chains и general numeric promotion.

## 6. Что реально дали книги и что не перенесено

### Mughal 1Z0-829/830

В текущую главу перенесены базовая двухосевая схема, narrowing constant with optional boxing, primitive/reference conversions и часть overload phases.

Не перенесены или чрезмерно сокращены:

- большая матрица conversion contexts и разрешённых chains;
- подробные reference assignment cases: class, interface, reference arrays, primitive arrays;
- `Object`, array covariance и `ArrayStoreException`;
- ambiguous overload case, где разные параметры требуют boxing/unboxing;
- расширенный набор fixed-arity/varargs overload examples;
- casting chains вида primitive → wrapper → supertype и reference → unboxing → widening;
- подробное сравнение cast и `instanceof`, включая pattern matching.

### Boyarsky 1Z0-829/830

Перенесены правила basic numeric promotion, часть casting examples, autoboxing limitations, `null` unboxing и популярные overload examples.

Недостаточно использованы:

- более плотные compile/non-compile sets для assigning/casting expressions;
- последствия расположения cast внутри выражения;
- reference/interface cast cases;
- неоднозначности перегрузки и `null`;
- wrapper/varargs combinations;
- связь conditional expressions и promotions.

Книги не могут закрыть новые нормативные части SE 25 полностью: testing contexts и современная general numeric promotion должны проверяться прежде всего по JLS SE 25. Но там, где книги дают практические задачи, текущая глава использовала их выборочно, несмотря на заявленный принцип равноценности.

## 7. Независимо пересобранная рекомендуемая структура

Ниже структура построена не как копия JLS, а как учебный маршрут. Двухосевая архитектура сохраняется.

### Chapter 5. Conversions, Target Typing, and Contexts

#### Part A. Mental Model and Conversion Kinds

**5.1 Target Type, Poly Expressions, and Conversions**

- static type versus target type;
- standalone и poly expressions;
- conversion, promotion и cast — не синонимы;
- compile-time typing versus runtime action;
- карта «expression form × context × permitted conversion».

**5.2 Conversion Kinds — Complete Map**

- полный актуальный каталог SE 25;
- identity и forbidden conversions;
- сводная навигационная таблица;
- отдельная historical note о value set conversion до Java 17.

**5.3 Primitive Conversions**

- widening primitive;
- exact preservation versus precision loss;
- narrowing primitive: integral, floating-to-integral, `double → float`;
- widening-and-narrowing `byte → char`;
- compile-time/runtime outcomes и безопасные API (`Math.toIntExact`).

**5.4 Reference Conversions**

- widening reference как subtyping;
- null type отдельно от widening;
- allowed narrowing conversions;
- class/interface, arrays, type variables, intersection types;
- final/sealed/disjoint types;
- checked versus unchecked narrowing;
- completely/partially unchecked и runtime checks;
- практическая лестница: compile-time error / warning / runtime CCE / safe conversion.

**5.5 Boxing and Unboxing Conversions**

- точный mapping primitive/wrapper;
- compile-time constant identity guarantee и запрет полагаться на wider cache;
- allocation не гарантируется на каждую упаковку, но возможен `OutOfMemoryError`;
- `null` unboxing и `NullPointerException`;
- permitted chains: boxing→widening reference, widening reference→unboxing→widening primitive;
- prohibited widening primitive→boxing;
- conditional/switch surprises ссылками на numeric contexts.

**5.6 Unchecked and Capture Conversions — Language Boundary**

- рабочее определение каждого вида;
- raw-to-parameterized warning example;
- `List<?>` helper/capture example;
- heap pollution boundary;
- формальные bounds и type inference делегированы Ch20.

**5.7 String Conversion and Forbidden Conversions**

- нормативная семантика primitive/reference/null;
- особый случай `toString()` returning null;
- невозможные boolean/numeric/reference conversions;
- string conversion versus parsing/value conversion.

#### Part B. Conversion Contexts

**5.8 Conversion Contexts — Complete Matrix**

- шесть крупных семейств, семь JLS kinds при раздельном счёте strict/loose invocation;
- отдельные колонки Assignment, Strict Invocation, Loose Invocation, String, Casting, Numeric, Testing;
- разрешённые одиночные и составные chains;
- target typing до conversion.

**5.9 Assignment Contexts**

- все синтаксические места assignment context;
- полный перечень chains;
- constant narrowing и narrowing→boxing;
- null, raw/unchecked tail;
- возможные runtime exceptions;
- arrays и assignment compatibility.

**5.10 Invocation Contexts and Overload Applicability**

- strict invocation;
- loose invocation;
- variable arity phase;
- absence of constant narrowing;
- conversion applicability versus most-specific selection;
- ambiguity examples;
- constructor invocation и generic method applicability;
- полная теория overload resolution остаётся в главе Methods, здесь — conversion layer.

**5.11 String Contexts**

- точная граница binary `+`;
- отличие string context от evaluation order и constant folding;
- короткий раздел со ссылкой на string conversion и Operators.

**5.12 Casting Contexts**

- primitive-target и reference-target conversion chains;
- полная практическая casting matrix;
- compile-time rejection, unchecked warning, runtime CCE/NPE, no runtime check;
- intersection casts;
- cast как источник target type для lambda/method reference.

**5.13 Numeric Contexts and Numeric Promotion**

- numeric arithmetic, array и choice contexts;
- unboxing first;
- unary, binary и general numeric promotion;
- conditional и standalone switch expressions;
- constant narrowing in numeric choice context;
- shifts как отдельное продвижение;
- результат operator versus последующий assignment context.

**5.14 Testing Contexts and Pattern Compatibility**

- `instanceof` patterns;
- pattern `switch` selectors;
- identity, widening reference и checked narrowing reference conversions;
- отсутствие unchecked narrowing;
- `null` и failed match;
- отличие проверки pattern от явного cast.

**5.15 Diagnostic Guide and Common Pitfalls**

- алгоритм разбора «компилируется ли выражение»;
- определить expression type/poly expression;
- определить target type/context;
- проверить разрешённую chain;
- определить warning/runtime action;
- компактная итоговая таблица ошибок без дублирования владельцев Ch4/Ch15/Ch20/Ch49.

Итого: 15 разделов вместо текущих 13. Рост числа файлов небольшой; глубина достигается главным образом внутренними подразделами 5.3–5.6 и 5.9–5.14.

## 8. Сравнение с предложенной в первом аудите структурой

| Элемент первого предложения | Решение после повторного аудита | Причина |
|---|---|---|
| 21 самостоятельный пункт | Сокращено до 15 разделов | Первая версия слишком буквально дробила JLS и противоречила принципу удобства |
| Отдельный Identity Conversion | Объединён с complete map в 5.2 | Тема слишком мала для отдельного учебного файла |
| Отдельные Widening и Narrowing Primitive | Объединены в большой 5.3 | Они лучше понимаются через одну карту потерь/сохранения; `byte → char` показывается рядом |
| Отдельные Widening и Narrowing Reference | Объединены в 5.4 с глубокими подразделами | Нужна общая модель subtyping/disjointness/runtime checks, а не два изолированных рассказа |
| Boxing и Unboxing отдельными пунктами | Объединены в 5.5 | Их главная учебная ценность — асимметрия и разрешённые цепочки |
| Unchecked и Capture отдельными пунктами | Один пограничный 5.6 | Формальный дом generics остаётся Ch20; Ch5 обязан дать рабочую модель, но не дублировать всю generics theory |
| String и Forbidden отдельно | Объединены в 5.7 | Обе темы компактны; одна показывает универсально разрешённый special context, другая — замыкание каталога |
| Strict и Loose Invocation как отдельные разделы | Один 5.10 с двумя подрежимами | Так делает и JLS §5.3; читателю важнее видеть фазы одной процедуры |
| Conversion chains как отдельная глава | Встроены в 5.8 matrix и каждый context | Отдельная глава создала бы повторение; chains должны быть рядом с местом применения |
| Runtime errors отдельной главой | Сведены в diagnostic 5.15 и локальные разделы | Исключения зависят от конкретной chain, а не образуют самостоятельный conversion kind |
| Historical value-set note | Сохранена только внутри 5.2 | Отдельный актуальный раздел создаёт ложное впечатление, что это SE 25 conversion kind |
| Target typing/poly expressions | Сохранено и поднято в 5.1 | Это обязательная рамка современной Chapter 5 |
| Testing contexts | Сохранено отдельным 5.14 | Это самостоятельная новая граница SE 25, которой нет в текущей главе |

Повторный вывод: идея первого предложения была верна по найденным пробелам, но структура была чрезмерно атомизирована. Новая версия лучше соответствует Working Contract.

## 9. Приоритет исправления

### P0 — исправить модель

1. Добавить 5.1 про target typing и poly expressions.
2. Убрать Value Set Conversion из актуального каталога.
3. Добавить widening-and-narrowing `byte → char`.
4. Перестроить contexts overview на SE 25.
5. Добавить Testing Contexts.
6. Переписать Numeric Contexts под arithmetic/array/choice и general promotion.

### P1 — закрыть нормативные границы

1. Расширить reference conversions.
2. Добавить unchecked/capture overview.
3. Добавить полные conversion chains в assignment/invocation/casting.
4. Отделить strict от loose invocation внутри единого раздела.
5. Исправить string conversion semantics.

### P2 — улучшить учебный слой

1. Перенести недостающие Mughal array/interface/overload examples.
2. Добавить Boyarsky compile/non-compile sets без дублирования.
3. Очистить 5.13 от неверных и чужих по владению тезисов.
4. Прогнать новый набор примеров на JDK 25, особенно pattern switch и numeric choice expressions.

## 10. Итоговый вердикт

Сомнения о полноте подтверждаются, но точнее, чем в первом аудите:

- базовый учебный слой conversion mechanics написан качественно;
- текущая структура основана в основном на модели JLS SE 16 и экзаменационных книгах;
- адаптация к Java 17–25 выполнена только для `strictfp`, но не для удаления value-set conversion, general numeric promotion и testing contexts;
- основная проблема — не количество примеров само по себе, а отсутствие современной общей модели target typing, complete conversion chains и новых contexts.

Текущую главу следует считать хорошим draft старого ядра, а не полной Chapter 5 для Java SE 25.
