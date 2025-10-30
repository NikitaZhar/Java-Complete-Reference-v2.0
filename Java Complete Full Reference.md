2025-09-29 21:50
Tags: #Content

*(база: Java SE 25, состояние на 29.09.2025)*

> Источники структуры: 
> Java SE Specifications (JLS/JVMS, SE 25), API Overview (SE 25), JDK 25 Documentation (Guides, Tools, Security, Specs).
> Boyarsky. Oracle Certified Professional Java SE 17 Developer Exam 1Z0-829
> Boyarsky. Oracle Certified Professional Java SE 21 Developer Exam 1Z0-830
> Mughal. Oracle Certified Professional Java SE 17 Developer Exam 1Z0-829
> Mughal. Oracle Certified Professional Java SE 21 Developer Exam 1Z0-830

[[Текст запроса]]

# Part I. Java Language Specification (JLS), Java SE 25
## [[Chapter 1. Introduction]]
## [[Chapter 2. Grammars (To Check)]]
## [[Chapter 3. Lexical Structure (to Check)]]


## [[Chapter 4. Types, Values, and Variables]]


### Chapter 5. Conversions and Contexts
5.1 Conversion Contexts  
5.2 Assignment Contexts  
5.3 Casting Contexts  
5.4 String Conversion  
5.5 Numeric Promotions  
5.6 Unboxing Conversion  
5.7 Value Set Conversion  
5.8 Widening and Narrowing Reference Conversions

### Chapter 6. Names
6.1 Declarations  
6.2 Names and Identifiers  
6.3 Scopes of Declarations  
6.4 Shadowing and Hiding  
6.5 Fully Qualified Names  
6.6 Access Control

### Chapter 7. Packages and Modules
7.1 Packages  
7.2 Compilation Units  
7.3 Package Declarations  
7.4 Module Declarations  
7.5 Visibility Rules

### Chapter 8. Classes
8.1 Class Declarations  
8.2 Class Members  
8.3 Fields  
8.4 Methods  
 8.4.1 Method Declarations  
 8.4.2 Method Signatures  
 8.4.3 Method Modifiers  
 8.4.3.1 abstract Methods  
 8.4.3.2 final Methods  
 8.4.4 Overloading  
8.5 Constructors  
8.6 Instance Initializers  
8.7 Static Initializers  
8.8 Enclosing Instances

### Chapter 9. Interfaces
9.1 Interface Declarations  
9.2 Interface Members  
9.3 Default Methods  
9.4 Functional Interfaces

### Chapter 10. Enums
10.1 Enum Types  
10.2 Enum Members  
10.3 Special Methods of Enums

### Chapter 11. Annotations
11.1 Annotation Types  
11.2 Annotation Declarations  
11.3 Annotation Processing

### Chapter 12. Records
12.1 Record Declarations  
12.2 Canonical Constructors  
12.3 Compact Constructors

### Chapter 13. Arrays
13.1 Array Types  
13.2 Array Creation and Access

### Chapter 14. Blocks, Statements, and Patterns
14.1 Blocks  
14.2 Local Variable Declarations  
14.3 If Statements  
14.4 Switch Statements and Expressions  
14.5 Loops (while, do, for)  
14.6 Break, Continue, and Return  
14.7 Pattern Matching Constructs

### Chapter 15. Expressions
15.1 Primary Expressions  
15.2 Class Instance Creation Expressions  
15.3 Array Creation Expressions  
15.4 Field Access Expressions  
15.5 Method Invocation Expressions  
15.6 Lambda Expressions  
15.7 Conditional Expressions  
15.8 Assignment Expressions

### Chapter 16. Exceptions, Assertions, and Control Transfer
16.1 Exception Types  
16.2 try-catch-finally  
16.3 throw Statements  
16.4 assert Statements

### Chapter 17. Threads and Locks
17.1 The Java Memory Model  
17.2 Synchronized Blocks  
17.3 Volatile Variables  
17.4 Final Fields and Initialization Safety

### Chapter 18. Generics
18.1 Type Parameters  
18.2 Generic Methods  
18.3 Wildcards  
18.4 Capture Conversion

### Chapter 19. Previews and Features
19.1 Overview of Preview Features
19.2 Pattern Matching for `switch` — evolution and preview stages
19.3 Record Patterns — preview vs standard behavior
19.4 String Templates (Preview in Java 21)
19.5 Scoped Values (Preview in Java 21)
19.6 Structured Concurrency (Incubating API overview)
19.7 Preview-Feature Lifecycle and Migration Strategy

### Chapter 20. Appendices
A. Formal Grammars  
B. Index of Keywords  
C. Bibliography

## Part II. Java Virtual Machine Specification (JVMS), Java SE 25

### Chapter 1. Introduction
1.1 Structure of the Specification  
1.2 Notation

### Chapter 2. The Structure of the Java Virtual Machine
2.1 The ClassFile Structure  
2.2 Data Types  
2.3 Run-Time Data Areas  
2.4 Frames  
2.5 Representation of Objects  
2.6 Method Area and Heap

### Chapter 3. Compiling for the Java Virtual Machine
3.1 Class and Interface Declarations  
3.2 Fields and Methods  
3.3 Constant Pool  
3.4 Bytecode Instructions  
3.5 Exceptions and Finally  
3.6 Modules and Annotations

### Chapter 4. The ClassFile Format
4.1 The ClassFile Structure  
4.2 The Constant Pool  
4.3 Field_info Structure  
4.4 Method_info Structure  
4.5 Attributes (Code, LineNumberTable, StackMapTable, etc.)

### Chapter 5. Verification of Class Files
5.1 Type Checking  
5.2 Stack Map Frames  
5.3 Bytecode Verification Process

### Chapter 6. The Instruction Set
6.1 Load and Store Instructions  
6.2 Arithmetic Instructions  
6.3 Type Conversion Instructions  
6.4 Object Creation and Manipulation  
6.5 Method Invocation and Return  
6.6 Control Transfer Instructions  
6.7 Synchronization Instructions

### Chapter 7. Class Libraries
7.1 Role of Class Libraries in the JVM  
7.2 Java Base Module and Core Packages  
   _(java.lang, java.util, java.io, java.net и др.)_  
7.3 Interaction between JVM and Core Classes  
   _(например, загрузка классов ClassLoader, ошибки ClassNotFoundException)_  
7.4 Required Bootstrap Classes and Initialization Order  
7.5 Runtime Support for Reflection and Dynamic Proxies  
7.6 Class Loading Mechanism and Delegation Model  
7.7 Native Methods and JNI Interaction  
7.8 Security Manager (Deprecated but Relevant)  
7.9 Service Loader and SPI Integration  
7.10 Reflection and Dynamic Proxies – Performance and Security Notes

### Chapter 8. Miscellaneous
8.1 Deprecation and Obsolescence in the JVM  
8.2 Backward Compatibility Considerations  
8.3 Implementation-Dependent Behavior  
8.4 Error Handling in the JVM  
8.5 Compliance and Testing Notes  
8.6 Platform-Specific Implementation Notes  
8.7 JVM Startup and Shutdown Sequence  
8.8 Error Reporting and Diagnostic Options  
8.9 Performance Guidelines and Implementation Notes

### Appendices
A. Summary of the Class File Format  
B. Summary of Instructions  
C. Glossary

## Part III. Practical Java Development
_(покрывает практическую работу с JDK, компиляцией, запуском, модулями, проектами)_

### Chapter 30. Java Development Kit in Practice
30.1 Installing and Configuring JDK  
30.2 Using `javac` — compilation, flags, options  
30.3 Using `java` — running programs, classpath, module-path  
30.4 Working with JAR files and manifests  
30.5 Tools for modular applications: `jdeps`, `jlink`, `jmod`  
30.6 Packaging applications with `jpackage`  
30.7 Using JShell for experiments

### Chapter 31. Program Structure and Modules
31.1 Source files, packages, compilation units  
31.2 Module system: `module-info.java`, exports, opens  
31.3 Migration of legacy code to modules  
31.4 Service loader and provider mechanism  
31.5 Main class and command-line arguments
31.6 Migrating from Classpath to Module-Path — typical steps and pitfalls
31.7 Automatic Modules and Unnamed Modules
31.8 Splitting Monolithic Applications into Modules
31.9 Layered Module Systems and Custom ClassLoaders

## Part IV. Core Java for Certification
_(покрывает языковые средства и стандартные библиотеки с практикой)_

### Chapter 40. Language Fundamentals
40.1 Primitive types, wrappers, autoboxing/unboxing  
40.2 Variables: local, instance, static, `final`, `var`, effectively final  
40.3 Operators and expressions, precedence and evaluation order  
40.4 Pattern matching in `instanceof` and `switch`  
40.5 Modern `switch` statements and expressions  
40.6 Records — declaration, canonical and compact constructors  
40.7 Sealed classes and interfaces — usage and restrictions

### Chapter 41. Classes, Objects, and Members
41.1 Class declaration, constructors, initialization blocks  
41.2 Inheritance, `super()`, `final`, `sealed`, `permits`  
41.3 Abstract classes and interfaces (including default and static methods)
## [[41.4 Overloading vs overriding]]
41.5 Nested, static nested, inner, local, and anonymous classes

### Chapter 42. Exceptions and Error Handling
42.1 Checked vs unchecked exceptions  
42.2 `try-with-resources` and AutoCloseable  
42.3 Multi-catch and suppressed exceptions  
42.4 Custom exception classes  
42.5 Assertions and usage scenarios

### Chapter 43. Java Memory Model and Garbage Collection
43.1 Java Memory Model overview  
43.2 Object reachability and GC process  
43.3 Finalization (legacy) and Cleaner API  
43.4 Common GC-related pitfalls

### Chapter 44. Generics
44.1 Generic classes and methods  
44.2 Bounded type parameters and wildcards  
44.3 Type inference and `var`  
44.4 Erasure and limitations of generics

## Part V. Standard API in Practice
_(практическая работа с ключевыми библиотеками, включая современные подходы)_

### Chapter 50. Strings, Text, and Formatting
50.1 Strings, immutability, `StringBuilder`, `StringBuffer`  
50.2 Text blocks and escape sequences  
50.3 Regular expressions (`java.util.regex`)  
50.4 Number and date formatting (`NumberFormat`, `DateTimeFormatter`)  
50.5 Locale-aware formatting
50.6 Internationalization API (Character Sets, Charsets, BreakIterator)

### Chapter 51. Collections and Data Structures
51.1 Collections Framework overview  
51.2 Interfaces and implementations: List, Set, Map, Queue, Deque  
51.3 HashMap, TreeMap, LinkedHashMap, HashSet, TreeSet  
51.4 PriorityQueue, ArrayDeque  
51.5 Immutable collections and factory methods  
51.6 Sequenced collections (Java 21+)  
51.7 `Optional` and best practices

### Chapter 52. Functional Programming and Streams
52.1 Lambda expressions — syntax and scoping  
52.2 Method references
## [[52.3 Built-in functional interfaces (Predicate, Function, Supplier, Consumer, Comparator)]]  
52.4 Streams API — creation, intermediate and terminal operations  
52.5 Primitive streams and OptionalInt/Long/Double  
52.6 Collectors, grouping, partitioning, summarizing  
52.7 Parallel streams and performance considerations

### Chapter 53. Concurrency and Multithreading
53.1 Threads — creation, lifecycle, join, interrupt  
53.2 Platform vs Virtual Threads (Project Loom)  
53.3 Synchronization, `volatile`, intrinsic locks  
53.4 Concurrency utilities — ExecutorService, Callable/Future, ScheduledExecutorService  
53.5 Concurrent collections and atomic classes  
53.6 Latches, barriers, semaphores  
53.7 CompletableFuture and async programming  
53.8 ForkJoinPool and parallel algorithms
53.9 Structured Concurrency API — motivation, concepts, examples
53.10 Scoped Values — usage and comparison with ThreadLocal
53.11 Best Practices for Mixing Virtual and Platform Threads

### Chapter 54. Input/Output and NIO.2
54.1 Classic I/O streams — InputStream, OutputStream, Reader, Writer  
54.2 Buffering and decoration  
54.3 Working with files — File, RandomAccessFile  
54.4 NIO.2 Path, Files, FileVisitor, WatchService  
54.5 Character encoding and decoding  
54.6 Channels, Buffers, MappedByteBuffer  
54.7 Working with ZIP/JAR archives
54.8 File Attribute Views and Advanced File Operations
54.9 Asynchronous I/O (AsynchronousFileChannel, CompletionHandler)

### Chapter 55. Serialization
55.1 Serializable and transient  
55.2 Custom serialization (readObject, writeObject, readResolve)  
55.3 Record serialization and compatibility

### Chapter 56. Database Access with JDBC
56.1 Connecting with DriverManager and DataSource  
56.2 Statement vs PreparedStatement  
56.3 ResultSet navigation and updates  
56.4 Transactions and savepoints  
56.5 Batch updates and metadata

### Chapter 57. Date, Time, and Localization
57.1 java.time API — LocalDate, LocalTime, LocalDateTime, Instant, ZonedDateTime  
57.2 Period and Duration  
57.3 TemporalAdjusters and ChronoUnit  
57.4 Locale and ResourceBundle  
57.5 Internationalized formatting of dates, numbers, messages


## [[Chapter 58. JSON Processing and Data Binding (Jackson, Gson, Jakarta JSON)]]

### [[Chapter 58. JSON Processing and Data Binding (Jackson, Gson, Jakarta JSON) - OLD]]


## Part VI. Advanced Java Topics
_(дополняет профессиональные аспекты)_

### Chapter 60. Modules and Deployment
60.1 Full JPMS model — exports, opens, requires  
60.2 Service provider mechanism  
60.3 Analysis and building with jdeps, jlink, jmod  
60.4 JAR files and manifest attributes  
60.5 Packaging with JPackage
60.6 Multi-Release JARs
60.7 Versioning and Module Resolution

### Chapter 61. Security
61.1 Java security model overview  
61.2 Permissions, policies, and providers  
61.3 KeyStore and certificate handling  
61.4 Code signing and verification
61.5 Java Cryptography Architecture (JCA) — KeyFactory, Cipher, MessageDigest
61.6 Secure Communication with JSSE — SSL/TLS basics, handshake, certificates
61.7 Java Authentication and Authorization Service (JAAS) — login modules and policies
61.8 Managing Keys and Certificates with KeyTool and Keystore
61.9 Working with Policy Files and Permissions

### Chapter 62. Annotations and Reflection
62.1 Defining and using annotations  
62.2 Runtime retention and metadata access  
62.3 Annotation processing (JSR-269)  
62.4 Reflection API and dynamic proxies

### Chapter 63. Testing and Tooling
63.1 Unit testing (JUnit as example)  
63.2 JShell for rapid prototyping  
63.3 Using javadoc and the standard doclet
63.4 Debugging (jdb and IDE tools)  
63.5 Monitoring and profiling with jcmd, jfr, jconsole, jmap, jstat, jhsdb
## [[63.6 Writing Documentation with Javadoc — tags, doclets, linking (to split and format)]]
63.7 JVM Monitoring Tools — `jps`, `jstack`, `jstat`, `jmap`, `jcmd`, `jhsdb`
63.8 Profiling and Observability — JFR, JMC, async-profiler
63.9 JIT Compilation and Tiered Optimization Overview
63.10 GC Tuning Basics — collectors, ergonomics, options, common patterns

