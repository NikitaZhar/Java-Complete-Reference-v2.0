# Новое полное оглавление Java Complete Reference

Статус: replacement candidate после атомарной пересборки. База: Java SE 25. Разделы с `source-required` являются обязательными детализированными закладками: писать их без утверждённого source dossier запрещено. Каждый chapter при написании завершается явно пронумерованным подразделом «Типичные ошибки и практические рекомендации» (для JVM reference — «Практические следствия»); эта повторяющаяся строка не размножена в структурном каталоге, чтобы не маскировать предметные темы.

## Part I. Назначение, платформа и рабочая среда

### Chapter 1. Границы и устройство руководства

1.1 Аудитория и практические маршруты чтения  
1.2 Java language, Java SE, JDK, JVM и экосистема  
1.3 Нормативные, учебные и продуктовые источники  
1.4 Правила версионирования: LTS, preview, incubator, experimental, withdrawn, legacy  
1.5 Правила примеров, ошибок, перекрёстных ссылок и единственного дома  
1.6 Как проверять утверждения и воспроизводить примеры  

**Source basis:** JLS/JVMS/Oracle/project-contract.

### Chapter 2. JDK, инструменты и первый проект

2.1 Выбор дистрибутива и архитектуры JDK  
2.2 Установка, JAVA_HOME, PATH и параллельные JDK  
2.3 JDK, JRE, JVM и runtime image  
2.4 Структура исходников и результатов компиляции  
2.5 javac: source, target, release, classpath, module-path, lint и diagnostics  
2.6 java: class/source/JAR/module launch modes и JVM options  
2.7 Compact source files и instance main methods Java 25  
2.8 JShell: snippets, imports, state и reset  
2.9 IDE, formatter, inspections, debugger и terminal workflow  
2.10 Типичные ошибки установки, компиляции и запуска  

**Source basis:** Boyarsky/Mughal/Oracle JDK docs.

## Part II. Лексика, типы и выражения языка Java

### Chapter 3. Грамматики и лексическая обработка

3.1 Context-free, lexical и syntactic grammars  
3.2 Grammar notation: productions, alternatives, optionality и repetition  
3.3 Unicode input, UTF-16 и raw input characters  
3.4 Три lexical translation steps и Unicode escapes  
3.5 Line terminators, input elements, tokens и longest possible translation  
3.6 Whitespace и comments; Unicode-escape hazards  
3.7 Identifiers, Unicode identifier rules и underscore  
3.8 Keywords, contextual keywords, reserved const/goto и literals true/false/null  
3.9 Separators и полный набор operators  
3.10 Типичные лексические ошибки и невидимые символы  

**Source basis:** JLS 2-3; books cross-check.

### Chapter 4. Литералы и primitive types

4.1 Decimal, hexadecimal, octal и binary integer literals  
4.2 Integer literal typing, min-value special case, overflow и compile-time errors  
4.3 Decimal и hexadecimal floating-point literals  
4.4 IEEE 754: finite values, infinities, NaN и signed zero  
4.5 boolean type and values  
4.6 char как UTF-16 code unit; code point и surrogate pair  
4.7 Character, string и text-block literals  
4.8 Escape sequences, indentation и incidental whitespace text blocks  
4.9 Null literal и отсутствие null type values  
4.10 Primitive default values, ranges и representation caveats  
4.11 Integer и floating-point operations, overflow, underflow и rounding  
4.12 Типичные ошибки literals/primitive semantics  

**Source basis:** JLS 3.10,4.2; Boyarsky/Mughal.

### Chapter 5. Reference types, values и variables

5.1 Classes, interfaces, arrays и type variables как reference types  
5.2 Objects, references, identity и null reference  
5.3 Static type, runtime class, subtype и substitutability  
5.4 Object и String как специальные predefined classes  
5.5 Type variables, parameterized, raw, reifiable и intersection types — обзор  
5.6 Subtyping: primitive, class/interface и array  
5.7 Least upper bound и type projections — назначение  
5.8 Виды variables: local, parameter, field, array component, exception и pattern variable  
5.9 Instance versus static fields; default initialization  
5.10 final variables, blank final и constant variables  
5.11 var: допустимые contexts, initializer constraints и non-denotable inferred types  
5.12 Pass-by-value для primitives и references  
5.13 Scope versus lifetime; reachability basics  
5.14 Типичные ошибки типов и переменных  

**Source basis:** JLS 4; Boyarsky/Mughal.

### Chapter 6. Conversions и conversion contexts

6.1 Identity conversion  
6.2 Widening primitive conversion и потеря точности  
6.3 Narrowing primitive conversion: truncation, saturation, NaN  
6.4 Combined widening-narrowing primitive conversion  
6.5 Widening reference conversion  
6.6 Narrowing reference conversion: allowed, checked, unchecked и runtime checks  
6.7 Boxing conversion, wrapper caches и allocation  
6.8 Unboxing conversion и null-induced NPE  
6.9 Unchecked conversion  
6.10 Capture conversion  
6.11 String conversion  
6.12 Forbidden conversions  
6.13 Assignment context и constant narrowing с optional boxing  
6.14 Strict/loose invocation contexts  
6.15 String context  
6.16 Casting context  
6.17 Numeric context: unary/binary promotion и shifts  
6.18 Testing context  
6.19 Типичные ошибки conversions  

**Source basis:** JLS 5; Mughal/Boyarsky.

### Chapter 7. Names, declarations, scope и access

7.1 Kinds of declarations и declared entities  
7.2 Simple, qualified, canonical и fully qualified names  
7.3 Scope каждого вида declaration  
7.4 Shadowing: fields, locals, parameters и type parameters  
7.5 Hiding members и static methods  
7.6 Obscuring и ambiguous names  
7.7 Syntactic classification и reclassification of names  
7.8 Meaning of package/type/expression/method names  
7.9 Access control: public, protected, package и private  
7.10 protected через inheritance между packages  
7.11 Static imports, collisions и local precedence  
7.12 Module imports Java 25 и ambiguity  
7.13 Forward references и illegal self-reference  
7.14 Типичные ошибки names/access  

**Source basis:** JLS 6; books.

### Chapter 8. Operators и evaluation

8.1 Operator precedence и associativity  
8.2 Postfix/prefix increment and decrement  
8.3 Unary plus/minus, complement и logical negation  
8.4 Multiplicative, additive и string concatenation  
8.5 Shift operators и distance masking  
8.6 Relational operators и numeric comparison  
8.7 Equality: primitives, references, boxing и NaN  
8.8 Bitwise/logical &, ^, |  
8.9 Conditional && и ||; short-circuit  
8.10 Conditional operator typing и poly expressions  
8.11 Assignment и compound assignment hidden cast  
8.12 Evaluation order of operands, arguments и array components  
8.13 Abrupt completion и skipped evaluation  
8.14 Overflow, side effects и expression readability  

**Source basis:** JLS 15; Boyarsky/Mughal.

### Chapter 9. Primary expressions, creation и invocation

9.1 Literals, class literals, this и qualified this  
9.2 Parenthesized expressions и standalone/poly expressions  
9.3 Class instance creation и enclosing instances  
9.4 Array creation, initializer и access expressions  
9.5 Field access versus name access  
9.6 Method invocation forms  
9.7 Method applicability: strict, loose и variable arity phases  
9.8 Most-specific method, ambiguity и return type irrelevance  
9.9 Boxing, widening и varargs in overload selection  
9.10 Generic method inference during invocation  
9.11 Method references: static, bound, unbound, super и constructor  
9.12 Lambda expressions — синтаксический обзор и ссылка на functional chapter  
9.13 Cast expressions и intersection casts  
9.14 instanceof and pattern matching  
9.15 Типичные ошибки creation/invocation  

**Source basis:** JLS 15; books.

## Part III. Statements, declarations и object model

### Chapter 10. Blocks, statements и control flow

10.1 Statements, expression statements, empty statement и blocks  
10.2 Local declarations и scope inside blocks  
10.3 if/else, dangling else и boolean-only conditions  
10.4 Traditional switch labels, fall-through и scope  
10.5 Switch expressions, arrow rules, yield и result typing  
10.6 Exhaustiveness, enum/sealed coverage и MatchException  
10.7 null handling, pattern dominance и guarded patterns  
10.8 while и do-while  
10.9 Basic for: initialization, condition, update и multiple expressions  
10.10 Enhanced for over arrays и Iterable  
10.11 Labeled statements  
10.12 break, continue и return  
10.13 Reachability, can-complete-normally и unreachable statements  
10.14 Типичные control-flow ошибки  

**Source basis:** JLS 14; books.

### Chapter 11. Patterns

11.1 Type patterns и pattern variables  
11.2 Flow scoping through &&, ||, ! и conditional branches  
11.3 Pattern matching for instanceof  
11.4 Pattern switch: compatibility, applicability и dominance  
11.5 Record patterns and nested record patterns  
11.6 Exhaustiveness and sealed hierarchies  
11.7 Guards and side effects  
11.8 null case and default interaction  
11.9 Primitive patterns preview Java 25  
11.10 Unboxing/exactness considerations in primitive patterns  
11.11 Pattern evolution and compatibility risks  
11.12 Типичные pattern ошибки  

**Source basis:** JLS 14/15 SE25 preview specs.

### Chapter 12. Methods

12.1 Method declaration components и signature  
12.2 Formal parameters, receiver parameter и varargs  
12.3 Result types, void и return rules  
12.4 throws clause и type variables  
12.5 Method modifiers and legal combinations  
12.6 Instance, static, abstract, final, native, synchronized и strictfp context  
12.7 Overloading versus overriding versus hiding  
12.8 Override-equivalent signatures и subsignatures  
12.9 Covariant return types  
12.10 Access and checked-exception restrictions in overriding  
12.11 Default-method inheritance interaction  
12.12 Bridge methods as compiler consequence  
12.13 Recursion, parameter passing и stack considerations  
12.14 API-level method design pitfalls  

**Source basis:** JLS 8.4; Boyarsky/Mughal.

### Chapter 13. Classes, fields и initialization

13.1 Top-level, member, local и implicitly declared classes  
13.2 Class modifiers: abstract, final, sealed, non-sealed, strictfp legacy  
13.3 Type parameters, superclass и superinterfaces  
13.4 Class body, member inheritance и member access  
13.5 Instance/static fields и field modifiers  
13.6 Field hiding, forward references и constant variables  
13.7 Static initializer rules и execution order  
13.8 Instance initializers and instance variable initializers  
13.9 Initialization order across inheritance hierarchy  
13.10 this and super expressions  
13.11 Abstract classes and methods  
13.12 Final classes/methods and extension constraints  
13.13 Sealed hierarchies, permits inference и direct-subclass obligations  
13.14 Typical class declaration/initialization failures  

**Source basis:** JLS 8; books.

### Chapter 14. Constructors и object construction

14.1 Constructor declaration, signature и accessibility  
14.2 Default constructor and implicit declaration  
14.3 Generic constructors and throws  
14.4 Constructor overloading and selection  
14.5 this(...) and super(...) chaining  
14.6 Flexible constructor bodies Java 25: prologue/epilogue boundary  
14.7 Restrictions before constructor invocation  
14.8 Initialization procedure from allocation to subclass body  
14.9 Exceptional completion и partially constructed objects  
14.10 Leaking this and overridable calls from constructors  
14.11 Telescoping constructors, factories and Builder cross-reference  
14.12 Defensive validation and immutable construction  
14.13 Типичные constructor errors  

**Source basis:** JLS 8.8; books; JEP513.

### Chapter 15. Nested types и enclosing context

15.1 Static nested classes  
15.2 Inner member classes  
15.3 Local classes  
15.4 Anonymous classes  
15.5 Local/anonymous interfaces, enums и records restrictions  
15.6 Enclosing instance and qualified Outer.this  
15.7 Qualified super and inner-class construction  
15.8 Capture of final/effectively-final local variables  
15.9 Shadowing across nested scopes  
15.10 Static declarations in inner/local contexts  
15.11 Serialization, memory retention и synthetic implementation details  
15.12 Когда предпочесть top-level или composition  

**Source basis:** JLS 8/9/14; books.

### Chapter 16. Interfaces и functional types

16.1 Interface declarations, type parameters и extends  
16.2 Implicit modifiers and interface member kinds  
16.3 Constant fields and initialization  
16.4 Abstract interface methods and Object-method interaction  
16.5 Default methods  
16.6 Static interface methods  
16.7 Private interface methods  
16.8 Inheritance, overriding and default-method conflicts  
16.9 Sealed interfaces  
16.10 Functional interface definition and accidental breakage  
16.11 Function type, intersection target and @FunctionalInterface  
16.12 Annotation interfaces — boundary to Ch.18  
16.13 Типичные interface design ошибки  

**Source basis:** JLS 9; books.

### Chapter 17. Enums и records

17.1 Enum declaration, implicit superclass и instance control  
17.2 Enum constants, arguments и constant-specific class bodies  
17.3 Enum constructors, fields, methods и abstract members  
17.4 values, valueOf, name, ordinal и identity  
17.5 Enum serialization rules  
17.6 EnumSet/EnumMap and strategy/singleton usage  
17.7 Record declaration, components and implicit members  
17.8 Canonical constructor: normal and compact forms  
17.9 Validation, assignment and constructor accessibility  
17.10 Record equality, hashCode and toString contracts  
17.11 Generic, nested, local and serialized records  
17.12 Record restrictions, mutable components and defensive copying  
17.13 Records, patterns and domain-model trade-offs  

**Source basis:** JLS 8.9-8.10; books.

### Chapter 18. Annotations

18.1 Annotation interface declarations and element types  
18.2 Default element values and restrictions  
18.3 Normal, marker and single-element annotations  
18.4 Declaration versus type-use contexts  
18.5 Repeatable annotations and container contract  
18.6 Meta-annotations: Target, Retention, Documented, Inherited, Repeatable  
18.7 Standard annotations: Override, Deprecated, SuppressWarnings, SafeVarargs, FunctionalInterface  
18.8 Retention and reflection visibility  
18.9 Annotation presence/inheritance semantics  
18.10 Compile-time annotation processing boundary and link to Ch.39  
18.11 Annotation-driven design trade-offs  

**Source basis:** JLS 9; Mughal; Oracle processing docs.

### Chapter 19. Arrays

19.1 Array types, component types and dimensions  
19.2 Array variables and covariance  
19.3 Creation expressions and negative sizes  
19.4 Initializers and nested initializers  
19.5 Access, bounds checks and evaluation order  
19.6 ArrayStoreException and runtime component type  
19.7 Array members length and clone  
19.8 Class objects and reflection for arrays  
19.9 char[] is not String; security implications  
19.10 Multidimensional/jagged arrays  
19.11 System.arraycopy and Arrays copy/fill/setAll  
19.12 Sorting, searching, compare, mismatch and deep operations  
19.13 Arrays.asList and collection conversions  
19.14 Performance, memory layout caveats and concurrency  

**Source basis:** JLS 10; books.

### Chapter 20. Exceptions, assertions и resource safety

20.1 Throwable hierarchy: checked, unchecked and Error  
20.2 Causes: throw, VM detection, linkage and asynchronous exceptions  
20.3 Compile-time exception analysis  
20.4 throws compatibility and precise rethrow  
20.5 Stack propagation and handler selection  
20.6 try/catch order, multi-catch and alternatives  
20.7 finally semantics, abrupt completion and exception masking  
20.8 throw statement and rethrow  
20.9 Try-with-resources translation and close order  
20.10 Suppressed exceptions and retrieval  
20.11 AutoCloseable versus Closeable  
20.12 Custom exception hierarchy and context preservation  
20.13 Interruption: restore/propagate policy  
20.14 Assertions syntax, enablement and appropriate use  
20.15 Exception boundaries, logging and anti-patterns  

**Source basis:** JLS 11/14; books.

### Chapter 21. Generics

21.1 Type parameters and parameterized types  
21.2 Generic classes, interfaces, methods and constructors  
21.3 Bounds and multiple/intersection bounds  
21.4 Invariance and subtyping of parameterized types  
21.5 Unbounded wildcards  
21.6 Upper-bounded wildcards and producer reads  
21.7 Lower-bounded wildcards and consumer writes  
21.8 PECS limitations and API intent  
21.9 Wildcard capture and helper methods  
21.10 Type inference: invocation, diamond and target typing  
21.11 Raw types and migration compatibility  
21.12 Erasure and erased signatures  
21.13 Reifiable and non-reifiable types  
21.14 Bridge methods and overriding implications  
21.15 Heap pollution and unchecked warnings  
21.16 Generic arrays and creation restrictions  
21.17 Varargs with non-reifiable types and @SafeVarargs  
21.18 Recursive bounds and comparable patterns  
21.19 Типичные generics design mistakes  

**Source basis:** JLS 4/5/8/9/15; Mughal/Boyarsky.

### Chapter 22. Definite assignment и other compile-time guarantees

22.1 Definitely assigned before use  
22.2 Definitely unassigned before assignment  
22.3 Blank final fields  
22.4 Constructor and initializer obligations  
22.5 Branches and conditional expressions  
22.6 Loops, break and continue  
22.7 try/catch/finally and abrupt completion  
22.8 Boolean expressions and pattern variables  
22.9 Effectively final capture  
22.10 Reachability versus definite assignment  
22.11 Representative compiler diagnostics  

**Source basis:** JLS 16 and cross-chapters.

## Part IV. Packages, modules, compatibility и build

### Chapter 23. Packages, compilation units и imports

23.1 Ordinary and compact compilation units  
23.2 Unnamed, named and observable packages  
23.3 Package declarations and package annotations  
23.4 Top-level type declarations and file-name rules  
23.5 Single-type and on-demand imports  
23.6 Single-static and static-on-demand imports  
23.7 Module import declarations Java 25  
23.8 Import ambiguity, redundancy and java.lang  
23.9 Package naming, cycles and encapsulation  
23.10 Source path, class output and package-directory conventions  

**Source basis:** JLS 7; books.

### Chapter 24. JPMS и services

24.1 Module declarations, names and compilation units  
24.2 requires, requires transitive and requires static  
24.3 exports and qualified exports  
24.4 opens, open modules and qualified opens  
24.5 uses and provides-with  
24.6 Readability, accessibility and module graph  
24.7 Resolution, roots, observable modules and upgrade paths  
24.8 Unnamed and automatic modules  
24.9 Split packages and duplicate modules  
24.10 Services and ServiceLoader lifecycle  
24.11 Module layers and custom configurations  
24.12 Migration from classpath and reflective-access failures  
24.13 JPMS design and granularity trade-offs  

**Source basis:** JLS 7; Mughal/Boyarsky; Oracle.

### Chapter 25. Binary compatibility и API evolution

25.1 Source, binary and behavioral compatibility  
25.2 Binary names and type evolution  
25.3 Adding/removing/changing fields  
25.4 Constant inlining and static constants  
25.5 Adding/removing/changing methods and constructors  
25.6 Overloading changes and source recompilation surprises  
25.7 Changing inheritance, interfaces, abstract/default methods  
25.8 Generics erasure and signature evolution  
25.9 Sealed/record/enum evolution  
25.10 Modules and accessibility evolution  
25.11 Serialization compatibility boundary  
25.12 Deprecation, replacement and migration windows  
25.13 Semantic versioning and compatibility tests  

**Source basis:** JLS 13; Oracle migration docs.

### Chapter 26. JAR, packaging и JDK deployment tools

26.1 JAR structure, entries and metadata  
26.2 Manifest syntax and main/module attributes  
26.3 Executable and modular JARs  
26.4 Multi-release JAR design and hazards  
26.5 Signing and verification  
26.6 jar tool operations  
26.7 jdeps static dependency analysis  
26.8 jmod files and intended use  
26.9 jlink runtime images, plugins and service binding  
26.10 jpackage application images/installers  
26.11 CDS/AppCDS overview and archive lifecycle  
26.12 Reproducible artifacts, timestamps and provenance  

**Source basis:** Oracle JAR/JDK tool specs.

### Chapter 27. Maven

27.1 Coordinates, POM model and effective POM _(source-required)_  
27.2 Standard directory layout and lifecycle phases _(source-required)_  
27.3 Packaging types and lifecycle bindings _(source-required)_  
27.4 Plugins, goals, executions and configuration _(source-required)_  
27.5 Dependencies, mediation, transitivity and optional dependencies _(source-required)_  
27.6 Scopes and classpaths _(source-required)_  
27.7 DependencyManagement, BOM import and version alignment _(source-required)_  
27.8 Repositories, mirrors, settings and credentials _(source-required)_  
27.9 Profiles and environment-dependent build risks _(source-required)_  
27.10 Multi-module reactor and parent versus aggregator _(source-required)_  
27.11 Compiler/test/surefire/failsafe/jar plugins _(source-required)_  
27.12 Toolchains and Java release configuration _(source-required)_  
27.13 Resource filtering and reproducible-build controls _(source-required)_  
27.14 Wrapper, CI batch mode and dependency cache _(source-required)_  
27.15 Enforcer, dependency analysis and supply-chain checks _(source-required)_  
27.16 Publishing snapshots/releases and metadata _(source-required)_  
27.17 Типичные Maven failures and diagnostics _(source-required)_  

**Source basis:** source-required: official Maven docs + approved guide.

### Chapter 28. Gradle

28.1 Gradle wrapper and version pinning _(source-required)_  
28.2 Build lifecycle, initialization/configuration/execution _(source-required)_  
28.3 Tasks, inputs/outputs and incremental execution _(source-required)_  
28.4 Plugins and Java plugin model _(source-required)_  
28.5 Groovy versus Kotlin DSL boundary _(source-required)_  
28.6 Dependency configurations and variant-aware resolution _(source-required)_  
28.7 Constraints, platforms/BOMs and version catalogs _(source-required)_  
28.8 Repositories, metadata and dependency verification _(source-required)_  
28.9 Java toolchains and compilation options _(source-required)_  
28.10 Source sets and custom test suites _(source-required)_  
28.11 Multi-project and composite builds _(source-required)_  
28.12 Convention plugins and build logic isolation _(source-required)_  
28.13 Build cache, configuration cache and parallelism _(source-required)_  
28.14 Dependency locking and reproducibility _(source-required)_  
28.15 Publishing and plugin management _(source-required)_  
28.16 Типичные Gradle performance/configuration failures _(source-required)_  

**Source basis:** source-required: official Gradle docs + approved guide.

## Part V. Fundamental Java APIs

### Chapter 29. Object contracts, ordering и utility runtime APIs

29.1 Object identity and getClass  
29.2 equals equivalence contract  
29.3 hashCode contract and hash-based consequences  
29.4 toString and diagnostic representation  
29.5 clone/Cloneable legacy and copy alternatives  
29.6 Objects utility methods  
29.7 Comparable natural ordering contract  
29.8 Comparator composition, null handling and consistency with equals  
29.9 Wrapper classes, valueOf and caches  
29.10 Math versus StrictMath  
29.11 System properties/environment/streams/arraycopy  
29.12 Runtime, shutdown hooks and process termination  
29.13 ProcessBuilder and ProcessHandle  
29.14 Типичные contract violations  

**Source basis:** Mughal/Boyarsky/Java API.

### Chapter 30. Numbers, decimal arithmetic и randomness

30.1 Numeric wrappers and parsing/formatting boundary  
30.2 Unsigned integer operations  
30.3 BigInteger construction and arithmetic  
30.4 BigDecimal construction from String versus double  
30.5 Scale, precision, MathContext and rounding modes  
30.6 BigDecimal equals versus compareTo  
30.7 Monetary calculation and division traps  
30.8 RandomGenerator hierarchy and algorithms  
30.9 Splittable/jumpable/leapable generators  
30.10 ThreadLocalRandom and concurrency boundary  
30.11 SecureRandom, seeding and security boundary  
30.12 Reproducibility in tests  

**Source basis:** Mughal/Boyarsky/Java API.

### Chapter 31. Strings, Unicode и text processing

31.1 String construction, immutability and pool  
31.2 Literal interning and intern  
31.3 Concatenation and compiler/runtime strategies  
31.4 Indexing by char versus code point  
31.5 Core query/search/subsequence methods  
31.6 Transformation, case, strip/indent and lines  
31.7 StringBuilder capacity, mutation and chaining  
31.8 StringBuffer legacy synchronization boundary  
31.9 Formatter, formatted and format specifiers  
31.10 Scanner and tokenization pitfalls  
31.11 Regular-expression syntax and Pattern/Matcher lifecycle  
31.12 Groups, regions, replacements and quoting  
31.13 Catastrophic backtracking and untrusted regex  
31.14 Charset, encoder/decoder and CodingErrorAction  
31.15 Normalization and locale-sensitive case mapping  
31.16 BreakIterator and text boundaries  

**Source basis:** Books/Java API/Unicode references.

### Chapter 32. Collections contracts и implementations

32.1 Iterable, Iterator and for-each protocol  
32.2 Collection contract and optional operations  
32.3 List and ListIterator contracts  
32.4 ArrayList and LinkedList trade-offs  
32.5 Set contract; HashSet and LinkedHashSet  
32.6 SortedSet/NavigableSet and TreeSet  
32.7 Queue and Deque operation families  
32.8 ArrayDeque and PriorityQueue  
32.9 Map contract and views  
32.10 HashMap, LinkedHashMap and TreeMap  
32.11 IdentityHashMap, WeakHashMap and EnumMap  
32.12 SequencedCollection/Set/Map Java 21  
32.13 Immutable factories versus unmodifiable views  
32.14 Collections utility algorithms and wrappers  
32.15 Fail-fast iterators and ConcurrentModificationException scope  
32.16 Mutable keys/elements and broken invariants  
32.17 Complexity, memory and implementation-choice guidance  

**Source basis:** Books/Java API.

### Chapter 33. Functional programming и lambdas

33.1 Functional-interface target typing  
33.2 Lambda parameter forms and return compatibility  
33.3 Expression versus block bodies  
33.4 Variable capture, shadowing and this  
33.5 Lambda identity and serialization warning  
33.6 Method/constructor reference forms  
33.7 Predicate, Consumer, Supplier and Function families  
33.8 Bi-arity and primitive specializations  
33.9 UnaryOperator and BinaryOperator  
33.10 Function composition, andThen and compose  
33.11 Comparator as functional application with link to Ch.29  
33.12 Side effects, purity and effectively-final state  
33.13 Lambda versus anonymous class semantics  

**Source basis:** JLS 15/9; books/Java API.

### Chapter 34. Optional и Stream API

34.1 Optional purpose and non-goals  
34.2 Creation, query, transformation and fallback  
34.3 orElse versus orElseGet evaluation  
34.4 Optional primitives  
34.5 Stream source, pipeline, laziness and single use  
34.6 Stateless/stateful intermediate operations  
34.7 map, flatMap, filter, distinct, sorted, limit/take/drop  
34.8 Terminal matching, finding, reduction and iteration  
34.9 Primitive streams and numeric aggregation  
34.10 Collector contract: supplier/accumulator/combiner/finisher  
34.11 Built-in collectors: grouping, partitioning, mapping, reducing  
34.12 Custom collectors and characteristics  
34.13 Spliterator characteristics and traversal  
34.14 Encounter order, unordered and short-circuiting  
34.15 Parallel streams, common pool and associativity  
34.16 Side effects, interference and stateful lambdas  

**Source basis:** Books/Java API.

### Chapter 35. Date, time, locale и internationalization

35.1 ISO chronology and temporal type selection  
35.2 LocalDate, LocalTime and LocalDateTime  
35.3 Instant and epoch timeline  
35.4 OffsetDateTime versus ZonedDateTime  
35.5 ZoneId, ZoneRules and DST gaps/overlaps  
35.6 Duration versus Period  
35.7 TemporalUnit, TemporalField and ChronoUnit  
35.8 TemporalAdjuster and queries  
35.9 Clock injection and deterministic tests  
35.10 Parsing/formatting with DateTimeFormatter  
35.11 Locale construction and language tags  
35.12 ResourceBundle lookup and fallback  
35.13 Properties files and encoding  
35.14 NumberFormat, CompactNumberFormat and currency  
35.15 MessageFormat, ChoiceFormat and pluralization limitations  
35.16 Legacy Date/Calendar/TimeZone interop  

**Source basis:** Books/Java API.

### Chapter 36. I/O streams и console

36.1 Byte versus character streams  
36.2 InputStream/OutputStream contracts and partial reads  
36.3 Reader/Writer and charset boundaries  
36.4 Buffering, decoration and filter streams  
36.5 Data streams and binary formats  
36.6 Print streams/writers and swallowed errors  
36.7 Console and password input  
36.8 Scanner delimiter/locale traps  
36.9 RandomAccessFile  
36.10 Piped streams and threading caveats  
36.11 try-with-resources ownership and close policy  
36.12 Flush, buffering and durability misconceptions  

**Source basis:** Books/Java API.

### Chapter 37. NIO.2, channels и archives

37.1 Path creation, normalization, resolution and relativization  
37.2 Default/non-default file systems  
37.3 Files create/read/write/copy/move/delete semantics  
37.4 Links, real paths and traversal safety  
37.5 DirectoryStream and Files.list/walk resource ownership  
37.6 FileVisitor and recursive operations  
37.7 File attributes and attribute views  
37.8 Temporary files and secure permissions  
37.9 WatchService semantics and overflow  
37.10 Channels and channel/stream adaptation  
37.11 Buffer state: position/limit/capacity/flip/compact  
37.12 Scatter/gather and file channels  
37.13 MappedByteBuffer and unmapping caveats  
37.14 AsynchronousFileChannel and CompletionHandler  
37.15 ZIP/JAR file systems  
37.16 Atomicity, locking, TOCTOU and path traversal  

**Source basis:** Books/Java API.

### Chapter 38. Networking и HTTP client

38.1 URI syntax, normalization and encoding  
38.2 URL/URLConnection legacy boundary  
38.3 InetAddress and DNS caveats  
38.4 TCP Socket/ServerSocket lifecycle  
38.5 UDP DatagramSocket semantics  
38.6 Timeouts, interruption and resource ownership  
38.7 HttpClient configuration and reuse  
38.8 HttpRequest bodies, headers, timeout and method  
38.9 BodyHandlers/BodySubscribers and streaming  
38.10 Synchronous and asynchronous send  
38.11 Redirects, proxies, authentication and cookies  
38.12 HTTP/2 and executor behavior  
38.13 TLS/SSLContext boundary  
38.14 WebSocket lifecycle, backpressure and listeners  
38.15 RMI legacy boundary and remote-object caveats  
38.16 Cancellation, retries and idempotency cross-reference  

**Source basis:** Java API/Oracle docs; source-required for resilience.

### Chapter 39. Serialization, JSON и XML

39.1 Serializable marker and object graph traversal  
39.2 serialVersionUID and compatible evolution  
39.3 transient and default serialization  
39.4 writeObject/readObject and validation  
39.5 writeReplace/readResolve and singleton hazards  
39.6 Externalizable boundary  
39.7 Record and enum serialization rules  
39.8 ObjectInputFilter and deserialization threats  
39.9 Why native serialization is not a new external protocol  
39.10 JSON tree, streaming and binding models  
39.11 Jackson bookmark: mapper/config/modules/annotations  
39.12 Gson bookmark and behavioral differences  
39.13 JSON-P/JSON-B bookmark  
39.14 Unknown fields, nullability, polymorphism and cycles  
39.15 XML DOM/SAX/StAX models  
39.16 Secure XML configuration and XXE prevention  
39.17 Schema/transform boundaries  

**Source basis:** Books/Java serialization spec; source-required libraries.

### Chapter 40. JDBC

40.1 Driver loading and JDBC URL  
40.2 DriverManager versus DataSource  
40.3 Connection lifecycle and pooling boundary  
40.4 Statement, PreparedStatement and CallableStatement  
40.5 Parameter binding and SQL injection  
40.6 ResultSet types, concurrency and holdability  
40.7 Column mapping, null and temporal values  
40.8 Generated keys and batch updates  
40.9 Transactions, auto-commit and boundaries  
40.10 Isolation levels and anomalies  
40.11 Savepoints and rollback  
40.12 DatabaseMetaData and ResultSetMetaData  
40.13 Large objects and streaming  
40.14 RowSet overview  
40.15 Resource cleanup and exception chains  

**Source basis:** Books/JDBC spec/API.

### Chapter 41. Reflection, annotation processing и runtime metaprogramming

41.1 Class objects, class literals and class discovery  
41.2 Reflection type model: Class, Type, ParameterizedType, TypeVariable and WildcardType  
41.3 Members: Field, Method, Constructor, Parameter and modifiers  
41.4 Declared versus inherited members and synthetic/bridge flags  
41.5 Reflective construction, invocation and field access  
41.6 AccessibleObject, strong encapsulation and module opens  
41.7 Annotations at runtime and repeatable/inherited lookup  
41.8 Arrays and enums through reflection  
41.9 Dynamic proxies, invocation handlers and Object methods  
41.10 MethodHandle lookup, access modes and invocation  
41.11 VarHandle access modes and memory-order boundary  
41.12 Annotation processing rounds, elements, types and filer  
41.13 Processor discovery, generated sources and incremental-build concerns  
41.14 Class-File API for reading, transforming and generating class files  
41.15 Performance, caching, security and framework-use trade-offs  

**Source basis:** JLS metadata boundary; Java API; Oracle tools.

## Part VI. Concurrency, JVM и performance

### Chapter 42. Java Memory Model

42.1 Inter-thread actions and executions  
42.2 Program order and synchronization order  
42.3 Happens-before relation  
42.4 Visibility, ordering and atomicity  
42.5 Data races and correctly synchronized programs  
42.6 Monitor lock/unlock semantics  
42.7 volatile read/write semantics  
42.8 Thread start/join and interruption edges  
42.9 Final-field initialization safety  
42.10 Word tearing and non-atomic compound actions  
42.11 Safe publication patterns  
42.12 This escape and unsafe construction  
42.13 Out-of-thin-air and practical reasoning limits  

**Source basis:** JLS 17; books.

### Chapter 43. Threads, locks и thread-safe state

43.1 Thread creation, states and lifecycle  
43.2 start versus run, join and sleep  
43.3 Interruption protocol and cancellation  
43.4 Intrinsic locks and synchronized methods/blocks  
43.5 Wait/notify/notifyAll condition protocol  
43.6 Lock and ReentrantLock  
43.7 Condition objects  
43.8 ReadWriteLock and StampedLock  
43.9 Atomics and compare-and-set  
43.10 Atomic field updaters and LongAdder family  
43.11 ThreadLocal and InheritableThreadLocal  
43.12 Immutable, confined and guarded state  
43.13 Deadlock, livelock, starvation and lock ordering  
43.14 False sharing and contention awareness  

**Source basis:** Books/Java API.

### Chapter 44. Executors, synchronizers и concurrent collections

44.1 Executor, ExecutorService and task submission  
44.2 Callable, Future and cancellation  
44.3 Lifecycle: shutdown, shutdownNow and awaitTermination  
44.4 ThreadPoolExecutor sizing, queues and rejection  
44.5 ScheduledExecutorService  
44.6 ForkJoinPool, work stealing and managed blocking  
44.7 CompletableFuture creation and execution policies  
44.8 Completion composition, combination and racing  
44.9 Exception, timeout and cancellation handling in CompletionStage  
44.10 CountDownLatch, CyclicBarrier, Phaser and Semaphore  
44.11 Exchanger and lock-support boundary  
44.12 BlockingQueue implementations  
44.13 ConcurrentHashMap atomic operations  
44.14 CopyOnWrite collections and snapshots  
44.15 ConcurrentSkipList collections  
44.16 Thread-safe collection selection  

**Source basis:** Books/Java API.

### Chapter 45. Virtual threads и structured concurrency

45.1 Platform versus virtual thread execution model  
45.2 Thread.ofVirtual and factories  
45.3 Virtual-thread-per-task executor  
45.4 Blocking, parking and scheduler behavior  
45.5 Pinning causes, diagnostics and mitigation  
45.6 CPU-bound work and bounded resources  
45.7 ThreadLocal costs and Scoped Values  
45.8 Virtual threads with synchronized/I/O libraries  
45.9 Structured Concurrency goals, task-tree model and non-goals  
45.10 StructuredTaskScope concepts and Java 25 preview status  
45.11 Failure propagation, cancellation and subtasks  
45.12 Observability and thread dumps  
45.13 Choosing async pipelines versus virtual threads  

**Source basis:** Oracle/OpenJDK docs.

### Chapter 46. JVM structure, class files и bytecode

46.1 JVM versus implementation and public/private design  
46.2 Primitive/reference JVM types and values  
46.3 Runtime areas: pc, stacks, heap, method area and native stacks  
46.4 Frames, local variables and operand stack  
46.5 Runtime constant pool and symbolic references  
46.6 Special methods init/clinit and signature-polymorphic methods  
46.7 ClassFile header, versions and access flags  
46.8 Names and field/method descriptors  
46.9 Constant-pool entry families  
46.10 Fields, methods and attributes  
46.11 Code, exception table, line/local variable and stack-map attributes  
46.12 Annotations, records, nestmates, modules and permitted subclasses attributes  
46.13 Instruction categories and operand stack effects  
46.14 Method invocation opcodes and dispatch  
46.15 invokedynamic, method handles and bootstrap methods  
46.16 CONSTANT_Dynamic  
46.17 javap inspection workflow  

**Source basis:** JVMS 1-6/Oracle.

### Chapter 47. Loading, linking и initialization

47.1 JVM startup and initial class/main selection  
47.2 Bootstrap, platform and application class loaders  
47.3 User-defined loaders and delegation  
47.4 Array-class creation and loader identity  
47.5 Loading constraints and class identity  
47.6 Modules/layers in loading  
47.7 Linking: verification, preparation and resolution  
47.8 Class/interface/field/method resolution  
47.9 Method selection and overriding at JVM level  
47.10 Dynamic constant/call-site resolution  
47.11 Initialization triggers and non-triggers  
47.12 Initialization order for classes/interfaces  
47.13 Circularity and erroneous classes  
47.14 Class unloading and loader leaks  
47.15 Native binding and JVM termination  
47.16 ClassNotFoundException versus NoClassDefFoundError and linkage errors  

**Source basis:** JLS 12/JVMS 5.

### Chapter 48. JIT, allocation и performance reasoning

48.1 Interpreter, profiling and tiered compilation  
48.2 Inlining and speculative optimization  
48.3 Deoptimization and uncommon traps  
48.4 Escape analysis and scalar replacement  
48.5 Allocation paths, TLAB and zeroing  
48.6 Object layout and compressed references caveat  
48.7 Branching, locality and cache effects  
48.8 Boxing, streams and allocation measurement  
48.9 Warmup, steady state and profile pollution  
48.10 Throughput, latency, percentiles and coordinated omission  
48.11 JMH harness, forks, warmups and Blackhole  
48.12 Dead-code elimination and constant folding pitfalls  
48.13 Measure-first optimization workflow  

**Source basis:** Oracle HotSpot docs; source-required JMH/perf refs.

### Chapter 49. Garbage collection и memory diagnostics

49.1 Garbage collection goals, liveness and automatic-reclamation limits  
49.2 Reachability graph and GC roots  
49.3 Strong, soft, weak and phantom references  
49.4 ReferenceQueue and Cleaner  
49.5 Finalization legacy and removal direction  
49.6 Heap regions/generations and allocation pressure  
49.7 Minor/major/full collection terminology caveats  
49.8 Serial, Parallel, G1, ZGC and Shenandoah availability boundary  
49.9 Stop-the-world, concurrent phases and barriers  
49.10 Ergonomics and collector selection  
49.11 Heap sizing and container limits  
49.12 GC unified logging and interpretation  
49.13 Memory leaks versus high allocation rate  
49.14 OutOfMemoryError variants  
49.15 Native-memory categories and off-heap accounting  
49.16 Heap dump acquisition and dominator analysis  
49.17 Class-loader leaks and metaspace  

**Source basis:** Oracle GC/tuning docs.

### Chapter 50. Native interop и advanced platform APIs

50.1 JNI architecture and legacy use cases  
50.2 Native-access restrictions and integrity warnings  
50.3 FFM arenas and lifetime  
50.4 MemorySegment access and thread confinement  
50.5 MemoryLayout, alignment and native-memory var handles  
50.6 Linker, downcalls, upcalls and symbol lookup  
50.7 ABI, errno and native error handling  
50.8 Vector API status and species  
50.9 Foreign/native safety, testing and packaging  

**Source basis:** Oracle/OpenJDK; source-required.

## Part VII. Design, API engineering и Clean Architecture

### Chapter 51. Clean code и refactoring

51.1 Names as domain vocabulary _(source-required)_  
51.2 Functions, command-query separation and side effects _(source-required)_  
51.3 Class cohesion and responsibility _(source-required)_  
51.4 Coupling, dependencies and information hiding _(source-required)_  
51.5 Primitive obsession and value objects _(source-required)_  
51.6 Null, Optional and explicit invariants _(source-required)_  
51.7 Comments versus executable clarity _(source-required)_  
51.8 Error-handling structure _(source-required)_  
51.9 Duplication versus coincidental similarity _(source-required)_  
51.10 Code smells: long method/class, feature envy, shotgun surgery _(source-required)_  
51.11 Safe refactoring and characterization tests _(source-required)_  
51.12 Complexity budgets and avoiding speculative abstractions _(source-required)_  

**Source basis:** source-required: approved engineering sources.

### Chapter 52. SOLID и object-oriented design

52.1 SRP: actor/reason to change _(source-required)_  
52.2 OCP: stable abstractions and extension mechanisms _(source-required)_  
52.3 LSP: preconditions, postconditions and invariants _(source-required)_  
52.4 LSP failure examples in Java hierarchies _(source-required)_  
52.5 ISP: role interfaces and client-specific contracts _(source-required)_  
52.6 DIP: policy ownership and dependency direction _(source-required)_  
52.7 Dependency injection versus Dependency Inversion _(source-required)_  
52.8 Composition over inheritance _(source-required)_  
52.9 Law of Demeter and tell-dont-ask boundary _(source-required)_  
52.10 Cohesion/coupling trade-offs _(source-required)_  
52.11 When SOLID creates indirection without value _(source-required)_  

**Source basis:** source-required: approved SOLID sources.

### Chapter 53. Patterns и Java idioms

53.1 Factory Method and Abstract Factory _(source-required)_  
53.2 Builder and staged construction trade-offs _(source-required)_  
53.3 Strategy and policy injection _(source-required)_  
53.4 Template Method versus composition _(source-required)_  
53.5 Command and undo/queue boundaries _(source-required)_  
53.6 Adapter, Facade and anti-corruption role _(source-required)_  
53.7 Decorator versus inheritance _(source-required)_  
53.8 Proxy variants and transparency limits _(source-required)_  
53.9 Observer/events and lifecycle leaks _(source-required)_  
53.10 State pattern and explicit state machines _(source-required)_  
53.11 Chain of Responsibility _(source-required)_  
53.12 Repository and Unit of Work boundaries _(source-required)_  
53.13 Singleton hazards and enum singleton _(source-required)_  
53.14 Pattern selection by forces and consequences _(source-required)_  
53.15 Anti-patterns and pattern overuse _(source-required)_  

**Source basis:** source-required: approved pattern sources.

### Chapter 54. API и library design

54.1 Audience, use cases and minimal surface  
54.2 Naming, symmetry and consistency  
54.3 Encapsulation and implementation freedom  
54.4 Mutability, ownership and defensive copies  
54.5 Nullability, empty values and Optional policy  
54.6 Parameter objects, builders and overload growth  
54.7 Generic API variance and wildcard exposure  
54.8 Callbacks, blocking and thread-safety contracts  
54.9 Exception taxonomy and failure atomicity  
54.10 Resource ownership and AutoCloseable APIs  
54.11 Equality, ordering and identity choices  
54.12 Extensibility versus sealed/final design  
54.13 Source/binary/behavior compatibility  
54.14 Deprecation, migration and semantic versioning  
54.15 Documentation, examples and compatibility tests  

**Source basis:** JLS13 + source-required API sources.

### Chapter 55. Clean Architecture foundations

55.1 Business rules versus implementation details _(source-required)_  
55.2 Entities and enterprise-wide policies _(source-required)_  
55.3 Use cases/interactors and application-specific policy _(source-required)_  
55.4 Input and output boundaries _(source-required)_  
55.5 Controllers, presenters and gateways _(source-required)_  
55.6 Dependency Rule _(source-required)_  
55.7 Architectural circles and direction of source dependencies _(source-required)_  
55.8 Boundary models and data crossing boundaries _(source-required)_  
55.9 Framework independence _(source-required)_  
55.10 UI independence _(source-required)_  
55.11 Database independence _(source-required)_  
55.12 External-service independence _(source-required)_  
55.13 Testability as architectural consequence _(source-required)_  
55.14 What Clean Architecture does not prescribe _(source-required)_  

**Source basis:** source-required: approved Clean Architecture sources.

### Chapter 56. Ports and Adapters implementation in Java

56.1 Driving and driven sides _(source-required)_  
56.2 Input ports and use-case interfaces _(source-required)_  
56.3 Output ports and gateway interfaces _(source-required)_  
56.4 Inbound web/CLI/message adapters _(source-required)_  
56.5 Outbound persistence/HTTP/message adapters _(source-required)_  
56.6 DTO, command, result and domain mapping _(source-required)_  
56.7 Composition root without framework _(source-required)_  
56.8 Constructor injection and lifecycle ownership _(source-required)_  
56.9 Configuration as outer-layer detail _(source-required)_  
56.10 Transactions around use cases _(source-required)_  
56.11 Package-by-feature versus package-by-layer _(source-required)_  
56.12 Module boundaries and JPMS options _(source-required)_  
56.13 Avoiding anemic wrappers and mapping explosion _(source-required)_  

**Source basis:** source-required.

### Chapter 57. Domain, application и modular monolith

57.1 Domain entities, value objects and aggregates _(source-required)_  
57.2 Invariants and consistency boundaries _(source-required)_  
57.3 Domain services versus application services _(source-required)_  
57.4 Commands, queries and use-case orchestration _(source-required)_  
57.5 Domain events versus integration events _(source-required)_  
57.6 Repository abstraction and persistence ignorance _(source-required)_  
57.7 Transaction boundaries and outbox bookmark _(source-required)_  
57.8 Modules, published interfaces and internal packages _(source-required)_  
57.9 Dependency cycles and module graph _(source-required)_  
57.10 Modular monolith definition, forces and fitness criteria _(source-required)_  
57.11 Modular-monolith communication _(source-required)_  
57.12 Schema ownership _(source-required)_  
57.13 Evolution toward or away from services _(source-required)_  
57.14 When rich domain model is unnecessary _(source-required)_  
57.15 When Clean Architecture is excessive _(source-required)_  

**Source basis:** source-required.

### Chapter 58. Distributed-system design boundaries

58.1 Remote call as partial-failure boundary _(source-required)_  
58.2 Timeout budgets and cancellation _(source-required)_  
58.3 Retries, backoff, jitter and retry storms _(source-required)_  
58.4 Idempotency keys and deduplication _(source-required)_  
58.5 Circuit breaker, bulkhead and rate limiting _(source-required)_  
58.6 Synchronous versus asynchronous integration _(source-required)_  
58.7 Message delivery: at-most/at-least/effectively-once _(source-required)_  
58.8 Ordering, partitioning and poison messages _(source-required)_  
58.9 Saga orchestration/choreography _(source-required)_  
58.10 Eventual consistency and user-visible states _(source-required)_  
58.11 Outbox/inbox patterns _(source-required)_  
58.12 Clock, identity and correlation _(source-required)_  
58.13 API versioning and tolerant readers _(source-required)_  
58.14 Observability and security across boundaries _(source-required)_  

**Source basis:** source-required.

## Part VIII. Testing и quality engineering

### Chapter 59. Testing fundamentals и JUnit

59.1 Purpose of tests and risk-based test portfolio _(source-required)_  
59.2 Unit, component, integration, contract, system and acceptance boundaries _(source-required)_  
59.3 Test pyramid, trophy and context-dependent mix _(source-required)_  
59.4 Arrange-Act-Assert/Given-When-Then _(source-required)_  
59.5 Test names as behavior specifications _(source-required)_  
59.6 JUnit platform, engine and Jupiter _(source-required)_  
59.7 Lifecycle, instance modes and nested tests _(source-required)_  
59.8 Assertions, grouped and exception assertions _(source-required)_  
59.9 Parameterized, repeated and dynamic tests _(source-required)_  
59.10 Tags, conditions, timeouts and parallel execution _(source-required)_  
59.11 Fixtures, builders and object mothers _(source-required)_  
59.12 Deterministic time, randomness, locale and environment _(source-required)_  
59.13 Testing exceptions and side effects _(source-required)_  
59.14 Test readability and refactoring _(source-required)_  

**Source basis:** source-required: JUnit docs + approved testing sources.

### Chapter 60. Test doubles и isolation

60.1 Test doubles: purpose, classification and isolation boundary _(source-required)_  
60.2 Dummy, stub, spy, mock and fake distinctions _(source-required)_  
60.3 State-based versus interaction-based testing _(source-required)_  
60.4 Constructor injection and seams _(source-required)_  
60.5 Hand-written fakes versus mocking frameworks _(source-required)_  
60.6 Stubbing and verification _(source-required)_  
60.7 Strictness, overspecification and brittle tests _(source-required)_  
60.8 Mocking static/final/time boundaries trade-offs _(source-required)_  
60.9 In-memory substitutes and semantic mismatch _(source-required)_  
60.10 Testing behavior instead of implementation _(source-required)_  
60.11 Fixture leakage and test isolation _(source-required)_  

**Source basis:** source-required.

### Chapter 61. Integration, database и Testcontainers testing

61.1 Integration-test process and lifecycle _(source-required)_  
61.2 Temporary filesystem and network resources _(source-required)_  
61.3 Database schema/migration testing _(source-required)_  
61.4 Transaction rollback and committed-state tests _(source-required)_  
61.5 Real database versus embedded substitute _(source-required)_  
61.6 Testcontainers architecture and Docker dependency _(source-required)_  
61.7 Container lifecycle, wait strategies and readiness _(source-required)_  
61.8 Networks, dependencies and reusable fixtures _(source-required)_  
61.9 Dynamic properties and framework integration _(source-required)_  
61.10 Parallel tests and data isolation _(source-required)_  
61.11 Image pinning, pull policy and CI cache _(source-required)_  
61.12 Ryuk/resource cleanup and failure modes _(source-required)_  
61.13 Messaging/broker integration tests _(source-required)_  
61.14 Performance and scope control _(source-required)_  

**Source basis:** source-required: Testcontainers docs.

### Chapter 62. HTTP, contract и end-to-end testing

62.1 In-process versus real-server HTTP tests _(source-required)_  
62.2 Request/response, validation and error-contract tests _(source-required)_  
62.3 Consumer-driven contract purpose _(source-required)_  
62.4 Provider verification and compatibility _(source-required)_  
62.5 Schema contracts and tolerant evolution _(source-required)_  
62.6 Authentication/authorization test matrix _(source-required)_  
62.7 Timeout/retry/idempotency tests _(source-required)_  
62.8 End-to-end scope and environment ownership _(source-required)_  
62.9 UI boundary bookmark _(source-required)_  
62.10 Flaky-test taxonomy, quarantine and repair _(source-required)_  
62.11 Test data management and cleanup _(source-required)_  

**Source basis:** source-required.

### Chapter 63. Advanced verification и static quality

63.1 Property-based generators, shrinking and invariants _(source-required)_  
63.2 Mutation testing and surviving mutants _(source-required)_  
63.3 Concurrency testing, latches and deterministic coordination _(source-required)_  
63.4 Stress, soak and race-detection limitations _(source-required)_  
63.5 Performance tests versus JMH microbenchmarks _(source-required)_  
63.6 Load-test workload and percentiles _(source-required)_  
63.7 Compiler warnings and -Xlint policy _(source-required)_  
63.8 Static analysis and bug patterns _(source-required)_  
63.9 Formatting and style checks _(source-required)_  
63.10 Architecture fitness functions _(source-required)_  
63.11 Dependency/license/vulnerability checks _(source-required)_  
63.12 Coverage: line, branch and mutation interpretation _(source-required)_  
63.13 Quality gates based on risk _(source-required)_  

**Source basis:** source-required.

### Chapter 64. Testing architecture and frameworks

64.1 Testing domain entities and value objects _(source-required)_  
64.2 Testing use-case interactors _(source-required)_  
64.3 Testing ports with fakes _(source-required)_  
64.4 Adapter integration tests _(source-required)_  
64.5 Architecture dependency tests _(source-required)_  
64.6 Spring test context scope and slicing bookmark _(source-required)_  
64.7 Jakarta runtime testing bookmark _(source-required)_  
64.8 Reactive/async testing bookmark _(source-required)_  
64.9 Containerized system tests _(source-required)_  
64.10 Balancing confidence, speed and maintenance cost _(source-required)_  

**Source basis:** source-required.

## Part IX. Frameworks и data access

### Chapter 65. Dependency Injection containers

65.1 DI container vocabulary and responsibilities _(source-required)_  
65.2 Constructor, setter and field injection trade-offs _(source-required)_  
65.3 Bean/component discovery and explicit registration _(source-required)_  
65.4 Scopes and lifecycle _(source-required)_  
65.5 Factories/providers and lazy dependencies _(source-required)_  
65.6 Qualifiers and ambiguity _(source-required)_  
65.7 Circular dependencies _(source-required)_  
65.8 Interceptors/decorators/proxies _(source-required)_  
65.9 Configuration and environment binding _(source-required)_  
65.10 Container shutdown and resource lifecycle _(source-required)_  
65.11 Testing with and without container _(source-required)_  
65.12 Framework leakage and DIP confusion _(source-required)_  
65.13 Spring Core bookmark _(source-required)_  
65.14 CDI bookmark _(source-required)_  
65.15 Guice bookmark _(source-required)_  

**Source basis:** source-required: Spring/CDI/Guice official docs.

### Chapter 66. Spring Boot

66.1 Spring Boot purpose, architecture and relationship to Spring Framework _(source-required)_  
66.2 Spring application context and Boot startup _(source-required)_  
66.3 Starters and dependency management _(source-required)_  
66.4 Auto-configuration conditions and diagnostics _(source-required)_  
66.5 Configuration properties, profiles and external config _(source-required)_  
66.6 Bean lifecycle and proxy-based behavior _(source-required)_  
66.7 MVC/REST controllers and serialization _(source-required)_  
66.8 Validation and exception mapping _(source-required)_  
66.9 HTTP clients and resilience boundary _(source-required)_  
66.10 DataSource, transactions and migrations _(source-required)_  
66.11 Spring Data boundary _(source-required)_  
66.12 Security filter-chain bookmark _(source-required)_  
66.13 Scheduling, async and messaging bookmarks _(source-required)_  
66.14 Actuator health, metrics and readiness _(source-required)_  
66.15 Test slices, context caching and Testcontainers _(source-required)_  
66.16 AOT/native image constraints _(source-required)_  
66.17 Production configuration and graceful shutdown _(source-required)_  

**Source basis:** source-required: official Spring docs.

### Chapter 67. Jakarta EE и MicroProfile

67.1 Platform profiles and runtime/container model _(source-required)_  
67.2 CDI injection, scopes, qualifiers and events _(source-required)_  
67.3 Jakarta REST resources and providers _(source-required)_  
67.4 Bean Validation _(source-required)_  
67.5 Jakarta Persistence boundary _(source-required)_  
67.6 Jakarta Transactions _(source-required)_  
67.7 Jakarta Security and authentication mechanisms _(source-required)_  
67.8 Jakarta Messaging _(source-required)_  
67.9 Concurrency utilities boundary _(source-required)_  
67.10 Packaging and deployment _(source-required)_  
67.11 MicroProfile Config _(source-required)_  
67.12 Health, Metrics/Telemetry and Fault Tolerance _(source-required)_  
67.13 REST Client and OpenAPI _(source-required)_  
67.14 Portability, vendor extensions and testing _(source-required)_  

**Source basis:** source-required: official specifications.

### Chapter 68. Persistence frameworks

68.1 Object-relational impedance and ORM trade-offs _(source-required)_  
68.2 JPA specification versus Hibernate implementation boundary _(source-required)_  
68.3 Persistence context and entity states _(source-required)_  
68.4 Identity, generated keys and equality _(source-required)_  
68.5 Basic, embedded and converted mappings _(source-required)_  
68.6 Associations and ownership _(source-required)_  
68.7 Fetch strategies and N+1 _(source-required)_  
68.8 Cascades and orphan removal _(source-required)_  
68.9 Queries, criteria and projections _(source-required)_  
68.10 Flush, dirty checking and transaction boundary _(source-required)_  
68.11 Optimistic and pessimistic locking _(source-required)_  
68.12 Batching and bulk operations _(source-required)_  
68.13 First/second-level/query caches _(source-required)_  
68.14 Schema generation versus migrations _(source-required)_  
68.15 jOOQ SQL-first model bookmark _(source-required)_  
68.16 MyBatis mapping model bookmark _(source-required)_  
68.17 JdbcTemplate bookmark _(source-required)_  
68.18 Choosing JDBC, mapper or ORM _(source-required)_  

**Source basis:** source-required: JPA/Hibernate/jOOQ/MyBatis docs.

### Chapter 69. Reactive и messaging frameworks

69.1 Reactive Streams Publisher/Subscriber/Subscription/Processor _(source-required)_  
69.2 java.util.concurrent.Flow mapping and adapters _(source-required)_  
69.3 Demand and backpressure _(source-required)_  
69.4 Cold versus hot publishers _(source-required)_  
69.5 Operators, scheduling and context _(source-required)_  
69.6 Error, cancellation and resource handling _(source-required)_  
69.7 Reactor/RxJava bookmark _(source-required)_  
69.8 Reactive HTTP/database boundary _(source-required)_  
69.9 Virtual threads versus reactive pipelines _(source-required)_  
69.10 Broker, queue, topic, partition and consumer group _(source-required)_  
69.11 Kafka producer/consumer delivery semantics _(source-required)_  
69.12 Offsets, rebalance and idempotent producer _(source-required)_  
69.13 JMS model bookmark _(source-required)_  
69.14 Serialization/schema evolution _(source-required)_  
69.15 Retry, dead-letter and poison messages _(source-required)_  
69.16 Testing and observability _(source-required)_  

**Source basis:** source-required: Reactive Streams/Reactor/Kafka/JMS docs.

### Chapter 70. Cloud-native and AOT frameworks

70.1 Build-time processing versus runtime reflection _(source-required)_  
70.2 Quarkus architecture bookmark _(source-required)_  
70.3 Micronaut architecture bookmark _(source-required)_  
70.4 Configuration and DI differences _(source-required)_  
70.5 Dev mode and testing _(source-required)_  
70.6 Native-image closed-world assumptions _(source-required)_  
70.7 Reflection/resource/proxy configuration _(source-required)_  
70.8 Initialization at build/run time _(source-required)_  
70.9 Startup, memory and throughput trade-offs _(source-required)_  
70.10 Observability and deployment _(source-required)_  
70.11 Framework selection criteria and lock-in _(source-required)_  

**Source basis:** source-required: Quarkus/Micronaut/GraalVM docs.

## Part X. Security, observability и diagnostics

### Chapter 71. Secure coding и supply chain

71.1 Threat modeling and trust boundaries  
71.2 Input validation and canonicalization  
71.3 Injection: SQL, command, template and log  
71.4 Path traversal and archive extraction  
71.5 SSRF and outbound-request controls  
71.6 Deserialization, polymorphic binding and gadget risks  
71.7 XML external entities  
71.8 Secrets and credential handling  
71.9 Sensitive data in memory/logs/errors  
71.10 Least privilege and secure defaults  
71.11 Dependency pinning, provenance and SBOM  
71.12 Vulnerability scanning and remediation  
71.13 Security Manager permanently disabled: legacy migration  
71.14 Security testing and review checklist  

**Source basis:** Mughal secure coding + Oracle + source-required.

### Chapter 72. Cryptography, TLS и identity

72.1 Cryptography goals, threat assumptions and misuse resistance  
72.2 JCA architecture and providers  
72.3 Secure algorithm and parameter selection  
72.4 MessageDigest and password-hashing distinction  
72.5 MAC  
72.6 Symmetric encryption and AEAD  
72.7 Public-key encryption and signatures  
72.8 Key generation, derivation and randomness  
72.9 KeyStore, certificates and keytool  
72.10 PKI and certificate validation  
72.11 JSSE, SSLContext and TLS handshake  
72.12 Hostname verification and trust managers  
72.13 Mutual TLS  
72.14 Authentication versus authorization  
72.15 JAAS historical/current context  
72.16 Crypto agility and key rotation  

**Source basis:** Oracle Security docs.

### Chapter 73. Logging, metrics и tracing

73.1 Events, logs, metrics and traces  
73.2 JUL architecture and configuration  
73.3 Logging facade versus implementation  
73.4 Levels and guarded/lazy logging  
73.5 Structured logging and stable fields  
73.6 Exception logging and duplicate logs  
73.7 Correlation IDs and context propagation  
73.8 Redaction and sensitive-data policy  
73.9 Metric types, labels and cardinality  
73.10 Health, readiness and liveness  
73.11 SLI/SLO and actionable signals  
73.12 Distributed tracing, spans and sampling  
73.13 OpenTelemetry bookmark  
73.14 Observability for async/virtual-thread flows  

**Source basis:** Mughal logging + source-required observability.

### Chapter 74. Debugging and production diagnostics

74.1 IDE and jdb debugging  
74.2 JDWP remote-debugging security  
74.3 Thread dumps and thread-state analysis  
74.4 Deadlock and contention diagnosis  
74.5 Heap dumps and retained-size analysis  
74.6 jps, jcmd, jstack, jmap and jstat  
74.7 jhsdb and serviceability boundary  
74.8 JFR recording, events and templates  
74.9 JMC analysis  
74.10 async-profiler CPU/allocation/lock profiling  
74.11 Native memory tracking  
74.12 GC and safepoint logs  
74.13 JMX/MBeans, connectors and remote-security boundary  
74.14 Production-safe evidence collection  
74.15 Incident timeline and hypothesis discipline  

**Source basis:** Oracle tool specs.

## Part XI. Containers, CI/CD и operations

### Chapter 75. Docker and containers for Java

75.1 Images, containers, layers and registries _(source-required)_  
75.2 Dockerfile instructions and build context _(source-required)_  
75.3 Multi-stage Java builds _(source-required)_  
75.4 Base-image selection and pinning _(source-required)_  
75.5 JAR/layered application image layout _(source-required)_  
75.6 Non-root users and filesystem permissions _(source-required)_  
75.7 Entrypoint, exec form and argument passing _(source-required)_  
75.8 Signals, PID 1 and graceful shutdown _(source-required)_  
75.9 CPU/memory limits and JVM container awareness _(source-required)_  
75.10 Heap/native-memory budgeting _(source-required)_  
75.11 GC in containers _(source-required)_  
75.12 Health checks and application readiness _(source-required)_  
75.13 Logs to stdout/stderr _(source-required)_  
75.14 Secrets and configuration mounts _(source-required)_  
75.15 Image scanning, SBOM and signing _(source-required)_  
75.16 CDS/AppCDS and startup optimization _(source-required)_  

**Source basis:** source-required: Docker + Oracle container docs.

### Chapter 76. CI pipelines for Java

76.1 Pipeline trigger, checkout and immutable revision _(source-required)_  
76.2 Pinned JDK and build-tool wrapper _(source-required)_  
76.3 Dependency caches versus reproducibility _(source-required)_  
76.4 Compile and unit-test stages _(source-required)_  
76.5 Integration tests and service containers _(source-required)_  
76.6 Testcontainers in CI _(source-required)_  
76.7 Static analysis and formatting _(source-required)_  
76.8 Security, license and dependency scanning _(source-required)_  
76.9 Artifact creation and provenance _(source-required)_  
76.10 Reports, coverage and test evidence _(source-required)_  
76.11 Secrets and least-privilege tokens _(source-required)_  
76.12 Matrix builds and supported JDKs _(source-required)_  
76.13 Parallelism, cancellation and flaky retries _(source-required)_  
76.14 Artifact repository publishing _(source-required)_  
76.15 GitHub Actions bookmark _(source-required)_  
76.16 GitLab CI bookmark _(source-required)_  
76.17 Jenkins bookmark _(source-required)_  

**Source basis:** source-required: platform docs.

### Chapter 77. Continuous delivery and deployment

77.1 Continuous Delivery definition, prerequisites and distinction from deployment _(source-required)_  
77.2 Build once, promote immutable artifact _(source-required)_  
77.3 Environment configuration and parity _(source-required)_  
77.4 Release metadata and traceability _(source-required)_  
77.5 Database migration compatibility _(source-required)_  
77.6 Expand-contract schema changes _(source-required)_  
77.7 Backward/forward application compatibility _(source-required)_  
77.8 Rolling deployment _(source-required)_  
77.9 Blue-green deployment _(source-required)_  
77.10 Canary deployment _(source-required)_  
77.11 Feature flags and kill switches _(source-required)_  
77.12 Readiness, startup and liveness semantics _(source-required)_  
77.13 Rollback versus roll-forward _(source-required)_  
77.14 Post-deployment verification _(source-required)_  
77.15 Kubernetes workload/resource/probe bookmark _(source-required)_  
77.16 ConfigMap/Secret boundary _(source-required)_  
77.17 Autoscaling and JVM implications _(source-required)_  
77.18 Disaster recovery and operational readiness _(source-required)_  

**Source basis:** source-required.

### Chapter 78. Production operation and reliability

78.1 Capacity, latency and throughput objectives _(source-required)_  
78.2 Timeout budgets across call chains _(source-required)_  
78.3 Resource pools and backpressure _(source-required)_  
78.4 Graceful degradation _(source-required)_  
78.5 Runbooks and alerts _(source-required)_  
78.6 Incident response and evidence preservation _(source-required)_  
78.7 Memory/CPU/thread leak triage _(source-required)_  
78.8 Safe runtime configuration changes _(source-required)_  
78.9 Backup/restore and data verification _(source-required)_  
78.10 Chaos/failure testing boundary _(source-required)_  
78.11 Postmortems and corrective actions _(source-required)_  
78.12 Upgrade and patch cadence _(source-required)_  

**Source basis:** source-required.

## Part XII. Documentation, migration и learning

### Chapter 79. Documentation and architecture records

79.1 Javadoc comment placement and first sentence  
79.2 Block and inline tags  
79.3 Links, references and inherited documentation  
79.4 Module/package/type/member documentation  
79.5 Standard doclet and generation options  
79.6 Snippet examples and executable verification  
79.7 README and getting-started contract  
79.8 ADR structure and decision lifecycle  
79.9 C4/architecture views bookmark  
79.10 API changelog and migration guide  
79.11 Documentation versioning and drift control  

**Source basis:** Oracle Javadoc docs + source-required.

### Chapter 80. Migration across Java and ecosystem versions

80.1 Release cadence and support policy  
80.2 Compile/runtime/source/binary matrix  
80.3 --release and multi-JDK testing  
80.4 Deprecated-for-removal and jdeprscan  
80.5 Illegal reflective access and strong encapsulation  
80.6 Classpath-to-module migration  
80.7 Preview/incubator feature migration  
80.8 Library and framework compatibility  
80.9 Serialization/data/schema compatibility  
80.10 Behavioral changes and regression tests  
80.11 Rolling upgrade compatibility  
80.12 Migration inventory and staged plan  

**Source basis:** Oracle migration docs + source-required frameworks.

### Chapter 81. Exercises, case study and certification map

81.1 Language rule exercises without new theory  
81.2 API and collections exercises  
81.3 Concurrency/JMM reasoning exercises  
81.4 JVM/diagnostics exercises  
81.5 Testing and build exercises  
81.6 Clean Architecture case study  
81.7 Framework adapter case study  
81.8 Docker/CI/CD delivery case study  
81.9 Secure-production-readiness review  
81.10 OCP 1Z0-829 objective map  
81.11 OCP 1Z0-830 objective map  
81.12 Answers linked to theoretical homes  

**Source basis:** Boyarsky/Mughal/project scope.

## Appendices

A. JLS SE 25 → атомарные темы → подразделы  
B. JVMS SE 25 → атомарные темы → подразделы  
C. Boyarsky/Mughal topic coverage map  
D. Java/JDK feature-version-status matrix  
E. Framework/tool version matrix  
F. JDK tools and diagnostic commands  
G. Anti-pattern and code-smell catalog  
H. Glossary and concept index  
I. Bibliography and source dossiers
