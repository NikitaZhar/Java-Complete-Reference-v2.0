2025-09-15 13:01
Tags: #SyntaxBasics

# Chapter 1. Syntax Basics

## 1.1 Source File Structure
Каждая программа на Java состоит из одного или более исходных файлов с расширением `.java`. Эти файлы называются **компиляционными единицами** (`compilation units`). Файл может содержать объявления пакета, импортов, а также одно или несколько объявлений типов (`classes`, `interfaces`, `enums`, `records`, `annotations`).

Формально структура файла определяется спецификацией `Java Language Specification (JLS §7.3)`

CompilationUnit:
```java
[PackageDeclaration] {ImportDeclaration} {TypeDeclaration}
```
Основные положения:
1. **Один исходный файл — один** `compilation unit`.
    - Файл должен иметь расширение `.java`.
    - Кодировка должна быть совместима с `Unicode` (обычно `UTF-8`).
2. **Package declaration.**
    - В начале файла может указываться пакет, к которому принадлежит код.
    - Может быть только одно объявление `package` в файле.
    - Если оно отсутствует, файл принадлежит `unnamed package` (не рекомендуется для реальных проектов).
3. **Import declarations.**
    - После пакета могут следовать одно или несколько объявлений `import`.
    - Поддерживаются обычные импорты (`import java.util.List;`) и статические (`import static java.lang.Math.PI;`).
    - Импорты действуют только внутри данного файла.
4. **Type declarations.**
    - Основное содержимое файла — объявления типов (`classes`, `interfaces`, `enums`, `records`, `annotation types`).
    - В одном файле может быть несколько типов, но **только один из них может быть** `public`, и его имя должно совпадать с именем файла (например, класс `MyClass` в `MyClass.java`).
    - Допускаются `package-private` типы без ограничений по количеству.
5. **Module declaration (Java 9+).**
    - Вместо обычного исходного файла может быть `module-info.java`.
    - В нём описывается модуль и его зависимости (`requires`, `exports`, `opens`, `provides`, `uses`).
6. **Комментарии и директивы.**
    - В файле разрешены комментарии `//`, `/* … */` и документационные комментарии `/** … */`.
    - Они могут находиться в любом месте, где синтаксис допускает `whitespace`.
7. **Лексические особенности.**
    - Весь исходный код проходит предварительную обработку `Unicode-escape`-последовательностей (`\uXXXX`), которая выполняется до токенизации.
    - Символы конца строки (`LF`, `CR`, `CRLF`) считаются эквивалентными.

Пример:
```java
// Файл: Example.java
package com.example.app;

import java.util.List;
import static java.lang.Math.PI;

public class Example {
    public static void main(String[] args) {
        System.out.println("Hello, world!");
        System.out.println("PI = " + PI);
    }
}

class Helper {}  // package-private тип
```
### [[1.1.1 Compilation Unit - минимальная единица кода]]
### [[1.1.2 Encoding and Unicode]]
### [[1.1.3 Module Declarations (Java 9+)]]
[[1.1.4 Package Declarations]]


### [[1.1.5 Import Declarations]]

### 1.1.6 Type Declarations Overview
- Classes
- Interfaces
- Enums
- Records
- Annotations
- Top-level и nested types
- Порядок элементов верхнего уровня в файле
### 1.1.7 Empty compilation units (JLS §7.3)
- Файл `.java` может содержать только комментарии и/или пробельные символы и при этом оставаться корректной _compilation unit_.
- Практическое применение: заглушки, временные файлы, тесты инструментов.

### [[1.1.8 Shebang line (Java 11+, JLS §7.3)]]

### 1.1.9 Compilation unit annotations (JLS §7.3)
- Аннотации на уровне единицы компиляции записываются **перед** `package` или `module`.
- Распространяются на весь файл.
- `@SuppressWarnings("all") package com.example;`
### 1.1.10 Уточнение: порядок объявлений типов внутри файла не важен.
В Java порядок объявлений верхнего уровня в одном файле не влияет на разрешение имён; _forward declarations_ не требуются.
Разница между “порядком в файле” и “порядком внутри класса”


***************************************
# Текущий анализ разделов

1) Что именно покрыто сейчас

## Глава 1. _Syntax Basics_ (`Java Complete Reference.md`)

Глава — это «хаб»: даёт обзор и список разделов (1.1.* и далее). Видно, что в ней уже выделены отдельные подразделы:

## 1.1.1 Compilation Unit

Сильные стороны:

- Чёткая структура `CompilationUnit` (JLS §7.3), порядок: `package → import → type`.
    
- Правила `public` типа и соответствия имени файла; несколько top-level типов (если не `public`); `package-private`.
    
- Упомянут `strictfp` для верхнеуровневых типов.
    
- Примеры ошибок; пустая единица компиляции; аннотации на уровне файла; shebang; line terminators; **краткое** про `module-info.java`.
    
- Есть раздел про виды `import` (single, on-demand, static).
    

Что выходит за рамки «ядра» темы:

- аннотации компиляционной единицы уже вынесены в **1.1.8** и **1.1.9** в самой главе — дубли.
    
- Линейные разделители и Unicode-escape — предмет **1.1.2** и **1.5** — частичный дубль.
    

## 1.1.2 Encoding and Unicode

Сильные стороны:

- JLS §3.1–3.5; JEP 400 (UTF-8 по умолчанию в JDK 18+); `javac -encoding`.
    
- Unicode-escape до лексического анализа; CR/LF/CRLF; BOM; `char` vs Unicode; суррогатные пары; примеры ошибок.
    
- Практическая ориентация (ошибки кодировок, BOM).
    

Пересечения:

- Line terminators и Unicode-escape дублируют положения, встречающиеся в **1.1.1** и в разделе **1.5 Unicode Escapes** самой главы.
    

## 1.1.3 Module Declarations (Java 9+)

Сильные стороны:

- Полный синтаксис `module-info.java` (open, requires [static|transitive], exports [to], opens [to], uses/provides).
    
- Read edges, ограничения `static`+`transitive`, unnamed/automatic modules, split packages, `ModuleLayer`, weak encapsulation.
    
- Аннотации модулей, тестовые нюансы (`--add-opens`), безопасность на уровне JPMS.
    

Пересечения:

- Частично дублируется упоминание модулей в **1.1.1** (где есть «альтернатива: module-info.java»).
    
- В **1.1.4** присутствуют большие куски про JPMS (qualified exports/opens, split packages, automatic modules) — дубль.
    

## 1.1.4 Package Declarations

Сильные стороны:

- JLS §7.4: синтаксис, позиция в файле, именование и соглашения, `package-info.java`, структура каталогов, практика для Spring/Jakarta, unnamed package и его ограничения, пакетная видимость, мини-кейс и чек-лист.
    
- Полезные практические разделы («Организация файлов», «Best Practices», «Ошибки»).
    

Пересечения/выход за рамки:

- Большой блок **про JPMS**: `exports/opens (qualified)`, split packages, automatic modules, `opens ... to` — это **тема 1.1.3**, а не объявления пакета.
    
- Таблица «Import vs Static Import» и блок «Import vs Static Import» — это **тема 1.1.5**, не 1.1.4.
    
- Ссылка «См. также: **1.2.1 Access Modifiers**» — **битая** (в главе 1.2.1 — Identifiers). Нужна корректировка ссылок.
    

---

# 2) Дубли и пересечения (точечно)

1. **Imports**
    

- Подробности импорта встречаются в **1.1.1** («Виды импортов») и в **1.1.4** («Import vs Static Import»), но «владельцем» темы должен быть **1.1.5 Import Declarations** (файл отсутствует).  
    **Итог:** явный дубль и разнос материала по двум страницам + отсутствует целевая страница.
    

2. **JPMS (модули)**
    

- **1.1.3** полностью покрывает модули, но в **1.1.4** есть большие вставки про `exports/opens`, split packages, automatic modules и даже «Особенности JPMS во фреймворках».  
    **Итог:** дубль. JPMS следует централизовать в **1.1.3**, а в **1.1.4** оставить только минимальную связку «пакеты — строительные блоки для экспортов».
    

3. **Shebang и аннотации единицы компиляции**
    

- Подробно в **1.1.1**, но эти темы уже вынесены в **1.1.8** и **1.1.9** внутри главы.  
    **Итог:** дубль внутри самой главы.
    

4. **Unicode / line terminators / escapes**
    

- В **1.1.2** это раскрыто полно. В **1.1.1** есть повтор (line terminators и замечания) + в главе есть отдельный **1.5 Unicode Escapes**.  
    **Итог:** фактическое трёхкратное присутствие. Нужна «единственная точка истины».
    

5. **Unnamed package**
    

- Упомянут и в **1.1.1**, и в **1.1.4**.  
    **Итог:** легкое пересечение допустимо (краткое предупреждение в 1.1.1), но подробности и кейсы логичнее держать в **1.1.4**.
    

---

# 3) Пропуски и несоответствия

- **[Важное] Нет файла 1.1.5 Import Declarations.**  
    При этом существенная часть материала по импортам «размазана» между **1.1.1** и **1.1.4**. Это и дубль, и структурный пробел.
    
- **Неверная перекрёстная ссылка в 1.1.4**: «См. также: 1.2.1 Access Modifiers» — такого раздела нет в текущей нумерации (1.2.1 у вас — _Identifiers_). Нужно исправить ссылку (например, на раздел доступа там, где он реально будет: вероятно **1.3.x** или **1.2.x**, в зависимости от финальной оглавной).
    
- **Цитирование JLS по модулям.**  
    В **1.1.3** корректно изложено содержание, но для единообразия хорошо бы явно пометить **JLS §7.7 Module Declarations**. (Сейчас явная ссылка именно на §7.7 в тексте не видна.)
    
- **Shebang**: в главе фигурирует как «Java 11+». Для полноты стоит сослаться на **JEP 330** (single-file source-code launch), если вы поддерживаете JEP-ссылки рядом с JEP 400 (кодировка).
    
- **package-info.java**: в **1.1.4** корректно сказано про аннотации/JavaDoc, но рядом приведены блоки про `exports ... to` и `opens ... to`, которые относятся к **module-info.java**, не к `package-info.java`. Это может создать двусмысленность. Нужна явная разграничивающая ремарка.
    

---

# 4) Рекомендации по структуре (конкретные правки)

## A. Централизация «владельцев» тем

- **1.1.1 Compilation Unit**  
    Оставить: структура файла (JLS §7.3), порядок `package → import → type`, правило `public` и имя файла, пустая единица, верхнеуровневые аннотации — **только** как краткая отсылка на **1.1.9**, без деталей; **краткая** ремарка про shebang — отсылка на **1.1.8**.  
    Убрать/вынести:
    
    - Подробности импортов → **1.1.5 Import Declarations**.
        
    - Подробности Unicode/line terminators → **1.1.2** (и/или **1.5**).
        
    - Модули `module-info.java` → **1.1.3** (оставить одну строку-отсылку).
        
- **1.1.2 Encoding and Unicode**  
    Оставить: кодировки исходников, JEP 400 (UTF-8 по умолчанию), BOM, line terminators, общая связь Java/Unicode, `javac -encoding`, практические кейсы.  
    Уточнить: перенаправить детальные разделы про **Unicode escapes** в **1.5 Unicode Escapes**, а здесь оставить краткое напоминание и ссылку.
    
- **1.1.3 Module Declarations**  
    Оставить всё по JPMS здесь: синтаксис, `open/exports/opens/uses/provides`, read edges, split packages, unnamed/automatic modules, `ModuleLayer`, weak encapsulation, тестовые флаги.  
    Добавить: явную ссылку на **JLS §7.7**.  
    (Опционально) Короткая ссылка на **1.1.4**: «экспортируется не “тип”, а **пакет**».
    
- **1.1.4 Package Declarations**  
    Оставить: JLS §7.4, синтаксис и место `package`, соглашения именования, `package-info.java` (только документация/аннотации!), структура каталогов, пакетная видимость (`package-private`), unnamed package, практики (Spring/Jakarta), кейсы/чек-лист.  
    Убрать/вынести:
    
    - Все блоки про **JPMS** (`exports/opens`, split packages, automatic modules) → **1.1.3**.
        
    - «Import vs Static Import» → **1.1.5**.  
        Исправить: битую ссылку «1.2.1 Access Modifiers» (заменить на реальный раздел про модификаторы доступа; или временно написать «см. раздел про модификаторы доступа» без номера).
        

## B. Доводим главу-хаб

- В **главе 1** оставить обзор плюс **ссылки**.  
    Избегать повторной «полной» подачи материалов, которые уже живут в отдельных файлах (shebang, file annotations, unicode escapes). Пусть глава выступает оглавлением + 1–2 ключевых тезиса на раздел.
    

## C. Закрываем пробелы

- **Создать 1.1.5 Import Declarations.md** и **вынести туда**:
    
    - Из **1.1.1**: виды импортов и их семантика.
        
    - Из **1.1.4**: «Import vs Static Import», таблицы/правила и best practices (`*` vs точечный импорт, static-import для констант и утилит).
        
    - В **главе 1** оставить ссылку и краткий synopsis.
        
- **Согласовать нумерацию и «см. также»**:
    
    - Привести ссылки к существующим номерам (особенно «Access Modifiers»).
        
    - Везде использовать единый стиль ссылок (как в 1.1.* уже сделано).
        

## D. Примечания точности

- В **1.1.4** рядом с `package-info.java` явно отметить: _экспорт пакетов делается в `module-info.java` (JPMS), а `package-info.java` — для JavaDoc/аннотаций; это разные механизмы_.
    
- В **1.1.1** оставить только **краткую** отсылку к shebang/annotations, без дублей примеров — они уже есть в **1.1.8/1.1.9**.
    
- В **1.1.2** указать, что подробная формализация `\uXXXX` собрана в **1.5**, чтобы исключить повтор.
    

---

# 5) Итоговое распределение ответственности (чтобы дубли не возвращались)

- **1.1.1 Compilation Unit** — **только** каркас файла и правила `public`/имя/порядок/пустота/верхнеуровневые аннотации (ссылками на 1.1.8/1.1.9), упоминание `module-info.java` одной строкой (ссылка на 1.1.3).
    
- **1.1.2 Encoding and Unicode** — кодировка исходников (JEP 400), BOM, line terminators, общие замечания про Unicode в исходниках; **детали escape — в 1.5**.
    
- **1.1.3 Module Declarations** — вся JPMS-логика и практика (включая split packages, automatic/unnamed modules, qualified exports/opens, тестовые флаги).
    
- **1.1.4 Package Declarations** — синтаксис/позиция/именование/`package-info.java`/структура каталогов/`package-private`/unnamed package/практика в фреймворках (без импортов и JPMS).
    
- **1.1.5 Import Declarations** — весь материал по import/static import (из 1.1.1 и 1.1.4), правила и анти-паттерны, рекомендации.
    

---

# 6) Короткое резюме

- **Дубли есть**:  
    — импорты (1.1.1 и 1.1.4) → в 1.1.5;  
    — JPMS (1.1.3 и 1.1.4, плюс упоминание в 1.1.1) → в 1.1.3;  
    — shebang и аннотации compilation unit (1.1.1 и 1.1.8/1.1.9) → оставить в 1.1.8/1.1.9, из 1.1.1 только ссылка;  
    — Unicode/line terminators (1.1.1, 1.1.2, 1.5) → оставить как **SOT** в 1.1.2/1.5.
    
    
***********************

**Важно!!!!!!**
Можно рассмотреть общую структуру на основе документации Oracle и стандарта языка Java
*****************




## 1.2 Identifiers and Keywords
### 1.2.1 Identifiers
- Правила именования (Unicode letters, digits, connecting, combining, ignorable chars)
- Запрет начинать с цифры
- Ограничение на использование зарезервированных слов

### 1.2.2 Keywords
- Полный список ключевых слов
- Новые ключевые слова (`sealed`, `permits`, `record` и др.)

### 1.2.3 Reserved Literals
- `true`
- `false`
- `null`

### 1.2.4 Contextual Keywords
- `var`, `yield`
- `record`, `sealed`, `non-sealed`, `permits`
- `exports`, `opens`, `module`, `requires`, `transitive`
- `uses`, `provides`, `to`, `with`, `open`

---

## 1.3 Separators and Whitespace
### 1.3.1 Separators
- `(` `)` `{` `}` `[` `]`
- `;` `,` `.`
- `...` `::` `@` `->`

### 1.3.2 Whitespace and Line Terminators
- Space, tab, form feed
- Line terminators (`LF`, `CRLF`, `CR`) и их эквивалентность

### 1.3.3 Influence on Lexical Analysis
- Token boundaries
- Пример: `int x=1; -y;`

---

## 1.4 Comments and Documentation
### 1.4.1 Single-line Comments
- `//`

### 1.4.2 Multi-line Comments
- `/* … */`

### 1.4.3 Documentation Comments
- `/** … */`
- Javadoc теги
- Генерация документации

### 1.4.4 Nesting Restrictions
- Нельзя вкладывать `/* … */` друг в друга

---

## 1.5 Unicode Escapes
### 1.5.1 Syntax
- Формат `\uXXXX`

### 1.5.2 Processing Stage
- Применимость до лексического анализа

### 1.5.3 Influence on Code
- Работа в комментариях и строках
- Пример с `// \u000A`

---

## 1.6 Expression Statements
### 1.6.1 Valid Expression Statements
- Assignment
- Pre/post increment/decrement
- Method invocation
- Object creation expression

### 1.6.2 Parenthesized Expressions
- Правила и примеры

---

## 1.7 Empty and Block Statements
### 1.7.1 Empty Statement
- `;`

### 1.7.2 Block Statement
- `{ … }`
- Scope introduction

---

## 1.8 Local Class and Interface Declarations
### 1.8.1 Local Classes
- Внутри методов и блоков

### 1.8.2 Local Interfaces
- Редко используемые, но допустимые


# Chapter 2. Build & Run Basics (CLI).

1. Использование компилятора и запуск из Терминала
    Предложенные пункты:
    
    - 2.1 “javac: базовая компиляция” — синопсис, компиляция одиночного файла. [Oracle Documentation](https://docs.oracle.com/en/java/javase/24/docs/specs/man/javac.html?utm_source=chatgpt.com)
    - 2.2 “java: запуск приложения” — запуск по полному имени класса, требование `public static void main(String[] args)` (и современные вариации/простые файлы при новых версиях можно кратко помянуть). [Oracle Documentation](https://docs.oracle.com/en/java/javase/21/docs/specs/man/java.html?utm_source=chatgpt.com)
    
2. Компиляция с использованием пакетов

    - 2.3 “Компиляция к иерархии пакетов: -d” — соответствие `package` ↔ директории, `javac -d out src/...`. [Oracle Documentation](https://docs.oracle.com/en/java/javase/11/tools/javac.html?utm_source=chatgpt.com)

3. classpath
    
    - 2.4 “Класс-путь: -cp / CLASSPATH, что по умолчанию” — `.` по умолчанию, замещение при указании `-cp`, советы не полагаться на глобальный `CLASSPATH`. [Oracle Documentation+1](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/classpath.html?utm_source=chatgpt.com)

4. Использование JAR

    - **2.5 “Сборка JAR: jar”** — что такое JAR, базовые команды, манифест, “исполняемый JAR” (`jar --create --file app.jar --main-class ...`). [Oracle Documentation](https://docs.oracle.com/javase/8/docs/technotes/tools/windows/jar.html?utm_source=chatgpt.com)
        
    - **2.6 “Запуск JAR: java -jar …”** — требования манифеста/`Main-Class`. [Oracle Documentation](https://docs.oracle.com/en/java/javase/21/docs/specs/man/java.html?utm_source=chatgpt.com)
        
5. **Компиляция/запуск с JAR’ами и каталогами в classpath**
    
    - **2.7 “Смешанный classpath (каталоги + JAR)”** — `-cp out:lib/*` (или `;` на Windows), подводные камни. [Oracle Documentation](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/classpath.html?utm_source=chatgpt.com)


> Примечание: если планируешь модульную тему (Java 9+), можно добавить позже отдельную главу про **Module System** с `--module-path` и манифестами/`module-info.java`. (Ссылка на инструменты останется та же, раздел man-pages Oracle). [Oracle Documentation](https://docs.oracle.com/en/java/javase/11/tools/tools-and-command-reference.html?utm_source=chatgpt.com)