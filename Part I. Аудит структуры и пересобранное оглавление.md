2026-07-03
Tags: #Content #Audit

> Критерий пересборки — не соответствие оригинальной нумерации JLS, а удобство и полнота структуры для практикующего разработчика. Совпадения с JLS сохранены там, где они и так удобны; расхождения — там, где это оправдано педагогически (Enums/Records/Annotations как отдельные главы, а не подпункты Classes/Interfaces).

---

## 1. Пересобранное оглавление Part I. Java Language Reference

### [[Chapter 1. Introduction (OK)]]
*(без изменений)*

### [[Chapter 2. Grammars (To Check)]]
*(без изменений, ждёт доработки по вашим пометкам)*

### [[Chapter 3. Lexical Structure]]
*(без изменений)*

### [[Chapter 4. Types, Values, and Variables]]
*(без изменений)*

### Chapter 5. Conversions and Contexts
5.1 Conversion Contexts
5.2 Assignment Contexts
5.3 Casting Contexts
5.4 String Conversion
5.5 Numeric Promotions
5.6 Unboxing Conversion
5.7 Value Set Conversion
5.8 Widening and Narrowing Reference Conversions
5.9 **(NEW)** Типичные ошибки: неявные сужающие контексты, потеря точности при `float`/`double`, `NaN`-ловушки в сравнениях, boxing в switch/generics

### Chapter 6. Names, Scope, and Access Control
*(переименовано: было «Names»)*
6.1 Declarations
6.2 Names and Identifiers
6.3 Scopes of Declarations
6.4 Shadowing and Hiding
6.5 Fully Qualified Names
6.6 Access Control
6.7 **(NEW)** Типичные ошибки: package-private vs protected, доступ через наследование в другом пакете, конфликт `import static` и локального имени

### Chapter 7. Packages and Modules
7.1 Packages
7.2 Compilation Units
7.3 Package Declarations
7.4 Module Declarations
7.5 Visibility Rules
7.6 **(NEW)** Типичные ошибки модульной системы (split packages, недостижимость через `requires transitive`) — краткая версия, глубокий разбор см. Part VI, Chapter 60

### Chapter 8. Classes
8.1 Class Declarations
8.2 Class Members
8.3 Fields
8.4 Methods
&nbsp;&nbsp;8.4.1 Method Declarations
&nbsp;&nbsp;8.4.2 Method Signatures
&nbsp;&nbsp;8.4.3 Method Modifiers
&nbsp;&nbsp;&nbsp;&nbsp;8.4.3.1 abstract Methods
&nbsp;&nbsp;&nbsp;&nbsp;8.4.3.2 final Methods
&nbsp;&nbsp;8.4.4 Overloading
8.5 Constructors
8.6 Instance Initializers
8.7 Static Initializers
8.8 Enclosing Instances
8.9 **(NEW — заполняет пробел)** Sealed Classes: `sealed`, `permits`, ограничения на иерархию
8.10 **(NEW — заполняет пробел)** Nested, Inner, Local, and Anonymous Classes: захват переменных, `Outer.this`, synthetic accessors — сейчас этот материал есть только практически в Part IV (41.5), на уровне спецификации отсутствует
8.11 **(NEW)** Типичные ошибки и best practices класса: телескопические конструкторы, утечка `this` в конструкторе, некорректная перегрузка vs переопределение

### Chapter 9. Interfaces
9.1 Interface Declarations
9.2 Interface Members
9.3 Default Methods
9.4 Functional Interfaces
9.5 **(NEW — заполняет пробел)** Sealed Interfaces
9.6 **(NEW — заполняет пробел)** Private Interface Methods (Java 9+) — не был упомянут вообще
9.7 **(NEW)** Типичные ошибки: diamond-конфликт default-методов, случайное превращение интерфейса в функциональный

### Chapter 10. Enums
10.1 Enum Types
10.2 Enum Members
10.3 Special Methods of Enums
10.4 **(NEW)** Enum как Singleton; EnumMap/EnumSet; enum с абстрактными методами на константах
10.5 **(NEW)** Типичные ошибки: сериализация enum, `ordinal()` как бизнес-значение, `valueOf`-исключения

### Chapter 11. Annotations
11.1 Annotation Types
11.2 Annotation Declarations
11.3 Annotation Processing
11.4 **(NEW)** Мета-аннотации: `@Retention`, `@Target`, `@Repeatable`, `@Inherited`
11.5 **(NEW)** Типичные ошибки и best practices: аннотации в рантайме vs compile-time, злоупотребление аннотациями вместо кода

### Chapter 12. Records
12.1 Record Declarations
12.2 Canonical Constructors
12.3 Compact Constructors
12.4 **(NEW)** Records и Pattern Matching (деконструкция) — перекрёстная ссылка на 14.7 / 22.3
12.5 **(NEW)** Records vs классические POJO/Lombok: когда уместны, когда нет
12.6 **(NEW)** Типичные ошибки: мутабельные поля внутри record, отсутствие валидации в компактном конструкторе, record и наследование (implements-only)

### [[Chapter 13. Arrays]]
*(без изменений — эталонный шаблон главы)*

### Chapter 14. Blocks, Statements, and Patterns
14.1 Blocks
14.2 Local Variable Declarations
14.3 If Statements
14.4 Switch Statements and Expressions
14.5 Loops (while, do, for)
14.6 Break, Continue, and Return
14.7 Pattern Matching Constructs
14.8 **(NEW — заполняет пробел)** Reachability of Statements (недостижимый код, пустые ветки, `while(true)` без `break`)
14.9 **(NEW)** Типичные ошибки: dangling else, fall-through в классическом switch, потерянный `yield` в switch-выражении

### Chapter 15. Expressions and Operators
*(переименовано: добавлены операторы из 3.12, чтобы не разрывать тему)*
15.1 Primary Expressions
15.2 Class Instance Creation Expressions
15.3 Array Creation Expressions
15.4 Field Access Expressions
15.5 Method Invocation Expressions
15.6 Lambda Expressions
15.7 Conditional Expressions
15.8 Assignment Expressions
15.9 **(NEW)** Порядок вычисления и побочные эффекты (evaluation order, short-circuit, side effects в аргументах)
15.10 **(NEW)** Типичные ошибки: переполнение `int` без предупреждений, приоритет операторов, `++`/`--` в сложных выражениях

### Chapter 16. Definite Assignment and Reachability
*(NEW ГЛАВА — заполняет пробел; сейчас DA/DU упомянуты только как «частая ловушка» в приложении к Chapter 1, без раскрытия)*
16.1 Definite Assignment для локальных переменных
16.2 DA в ветвлениях, циклах, try-catch-finally
16.3 DA и переменные образцов (`instanceof`/`switch` patterns)
16.4 DA и Effectively Final
16.5 Типичные ошибки: «variable might not have been initialized», ловушки в тернарном оператore

### Chapter 17. Exceptions and Assertions
*(было объединено с control transfer — control transfer перенесён в 14.6)*
17.1 Exception Types (checked / unchecked / Error)
17.2 try-catch-finally
17.3 try-with-resources и подавленные исключения (suppressed)
17.4 Multi-catch
17.5 throw Statements
17.6 assert Statements
17.7 Философия checked vs unchecked: когда что выбирать
17.8 Типичные ошибки: проглатывание исключений, исключение в finally маскирует исходное, catch(Exception e) как антипаттерн

### Chapter 18. Execution: Loading, Linking, and Initialization
*(NEW ГЛАВА — заполняет пробел; сейчас порядок инициализации не описан нигде системно, только упомянут в FAQ Chapter 1)*
18.1 Три фазы: Loading → Linking → Initialization
18.2 Что триггерит инициализацию класса
18.3 Порядок статических инициализаторов и полей
18.4 Class unloading; финализация (legacy) — перекрёстная ссылка на Cleaner API (Part IV, 43.3)
18.5 Типичные ошибки: циклические зависимости статических полей, `ExceptionInInitializerError`, ленивая инициализация синглтонов

### Chapter 19. Threads and Locks (Java Memory Model)
19.1 The Java Memory Model
19.2 Synchronized Blocks
19.3 Volatile Variables
19.4 Final Fields and Initialization Safety
19.5 **(NEW)** Типичные ошибки на уровне памяти: publication без happens-before, ложные предположения о видимости — практическое применение API см. Part IV, Chapter 53

### Chapter 20. Generics and Type Inference
20.1 Type Parameters
20.2 Generic Methods
20.3 Wildcards
20.4 Capture Conversion
20.5 **(NEW)** Type Erasure на практике: что теряется, что остаётся
20.6 **(NEW)** Типичные ошибки: heap pollution, unchecked warnings, невозможность `new T()`, wildcard vs generic method

### Chapter 21. Binary Compatibility
*(NEW ГЛАВА — заполняет пробел; сейчас тема отсутствует полностью)*
21.1 Что ломает бинарную совместимость, а что нет
21.2 Source-compatible vs binary-compatible vs behavior-compatible изменения
21.3 Практические рекомендации для авторов библиотек (перекрёстная ссылка на Part VI, Chapter 64 — API design)

### Chapter 22. Previews and Features
*(перенумеровано из 19, содержимое без изменений)*
22.1 Overview of Preview Features
22.2 Pattern Matching for `switch` — эволюция и стадии preview
22.3 Record Patterns — preview vs standard
22.4 String Templates (Preview in Java 21, статус в SE 25 — уточнить)
22.5 Scoped Values
22.6 Structured Concurrency
22.7 Preview-Feature Lifecycle and Migration Strategy

### Chapter 23. Appendices
A. Formal Grammars
B. Index of Keywords
C. Bibliography
D. **(NEW)** Таблица соответствия: главы этой книги ↔ параграфы официального JLS SE 25 (нужна, раз мы сознательно отошли от прямой нумерации — иначе теряется возможность быстрой сверки с первоисточником)
E. **(NEW)** Сводная таблица «Since Java X»: в каком релизе появилась/финализирована каждая языковая фича, упомянутая в книге

---

## 2. Полный аудит остальных частей: пропуски

| Часть | Пропуск | Предлагаемое место |
|---|---|---|
| Part II (JVMS) | `invokedynamic` / `MethodHandle` — как компилируются лямбды и method reference | новая подглава в Ch.3 или Ch.6 |
| Part II (JVMS) | Constant Dynamic (condy) — можно кратко | подглава в Ch.4 |
| Part III (Практика JDK) | Build-инструменты: Maven/Gradle (жизненный цикл, зависимости, минимально необходимое) | новая Chapter 32 |
| Part III | Дистрибутивы JDK и стратегия версий (Temurin, GraalVM, Corretto, LTS-каденция, как выбирать) | новая Chapter 33 |
| Part III | Class Data Sharing / AppCDS — ускорение старта JVM | подглава в Ch.30 |
| Part III / VII | Контейнеризация JVM (лимиты памяти в контейнере, CDS в Docker) | новая глава (см. п.4) |
| Part IV (Сертификация) | Enums в практике — нет параллельной подглавы, хотя Records (40.6) и Sealed (40.7) есть | добавить 40.x Enums in Practice |
| Part V (API) | **`java.lang` essentials**: контракт `Object` (`equals`/`hashCode`/`toString`), `Comparable` vs `Comparator`, кэш `Integer` (-128..127) и связанные `==`-ловушки, `Math`, `System`, `Runtime` | новая Chapter 49, перед Strings |
| Part V (API) | **Networking**: `java.net` (Socket/URL), `HttpClient` (sync/async, Java 11+), WebSocket-клиент — отсутствует полностью | новая Chapter 59 |
| Part V (API) | `BigDecimal`/`BigInteger`: масштаб, округление, `compareTo` vs `equals` | подглава в Ch.49 или Ch.50 |
| Part V (API) | `Random`/`SecureRandom`/`RandomGenerator` (JEP 356) | подглава в Ch.51 |
| Part V (API) | Process API: `ProcessBuilder`, `ProcessHandle` | подглава в Ch.54 |
| Part VI (Продвинутое) | **Foreign Function & Memory API** (Project Panama, замена JNI) — критично для книги «на базе SE 25» | новая Chapter 65 |
| Part VI | Vector API (SIMD, incubating) — кратко, для полноты картины | подглава в Ch.65 |
| Part VI | **Java Idioms & Design Patterns**: Builder, Immutable Value Objects, Fluent API, defensive copying, fail-fast — то, что явно просили как «best practice» | новая Chapter 64 |
| Part VI | API design & library authoring (naming, exception design, версионирование) — перекрёстная ссылка на Part I, Chapter 21 | подглава в Ch.64 |
| Part VI | Каталог антипаттернов и code smells (God Object, exception swallowing, мутабельные статики) | новая глава или Appendix |

---

## 3. Найденные дублирования

| Где | Что дублируется | Рекомендация |
|---|---|---|
| 63.5 и 63.7 | Оба перечисляют одни и те же инструменты (`jcmd`, `jstat`, `jmap`, `jhsdb`) под разными заголовками | Слить в одну подглаву «Мониторинг и диагностика JVM» |
| 63.5 и 63.8 | `JFR` упомянут в обеих | Развести чётко: 63.5 = инструменты диагностики (jps/jstack/jstat/jmap/jcmd/jhsdb), отдельная подглава = профилирование (JFR/JMC/async-profiler) |
| 63.3 и 63.6 | Оба про Javadoc, разные акценты не разведены явно | Не сливать, но переименовать для ясности: 63.3 — «Javadoc как инструмент (генерация)», 63.6 — «Стиль и практики документирования» |
| Part I Ch.20 (Generics) и Part IV Ch.44 (Generics) | Риск пересказа одной темы дважды | Не дублировать контент: Part I — нормативный слой (термины, точные правила), Part IV — тренировочный слой (ловушки, quiz-примеры) со ссылками на Part I вместо повторной теории |
| Part I Ch.19 (Threads/JMM) и Part IV Ch.53 (Concurrency) | Аналогично — формальная модель памяти vs практическое API | Тот же принцип разделения |
| Part I Ch.8/9 vs Part IV Ch.40/41 | Широкое пересечение (примитивы, sealed, records, pattern matching объясняются дважды) | Общий принцип: Part IV не пересказывает теорию, а даёт «что выведет этот код» / разбор неверных ответов с отсылкой к конкретному пункту Part I |
| Part III Ch.31.2 (модули, вводно) и Part VI Ch.60 (модули, глубоко) | Потенциальное дублирование механики JPMS | Явно развести по глубине: 31.2 — «как написать и запустить module-info.java», 60.1 — «алгоритм разрешения модулей, service loader на уровне механики» |

---

## 4. Предложение: опциональная Part VII

Отдельно стоит рассмотреть — но это уже выход за пределы «языка и платформы» в сторону общей инженерной практики:

**Part VII. Инженерная практика вокруг Java** *(опционально, требует вашего решения о scope)*
- Логирование: JUL vs SLF4J/Logback — концепции, не привязка к конкретному фреймворку
- Конфигурация приложений: `Properties`, переменные окружения, паттерны внешней конфигурации
- Основы DI как концепции (framework-agnostic), прежде чем читатель уйдёт в Spring/Micronaut
- Тестирование глубже: параметризованные тесты, моки как концепция, property-based testing
- Контейнеризация: JVM в Docker, лимиты памяти, CDS/AppCDS в контейнере
- Наблюдаемость: базовые понятия метрик/трейсинга (без привязки к конкретному стеку)

Это логичное продолжение, но решение — намеренно ваше: с одной стороны, это то, что реально нужно «практикующему разработчику», с другой — книга рискует расшириться за пределы «Java как языка и платформы» в сторону общего software engineering. Можно оставить как явно помеченную опциональную часть, которая растёт по мере вашей реальной разработки (вы упомянули, что материал будет добавляться по ходу дела) — это хорошо ложится именно сюда.

---

## 5. Итоговая сводка изменений в Part I

- Было 20 глав → стало 23: добавлены Ch.16 (Definite Assignment), Ch.18 (Execution), Ch.21 (Binary Compatibility) как полноценные новые главы.
- Заполнены пробелы внутри существующих глав: Sealed Classes/Interfaces (8.9, 9.5), Nested/Inner Classes на уровне спецификации (8.10), Private Interface Methods (9.6), Reachability (14.8).
- Во все главы 5–22 добавлена финальная подглава «Типичные ошибки / best practices» по образцу Chapter 13 (Arrays) — единообразный шаблон на всю Part I.
- Control-transfer statements (`break`/`continue`/`return`) остались в Blocks/Statements (14.6), а не смешаны с Exceptions — более чистое разделение по смыслу.
- Добавлено приложение-мэппинг «глава книги ↔ параграф JLS SE 25» — раз вы намеренно отошли от прямой нумерации, эта таблица восстанавливает возможность быстрой сверки с первоисточником без переверстки всей книги под JLS.
