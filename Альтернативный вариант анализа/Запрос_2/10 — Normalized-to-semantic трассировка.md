# Normalized-to-semantic трассировка

Совместно с `02 — Source-to-normalized трассировка.md` образует полный путь source record → Normalized ID → Semantic ID.

| Normalized ID | Semantic ID | Topic | Cluster status | Source records |
|---|---|---|---|---|
| N-0001 | C-0001 | `@Deprecated` | unchanged | JLS SE 25#JLS-9.6.4.6 |
| N-0002 | C-0002 | `@FunctionalInterface` | unchanged | JLS SE 25#JLS-9.6.4.9 |
| N-0003 | C-0003 | `@Inherited` | unchanged | JLS SE 25#JLS-9.6.4.3 |
| N-0004 | C-0004 | `@Override` | unchanged | JLS SE 25#JLS-9.6.4.4 |
| N-0005 | C-0005 | `@Repeatable` | unchanged | JLS SE 25#JLS-9.6.4.8 |
| N-0006 | C-0006 | `@Retention` | unchanged | JLS SE 25#JLS-9.6.4.2 |
| N-0007 | C-0007 | `@SafeVarargs` | unchanged | JLS SE 25#JLS-9.6.4.7 |
| N-0008 | C-0008 | `@SuppressWarnings` | unchanged | JLS SE 25#JLS-9.6.4.5 |
| N-0009 | C-0009 | `@Target` | unchanged | JLS SE 25#JLS-9.6.4.1 |
| N-0010 | C-0010 | A Bit of History | unchanged | JVMS SE 25#JVMS-1.1 |
| N-0011 | C-0011 | aaload | structured-merge | JVMS SE 25#JVMS-0145 |
| N-0012 | C-0011 | aaload | structured-merge | JVMS SE 25#JVMS-0296 |
| N-0013 | C-0012 | aastore | structured-merge | JVMS SE 25#JVMS-0146 |
| N-0014 | C-0012 | aastore | structured-merge | JVMS SE 25#JVMS-0297 |
| N-0015 | C-0013 | About the MANIFEST.MF File | unchanged | Boyarsky 1Z0-830#S-0369 |
| N-0016 | C-0014 | Abrupt Completion of `do` Statement | unchanged | JLS SE 25#JLS-14.13.1 |
| N-0017 | C-0015 | Abrupt Completion of `for` Statement | unchanged | JLS SE 25#JLS-14.14.1.3 |
| N-0018 | C-0016 | Abrupt Completion of `while` Statement | unchanged | JLS SE 25#JLS-14.12.1 |
| N-0019 | C-0017 | Abrupt Method Invocation Completion | unchanged | JVMS SE 25#JVMS-2.6.5 |
| N-0020 | C-0018 | `abstract` Classes | structured-merge | JLS SE 25#JLS-13.4.1 |
| N-0021 | C-0018 | `abstract` Classes | structured-merge | JLS SE 25#JLS-8.1.1.1 |
| N-0022 | C-0019 | `abstract` Interfaces | unchanged | JLS SE 25#JLS-9.1.1.1 |
| N-0023 | C-0020 | `abstract` Methods | structured-merge | JLS SE 25#JLS-13.4.16 |
| N-0024 | C-0020 | `abstract` Methods | structured-merge | JLS SE 25#JLS-8.4.3.1 |
| N-0025 | C-0021 | Access Control | unchanged | JLS SE 25#JLS-6.6 |
| N-0026 | C-0022 | Access Control | unchanged | JVMS SE 25#JVMS-5.4.4 |
| N-0027 | C-0023 | Access Modifiers | merge | Boyarsky 1Z0-829#S-0132; Boyarsky 1Z0-830#S-0116 |
| N-0028 | C-0023 | Access Modifiers | merge | Mughal 1Z0-829#M829-6.5; Mughal 1Z0-830#M830-P2-6.5 |
| N-0029 | C-0024 | Access to a `protected` Constructor | unchanged | JLS SE 25#JLS-6.6.2.2 |
| N-0030 | C-0025 | Access to a `protected` Member | unchanged | JLS SE 25#JLS-6.6.2.1 |
| N-0031 | C-0026 | Accessing a static Variable or Method | unchanged | Boyarsky 1Z0-829#S-0157; Boyarsky 1Z0-830#S-0142 |
| N-0032 | C-0027 | Accessing Data with volatile | unchanged | Boyarsky 1Z0-829#S-0436 |
| N-0033 | C-0028 | Accessing Elements of a Vararg | unchanged | Boyarsky 1Z0-829#S-0147; Boyarsky 1Z0-830#S-0132 |
| N-0034 | C-0029 | Accessing static Data | unchanged | Boyarsky 1Z0-829#S-0155; Boyarsky 1Z0-830#S-0140 |
| N-0035 | C-0030 | Accessing Superclass Members using `super` | unchanged | JLS SE 25#JLS-15.11.2 |
| N-0036 | C-0031 | Accessing the Run-Time Constant Pool | unchanged | JVMS SE 25#JVMS-3.4 |
| N-0037 | C-0032 | Accessing the this Reference | unchanged | Boyarsky 1Z0-829#S-0182; Boyarsky 1Z0-830#S-0168 |
| N-0038 | C-0033 | Accessors for Java Virtual Machine Artifacts | unchanged | JVMS SE 25#JVMS-4.10.1.1 |
| N-0039 | C-0034 | Accounting for Daylight Saving Time | unchanged | Boyarsky 1Z0-829#S-0129; Boyarsky 1Z0-830#S-0113 |
| N-0040 | C-0035 | aconst_null | structured-merge | JVMS SE 25#JVMS-0147 |
| N-0041 | C-0035 | aconst_null | structured-merge | JVMS SE 25#JVMS-0298 |
| N-0042 | C-0036 | Acquiring Input with Console | unchanged | Boyarsky 1Z0-829#S-0482; Boyarsky 1Z0-830#S-0460 |
| N-0043 | C-0037 | Actions | unchanged | JLS SE 25#JLS-17.4.2 |
| N-0044 | C-0038 | Adapter integration tests | unchanged | Engineering scope#ENG-0264 |
| N-0045 | C-0039 | Adding a finally Block | unchanged | Boyarsky 1Z0-829#S-0354; Boyarsky 1Z0-830#S-0305 |
| N-0046 | C-0040 | Adding a Service Provider | unchanged | Boyarsky 1Z0-829#S-0397; Boyarsky 1Z0-830#S-0352 |
| N-0047 | C-0041 | Adding Data | unchanged | Boyarsky 1Z0-829#S-0273 |
| N-0048 | C-0042 | Adding Object Methods | unchanged | Boyarsky 1Z0-829#S-0250; Boyarsky 1Z0-830#S-0252 |
| N-0049 | C-0043 | Adding Optional Labels | unchanged | Boyarsky 1Z0-829#S-0089; Boyarsky 1Z0-830#S-0066 |
| N-0050 | C-0044 | Additional Argument Constraints | unchanged | JLS SE 25#JLS-18.5.2.2 |
| N-0051 | C-0045 | Additional Security Guidelines | unchanged | Mughal 1Z0-829#M829-26.4; Mughal 1Z0-830#M830-P2-26.4 |
| N-0052 | C-0046 | Additive Operators | unchanged | JLS SE 25#JLS-15.18 |
| N-0053 | C-0047 | Advantages of Exception Handling | unchanged | Mughal 1Z0-829#M829-7.8; Mughal 1Z0-830#M830-P2-7.8 |
| N-0054 | C-0048 | Aggregation | unchanged | Mughal 1Z0-829#M829-1.7; Mughal 1Z0-830#M830-P2-1.7 |
| N-0055 | C-0049 | Allowed Narrowing Reference Conversion | unchanged | JLS SE 25#JLS-5.1.6.1 |
| N-0056 | C-0050 | aload | unchanged | JVMS SE 25#JVMS-0299 |
| N-0057 | C-0051 | aload_<n> | unchanged | JVMS SE 25#JVMS-0300 |
| N-0058 | C-0052 | An Array of Characters Is Not a `String` | unchanged | JLS SE 25#JLS-10.9 |
| N-0059 | C-0053 | anewarray | structured-merge | JVMS SE 25#JVMS-0149 |
| N-0060 | C-0053 | anewarray | structured-merge | JVMS SE 25#JVMS-0301 |
| N-0061 | C-0054 | Annotation Interface Elements | unchanged | JLS SE 25#JLS-9.6.1 |
| N-0062 | C-0055 | Annotation Interfaces | structured-merge | JLS SE 25#JLS-13.5.8 |
| N-0063 | C-0055 | Annotation Interfaces | structured-merge | JLS SE 25#JLS-9.6 |
| N-0064 | C-0056 | Annotations | unchanged | JLS SE 25#JLS-9.7 |
| N-0065 | C-0057 | Annotations | unchanged | JVMS SE 25#JVMS-3.15 |
| N-0066 | C-0058 | Anonymous Class Declarations | unchanged | JLS SE 25#JLS-15.9.5 |
| N-0067 | C-0059 | Anonymous Classes | unchanged | Mughal 1Z0-829#M829-9.6; Mughal 1Z0-830#M830-P2-9.6 |
| N-0068 | C-0060 | Anonymous Constructors | unchanged | JLS SE 25#JLS-15.9.5.1 |
| N-0069 | C-0061 | Appendix Answers to Review Questions | unchanged | Boyarsky 1Z0-830#S-0468 |
| N-0070 | C-0062 | Appendix Answers to the Review Questions | unchanged | Boyarsky 1Z0-829#S-0518 |
| N-0071 | C-0063 | Application Security Overview | unchanged | Mughal 1Z0-829#M829-26.1; Mughal 1Z0-830#M830-P2-26.1 |
| N-0072 | C-0064 | Applying a Multi-catch Block | unchanged | Boyarsky 1Z0-829#S-0353; Boyarsky 1Z0-830#S-0304 |
| N-0073 | C-0065 | Applying Access Modifiers | unchanged | Boyarsky 1Z0-829#S-0149; Boyarsky 1Z0-830#S-0134 |
| N-0074 | C-0066 | Applying Annotations | unchanged | Mughal 1Z0-829#M829-25.3; Mughal 1Z0-830#M830-P2-25.3 |
| N-0075 | C-0067 | Applying Class Access Modifiers | unchanged | Boyarsky 1Z0-829#S-0181; Boyarsky 1Z0-830#S-0167 |
| N-0076 | C-0068 | Applying Effectively Final | unchanged | Boyarsky 1Z0-829#S-0358; Boyarsky 1Z0-830#S-0310 |
| N-0077 | C-0069 | Applying Guarded Logging | unchanged | Mughal 1Z0-829#M829-G.4 |
| N-0078 | C-0070 | Applying Pattern Matching to a Sealed Class | unchanged | Boyarsky 1Z0-830#S-0219 |
| N-0079 | C-0071 | Applying Records | unchanged | Boyarsky 1Z0-829#S-0228; Boyarsky 1Z0-830#S-0223 |
| N-0080 | C-0072 | Applying Scope to Classes | unchanged | Boyarsky 1Z0-829#S-0045 |
| N-0081 | C-0073 | Applying switch Statements | unchanged | Boyarsky 1Z0-829#S-0077 |
| N-0082 | C-0074 | Applying the Serializable Interface | unchanged | Boyarsky 1Z0-829#S-0473; Boyarsky 1Z0-830#S-0448 |
| N-0083 | C-0075 | Applying Unary Operators | unchanged | Boyarsky 1Z0-829#S-0054; Boyarsky 1Z0-830#S-0016 |
| N-0084 | C-0076 | Architecture dependency tests | unchanged | Engineering scope#ENG-0265 |
| N-0085 | C-0077 | Architecture fitness functions | unchanged | Engineering scope#ENG-0257 |
| N-0086 | C-0078 | areturn | structured-merge | JVMS SE 25#JVMS-0150 |
| N-0087 | C-0078 | areturn | structured-merge | JVMS SE 25#JVMS-0302 |
| N-0088 | C-0079 | Argument Lists are Evaluated Left-to-Right | unchanged | JLS SE 25#JLS-15.7.4 |
| N-0089 | C-0080 | Arithmetic | unchanged | JVMS SE 25#JVMS-3.3 |
| N-0090 | C-0081 | Arithmetic Instructions | unchanged | JVMS SE 25#JVMS-2.11.3 |
| N-0091 | C-0082 | Arithmetic Operators | unchanged | Boyarsky 1Z0-829#S-0058; Boyarsky 1Z0-830#S-0020 |
| N-0092 | C-0083 | Array Access | unchanged | JLS SE 25#JLS-10.4 |
| N-0093 | C-0084 | Array Access Expressions | unchanged | JLS SE 25#JLS-15.10.3 |
| N-0094 | C-0085 | Array Creation | unchanged | JLS SE 25#JLS-10.3 |
| N-0095 | C-0086 | Array Creation Expressions | unchanged | JLS SE 25#JLS-15.10.1 |
| N-0096 | C-0087 | Array Initializers | unchanged | JLS SE 25#JLS-10.6 |
| N-0097 | C-0088 | Array Members | unchanged | JLS SE 25#JLS-10.7 |
| N-0098 | C-0089 | Array Store Exception | unchanged | JLS SE 25#JLS-10.5 |
| N-0099 | C-0090 | Array Types | unchanged | JLS SE 25#JLS-10.1 |
| N-0100 | C-0091 | Array Variables | unchanged | JLS SE 25#JLS-10.2 |
| N-0101 | C-0092 | arraylength | structured-merge | JVMS SE 25#JVMS-0151 |
| N-0102 | C-0092 | arraylength | structured-merge | JVMS SE 25#JVMS-0303 |
| N-0103 | C-0093 | Arrays | merge | Boyarsky 1Z0-829#S-0170; Boyarsky 1Z0-830#S-0156 |
| N-0104 | C-0094 | Arrays | unchanged | JVMS SE 25#JVMS-3.9 |
| N-0105 | C-0093 | Arrays | merge | Mughal 1Z0-829#M829-3.9; Mughal 1Z0-830#M830-P2-3.9 |
| N-0106 | C-0095 | Artifact repository publishing | unchanged | Engineering scope#ENG-0419 |
| N-0107 | C-0096 | `assert` Statements | unchanged | JLS SE 25#JLS-16.2.8 |
| N-0108 | C-0097 | Assigning Values | unchanged | Boyarsky 1Z0-829#S-0060; Boyarsky 1Z0-830#S-0022 |
| N-0109 | C-0098 | Assignment Contexts | unchanged | JLS SE 25#JLS-5.2 |
| N-0110 | C-0099 | Assignment Expressions | unchanged | JLS SE 25#JLS-16.1.8 |
| N-0111 | C-0100 | Assignment Operator | unchanged | Boyarsky 1Z0-829#S-0061; Boyarsky 1Z0-830#S-0023 |
| N-0112 | C-0101 | Assignment Operators | unchanged | JLS SE 25#JLS-15.26 |
| N-0113 | C-0102 | Assumptions: The Meaning of "Must" | unchanged | JVMS SE 25#JVMS-6.1 |
| N-0114 | C-0103 | astore | unchanged | JVMS SE 25#JVMS-0304 |
| N-0115 | C-0104 | astore_<n> | unchanged | JVMS SE 25#JVMS-0305 |
| N-0116 | C-0105 | Asynchronous Exceptions | unchanged | JLS SE 25#JLS-11.1.3 |
| N-0117 | C-0106 | athrow | structured-merge | JVMS SE 25#JVMS-0153 |
| N-0118 | C-0106 | athrow | structured-merge | JVMS SE 25#JVMS-0306 |
| N-0119 | C-0107 | Attributes | unchanged | JVMS SE 25#JVMS-4.7 |
| N-0120 | C-0108 | Autoboxing | unchanged | Boyarsky 1Z0-829#S-0169; Boyarsky 1Z0-830#S-0155 |
| N-0121 | C-0109 | Automatic Modules | unchanged | Boyarsky 1Z0-829#S-0410; Boyarsky 1Z0-830#S-0368 |
| N-0122 | C-0110 | Automating Resource Management | unchanged | Boyarsky 1Z0-829#S-0355; Boyarsky 1Z0-830#S-0307 |
| N-0123 | C-0111 | baload | structured-merge | JVMS SE 25#JVMS-0154 |
| N-0124 | C-0111 | baload | structured-merge | JVMS SE 25#JVMS-0307 |
| N-0125 | C-0112 | Basic Language Elements | unchanged | Mughal 1Z0-829#M829-2.1; Mughal 1Z0-830#M830-P2-2.1 |
| N-0126 | C-0113 | Basic `try`-with-resources | unchanged | JLS SE 25#JLS-14.20.3.1 |
| N-0127 | C-0114 | Basics of Annotations | unchanged | Mughal 1Z0-829#M829-25.1; Mughal 1Z0-830#M830-P2-25.1 |
| N-0128 | C-0115 | Basics of Try-with-Resources | structured-merge | Boyarsky 1Z0-829#S-0357; Boyarsky 1Z0-830#S-0309 |
| N-0129 | C-0116 | bastore | structured-merge | JVMS SE 25#JVMS-0155 |
| N-0130 | C-0116 | bastore | structured-merge | JVMS SE 25#JVMS-0308 |
| N-0131 | C-0117 | Bean Validation | unchanged | Engineering scope#ENG-0306 |
| N-0132 | C-0118 | Benefits of Modules | unchanged | Boyarsky 1Z0-829#S-0378; Boyarsky 1Z0-830#S-0330 |
| N-0133 | C-0119 | Best Practices for Using Virtual Threads | unchanged | Mughal 1Z0-830#M830-P1-3.8 |
| N-0134 | C-0120 | Binding Native Method Implementations | unchanged | JVMS SE 25#JVMS-5.6 |
| N-0135 | C-0121 | bipush | structured-merge | JVMS SE 25#JVMS-0156 |
| N-0136 | C-0121 | bipush | structured-merge | JVMS SE 25#JVMS-0309 |
| N-0137 | C-0122 | Bitwise Complement Operator `~` | unchanged | JLS SE 25#JLS-15.15.5 |
| N-0138 | C-0123 | Bitwise Operators | unchanged | Boyarsky 1Z0-830#S-0031 |
| N-0139 | C-0124 | Blocks | structured-merge | JLS SE 25#JLS-14.2 |
| N-0140 | C-0124 | Blocks | structured-merge | JLS SE 25#JLS-16.2.2 |
| N-0141 | C-0124 | Blocks | structured-merge | JLS SE 25#JLS-6.3.2.1 |
| N-0142 | C-0125 | Blue-green deployment | unchanged | Engineering scope#ENG-0431 |
| N-0143 | C-0126 | Bookmarking with Savepoints | unchanged | Boyarsky 1Z0-829#S-0515 |
| N-0144 | C-0127 | Boolean Conditional Expressions | unchanged | JLS SE 25#JLS-15.25.1 |
| N-0145 | C-0128 | Boolean Constant Expressions | unchanged | JLS SE 25#JLS-16.1.1 |
| N-0146 | C-0129 | Boolean Expressions | unchanged | Mughal 1Z0-829#M829-2.11; Mughal 1Z0-830#M830-P2-2.11 |
| N-0147 | C-0130 | Boolean Literals | unchanged | JLS SE 25#JLS-3.10.3 |
| N-0148 | C-0131 | Bounded Type Parameters | unchanged | Mughal 1Z0-829#M829-11.6; Mughal 1Z0-830#M830-P2-11.6 |
| N-0149 | C-0132 | Bounding Generic Types | unchanged | Boyarsky 1Z0-829#S-0316 |
| N-0150 | C-0133 | Bounds | unchanged | JLS SE 25#JLS-18.1.3 |
| N-0151 | C-0134 | Bounds Involving Capture Conversion | unchanged | JLS SE 25#JLS-18.3.2 |
| N-0152 | C-0135 | Boxing Conversion | unchanged | JLS SE 25#JLS-5.1.7 |
| N-0153 | C-0136 | Building a JDBC URL | unchanged | Boyarsky 1Z0-829#S-0495 |
| N-0154 | C-0137 | Building Streams | unchanged | Mughal 1Z0-829#M829-16.4; Mughal 1Z0-830#M830-P2-16.4 |
| N-0155 | C-0138 | Bundling Resources | unchanged | Mughal 1Z0-829#M829-18.3; Mughal 1Z0-830#M830-P2-18.3 |
| N-0156 | C-0139 | Calculating Exponents | unchanged | Boyarsky 1Z0-829#S-0120; Boyarsky 1Z0-830#S-0100 |
| N-0157 | C-0140 | Calculating with Math APIs | unchanged | Boyarsky 1Z0-829#S-0116; Boyarsky 1Z0-830#S-0096 |
| N-0158 | C-0141 | Calling a CallableStatement | unchanged | Boyarsky 1Z0-829#S-0506 |
| N-0159 | C-0142 | Calling a Procedure without Parameters | unchanged | Boyarsky 1Z0-829#S-0507 |
| N-0160 | C-0143 | Calling Basic Methods | unchanged | Boyarsky 1Z0-829#S-0296 |
| N-0161 | C-0144 | Calling Constructors | unchanged | Boyarsky 1Z0-829#S-0024 |
| N-0162 | C-0145 | Calling Constructors | merge | Boyarsky 1Z0-829#S-0255 |
| N-0163 | C-0145 | Calling Constructors | merge | Boyarsky 1Z0-830#S-0257 |
| N-0164 | C-0146 | Calling Instance Methods on a Parameter | unchanged | Boyarsky 1Z0-829#S-0254; Boyarsky 1Z0-830#S-0256 |
| N-0165 | C-0147 | Calling Instance Methods on a Particular Object | unchanged | Boyarsky 1Z0-829#S-0253; Boyarsky 1Z0-830#S-0255 |
| N-0166 | C-0148 | Calling Methods That Throw Exceptions | unchanged | Boyarsky 1Z0-829#S-0343; Boyarsky 1Z0-830#S-0294 |
| N-0167 | C-0149 | Calling Methods with Varargs | unchanged | Boyarsky 1Z0-829#S-0146; Boyarsky 1Z0-830#S-0131 |
| N-0168 | C-0150 | Calling Overloaded Constructors with this() | unchanged | Boyarsky 1Z0-829#S-0187; Boyarsky 1Z0-830#S-0173 |
| N-0169 | C-0151 | Calling Parent Constructors with super() | unchanged | Boyarsky 1Z0-829#S-0188; Boyarsky 1Z0-830#S-0175 |
| N-0170 | C-0152 | Calling run() Instead of start() | unchanged | Boyarsky 1Z0-830#S-0384 |
| N-0171 | C-0153 | Calling static Methods | unchanged | Boyarsky 1Z0-829#S-0252; Boyarsky 1Z0-830#S-0254 |
| N-0172 | C-0154 | Calling the super Reference | merge | Boyarsky 1Z0-829#S-0183 |
| N-0173 | C-0155 | caload | structured-merge | JVMS SE 25#JVMS-0157 |
| N-0174 | C-0155 | caload | structured-merge | JVMS SE 25#JVMS-0310 |
| N-0175 | C-0156 | Canary deployment | unchanged | Engineering scope#ENG-0432 |
| N-0176 | C-0157 | Capture Conversion | unchanged | JLS SE 25#JLS-5.1.10 |
| N-0177 | C-0158 | Case null Is Considered Pattern Matching | unchanged | Boyarsky 1Z0-830#S-0055 |
| N-0178 | C-0159 | Cast Expressions | unchanged | JLS SE 25#JLS-15.16 |
| N-0179 | C-0160 | Casting Contexts | unchanged | JLS SE 25#JLS-5.5 |
| N-0180 | C-0161 | Casting Objects | unchanged | Boyarsky 1Z0-829#S-0240; Boyarsky 1Z0-830#S-0240 |
| N-0181 | C-0162 | Casting Values | unchanged | Boyarsky 1Z0-829#S-0062; Boyarsky 1Z0-830#S-0024 |
| N-0182 | C-0163 | castore | structured-merge | JVMS SE 25#JVMS-0158 |
| N-0183 | C-0163 | castore | structured-merge | JVMS SE 25#JVMS-0311 |
| N-0184 | C-0164 | Categories of Modules | unchanged | Mughal 1Z0-829#M829-19.11; Mughal 1Z0-830#M830-P2-19.11 |
| N-0185 | C-0165 | CDI bookmark | unchanged | Engineering scope#ENG-0284 |
| N-0186 | C-0166 | Chain of Responsibility | unchanged | Engineering scope#ENG-0122 |
| N-0187 | C-0167 | Chaining catch Blocks | unchanged | Boyarsky 1Z0-829#S-0352; Boyarsky 1Z0-830#S-0303 |
| N-0188 | C-0168 | Chaining Optionals | unchanged | Boyarsky 1Z0-829#S-0335 |
| N-0189 | C-0169 | Chapter 1: Building Blocks | unchanged | Boyarsky 1Z0-829#S-0519; Boyarsky 1Z0-830#S-0469 |
| N-0190 | C-0170 | Chapter 10: Streams | unchanged | Boyarsky 1Z0-829#S-0528; Boyarsky 1Z0-830#S-0478 |
| N-0191 | C-0171 | Chapter 12: Modules | unchanged | Boyarsky 1Z0-829#S-0530; Boyarsky 1Z0-830#S-0480 |
| N-0192 | C-0172 | Chapter 13: Concurrency | unchanged | Boyarsky 1Z0-829#S-0531; Boyarsky 1Z0-830#S-0481 |
| N-0193 | C-0173 | Chapter 15: JDBC | unchanged | Boyarsky 1Z0-829#S-0533 |
| N-0194 | C-0174 | Chapter 2: Operators | unchanged | Boyarsky 1Z0-829#S-0520; Boyarsky 1Z0-830#S-0470 |
| N-0195 | C-0175 | Chapter 3: Making Decisions | unchanged | Boyarsky 1Z0-829#S-0521; Boyarsky 1Z0-830#S-0471 |
| N-0196 | C-0176 | Chapter 4: Core APIs | unchanged | Boyarsky 1Z0-829#S-0522; Boyarsky 1Z0-830#S-0472 |
| N-0197 | C-0177 | Chapter 5: Methods | unchanged | Boyarsky 1Z0-829#S-0523; Boyarsky 1Z0-830#S-0473 |
| N-0198 | C-0178 | Chapter 6: Class Design | unchanged | Boyarsky 1Z0-829#S-0524; Boyarsky 1Z0-830#S-0474 |
| N-0199 | C-0179 | Chapter 7: Beyond Classes | unchanged | Boyarsky 1Z0-829#S-0525; Boyarsky 1Z0-830#S-0475 |
| N-0200 | C-0180 | Character Encoding in Java | unchanged | Boyarsky 1Z0-830#S-0440 |
| N-0201 | C-0181 | Character Literals | unchanged | JLS SE 25#JLS-3.10.4 |
| N-0202 | C-0182 | Characteristics of a Hierarchical File System | unchanged | Mughal 1Z0-829#M829-21.1; Mughal 1Z0-830#M830-P2-21.1 |
| N-0203 | C-0183 | Check Contents | unchanged | Boyarsky 1Z0-829#S-0277 |
| N-0204 | C-0184 | checkcast | structured-merge | JVMS SE 25#JVMS-0159 |
| N-0205 | C-0184 | checkcast | structured-merge | JVMS SE 25#JVMS-0312 |
| N-0206 | C-0185 | Checked Exception Classes | unchanged | Boyarsky 1Z0-829#S-0348; Boyarsky 1Z0-830#S-0299 |
| N-0207 | C-0186 | Checked Exception Constraints | unchanged | JLS SE 25#JLS-18.2.5 |
| N-0208 | C-0187 | Checking Functional Interfaces | unchanged | Boyarsky 1Z0-829#S-0263; Boyarsky 1Z0-830#S-0265 |
| N-0209 | C-0188 | Choosing the Most Specific Method | unchanged | JLS SE 25#JLS-15.12.2.5 |
| N-0210 | C-0189 | ChronoUnit for Differences | unchanged | Boyarsky 1Z0-830#S-0110 |
| N-0211 | C-0190 | Circular dependencies | unchanged | Engineering scope#ENG-0277 |
| N-0212 | C-0191 | Class Declarations | structured-merge | JLS SE 25#JLS-8.1 |
| N-0213 | C-0191 | Class Declarations | structured-merge | Mughal 1Z0-829#M829-3.1; Mughal 1Z0-830#M830-P2-3.1 |
| N-0214 | C-0192 | Class Initialization Methods | unchanged | JVMS SE 25#JVMS-2.9.2 |
| N-0215 | C-0193 | Class Instance Creation Expressions | unchanged | JLS SE 25#JLS-15.9 |
| N-0216 | C-0194 | Class Libraries | unchanged | JVMS SE 25#JVMS-2.12 |
| N-0217 | C-0195 | Class Literals | unchanged | JLS SE 25#JLS-15.8.2 |
| N-0218 | C-0196 | Class Loader Consistency | unchanged | JLS SE 25#JLS-12.2.2 |
| N-0219 | C-0197 | Class Members | unchanged | JLS SE 25#JLS-8.2 |
| N-0220 | C-0198 | Class Modifiers | structured-merge | Boyarsky 1Z0-829#S-0176; Boyarsky 1Z0-830#S-0162 |
| N-0221 | C-0198 | Class Modifiers | structured-merge | JLS SE 25#JLS-8.1.1 |
| N-0222 | C-0199 | `Class` Objects for Arrays | unchanged | JLS SE 25#JLS-10.8 |
| N-0223 | C-0200 | Class Type Parameters | unchanged | JLS SE 25#JLS-13.4.5 |
| N-0224 | C-0201 | Classes | unchanged | Mughal 1Z0-829#M829-1.2; Mughal 1Z0-830#M830-P2-1.2 |
| N-0225 | C-0202 | Classpath-to-module migration | unchanged | Engineering scope#ENG-0469 |
| N-0226 | C-0203 | Clearing the Collection | unchanged | Boyarsky 1Z0-829#S-0276 |
| N-0227 | C-0204 | Closing Database Resources | unchanged | Boyarsky 1Z0-829#S-0517 |
| N-0228 | C-0205 | Closing System Streams | unchanged | Boyarsky 1Z0-829#S-0481; Boyarsky 1Z0-830#S-0459 |
| N-0229 | C-0206 | Coding Functional Interfaces | unchanged | Boyarsky 1Z0-829#S-0248; Boyarsky 1Z0-830#S-0249 |
| N-0230 | C-0207 | Collecting Results | unchanged | Boyarsky 1Z0-829#S-0337 |
| N-0231 | C-0208 | Collections | unchanged | Mughal 1Z0-829#M829-15.2; Mughal 1Z0-830#M830-P2-15.2 |
| N-0232 | C-0209 | Collections with Well-Defined Encounter Order | unchanged | Mughal 1Z0-830#M830-P1-2.1 |
| N-0233 | C-0210 | Collectors | unchanged | Mughal 1Z0-829#M829-16.8; Mughal 1Z0-830#M830-P2-16.8 |
| N-0234 | C-0211 | Comments | structured-merge | Boyarsky 1Z0-829#S-0007 |
| N-0235 | C-0211 | Comments | structured-merge | JLS SE 25#JLS-3.7 |
| N-0236 | C-0212 | Compact Canonical Constructors | unchanged | JLS SE 25#JLS-8.10.4.2 |
| N-0237 | C-0213 | Comparing | unchanged | Boyarsky 1Z0-829#S-0113; Boyarsky 1Z0-830#S-0093 |
| N-0238 | C-0214 | Comparing Callable Statement Parameters | unchanged | Boyarsky 1Z0-829#S-0511 |
| N-0239 | C-0215 | Comparing Collection Types | unchanged | Boyarsky 1Z0-829#S-0302 |
| N-0240 | C-0216 | Comparing Data with a Comparator | unchanged | Boyarsky 1Z0-829#S-0305 |
| N-0241 | C-0217 | Comparing Deque Implementations | unchanged | Boyarsky 1Z0-829#S-0291 |
| N-0242 | C-0218 | Comparing List Implementations | unchanged | Boyarsky 1Z0-829#S-0282 |
| N-0243 | C-0219 | Comparing Map Implementations | unchanged | Boyarsky 1Z0-829#S-0294 |
| N-0244 | C-0220 | Comparing Multiple Fields | unchanged | Boyarsky 1Z0-829#S-0307 |
| N-0245 | C-0221 | Comparing Set Implementations | unchanged | Boyarsky 1Z0-829#S-0288 |
| N-0246 | C-0222 | Comparing to Virtual Threads | unchanged | Boyarsky 1Z0-830#S-0380 |
| N-0247 | C-0223 | Comparing Types of Modules | unchanged | Boyarsky 1Z0-829#S-0408; Boyarsky 1Z0-830#S-0366 |
| N-0248 | C-0224 | Comparing Values | unchanged | Boyarsky 1Z0-829#S-0065; Boyarsky 1Z0-830#S-0027 |
| N-0249 | C-0225 | Compilation Units | unchanged | JLS SE 25#JLS-7.3 |
| N-0250 | C-0226 | Compile-Time Checking of Exceptions | unchanged | JLS SE 25#JLS-11.2 |
| N-0251 | C-0227 | Compile-Time Declaration of a Method Reference | unchanged | JLS SE 25#JLS-15.13.1 |
| N-0252 | C-0228 | Compile-Time Step 1: Determine Type to Search | unchanged | JLS SE 25#JLS-15.12.1 |
| N-0253 | C-0229 | Compile-Time Step 2: Determine Method Signature | unchanged | JLS SE 25#JLS-15.12.2 |
| N-0254 | C-0230 | Compile-Time Step 3: Is the Chosen Method Appropriate? | unchanged | JLS SE 25#JLS-15.12.3 |
| N-0255 | C-0231 | Compiling `finally` | unchanged | JVMS SE 25#JVMS-3.13 |
| N-0256 | C-0232 | Compiling Our First Module | unchanged | Boyarsky 1Z0-829#S-0381; Boyarsky 1Z0-830#S-0333 |
| N-0257 | C-0233 | Compiling Sealed Classes | unchanged | Boyarsky 1Z0-829#S-0221; Boyarsky 1Z0-830#S-0214 |
| N-0258 | C-0234 | Compiling Switches | unchanged | JVMS SE 25#JVMS-3.10 |
| N-0259 | C-0235 | Compiling to Another Directory | unchanged | Boyarsky 1Z0-829#S-0019 |
| N-0260 | C-0236 | Compiling with JAR Files | unchanged | Boyarsky 1Z0-829#S-0020 |
| N-0261 | C-0237 | Complementary Pairs of Bounds | unchanged | JLS SE 25#JLS-18.3.1 |
| N-0262 | C-0238 | Composition over inheritance | unchanged | Engineering scope#ENG-0108 |
| N-0263 | C-0239 | Composition root without framework | unchanged | Engineering scope#ENG-0162 |
| N-0264 | C-0240 | Compound Assignment Operators | structured-merge | Boyarsky 1Z0-829#S-0063; Boyarsky 1Z0-830#S-0025 |
| N-0265 | C-0240 | Compound Assignment Operators | structured-merge | JLS SE 25#JLS-15.26.2 |
| N-0266 | C-0241 | Compute Target Reference (If Necessary) | unchanged | JLS SE 25#JLS-15.12.4.1 |
| N-0267 | C-0242 | Concatenating | unchanged | Boyarsky 1Z0-829#S-0097; Boyarsky 1Z0-830#S-0074 |
| N-0268 | C-0243 | Conceptualizing the File System | unchanged | Boyarsky 1Z0-829#S-0455; Boyarsky 1Z0-830#S-0424 |
| N-0269 | C-0244 | Concurrency utilities boundary | unchanged | Engineering scope#ENG-0311 |
| N-0270 | C-0245 | Conditional Operator `? :` | structured-merge | JLS SE 25#JLS-15.25 |
| N-0271 | C-0245 | Conditional Operator `? :` | structured-merge | JLS SE 25#JLS-16.1.5 |
| N-0272 | C-0245 | Conditional Operator `? :` | structured-merge | JLS SE 25#JLS-6.3.1.4 |
| N-0273 | C-0246 | Conditional Operators | unchanged | Boyarsky 1Z0-829#S-0069; Boyarsky 1Z0-830#S-0032 |
| N-0274 | C-0247 | Conditional-Or Operator `&#124;&#124;` | structured-merge | JLS SE 25#JLS-15.24 |
| N-0275 | C-0247 | Conditional-Or Operator `&#124;&#124;` | structured-merge | JLS SE 25#JLS-16.1.3 |
| N-0276 | C-0247 | Conditional-Or Operator `&#124;&#124;` | structured-merge | JLS SE 25#JLS-6.3.1.2 |
| N-0277 | C-0248 | Configuration as outer-layer detail | unchanged | Engineering scope#ENG-0164 |
| N-0278 | C-0249 | Configuring Logging | unchanged | Mughal 1Z0-829#M829-G.2 |
| N-0279 | C-0250 | Connecting to a Database | unchanged | Boyarsky 1Z0-829#S-0494 |
| N-0280 | C-0251 | Constant Expressions | unchanged | JLS SE 25#JLS-15.29 |
| N-0281 | C-0252 | Constraint Formulas | unchanged | JLS SE 25#JLS-18.1.2 |
| N-0282 | C-0253 | Constraints on Java Virtual Machine Code | unchanged | JVMS SE 25#JVMS-4.9 |
| N-0283 | C-0254 | Constructing for Loops | unchanged | Boyarsky 1Z0-829#S-0084; Boyarsky 1Z0-830#S-0060 |
| N-0284 | C-0255 | Constructing Initial Object State | unchanged | Mughal 1Z0-829#M829-10.9; Mughal 1Z0-830#M830-P2-10.9 |
| N-0285 | C-0256 | Constructing Locales | unchanged | Mughal 1Z0-830#M830-P1-C.2 |
| N-0286 | C-0257 | Constructor Body | unchanged | JLS SE 25#JLS-8.8.7 |
| N-0287 | C-0258 | Constructor Declarations | unchanged | JLS SE 25#JLS-8.8 |
| N-0288 | C-0259 | Constructor Invocations | unchanged | JLS SE 25#JLS-8.8.7.1 |
| N-0289 | C-0260 | Constructor Modifiers | unchanged | JLS SE 25#JLS-8.8.3 |
| N-0290 | C-0261 | Constructor Overloading | unchanged | JLS SE 25#JLS-8.8.8 |
| N-0291 | C-0262 | Constructor Signature | unchanged | JLS SE 25#JLS-8.8.2 |
| N-0292 | C-0263 | Constructor Throws | unchanged | JLS SE 25#JLS-8.8.5 |
| N-0293 | C-0264 | Constructors | unchanged | Mughal 1Z0-829#M829-3.7; Mughal 1Z0-830#M830-P2-3.7 |
| N-0294 | C-0265 | Consumer-driven contract purpose | unchanged | Engineering scope#ENG-0239 |
| N-0295 | C-0266 | Consumers | unchanged | Mughal 1Z0-829#M829-13.7; Mughal 1Z0-830#M830-P2-13.7 |
| N-0296 | C-0267 | Containerized system tests | unchanged | Engineering scope#ENG-0269 |
| N-0297 | C-0268 | Context-Free Grammars | unchanged | JLS SE 25#JLS-2.1 |
| N-0298 | C-0269 | Contexts for Defining Lambda Expressions | unchanged | Mughal 1Z0-829#M829-13.14; Mughal 1Z0-830#M830-P2-13.14 |
| N-0299 | C-0270 | Control Transfer Instructions | unchanged | JVMS SE 25#JVMS-2.11.7 |
| N-0300 | C-0271 | Controlling Data with Transactions | unchanged | Boyarsky 1Z0-829#S-0513 |
| N-0301 | C-0272 | Controlling Flow with Branching | unchanged | Boyarsky 1Z0-829#S-0087; Boyarsky 1Z0-830#S-0064 |
| N-0302 | C-0273 | Conversions | unchanged | Mughal 1Z0-829#M829-2.3; Mughal 1Z0-830#M830-P2-2.3 |
| N-0303 | C-0274 | Converting an ArrayList<E> to an Array | unchanged | Mughal 1Z0-829#M829-12.6; Mughal 1Z0-830#M830-P2-12.6 |
| N-0304 | C-0275 | Converting from List to an Array | unchanged | Boyarsky 1Z0-829#S-0286 |
| N-0305 | C-0276 | Copy on Read Accessor Methods | unchanged | Boyarsky 1Z0-830#S-0199 |
| N-0306 | C-0277 | Counting Elements | unchanged | Boyarsky 1Z0-829#S-0275 |
| N-0307 | C-0278 | Creating .class Files for Inner Classes | unchanged | Boyarsky 1Z0-830#S-0231 |
| N-0308 | C-0279 | Creating a Care Module | unchanged | Boyarsky 1Z0-829#S-0386; Boyarsky 1Z0-830#S-0339 |
| N-0309 | C-0280 | Creating a Comparable Class | unchanged | Boyarsky 1Z0-829#S-0304 |
| N-0310 | C-0281 | Creating a Concrete Class | unchanged | Boyarsky 1Z0-829#S-0202; Boyarsky 1Z0-830#S-0194 |
| N-0311 | C-0282 | Creating a Constructor | unchanged | Boyarsky 1Z0-829#S-0185; Boyarsky 1Z0-830#S-0171 |
| N-0312 | C-0283 | Creating a File or Path | unchanged | Boyarsky 1Z0-829#S-0456; Boyarsky 1Z0-830#S-0426 |
| N-0313 | C-0284 | Creating a Generic Record | unchanged | Boyarsky 1Z0-829#S-0315 |
| N-0314 | C-0285 | Creating a JAR File | unchanged | Boyarsky 1Z0-829#S-0021 |
| N-0315 | C-0286 | Creating a List with a Constructor | unchanged | Boyarsky 1Z0-829#S-0284 |
| N-0316 | C-0287 | Creating a List with a Factory | unchanged | Boyarsky 1Z0-829#S-0283 |
| N-0317 | C-0288 | Creating a main() Method | unchanged | Boyarsky 1Z0-829#S-0010 |
| N-0318 | C-0289 | Creating a Modular Application | unchanged | Mughal 1Z0-829#M829-19.5; Mughal 1Z0-830#M830-P2-19.5 |
| N-0319 | C-0290 | Creating a New Package | unchanged | Boyarsky 1Z0-829#S-0017 |
| N-0320 | C-0291 | Creating a Resource Bundle | unchanged | Boyarsky 1Z0-829#S-0370; Boyarsky 1Z0-830#S-0322 |
| N-0321 | C-0292 | Creating a Service | unchanged | Boyarsky 1Z0-829#S-0393; Boyarsky 1Z0-830#S-0347 |
| N-0322 | C-0293 | Creating a Service Locator | unchanged | Boyarsky 1Z0-829#S-0395; Boyarsky 1Z0-830#S-0349 |
| N-0323 | C-0294 | Creating a static Nested Class | unchanged | Boyarsky 1Z0-829#S-0234; Boyarsky 1Z0-830#S-0233 |
| N-0324 | C-0295 | Creating a StringBuilder | unchanged | Boyarsky 1Z0-829#S-0102; Boyarsky 1Z0-830#S-0080 |
| N-0325 | C-0296 | Creating a Thread | unchanged | Boyarsky 1Z0-829#S-0422; Boyarsky 1Z0-830#S-0382 |
| N-0326 | C-0297 | Creating Abstract Classes | unchanged | Boyarsky 1Z0-829#S-0199; Boyarsky 1Z0-830#S-0191 |
| N-0327 | C-0298 | Creating an Array of Primitives | unchanged | Boyarsky 1Z0-829#S-0108; Boyarsky 1Z0-830#S-0087 |
| N-0328 | C-0299 | Creating an Array with Reference Variables | unchanged | Boyarsky 1Z0-829#S-0109; Boyarsky 1Z0-830#S-0089 |
| N-0329 | C-0300 | Creating an Optional | unchanged | Boyarsky 1Z0-829#S-0320 |
| N-0330 | C-0301 | Creating Array Classes | unchanged | JVMS SE 25#JVMS-5.3.3 |
| N-0331 | C-0302 | Creating Classes | unchanged | Boyarsky 1Z0-829#S-0179; Boyarsky 1Z0-830#S-0165 |
| N-0332 | C-0303 | Creating Constructors in Abstract Classes | unchanged | Boyarsky 1Z0-829#S-0203; Boyarsky 1Z0-830#S-0195 |
| N-0333 | C-0304 | Creating Decision-Making Statements | unchanged | Boyarsky 1Z0-829#S-0072; Boyarsky 1Z0-830#S-0036 |
| N-0334 | C-0305 | Creating Directory Entries | unchanged | Mughal 1Z0-829#M829-21.7; Mughal 1Z0-830#M830-P2-21.7 |
| N-0335 | C-0306 | Creating Generic Classes | unchanged | Boyarsky 1Z0-829#S-0311 |
| N-0336 | C-0307 | Creating Immutable Objects | unchanged | Boyarsky 1Z0-829#S-0205; Boyarsky 1Z0-830#S-0197 |
| N-0337 | C-0308 | Creating JAR Files | unchanged | Mughal 1Z0-829#M829-19.7; Mughal 1Z0-830#M830-P2-19.7 |
| N-0338 | C-0309 | Creating Java Runtime Images with jlink | unchanged | Boyarsky 1Z0-830#S-0362 |
| N-0339 | C-0310 | Creating Java Runtimes with jlink | unchanged | Boyarsky 1Z0-829#S-0406 |
| N-0340 | C-0311 | Creating List Views | unchanged | Mughal 1Z0-829#M829-12.7; Mughal 1Z0-830#M830-P2-12.7 |
| N-0341 | C-0312 | Creating Local Variables | unchanged | Boyarsky 1Z0-829#S-0038 |
| N-0342 | C-0313 | Creating Methods with Varargs | unchanged | Boyarsky 1Z0-829#S-0145; Boyarsky 1Z0-830#S-0129 |
| N-0343 | C-0314 | Creating Nested Classes | unchanged | Boyarsky 1Z0-829#S-0232; Boyarsky 1Z0-830#S-0229 |
| N-0344 | C-0315 | Creating Objects | unchanged | Boyarsky 1Z0-829#S-0023; Boyarsky 1Z0-830#S-0006 |
| N-0345 | C-0316 | Creating Parallel Streams | unchanged | Boyarsky 1Z0-829#S-0450; Boyarsky 1Z0-830#S-0415 |
| N-0346 | C-0317 | Creating Path Objects | unchanged | Mughal 1Z0-829#M829-21.2; Mughal 1Z0-830#M830-P2-21.2 |
| N-0347 | C-0318 | Creating Primitive Streams | unchanged | Boyarsky 1Z0-829#S-0329 |
| N-0348 | C-0319 | Creating Runtime Images | unchanged | Mughal 1Z0-829#M829-19.10; Mughal 1Z0-830#M830-P2-19.10 |
| N-0349 | C-0320 | Creating Self-Contained Java Applications with jpackage | unchanged | Boyarsky 1Z0-830#S-0363 |
| N-0350 | C-0321 | Creating Simple Enums | unchanged | Boyarsky 1Z0-829#S-0216; Boyarsky 1Z0-830#S-0210 |
| N-0351 | C-0322 | Creating Stream Sources | unchanged | Boyarsky 1Z0-829#S-0324 |
| N-0352 | C-0323 | Creating the Files | unchanged | Boyarsky 1Z0-829#S-0380; Boyarsky 1Z0-830#S-0332 |
| N-0353 | C-0324 | Creating the Staff Module | unchanged | Boyarsky 1Z0-829#S-0388; Boyarsky 1Z0-830#S-0341 |
| N-0354 | C-0325 | Creating the Talks Module | unchanged | Boyarsky 1Z0-829#S-0387; Boyarsky 1Z0-830#S-0340 |
| N-0355 | C-0326 | Creating Threads | unchanged | Mughal 1Z0-829#M829-22.3; Mughal 1Z0-830#M830-P2-22.3 |
| N-0356 | C-0327 | Creating Threads with the Concurrency API | unchanged | Boyarsky 1Z0-829#S-0427; Boyarsky 1Z0-830#S-0388 |
| N-0357 | C-0328 | Creating Wrapper Classes | unchanged | Boyarsky 1Z0-829#S-0032 |
| N-0358 | C-0329 | Creation of New Class Instances | unchanged | JLS SE 25#JLS-12.5 |
| N-0359 | C-0330 | Current Preview Language Features | unchanged | JLS SE 25#JLS-1.5.2 |
| N-0360 | C-0331 | Current Preview VM Features | unchanged | JVMS SE 25#JVMS-1.5.2 |
| N-0361 | C-0332 | Currying Functions | unchanged | Mughal 1Z0-829#M829-13.12; Mughal 1Z0-830#M830-P2-13.12 |
| N-0362 | C-0333 | Customizing Records | unchanged | Boyarsky 1Z0-829#S-0231; Boyarsky 1Z0-830#S-0228 |
| N-0363 | C-0334 | Customizing Result Sets | unchanged | Mughal 1Z0-829#M829-24.6; Mughal 1Z0-830#M830-P2-24.6 |
| N-0364 | C-0335 | Customizing Serialization | unchanged | Boyarsky 1Z0-830#S-0455 |
| N-0365 | C-0336 | d2f | unchanged | JVMS SE 25#JVMS-0313 |
| N-0366 | C-0337 | d2i | unchanged | JVMS SE 25#JVMS-0314 |
| N-0367 | C-0338 | d2l | unchanged | JVMS SE 25#JVMS-0315 |
| N-0368 | C-0339 | dadd | structured-merge | JVMS SE 25#JVMS-0161 |
| N-0369 | C-0339 | dadd | structured-merge | JVMS SE 25#JVMS-0316 |
| N-0370 | C-0340 | daload | structured-merge | JVMS SE 25#JVMS-0162 |
| N-0371 | C-0340 | daload | structured-merge | JVMS SE 25#JVMS-0317 |
| N-0372 | C-0341 | dastore | structured-merge | JVMS SE 25#JVMS-0163 |
| N-0373 | C-0341 | dastore | structured-merge | JVMS SE 25#JVMS-0318 |
| N-0374 | C-0342 | Data Types | unchanged | JVMS SE 25#JVMS-2.2 |
| N-0375 | C-0343 | Database independence | unchanged | Engineering scope#ENG-0152 |
| N-0376 | C-0344 | Database migration compatibility | unchanged | Engineering scope#ENG-0427 |
| N-0377 | C-0345 | dcmp<op> | structured-merge | JVMS SE 25#JVMS-0164 |
| N-0378 | C-0345 | dcmp<op> | structured-merge | JVMS SE 25#JVMS-0319 |
| N-0379 | C-0346 | dconst_<d> | structured-merge | JVMS SE 25#JVMS-0165 |
| N-0380 | C-0346 | dconst_<d> | structured-merge | JVMS SE 25#JVMS-0320 |
| N-0381 | C-0347 | ddiv | structured-merge | JVMS SE 25#JVMS-0166 |
| N-0382 | C-0347 | ddiv | structured-merge | JVMS SE 25#JVMS-0321 |
| N-0383 | C-0348 | Dealing with an Empty Optional | unchanged | Boyarsky 1Z0-829#S-0321 |
| N-0384 | C-0349 | Declarations | unchanged | JLS SE 25#JLS-6.1 |
| N-0385 | C-0350 | Declaring a Sealed Class | unchanged | Boyarsky 1Z0-829#S-0220; Boyarsky 1Z0-830#S-0213 |
| N-0386 | C-0351 | Declaring a Subclass | unchanged | Boyarsky 1Z0-829#S-0175; Boyarsky 1Z0-830#S-0161 |
| N-0387 | C-0352 | Declaring Abstract Methods | unchanged | Boyarsky 1Z0-829#S-0201; Boyarsky 1Z0-830#S-0193 |
| N-0388 | C-0353 | Declaring an Immutable Class | unchanged | Boyarsky 1Z0-829#S-0206; Boyarsky 1Z0-830#S-0198 |
| N-0389 | C-0354 | Declaring an Inner Class | unchanged | Boyarsky 1Z0-829#S-0233; Boyarsky 1Z0-830#S-0230 |
| N-0390 | C-0355 | Declaring Annotation Types | unchanged | Mughal 1Z0-829#M829-25.2; Mughal 1Z0-830#M830-P2-25.2 |
| N-0391 | C-0356 | Declaring Concrete Interface Methods | unchanged | Boyarsky 1Z0-829#S-0214; Boyarsky 1Z0-830#S-0207 |
| N-0392 | C-0357 | Declaring Constructors | merge | Boyarsky 1Z0-829#S-0184 |
| N-0393 | C-0358 | Declaring Constructors | merge | Boyarsky 1Z0-829#S-0230 |
| N-0394 | C-0357 | Declaring Constructors | merge | Boyarsky 1Z0-830#S-0170 |
| N-0395 | C-0358 | Declaring Constructors | merge | Boyarsky 1Z0-830#S-0225 |
| N-0396 | C-0359 | Declaring Multiple Variables | unchanged | Boyarsky 1Z0-829#S-0036 |
| N-0397 | C-0360 | Declaring the Service Provider Interface | unchanged | Boyarsky 1Z0-829#S-0394; Boyarsky 1Z0-830#S-0348 |
| N-0398 | C-0361 | Declaring Variables | unchanged | Boyarsky 1Z0-829#S-0034; Boyarsky 1Z0-830#S-0008 |
| N-0399 | C-0362 | Default Constructor | structured-merge | JLS SE 25#JLS-8.8.9 |
| N-0400 | C-0363 | Defaults for Annotation Interface Elements | unchanged | JLS SE 25#JLS-9.6.2 |
| N-0401 | C-0364 | Deferring the Task | unchanged | Boyarsky 1Z0-830#S-0383 |
| N-0402 | C-0365 | Defining a Functional Interface | unchanged | Boyarsky 1Z0-829#S-0249; Boyarsky 1Z0-830#S-0250 |
| N-0403 | C-0366 | Defining an Anonymous Class | unchanged | Boyarsky 1Z0-829#S-0236; Boyarsky 1Z0-830#S-0236 |
| N-0404 | C-0367 | Defining Text Blocks | unchanged | Boyarsky 1Z0-829#S-0033 |
| N-0405 | C-0368 | Dependences | unchanged | JLS SE 25#JLS-7.7.1 |
| N-0406 | C-0369 | Dependency Rule | unchanged | Engineering scope#ENG-0147 |
| N-0407 | C-0370 | Deques | merge | Mughal 1Z0-829#M829-15.7; Mughal 1Z0-830#M830-P2-15.7 |
| N-0408 | C-0370 | Deques | merge | Mughal 1Z0-830#M830-P1-2.5 |
| N-0409 | C-0371 | Deriving a Class from a `class` File Representation | unchanged | JVMS SE 25#JVMS-5.3.5 |
| N-0410 | C-0372 | Describing with jar | unchanged | Boyarsky 1Z0-829#S-0402; Boyarsky 1Z0-830#S-0358 |
| N-0411 | C-0373 | Descriptors | unchanged | JVMS SE 25#JVMS-4.3 |
| N-0412 | C-0374 | Design Principle: Encapsulation | unchanged | Mughal 1Z0-829#M829-6.1; Mughal 1Z0-830#M830-P2-6.1 |
| N-0413 | C-0375 | Designing Methods | unchanged | Boyarsky 1Z0-829#S-0131; Boyarsky 1Z0-830#S-0115 |
| N-0414 | C-0376 | Destroying Objects | unchanged | Boyarsky 1Z0-829#S-0047; Boyarsky 1Z0-830#S-0011 |
| N-0415 | C-0377 | Detailed Initialization Procedure | unchanged | JLS SE 25#JLS-12.4.2 |
| N-0416 | C-0378 | Details on `protected` Access | unchanged | JLS SE 25#JLS-6.6.2 |
| N-0417 | C-0379 | Determining Accessibility | unchanged | JLS SE 25#JLS-6.6.1 |
| N-0418 | C-0380 | Determining Enclosing Instances | unchanged | JLS SE 25#JLS-15.9.2 |
| N-0419 | C-0381 | Determining Equality | unchanged | Boyarsky 1Z0-829#S-0280 |
| N-0420 | C-0382 | Determining the Class being Instantiated | unchanged | JLS SE 25#JLS-15.9.1 |
| N-0421 | C-0383 | Determining the Meaning of a Name | unchanged | JLS SE 25#JLS-6.5 |
| N-0422 | C-0384 | Determining the Order | unchanged | Boyarsky 1Z0-829#S-0414; Boyarsky 1Z0-830#S-0373 |
| N-0423 | C-0385 | Determining which Switch Label Applies at Run Time | unchanged | JLS SE 25#JLS-14.11.1.2 |
| N-0424 | C-0386 | Discovering File Attributes | unchanged | Boyarsky 1Z0-829#S-0485; Boyarsky 1Z0-830#S-0463 |
| N-0425 | C-0387 | Discovering Modules | unchanged | Boyarsky 1Z0-829#S-0399; Boyarsky 1Z0-830#S-0354 |
| N-0426 | C-0388 | Distinguishing Thread Types | unchanged | Boyarsky 1Z0-829#S-0423 |
| N-0427 | C-0389 | Diving into the Module Declaration | unchanged | Boyarsky 1Z0-829#S-0389; Boyarsky 1Z0-830#S-0342 |
| N-0428 | C-0390 | dload | unchanged | JVMS SE 25#JVMS-0322 |
| N-0429 | C-0391 | dload_<n> | unchanged | JVMS SE 25#JVMS-0323 |
| N-0430 | C-0392 | dmul | structured-merge | JVMS SE 25#JVMS-0168 |
| N-0431 | C-0392 | dmul | structured-merge | JVMS SE 25#JVMS-0324 |
| N-0432 | C-0393 | dneg | structured-merge | JVMS SE 25#JVMS-0169 |
| N-0433 | C-0393 | dneg | structured-merge | JVMS SE 25#JVMS-0325 |
| N-0434 | C-0394 | `do` Statements | structured-merge | JLS SE 25#JLS-16.2.11 |
| N-0435 | C-0394 | `do` Statements | structured-merge | JLS SE 25#JLS-6.3.2.4 |
| N-0436 | C-0395 | Downloading a JDK | unchanged | Boyarsky 1Z0-829#S-0004 |
| N-0437 | C-0396 | drem | structured-merge | JVMS SE 25#JVMS-0170 |
| N-0438 | C-0396 | drem | structured-merge | JVMS SE 25#JVMS-0326 |
| N-0439 | C-0397 | dreturn | structured-merge | JVMS SE 25#JVMS-0171 |
| N-0440 | C-0397 | dreturn | structured-merge | JVMS SE 25#JVMS-0327 |
| N-0441 | C-0398 | dstore | unchanged | JVMS SE 25#JVMS-0328 |
| N-0442 | C-0399 | dstore_<n> | unchanged | JVMS SE 25#JVMS-0329 |
| N-0443 | C-0400 | dsub | structured-merge | JVMS SE 25#JVMS-0173 |
| N-0444 | C-0400 | dsub | structured-merge | JVMS SE 25#JVMS-0330 |
| N-0445 | C-0401 | dup | structured-merge | JVMS SE 25#JVMS-0174 |
| N-0446 | C-0401 | dup | structured-merge | JVMS SE 25#JVMS-0331 |
| N-0447 | C-0402 | dup2 | structured-merge | JVMS SE 25#JVMS-0177 |
| N-0448 | C-0402 | dup2 | structured-merge | JVMS SE 25#JVMS-0334 |
| N-0449 | C-0403 | dup2_x1 | structured-merge | JVMS SE 25#JVMS-0178 |
| N-0450 | C-0403 | dup2_x1 | structured-merge | JVMS SE 25#JVMS-0335 |
| N-0451 | C-0404 | dup2_x2 | structured-merge | JVMS SE 25#JVMS-0179 |
| N-0452 | C-0404 | dup2_x2 | structured-merge | JVMS SE 25#JVMS-0336 |
| N-0453 | C-0405 | dup_x1 | structured-merge | JVMS SE 25#JVMS-0175 |
| N-0454 | C-0405 | dup_x1 | structured-merge | JVMS SE 25#JVMS-0332 |
| N-0455 | C-0406 | dup_x2 | structured-merge | JVMS SE 25#JVMS-0176 |
| N-0456 | C-0406 | dup_x2 | structured-merge | JVMS SE 25#JVMS-0333 |
| N-0457 | C-0407 | Dynamic Linking | unchanged | JVMS SE 25#JVMS-2.6.3 |
| N-0458 | C-0408 | Effectively Final Variables | unchanged | Boyarsky 1Z0-829#S-0142; Boyarsky 1Z0-830#S-0126 |
| N-0459 | C-0409 | Empty Statements | unchanged | JLS SE 25#JLS-16.2.1 |
| N-0460 | C-0410 | Encapsulating Data with Records | unchanged | Boyarsky 1Z0-829#S-0226; Boyarsky 1Z0-830#S-0221 |
| N-0461 | C-0411 | Enhancing with Files | unchanged | Boyarsky 1Z0-829#S-0469; Boyarsky 1Z0-830#S-0443 |
| N-0462 | C-0412 | Ensuring That a Class Is Serializable | unchanged | Boyarsky 1Z0-829#S-0475; Boyarsky 1Z0-830#S-0450 |
| N-0463 | C-0413 | Enum Body Declarations | unchanged | JLS SE 25#JLS-8.9.2 |
| N-0464 | C-0414 | Enum Classes | unchanged | JLS SE 25#JLS-8.9 |
| N-0465 | C-0415 | Enum Constants | unchanged | JLS SE 25#JLS-8.9.1 |
| N-0466 | C-0416 | Enum Members | unchanged | JLS SE 25#JLS-8.9.3 |
| N-0467 | C-0417 | Enum Types | unchanged | Mughal 1Z0-829#M829-5.13; Mughal 1Z0-830#M830-P2-5.13 |
| N-0468 | C-0418 | Equality | unchanged | Mughal 1Z0-829#M829-2.13; Mughal 1Z0-830#M830-P2-2.13 |
| N-0469 | C-0419 | Equality Operators | structured-merge | Boyarsky 1Z0-829#S-0066; Boyarsky 1Z0-830#S-0028 |
| N-0470 | C-0419 | Equality Operators | structured-merge | JLS SE 25#JLS-15.21 |
| N-0471 | C-0420 | Error Classes | unchanged | Boyarsky 1Z0-829#S-0349; Boyarsky 1Z0-830#S-0300 |
| N-0472 | C-0421 | Error-handling structure | unchanged | Engineering scope#ENG-0096 |
| N-0473 | C-0422 | Escape Sequences | unchanged | JLS SE 25#JLS-3.10.7 |
| N-0474 | C-0423 | Establishing a Database Connection | unchanged | Mughal 1Z0-829#M829-24.3; Mughal 1Z0-830#M830-P2-24.3 |
| N-0475 | C-0424 | Evaluate Arguments | unchanged | JLS SE 25#JLS-15.12.4.2 |
| N-0476 | C-0425 | Evaluate Left-Hand Operand First | unchanged | JLS SE 25#JLS-15.7.1 |
| N-0477 | C-0426 | Evaluate Operands before Operation | unchanged | JLS SE 25#JLS-15.7.2 |
| N-0478 | C-0427 | Evaluation Order | unchanged | JLS SE 25#JLS-15.7 |
| N-0479 | C-0428 | Evaluation Order for Other Expressions | unchanged | JLS SE 25#JLS-15.7.5 |
| N-0480 | C-0429 | Evaluation Order of Operands | unchanged | Mughal 1Z0-829#M829-2.6; Mughal 1Z0-830#M830-P2-2.6 |
| N-0481 | C-0430 | Evolution of Classes | unchanged | JLS SE 25#JLS-13.4 |
| N-0482 | C-0431 | Evolution of Enum Classes | unchanged | JLS SE 25#JLS-13.4.26 |
| N-0483 | C-0432 | Evolution of Interfaces | unchanged | JLS SE 25#JLS-13.5 |
| N-0484 | C-0433 | Evolution of Record Classes | unchanged | JLS SE 25#JLS-13.4.27 |
| N-0485 | C-0434 | Evolution toward or away from services | unchanged | Engineering scope#ENG-0181 |
| N-0486 | C-0435 | Example Programs | unchanged | JLS SE 25#JLS-1.2 |
| N-0487 | C-0436 | Exception Analysis of Expressions | unchanged | JLS SE 25#JLS-11.2.1 |
| N-0488 | C-0437 | Exception Checking | unchanged | JLS SE 25#JLS-11.2.3 |
| N-0489 | C-0438 | Exception List | unchanged | Boyarsky 1Z0-829#S-0138; Boyarsky 1Z0-830#S-0122 |
| N-0490 | C-0439 | Exception Types | unchanged | Mughal 1Z0-829#M829-7.2; Mughal 1Z0-830#M830-P2-7.2 |
| N-0491 | C-0440 | Exceptions | unchanged | JVMS SE 25#JVMS-2.10 |
| N-0492 | C-0441 | Executing a PreparedStatement | unchanged | Boyarsky 1Z0-829#S-0499 |
| N-0493 | C-0442 | Executing Instance Initializer Blocks | unchanged | Boyarsky 1Z0-829#S-0026 |
| N-0494 | C-0443 | Execution of a `switch` Statement | unchanged | JLS SE 25#JLS-14.11.3 |
| N-0495 | C-0444 | Execution of `try`-`catch` | unchanged | JLS SE 25#JLS-14.20.1 |
| N-0496 | C-0445 | Executions | unchanged | JLS SE 25#JLS-17.4.6 |
| N-0497 | C-0446 | Exhaustive Switch Blocks | unchanged | JLS SE 25#JLS-14.11.1.1 |
| N-0498 | C-0447 | Expand-contract schema changes | unchanged | Engineering scope#ENG-0428 |
| N-0499 | C-0448 | Exploring a Bottom-Up Migration Strategy | unchanged | Boyarsky 1Z0-829#S-0415; Boyarsky 1Z0-830#S-0374 |
| N-0500 | C-0449 | Exploring a Module | unchanged | Boyarsky 1Z0-829#S-0377; Boyarsky 1Z0-830#S-0329 |
| N-0501 | C-0450 | Exploring a Top-Down Migration Strategy | unchanged | Boyarsky 1Z0-829#S-0416; Boyarsky 1Z0-830#S-0375 |
| N-0502 | C-0451 | Exploring Modules | unchanged | Mughal 1Z0-829#M829-19.13; Mughal 1Z0-830#M830-P2-19.13 |
| N-0503 | C-0452 | Exported Types | unchanged | Boyarsky 1Z0-830#S-0344 |
| N-0504 | C-0453 | Exporting a Package | unchanged | Boyarsky 1Z0-829#S-0390; Boyarsky 1Z0-830#S-0343 |
| N-0505 | C-0454 | Expression Compatibility Constraints | unchanged | JLS SE 25#JLS-18.2.1 |
| N-0506 | C-0455 | Expression Names | unchanged | JLS SE 25#JLS-15.14.1 |
| N-0507 | C-0456 | Expression Statements | structured-merge | JLS SE 25#JLS-14.8 |
| N-0508 | C-0456 | Expression Statements | structured-merge | JLS SE 25#JLS-16.2.6 |
| N-0509 | C-0457 | Extended `try`-with-resources | unchanged | JLS SE 25#JLS-14.20.3.2 |
| N-0510 | C-0458 | Extending a Class | unchanged | Boyarsky 1Z0-829#S-0180; Boyarsky 1Z0-830#S-0166 |
| N-0511 | C-0459 | Extending an Interface | unchanged | Boyarsky 1Z0-829#S-0211; Boyarsky 1Z0-830#S-0204 |
| N-0512 | C-0460 | External-service independence | unchanged | Engineering scope#ENG-0153 |
| N-0513 | C-0461 | Externalizable boundary | unchanged | Engineering scope#ENG-0055 |
| N-0514 | C-0462 | f2d | unchanged | JVMS SE 25#JVMS-0337 |
| N-0515 | C-0463 | f2i | unchanged | JVMS SE 25#JVMS-0338 |
| N-0516 | C-0464 | f2l | unchanged | JVMS SE 25#JVMS-0339 |
| N-0517 | C-0465 | Facilitating Garbage Collection | unchanged | Mughal 1Z0-829#M829-10.3; Mughal 1Z0-830#M830-P2-10.3 |
| N-0518 | C-0466 | fadd | structured-merge | JVMS SE 25#JVMS-0181 |
| N-0519 | C-0466 | fadd | structured-merge | JVMS SE 25#JVMS-0340 |
| N-0520 | C-0467 | Failing to Compile with a Cyclic Dependency | unchanged | Boyarsky 1Z0-829#S-0418; Boyarsky 1Z0-830#S-0377 |
| N-0521 | C-0468 | faload | structured-merge | JVMS SE 25#JVMS-0182 |
| N-0522 | C-0468 | faload | structured-merge | JVMS SE 25#JVMS-0341 |
| N-0523 | C-0469 | fastore | structured-merge | JVMS SE 25#JVMS-0183 |
| N-0524 | C-0469 | fastore | structured-merge | JVMS SE 25#JVMS-0342 |
| N-0525 | C-0470 | fcmp<op> | structured-merge | JVMS SE 25#JVMS-0184 |
| N-0526 | C-0470 | fcmp<op> | structured-merge | JVMS SE 25#JVMS-0343 |
| N-0527 | C-0471 | fconst_<f> | structured-merge | JVMS SE 25#JVMS-0185 |
| N-0528 | C-0471 | fconst_<f> | structured-merge | JVMS SE 25#JVMS-0344 |
| N-0529 | C-0472 | fdiv | structured-merge | JVMS SE 25#JVMS-0186 |
| N-0530 | C-0472 | fdiv | structured-merge | JVMS SE 25#JVMS-0345 |
| N-0531 | C-0473 | Feedback | unchanged | JLS SE 25#JLS-1.6 |
| N-0532 | C-0474 | Feedback | unchanged | JVMS SE 25#JVMS-1.6 |
| N-0533 | C-0475 | Field Access Expressions | unchanged | JLS SE 25#JLS-15.11 |
| N-0534 | C-0476 | Field Access Using a Primary | unchanged | JLS SE 25#JLS-15.11.1 |
| N-0535 | C-0477 | Field (Constant) Declarations | unchanged | JLS SE 25#JLS-9.3 |
| N-0536 | C-0478 | Field Declarations | structured-merge | JLS SE 25#JLS-13.4.8 |
| N-0537 | C-0478 | Field Declarations | structured-merge | JLS SE 25#JLS-13.5.6 |
| N-0538 | C-0478 | Field Declarations | structured-merge | JLS SE 25#JLS-8.3 |
| N-0539 | C-0479 | Field Descriptors | unchanged | JVMS SE 25#JVMS-4.3.2 |
| N-0540 | C-0480 | Field Initialization | unchanged | JLS SE 25#JLS-8.3.2 |
| N-0541 | C-0481 | Field Initializer Expressions | unchanged | Mughal 1Z0-829#M829-10.6; Mughal 1Z0-830#M830-P2-10.6 |
| N-0542 | C-0482 | Field Modifiers | unchanged | JLS SE 25#JLS-8.3.1 |
| N-0543 | C-0483 | Field Resolution | unchanged | JVMS SE 25#JVMS-5.4.3.2 |
| N-0544 | C-0484 | Fields | unchanged | JVMS SE 25#JVMS-4.5 |
| N-0545 | C-0485 | `final` Classes | unchanged | JLS SE 25#JLS-13.4.2.3 |
| N-0546 | C-0486 | Final Declarations | unchanged | Mughal 1Z0-829#M829-5.5; Mughal 1Z0-830#M830-P2-5.5 |
| N-0547 | C-0487 | `final` Field Semantics | unchanged | JLS SE 25#JLS-17.5 |
| N-0548 | C-0488 | `final` Fields | unchanged | JLS SE 25#JLS-8.3.1.2 |
| N-0549 | C-0489 | `final` Methods | structured-merge | JLS SE 25#JLS-13.4.17 |
| N-0550 | C-0489 | `final` Methods | structured-merge | JLS SE 25#JLS-8.4.3.3 |
| N-0551 | C-0490 | `final` Variables | unchanged | JLS SE 25#JLS-4.12.4 |
| N-0552 | C-0491 | Finalization of Class Instances | unchanged | JLS SE 25#JLS-12.6 |
| N-0553 | C-0492 | Flexibility with Wildcard Parameterized Types | unchanged | Mughal 1Z0-829#M829-11.10; Mughal 1Z0-830#M830-P2-11.10 |
| N-0554 | C-0493 | fload | unchanged | JVMS SE 25#JVMS-0346 |
| N-0555 | C-0494 | fload_<n> | unchanged | JVMS SE 25#JVMS-0347 |
| N-0556 | C-0495 | Floating-Point Arithmetic | unchanged | JVMS SE 25#JVMS-2.8 |
| N-0557 | C-0496 | Floating-point Expressions | unchanged | JLS SE 25#JLS-15.4 |
| N-0558 | C-0497 | Floating-Point Literals | unchanged | JLS SE 25#JLS-3.10.2 |
| N-0559 | C-0498 | Floating-Point Operations | unchanged | JLS SE 25#JLS-4.2.4 |
| N-0560 | C-0499 | fmul | structured-merge | JVMS SE 25#JVMS-0188 |
| N-0561 | C-0499 | fmul | structured-merge | JVMS SE 25#JVMS-0348 |
| N-0562 | C-0500 | fneg | structured-merge | JVMS SE 25#JVMS-0189 |
| N-0563 | C-0500 | fneg | structured-merge | JVMS SE 25#JVMS-0349 |
| N-0564 | C-0501 | Following the Order of Initialization | unchanged | Boyarsky 1Z0-829#S-0027 |
| N-0565 | C-0502 | `for` Statements | structured-merge | JLS SE 25#JLS-16.2.12 |
| N-0566 | C-0502 | `for` Statements | structured-merge | JLS SE 25#JLS-6.3.2.5 |
| N-0567 | C-0503 | Forbidden Conversions | unchanged | JLS SE 25#JLS-5.1.12 |
| N-0568 | C-0504 | Formal Parameters | structured-merge | JLS SE 25#JLS-8.4.1 |
| N-0569 | C-0504 | Formal Parameters | structured-merge | JLS SE 25#JLS-8.8.1 |
| N-0570 | C-0505 | Format Checking | unchanged | JVMS SE 25#JVMS-4.8 |
| N-0571 | C-0506 | Format of Examples | unchanged | JVMS SE 25#JVMS-3.1 |
| N-0572 | C-0507 | Format of Instruction Descriptions | unchanged | JVMS SE 25#JVMS-6.4 |
| N-0573 | C-0508 | Formatting Messages | unchanged | Boyarsky 1Z0-829#S-0373; Boyarsky 1Z0-830#S-0325 |
| N-0574 | C-0509 | Formatting Numbers | unchanged | Boyarsky 1Z0-829#S-0361; Boyarsky 1Z0-830#S-0313 |
| N-0575 | C-0510 | Formatting Values | unchanged | Boyarsky 1Z0-829#S-0360; Boyarsky 1Z0-830#S-0312 |
| N-0576 | C-0511 | Forms of Expressions | unchanged | JLS SE 25#JLS-15.2 |
| N-0577 | C-0512 | Frames | unchanged | JVMS SE 25#JVMS-2.6 |
| N-0578 | C-0513 | Framework independence | unchanged | Engineering scope#ENG-0150 |
| N-0579 | C-0514 | frem | structured-merge | JVMS SE 25#JVMS-0190 |
| N-0580 | C-0514 | frem | structured-merge | JVMS SE 25#JVMS-0350 |
| N-0581 | C-0515 | freturn | structured-merge | JVMS SE 25#JVMS-0191 |
| N-0582 | C-0515 | freturn | structured-merge | JVMS SE 25#JVMS-0351 |
| N-0583 | C-0516 | fstore | unchanged | JVMS SE 25#JVMS-0352 |
| N-0584 | C-0517 | fstore_<n> | unchanged | JVMS SE 25#JVMS-0353 |
| N-0585 | C-0518 | fsub | structured-merge | JVMS SE 25#JVMS-0193 |
| N-0586 | C-0518 | fsub | structured-merge | JVMS SE 25#JVMS-0354 |
| N-0587 | C-0519 | Function Types | unchanged | JLS SE 25#JLS-9.9 |
| N-0588 | C-0520 | Functional Interface Parameterization Inference | unchanged | JLS SE 25#JLS-18.5.3 |
| N-0589 | C-0521 | Functional Interfaces | structured-merge | JLS SE 25#JLS-9.8 |
| N-0590 | C-0521 | Functional Interfaces | structured-merge | Mughal 1Z0-829#M829-13.1; Mughal 1Z0-830#M830-P2-13.1 |
| N-0591 | C-0522 | Functions | unchanged | Mughal 1Z0-829#M829-13.8; Mughal 1Z0-830#M830-P2-13.8 |
| N-0592 | C-0523 | Garbage Collection | unchanged | Mughal 1Z0-829#M829-10.1; Mughal 1Z0-830#M830-P2-10.1 |
| N-0593 | C-0524 | GC in containers | unchanged | Engineering scope#ENG-0400 |
| N-0594 | C-0525 | Generating Random Numbers | unchanged | Boyarsky 1Z0-829#S-0121; Boyarsky 1Z0-830#S-0101 |
| N-0595 | C-0526 | Generic Constructors | unchanged | JLS SE 25#JLS-8.8.4 |
| N-0596 | C-0527 | Generic Methods | unchanged | JLS SE 25#JLS-8.4.4 |
| N-0597 | C-0528 | getfield | structured-merge | JVMS SE 25#JVMS-0194 |
| N-0598 | C-0528 | getfield | structured-merge | JVMS SE 25#JVMS-0355 |
| N-0599 | C-0529 | getstatic | structured-merge | JVMS SE 25#JVMS-0195 |
| N-0600 | C-0529 | getstatic | structured-merge | JVMS SE 25#JVMS-0356 |
| N-0601 | C-0530 | Getting a Database Connection | unchanged | Boyarsky 1Z0-829#S-0496 |
| N-0602 | C-0531 | Getting Data for a Column | unchanged | Boyarsky 1Z0-829#S-0504 |
| N-0603 | C-0532 | Getting Data from a ResultSet | unchanged | Boyarsky 1Z0-829#S-0502 |
| N-0604 | C-0533 | Getting Details with java | unchanged | Boyarsky 1Z0-829#S-0401; Boyarsky 1Z0-830#S-0356 |
| N-0605 | C-0534 | Getting Values Safely | unchanged | Boyarsky 1Z0-829#S-0298 |
| N-0606 | C-0535 | GitHub Actions bookmark | unchanged | Engineering scope#ENG-0420 |
| N-0607 | C-0536 | GitLab CI bookmark | unchanged | Engineering scope#ENG-0421 |
| N-0608 | C-0537 | goto | unchanged | JVMS SE 25#JVMS-0357 |
| N-0609 | C-0538 | goto_w | unchanged | JVMS SE 25#JVMS-0358 |
| N-0610 | C-0539 | Graceful degradation | unchanged | Engineering scope#ENG-0444 |
| N-0611 | C-0540 | Grammar Notation | unchanged | JLS SE 25#JLS-2.4 |
| N-0612 | C-0541 | Grammar Notation | unchanged | JVMS SE 25#JVMS-4.3.1 |
| N-0613 | C-0542 | Guice bookmark | unchanged | Engineering scope#ENG-0285 |
| N-0614 | C-0543 | Handling Exceptions | unchanged | Boyarsky 1Z0-829#S-0350; Boyarsky 1Z0-830#S-0301 |
| N-0615 | C-0544 | Handling Methods That Declare IOException | unchanged | Boyarsky 1Z0-829#S-0459; Boyarsky 1Z0-830#S-0430 |
| N-0616 | C-0545 | Happens-before Order | unchanged | JLS SE 25#JLS-17.4.5 |
| N-0617 | C-0546 | Heap | unchanged | JVMS SE 25#JVMS-2.5.3 |
| N-0618 | C-0547 | Hiding (by Class Methods) | unchanged | JLS SE 25#JLS-8.4.8.2 |
| N-0619 | C-0548 | Hiding Static Methods | unchanged | Boyarsky 1Z0-829#S-0196; Boyarsky 1Z0-830#S-0188 |
| N-0620 | C-0549 | Hiding Variables | unchanged | Boyarsky 1Z0-829#S-0197; Boyarsky 1Z0-830#S-0189 |
| N-0621 | C-0550 | How the Online Proctored Exam Is Conducted | unchanged | Mughal 1Z0-829#M829-A.3 |
| N-0622 | C-0551 | How to Make a Class Serializable | unchanged | Boyarsky 1Z0-830#S-0451 |
| N-0623 | C-0552 | i2b | unchanged | JVMS SE 25#JVMS-0359 |
| N-0624 | C-0553 | i2c | unchanged | JVMS SE 25#JVMS-0360 |
| N-0625 | C-0554 | i2d | unchanged | JVMS SE 25#JVMS-0361 |
| N-0626 | C-0555 | i2f | unchanged | JVMS SE 25#JVMS-0362 |
| N-0627 | C-0556 | i2l | unchanged | JVMS SE 25#JVMS-0363 |
| N-0628 | C-0557 | i2s | unchanged | JVMS SE 25#JVMS-0364 |
| N-0629 | C-0558 | iadd | structured-merge | JVMS SE 25#JVMS-0198 |
| N-0630 | C-0558 | iadd | structured-merge | JVMS SE 25#JVMS-0365 |
| N-0631 | C-0559 | iaload | structured-merge | JVMS SE 25#JVMS-0199 |
| N-0632 | C-0559 | iaload | structured-merge | JVMS SE 25#JVMS-0366 |
| N-0633 | C-0560 | iand | structured-merge | JVMS SE 25#JVMS-0200 |
| N-0634 | C-0560 | iand | structured-merge | JVMS SE 25#JVMS-0367 |
| N-0635 | C-0561 | iastore | structured-merge | JVMS SE 25#JVMS-0201 |
| N-0636 | C-0561 | iastore | structured-merge | JVMS SE 25#JVMS-0368 |
| N-0637 | C-0562 | iconst_<i> | structured-merge | JVMS SE 25#JVMS-0202 |
| N-0638 | C-0562 | iconst_<i> | structured-merge | JVMS SE 25#JVMS-0369 |
| N-0639 | C-0563 | Identifiers | unchanged | JLS SE 25#JLS-3.8 |
| N-0640 | C-0564 | Identify Potentially Applicable Methods | unchanged | JLS SE 25#JLS-15.12.2.1 |
| N-0641 | C-0565 | Identifying Built-in Modules | unchanged | Boyarsky 1Z0-829#S-0400; Boyarsky 1Z0-830#S-0355 |
| N-0642 | C-0566 | Identifying Identifiers | unchanged | Boyarsky 1Z0-829#S-0035 |
| N-0643 | C-0567 | Identifying the Structure of a Relational Database | unchanged | Boyarsky 1Z0-829#S-0491 |
| N-0644 | C-0568 | Identifying Threading Problems | unchanged | Boyarsky 1Z0-829#S-0446; Boyarsky 1Z0-830#S-0410 |
| N-0645 | C-0569 | Identity Conversion | unchanged | JLS SE 25#JLS-5.1.1 |
| N-0646 | C-0570 | idiv | structured-merge | JVMS SE 25#JVMS-0203 |
| N-0647 | C-0570 | idiv | structured-merge | JVMS SE 25#JVMS-0370 |
| N-0648 | C-0571 | `if` Statements | structured-merge | JLS SE 25#JLS-16.2.7 |
| N-0649 | C-0571 | `if` Statements | structured-merge | JLS SE 25#JLS-6.3.2.2 |
| N-0650 | C-0572 | if<cond> | structured-merge | JVMS SE 25#JVMS-0206 |
| N-0651 | C-0572 | if<cond> | structured-merge | JVMS SE 25#JVMS-0373 |
| N-0652 | C-0573 | if_acmp<cond> | structured-merge | JVMS SE 25#JVMS-0204 |
| N-0653 | C-0573 | if_acmp<cond> | structured-merge | JVMS SE 25#JVMS-0371 |
| N-0654 | C-0574 | if_icmp<cond> | structured-merge | JVMS SE 25#JVMS-0205 |
| N-0655 | C-0574 | if_icmp<cond> | structured-merge | JVMS SE 25#JVMS-0372 |
| N-0656 | C-0575 | ifnonnull | unchanged | JVMS SE 25#JVMS-0374 |
| N-0657 | C-0576 | ifnull | unchanged | JVMS SE 25#JVMS-0375 |
| N-0658 | C-0577 | iinc | structured-merge | JVMS SE 25#JVMS-0208 |
| N-0659 | C-0577 | iinc | structured-merge | JVMS SE 25#JVMS-0376 |
| N-0660 | C-0578 | iload | unchanged | JVMS SE 25#JVMS-0377 |
| N-0661 | C-0579 | iload_<n> | unchanged | JVMS SE 25#JVMS-0378 |
| N-0662 | C-0580 | Implementing a Simplified Generic Stack | unchanged | Mughal 1Z0-829#M829-11.8; Mughal 1Z0-830#M830-P2-11.8 |
| N-0663 | C-0581 | Implementing Finalization | unchanged | JLS SE 25#JLS-12.6.1 |
| N-0664 | C-0582 | Implementing Generic Interfaces | unchanged | Boyarsky 1Z0-829#S-0313 |
| N-0665 | C-0583 | Implementing Immutability | unchanged | Mughal 1Z0-829#M829-6.7; Mughal 1Z0-830#M830-P2-6.7 |
| N-0666 | C-0584 | Implementing Inheritance | unchanged | Mughal 1Z0-829#M829-5.1; Mughal 1Z0-830#M830-P2-5.1 |
| N-0667 | C-0585 | Implementing Interfaces | unchanged | Boyarsky 1Z0-829#S-0209; Boyarsky 1Z0-830#S-0202 |
| N-0668 | C-0586 | Implementing Supplier | unchanged | Boyarsky 1Z0-829#S-0258; Boyarsky 1Z0-830#S-0260 |
| N-0669 | C-0587 | Implementing the equals() Method | unchanged | Mughal 1Z0-829#M829-14.2; Mughal 1Z0-830#M830-P2-14.2 |
| N-0670 | C-0588 | Implementing the hashCode() Method | unchanged | Mughal 1Z0-829#M829-14.3; Mughal 1Z0-830#M830-P2-14.3 |
| N-0671 | C-0589 | Implementing the java.lang.Comparable<E> Interface | unchanged | Mughal 1Z0-829#M829-14.4; Mughal 1Z0-830#M830-P2-14.4 |
| N-0672 | C-0590 | Implementing the java.util.Comparator<E> Interface | unchanged | Mughal 1Z0-829#M829-14.5; Mughal 1Z0-830#M830-P2-14.5 |
| N-0673 | C-0591 | Implementing Transaction Control | unchanged | Mughal 1Z0-829#M829-24.8; Mughal 1Z0-830#M830-P2-24.8 |
| N-0674 | C-0592 | Implicitly Declared Classes | unchanged | JLS SE 25#JLS-8.1.8 |
| N-0675 | C-0593 | Import Declarations | unchanged | JLS SE 25#JLS-7.5 |
| N-0676 | C-0594 | Important String Methods | unchanged | Boyarsky 1Z0-829#S-0098; Boyarsky 1Z0-830#S-0075 |
| N-0677 | C-0595 | Important StringBuilder Methods | unchanged | Boyarsky 1Z0-829#S-0103; Boyarsky 1Z0-830#S-0081 |
| N-0678 | C-0596 | Improving Access with Synchronized Blocks | unchanged | Boyarsky 1Z0-829#S-0438; Boyarsky 1Z0-830#S-0400 |
| N-0679 | C-0597 | imul | structured-merge | JVMS SE 25#JVMS-0210 |
| N-0680 | C-0597 | imul | structured-merge | JVMS SE 25#JVMS-0379 |
| N-0681 | C-0598 | Incorporation | unchanged | JLS SE 25#JLS-18.3 |
| N-0682 | C-0599 | Increasing Concurrency with Pools | unchanged | Boyarsky 1Z0-829#S-0433; Boyarsky 1Z0-830#S-0396 |
| N-0683 | C-0600 | Incrementation Part of `for` Statement | unchanged | JLS SE 25#JLS-16.2.12.2 |
| N-0684 | C-0601 | Index | unchanged | Boyarsky 1Z0-830#S-0483 |
| N-0685 | C-0602 | ineg | structured-merge | JVMS SE 25#JVMS-0211 |
| N-0686 | C-0602 | ineg | structured-merge | JVMS SE 25#JVMS-0380 |
| N-0687 | C-0603 | Inference Variables | unchanged | JLS SE 25#JLS-18.1.1 |
| N-0688 | C-0604 | Inferring the Type with var | unchanged | Boyarsky 1Z0-829#S-0041 |
| N-0689 | C-0605 | Infinite Loops | unchanged | Boyarsky 1Z0-829#S-0083; Boyarsky 1Z0-830#S-0059 |
| N-0690 | C-0606 | Inheritance | unchanged | Mughal 1Z0-829#M829-1.6; Mughal 1Z0-830#M830-P2-1.6 |
| N-0691 | C-0607 | Inheriting an Interface | unchanged | Boyarsky 1Z0-829#S-0212; Boyarsky 1Z0-830#S-0205 |
| N-0692 | C-0608 | Inheriting Members | unchanged | Boyarsky 1Z0-829#S-0193; Boyarsky 1Z0-830#S-0184 |
| N-0693 | C-0609 | Inheriting Methods with Override-Equivalent Signatures | structured-merge | JLS SE 25#JLS-8.4.8.4 |
| N-0694 | C-0609 | Inheriting Methods with Override-Equivalent Signatures | structured-merge | JLS SE 25#JLS-9.4.1.3 |
| N-0695 | C-0610 | Inheriting Object | unchanged | Boyarsky 1Z0-829#S-0178; Boyarsky 1Z0-830#S-0164 |
| N-0696 | C-0611 | Initial Values of Variables | unchanged | JLS SE 25#JLS-4.12.5 |
| N-0697 | C-0612 | Initialization | unchanged | JVMS SE 25#JVMS-5.5 |
| N-0698 | C-0613 | Initialization of Fields in Interfaces | unchanged | JLS SE 25#JLS-9.3.1 |
| N-0699 | C-0614 | Initialization of `for` Statement | unchanged | JLS SE 25#JLS-14.14.1.1 |
| N-0700 | C-0615 | Initialization Part of `for` Statement | unchanged | JLS SE 25#JLS-16.2.12.1 |
| N-0701 | C-0616 | Initialize Class X | unchanged | Boyarsky 1Z0-830#S-0180 |
| N-0702 | C-0617 | Initialize the Initial Class or Interface: Execute Initializers | unchanged | JLS SE 25#JLS-12.1.3 |
| N-0703 | C-0618 | Initializers | unchanged | Mughal 1Z0-829#M829-10.5; Mughal 1Z0-830#M830-P2-10.5 |
| N-0704 | C-0619 | Initializing Classes | unchanged | Boyarsky 1Z0-829#S-0190; Boyarsky 1Z0-830#S-0179 |
| N-0705 | C-0620 | Initializing final Fields | unchanged | Boyarsky 1Z0-829#S-0191; Boyarsky 1Z0-830#S-0182 |
| N-0706 | C-0621 | Initializing Instances | unchanged | Boyarsky 1Z0-829#S-0192; Boyarsky 1Z0-830#S-0183 |
| N-0707 | C-0622 | Initializing Objects | unchanged | Boyarsky 1Z0-829#S-0189; Boyarsky 1Z0-830#S-0178 |
| N-0708 | C-0623 | Initializing Variables | unchanged | Boyarsky 1Z0-829#S-0037; Boyarsky 1Z0-830#S-0009 |
| N-0709 | C-0624 | Inner Classes Require an Instance | unchanged | Boyarsky 1Z0-830#S-0232 |
| N-0710 | C-0625 | Inserting Implicit Modifiers | unchanged | Boyarsky 1Z0-829#S-0213; Boyarsky 1Z0-830#S-0206 |
| N-0711 | C-0626 | Instance Initialization Methods | unchanged | JVMS SE 25#JVMS-2.9.1 |
| N-0712 | C-0627 | Instance Initializer Blocks | unchanged | Mughal 1Z0-829#M829-10.8; Mughal 1Z0-830#M830-P2-10.8 |
| N-0713 | C-0628 | Instance Initializers | unchanged | JLS SE 25#JLS-8.6 |
| N-0714 | C-0629 | Instance Members | unchanged | Mughal 1Z0-829#M829-1.4; Mughal 1Z0-830#M830-P2-1.4 |
| N-0715 | C-0630 | Instance Variable Modifiers | unchanged | Boyarsky 1Z0-829#S-0143; Boyarsky 1Z0-830#S-0127 |
| N-0716 | C-0631 | instanceof | structured-merge | JVMS SE 25#JVMS-0212 |
| N-0717 | C-0631 | instanceof | structured-merge | JVMS SE 25#JVMS-0381 |
| N-0718 | C-0632 | Instruction Representation | unchanged | JVMS SE 25#JVMS-4.10.1.3 |
| N-0719 | C-0633 | Instruction Set Summary | unchanged | JVMS SE 25#JVMS-2.11 |
| N-0720 | C-0634 | Instructions | unchanged | JVMS SE 25#JVMS-6.5 |
| N-0721 | C-0635 | Integer Literals | unchanged | JLS SE 25#JLS-3.10.1 |
| N-0722 | C-0636 | Integer Operations | unchanged | JLS SE 25#JLS-4.2.2 |
| N-0723 | C-0637 | Interacting with NIO.2 Paths | unchanged | Boyarsky 1Z0-829#S-0461; Boyarsky 1Z0-830#S-0432 |
| N-0724 | C-0638 | Interacting with Users | unchanged | Boyarsky 1Z0-829#S-0478; Boyarsky 1Z0-830#S-0456 |
| N-0725 | C-0639 | Interaction with the Memory Model | unchanged | JLS SE 25#JLS-12.6.2 |
| N-0726 | C-0640 | Interface Declarations | unchanged | JLS SE 25#JLS-9.1 |
| N-0727 | C-0641 | Interface Members | structured-merge | JLS SE 25#JLS-13.5.4 |
| N-0728 | C-0641 | Interface Members | structured-merge | JLS SE 25#JLS-9.2 |
| N-0729 | C-0642 | Interface Method Body | unchanged | JLS SE 25#JLS-9.4.3 |
| N-0730 | C-0643 | Interface Method Declarations | structured-merge | JLS SE 25#JLS-13.5.7 |
| N-0731 | C-0644 | Interface Method Resolution | unchanged | JVMS SE 25#JVMS-5.4.3.4 |
| N-0732 | C-0645 | Interface Modifiers | unchanged | JLS SE 25#JLS-9.1.1 |
| N-0733 | C-0646 | Interface Type Parameters | unchanged | JLS SE 25#JLS-13.5.5 |
| N-0734 | C-0647 | Interfaces | unchanged | Mughal 1Z0-829#M829-5.6; Mughal 1Z0-830#M830-P2-5.6 |
| N-0735 | C-0648 | Intermediate Stream Operations | unchanged | Mughal 1Z0-829#M829-16.5; Mughal 1Z0-830#M830-P2-16.5 |
| N-0736 | C-0649 | Interrupting a Thread | unchanged | Boyarsky 1Z0-829#S-0426 |
| N-0737 | C-0650 | Interruptions | unchanged | JLS SE 25#JLS-17.2.3 |
| N-0738 | C-0651 | Intersection Types | unchanged | JLS SE 25#JLS-4.9 |
| N-0739 | C-0652 | Introducing Abstract Classes | unchanged | Boyarsky 1Z0-829#S-0200; Boyarsky 1Z0-830#S-0192 |
| N-0740 | C-0653 | Introducing Generics | unchanged | Mughal 1Z0-829#M829-11.1; Mughal 1Z0-830#M830-P2-11.1 |
| N-0741 | C-0654 | Introducing Modules | unchanged | Boyarsky 1Z0-829#S-0376; Boyarsky 1Z0-830#S-0328 |
| N-0742 | C-0655 | Introducing ReentrantReadWriteLock | unchanged | Boyarsky 1Z0-830#S-0403 |
| N-0743 | C-0656 | Introducing Sequenced Collections | unchanged | Boyarsky 1Z0-830#S-0280 |
| N-0744 | C-0657 | Introducing switch | unchanged | Boyarsky 1Z0-830#S-0046 |
| N-0745 | C-0658 | Introducing the Interfaces of JDBC | unchanged | Boyarsky 1Z0-829#S-0493 |
| N-0746 | C-0659 | Introducing the Single-Thread Executor | unchanged | Boyarsky 1Z0-829#S-0428; Boyarsky 1Z0-830#S-0389 |
| N-0747 | C-0660 | Introducing Threads | unchanged | Boyarsky 1Z0-829#S-0420; Boyarsky 1Z0-830#S-0379 |
| N-0748 | C-0661 | Introducing Try-with-Resources | unchanged | Boyarsky 1Z0-829#S-0356; Boyarsky 1Z0-830#S-0308 |
| N-0749 | C-0662 | Introduction to JDBC | unchanged | Mughal 1Z0-829#M829-24.2; Mughal 1Z0-830#M830-P2-24.2 |
| N-0750 | C-0663 | Introduction to Relational Databases | unchanged | Mughal 1Z0-829#M829-24.1; Mughal 1Z0-830#M830-P2-24.1 |
| N-0751 | C-0664 | Introduction to Streams | unchanged | Mughal 1Z0-829#M829-16.1; Mughal 1Z0-830#M830-P2-16.1 |
| N-0752 | C-0665 | Investigating Callable | unchanged | Boyarsky 1Z0-830#S-0393 |
| N-0753 | C-0666 | Invocation Applicability Inference | unchanged | JLS SE 25#JLS-18.5.1 |
| N-0754 | C-0667 | Invocation Contexts | unchanged | JLS SE 25#JLS-5.3 |
| N-0755 | C-0668 | Invocation Type Inference | unchanged | JLS SE 25#JLS-18.5.2 |
| N-0756 | C-0669 | Invoke a `main` Method | unchanged | JLS SE 25#JLS-12.1.4 |
| N-0757 | C-0670 | invokedynamic | structured-merge | JVMS SE 25#JVMS-0213 |
| N-0758 | C-0670 | invokedynamic | structured-merge | JVMS SE 25#JVMS-0382 |
| N-0759 | C-0671 | invokeinterface | structured-merge | JVMS SE 25#JVMS-0214 |
| N-0760 | C-0671 | invokeinterface | structured-merge | JVMS SE 25#JVMS-0383 |
| N-0761 | C-0672 | invokespecial | structured-merge | JVMS SE 25#JVMS-0215 |
| N-0762 | C-0672 | invokespecial | structured-merge | JVMS SE 25#JVMS-0384 |
| N-0763 | C-0673 | invokestatic | structured-merge | JVMS SE 25#JVMS-0216 |
| N-0764 | C-0673 | invokestatic | structured-merge | JVMS SE 25#JVMS-0385 |
| N-0765 | C-0674 | invokevirtual | structured-merge | JVMS SE 25#JVMS-0217 |
| N-0766 | C-0674 | invokevirtual | structured-merge | JVMS SE 25#JVMS-0386 |
| N-0767 | C-0675 | Invoking from a Consumer | unchanged | Boyarsky 1Z0-829#S-0396; Boyarsky 1Z0-830#S-0351 |
| N-0768 | C-0676 | Invoking Garbage Collection Programmatically | unchanged | Mughal 1Z0-829#M829-10.4; Mughal 1Z0-830#M830-P2-10.4 |
| N-0769 | C-0677 | Invoking Methods | unchanged | JVMS SE 25#JVMS-3.7 |
| N-0770 | C-0678 | ior | unchanged | JVMS SE 25#JVMS-0387 |
| N-0771 | C-0679 | irem | unchanged | JVMS SE 25#JVMS-0388 |
| N-0772 | C-0680 | ireturn | structured-merge | JVMS SE 25#JVMS-0219 |
| N-0773 | C-0680 | ireturn | structured-merge | JVMS SE 25#JVMS-0389 |
| N-0774 | C-0681 | ishl | unchanged | JVMS SE 25#JVMS-0390 |
| N-0775 | C-0682 | ishr | unchanged | JVMS SE 25#JVMS-0391 |
| N-0776 | C-0683 | istore | unchanged | JVMS SE 25#JVMS-0392 |
| N-0777 | C-0684 | istore_<n> | unchanged | JVMS SE 25#JVMS-0393 |
| N-0778 | C-0685 | isub | unchanged | JVMS SE 25#JVMS-0394 |
| N-0779 | C-0686 | Iterating | unchanged | Boyarsky 1Z0-829#S-0279 |
| N-0780 | C-0687 | Iterating Over an ArrayList<E> | unchanged | Mughal 1Z0-829#M829-12.5; Mughal 1Z0-830#M830-P2-12.5 |
| N-0781 | C-0688 | Iterating through a Map | unchanged | Boyarsky 1Z0-829#S-0297 |
| N-0782 | C-0689 | Iteration of `for` Statement | unchanged | JLS SE 25#JLS-14.14.1.2 |
| N-0783 | C-0690 | Iteration Statements | unchanged | Mughal 1Z0-829#M829-4.4; Mughal 1Z0-830#M830-P2-4.4 |
| N-0784 | C-0691 | iushr | unchanged | JVMS SE 25#JVMS-0395 |
| N-0785 | C-0692 | ixor | unchanged | JVMS SE 25#JVMS-0396 |
| N-0786 | C-0693 | Jakarta Messaging | unchanged | Engineering scope#ENG-0310 |
| N-0787 | C-0694 | Jakarta Persistence boundary | unchanged | Engineering scope#ENG-0307 |
| N-0788 | C-0695 | Jakarta runtime testing bookmark | unchanged | Engineering scope#ENG-0267 |
| N-0789 | C-0696 | Jakarta Transactions | unchanged | Engineering scope#ENG-0308 |
| N-0790 | C-0697 | Java Security Policies | unchanged | Mughal 1Z0-829#M829-26.3; Mughal 1Z0-830#M830-P2-26.3 |
| N-0791 | C-0698 | Java Source File Structure | unchanged | Mughal 1Z0-829#M829-6.2; Mughal 1Z0-830#M830-P2-6.2 |
| N-0792 | C-0699 | Java Virtual Machine Stacks | unchanged | JVMS SE 25#JVMS-2.5.2 |
| N-0793 | C-0700 | Java Virtual Machine Startup | unchanged | JLS SE 25#JLS-12.1 |
| N-0794 | C-0701 | Java Virtual Machine Startup | unchanged | JVMS SE 25#JVMS-5.2 |
| N-0795 | C-0702 | Java Virtual Machine Termination | unchanged | JVMS SE 25#JVMS-5.7 |
| N-0796 | C-0703 | JdbcTemplate bookmark | unchanged | Engineering scope#ENG-0333 |
| N-0797 | C-0704 | Jenkins bookmark | unchanged | Engineering scope#ENG-0422 |
| N-0798 | C-0705 | JMS model bookmark | unchanged | Engineering scope#ENG-0347 |
| N-0799 | C-0706 | jOOQ SQL-first model bookmark | unchanged | Engineering scope#ENG-0331 |
| N-0800 | C-0707 | jsr | unchanged | JVMS SE 25#JVMS-0397 |
| N-0801 | C-0708 | jsr_w | unchanged | JVMS SE 25#JVMS-0398 |
| N-0802 | C-0709 | Keywords | unchanged | JLS SE 25#JLS-3.9 |
| N-0803 | C-0710 | Kinds of Conversion | unchanged | JLS SE 25#JLS-5.1 |
| N-0804 | C-0711 | Kinds of Patterns | unchanged | JLS SE 25#JLS-14.30.1 |
| N-0805 | C-0712 | Kinds of Variables | unchanged | JLS SE 25#JLS-4.12.3 |
| N-0806 | C-0713 | l2d | unchanged | JVMS SE 25#JVMS-0399 |
| N-0807 | C-0714 | l2f | unchanged | JVMS SE 25#JVMS-0400 |
| N-0808 | C-0715 | l2i | unchanged | JVMS SE 25#JVMS-0401 |
| N-0809 | C-0716 | Labeled Statements | structured-merge | JLS SE 25#JLS-14.7 |
| N-0810 | C-0716 | Labeled Statements | structured-merge | JLS SE 25#JLS-16.2.5 |
| N-0811 | C-0716 | Labeled Statements | structured-merge | JLS SE 25#JLS-6.3.2.7 |
| N-0812 | C-0716 | Labeled Statements | structured-merge | Mughal 1Z0-829#M829-4.10; Mughal 1Z0-830#M830-P2-4.10 |
| N-0813 | C-0717 | ladd | structured-merge | JVMS SE 25#JVMS-0224 |
| N-0814 | C-0717 | ladd | structured-merge | JVMS SE 25#JVMS-0402 |
| N-0815 | C-0718 | laload | structured-merge | JVMS SE 25#JVMS-0225 |
| N-0816 | C-0718 | laload | structured-merge | JVMS SE 25#JVMS-0403 |
| N-0817 | C-0719 | Lambda Body | unchanged | JLS SE 25#JLS-15.27.2 |
| N-0818 | C-0720 | Lambda Expressions | structured-merge | JLS SE 25#JLS-15.27 |
| N-0819 | C-0720 | Lambda Expressions | structured-merge | Mughal 1Z0-829#M829-13.2; Mughal 1Z0-830#M830-P2-13.2 |
| N-0820 | C-0721 | Lambda Parameters | unchanged | JLS SE 25#JLS-15.27.1 |
| N-0821 | C-0722 | land | structured-merge | JVMS SE 25#JVMS-0226 |
| N-0822 | C-0722 | land | structured-merge | JVMS SE 25#JVMS-0404 |
| N-0823 | C-0723 | lastore | structured-merge | JVMS SE 25#JVMS-0227 |
| N-0824 | C-0723 | lastore | structured-merge | JVMS SE 25#JVMS-0405 |
| N-0825 | C-0724 | lcmp | structured-merge | JVMS SE 25#JVMS-0228 |
| N-0826 | C-0724 | lcmp | structured-merge | JVMS SE 25#JVMS-0406 |
| N-0827 | C-0725 | lconst_<l> | structured-merge | JVMS SE 25#JVMS-0229 |
| N-0828 | C-0725 | lconst_<l> | structured-merge | JVMS SE 25#JVMS-0407 |
| N-0829 | C-0726 | ldc | unchanged | JVMS SE 25#JVMS-0408 |
| N-0830 | C-0727 | ldc2_w | unchanged | JVMS SE 25#JVMS-0410 |
| N-0831 | C-0728 | ldc_w | unchanged | JVMS SE 25#JVMS-0409 |
| N-0832 | C-0729 | ldiv | structured-merge | JVMS SE 25#JVMS-0231 |
| N-0833 | C-0729 | ldiv | structured-merge | JVMS SE 25#JVMS-0411 |
| N-0834 | C-0730 | Learning about Dependencies with jdeps | unchanged | Boyarsky 1Z0-829#S-0403; Boyarsky 1Z0-830#S-0359 |
| N-0835 | C-0731 | Learning about the Environment | unchanged | Boyarsky 1Z0-829#S-0002; Boyarsky 1Z0-830#S-0002 |
| N-0836 | C-0732 | Learning Lambda Syntax | unchanged | Boyarsky 1Z0-829#S-0247; Boyarsky 1Z0-830#S-0247 |
| N-0837 | C-0733 | Learning the Functional Interfaces for Primitives | unchanged | Boyarsky 1Z0-829#S-0265; Boyarsky 1Z0-830#S-0267 |
| N-0838 | C-0734 | Least Upper Bound | unchanged | JLS SE 25#JLS-4.10.4 |
| N-0839 | C-0735 | Lexical Literals | unchanged | JLS SE 25#JLS-15.8.1 |
| N-0840 | C-0736 | Lexical Translations | unchanged | JLS SE 25#JLS-3.2 |
| N-0841 | C-0737 | Limitations of the Java Virtual Machine | unchanged | JVMS SE 25#JVMS-4.11 |
| N-0842 | C-0738 | Limiting Scope | unchanged | Boyarsky 1Z0-829#S-0043 |
| N-0843 | C-0739 | Line Terminators | unchanged | JLS SE 25#JLS-3.4 |
| N-0844 | C-0740 | Linking | unchanged | JVMS SE 25#JVMS-5.4 |
| N-0845 | C-0741 | Linking Streams to the Underlying Data | unchanged | Boyarsky 1Z0-829#S-0334 |
| N-0846 | C-0742 | Listing Parameters | unchanged | Boyarsky 1Z0-829#S-0267; Boyarsky 1Z0-830#S-0269 |
| N-0847 | C-0743 | Lists | merge | Mughal 1Z0-829#M829-12.1; Mughal 1Z0-830#M830-P2-12.1 |
| N-0848 | C-0743 | Lists | merge | Mughal 1Z0-829#M829-15.3; Mughal 1Z0-830#M830-P2-15.3 |
| N-0849 | C-0744 | Literals | unchanged | JLS SE 25#JLS-3.10 |
| N-0850 | C-0745 | lload | unchanged | JVMS SE 25#JVMS-0412 |
| N-0851 | C-0746 | lload_<n> | unchanged | JVMS SE 25#JVMS-0413 |
| N-0852 | C-0747 | lmul | structured-merge | JVMS SE 25#JVMS-0233 |
| N-0853 | C-0747 | lmul | structured-merge | JVMS SE 25#JVMS-0414 |
| N-0854 | C-0748 | lneg | structured-merge | JVMS SE 25#JVMS-0234 |
| N-0855 | C-0748 | lneg | structured-merge | JVMS SE 25#JVMS-0415 |
| N-0856 | C-0749 | Load the Initial Class or Interface | unchanged | JLS SE 25#JLS-12.1.1 |
| N-0857 | C-0750 | Loading Constraints | unchanged | JVMS SE 25#JVMS-5.3.4 |
| N-0858 | C-0751 | Loading Properties with Resource Bundles | unchanged | Boyarsky 1Z0-829#S-0369; Boyarsky 1Z0-830#S-0321 |
| N-0859 | C-0752 | Loading Using a User-defined Class Loader | unchanged | JVMS SE 25#JVMS-5.3.2 |
| N-0860 | C-0753 | Loading Using the Bootstrap Class Loader | unchanged | JVMS SE 25#JVMS-5.3.1 |
| N-0861 | C-0754 | Local Classes | unchanged | Mughal 1Z0-829#M829-9.4; Mughal 1Z0-830#M830-P2-9.4 |
| N-0862 | C-0755 | Local Variable Declaration Statements | structured-merge | JLS SE 25#JLS-14.4.2 |
| N-0863 | C-0755 | Local Variable Declaration Statements | structured-merge | JLS SE 25#JLS-16.2.4 |
| N-0864 | C-0756 | Local Variable Declarations | unchanged | JLS SE 25#JLS-14.4 |
| N-0865 | C-0757 | Local Variable Modifiers | unchanged | Boyarsky 1Z0-829#S-0141; Boyarsky 1Z0-830#S-0125 |
| N-0866 | C-0758 | Local Variable Type Inference | unchanged | Mughal 1Z0-829#M829-3.13; Mughal 1Z0-830#M830-P2-3.13 |
| N-0867 | C-0759 | Local Variables | unchanged | JVMS SE 25#JVMS-2.6.1 |
| N-0868 | C-0760 | Localizing Dates | unchanged | Boyarsky 1Z0-829#S-0367; Boyarsky 1Z0-830#S-0319 |
| N-0869 | C-0761 | Localizing Numbers | unchanged | Boyarsky 1Z0-829#S-0366; Boyarsky 1Z0-830#S-0318 |
| N-0870 | C-0762 | Locate Method to Invoke | unchanged | JLS SE 25#JLS-15.12.4.4 |
| N-0871 | C-0763 | Logical Complement Operator `!` | structured-merge | JLS SE 25#JLS-15.15.6 |
| N-0872 | C-0763 | Logical Complement Operator `!` | structured-merge | JLS SE 25#JLS-16.1.4 |
| N-0873 | C-0763 | Logical Complement Operator `!` | structured-merge | JLS SE 25#JLS-6.3.1.3 |
| N-0874 | C-0764 | Logical Operators | unchanged | Boyarsky 1Z0-829#S-0068; Boyarsky 1Z0-830#S-0030 |
| N-0875 | C-0765 | Looking at a Lambda Example | unchanged | Boyarsky 1Z0-829#S-0246; Boyarsky 1Z0-830#S-0246 |
| N-0876 | C-0766 | lookupswitch | structured-merge | JVMS SE 25#JVMS-0235 |
| N-0877 | C-0766 | lookupswitch | structured-merge | JVMS SE 25#JVMS-0416 |
| N-0878 | C-0767 | lor | unchanged | JVMS SE 25#JVMS-0417 |
| N-0879 | C-0768 | lrem | unchanged | JVMS SE 25#JVMS-0418 |
| N-0880 | C-0769 | lreturn | structured-merge | JVMS SE 25#JVMS-0237 |
| N-0881 | C-0769 | lreturn | structured-merge | JVMS SE 25#JVMS-0419 |
| N-0882 | C-0770 | lshl | unchanged | JVMS SE 25#JVMS-0420 |
| N-0883 | C-0771 | lshr | unchanged | JVMS SE 25#JVMS-0421 |
| N-0884 | C-0772 | LSP failure examples in Java hierarchies | unchanged | Engineering scope#ENG-0104 |
| N-0885 | C-0773 | lstore | unchanged | JVMS SE 25#JVMS-0422 |
| N-0886 | C-0774 | lstore_<n> | unchanged | JVMS SE 25#JVMS-0423 |
| N-0887 | C-0775 | lsub | unchanged | JVMS SE 25#JVMS-0424 |
| N-0888 | C-0776 | lushr | unchanged | JVMS SE 25#JVMS-0425 |
| N-0889 | C-0777 | lxor | unchanged | JVMS SE 25#JVMS-0426 |
| N-0890 | C-0778 | Major Components of Java | unchanged | Boyarsky 1Z0-829#S-0003 |
| N-0891 | C-0779 | Making Decisions with the Ternary Operator | unchanged | Boyarsky 1Z0-829#S-0070; Boyarsky 1Z0-830#S-0033 |
| N-0892 | C-0780 | Making the Case for Modules | unchanged | Mughal 1Z0-829#M829-19.1; Mughal 1Z0-830#M830-P2-19.1 |
| N-0893 | C-0781 | Managing a Thread’s Life Cycle | unchanged | Boyarsky 1Z0-829#S-0424; Boyarsky 1Z0-830#S-0386 |
| N-0894 | C-0782 | Managing File Attributes | unchanged | Mughal 1Z0-829#M829-21.6; Mughal 1Z0-830#M830-P2-21.6 |
| N-0895 | C-0783 | Managing Race Conditions | unchanged | Boyarsky 1Z0-829#S-0448; Boyarsky 1Z0-830#S-0412 |
| N-0896 | C-0784 | Managing Variable Scope | unchanged | Boyarsky 1Z0-829#S-0042; Boyarsky 1Z0-830#S-0010 |
| N-0897 | C-0785 | Manipulating Input Streams | unchanged | Boyarsky 1Z0-829#S-0484; Boyarsky 1Z0-830#S-0462 |
| N-0898 | C-0786 | Map Implementations | unchanged | Mughal 1Z0-829#M829-15.9; Mughal 1Z0-830#M830-P2-15.9 |
| N-0899 | C-0787 | Mapping Streams | unchanged | Boyarsky 1Z0-829#S-0330 |
| N-0900 | C-0788 | Maps | unchanged | Mughal 1Z0-829#M829-15.8; Mughal 1Z0-830#M830-P2-15.8 |
| N-0901 | C-0789 | Marker Annotations | unchanged | JLS SE 25#JLS-9.7.2 |
| N-0902 | C-0790 | Marking Data transient | unchanged | Boyarsky 1Z0-829#S-0474; Boyarsky 1Z0-830#S-0449 |
| N-0903 | C-0791 | Meaning of Expression Names | unchanged | JLS SE 25#JLS-6.5.6 |
| N-0904 | C-0792 | Meaning of Method Names | unchanged | JLS SE 25#JLS-6.5.7 |
| N-0905 | C-0793 | Meaning of PackageOrTypeNames | unchanged | JLS SE 25#JLS-6.5.4 |
| N-0906 | C-0794 | Meaning of Type Names | unchanged | JLS SE 25#JLS-6.5.5 |
| N-0907 | C-0795 | Measure-first optimization workflow | unchanged | Engineering scope#ENG-0079 |
| N-0908 | C-0796 | Members Automatically Added to Records | unchanged | Boyarsky 1Z0-830#S-0224 |
| N-0909 | C-0797 | Memory Model | unchanged | JLS SE 25#JLS-17.4 |
| N-0910 | C-0798 | Merging Data | unchanged | Boyarsky 1Z0-829#S-0301 |
| N-0911 | C-0799 | Meta-Annotations | unchanged | Mughal 1Z0-829#M829-25.4; Mughal 1Z0-830#M830-P2-25.4 |
| N-0912 | C-0800 | Method Area | unchanged | JVMS SE 25#JVMS-2.5.4 |
| N-0913 | C-0801 | Method Body | structured-merge | Boyarsky 1Z0-829#S-0139; Boyarsky 1Z0-830#S-0123 |
| N-0914 | C-0801 | Method Body | structured-merge | JLS SE 25#JLS-8.4.7 |
| N-0915 | C-0802 | Method Chaining | unchanged | Boyarsky 1Z0-829#S-0099; Boyarsky 1Z0-830#S-0077 |
| N-0916 | C-0643 | Method Declarations | structured-merge | JLS SE 25#JLS-8.4 |
| N-0917 | C-0643 | Method Declarations | structured-merge | JLS SE 25#JLS-9.4 |
| N-0918 | C-0643 | Method Declarations | structured-merge | Mughal 1Z0-829#M829-3.2; Mughal 1Z0-830#M830-P2-3.2 |
| N-0919 | C-0803 | Method Descriptors | unchanged | JVMS SE 25#JVMS-4.3.3 |
| N-0920 | C-0804 | Method Invocation Conversions Involving References | unchanged | Mughal 1Z0-829#M829-5.10; Mughal 1Z0-830#M830-P2-5.10 |
| N-0921 | C-0805 | Method Invocation Expressions | unchanged | JLS SE 25#JLS-15.12 |
| N-0922 | C-0806 | Method Invocation Type | unchanged | JLS SE 25#JLS-15.12.2.6 |
| N-0923 | C-0807 | Method Modifiers | unchanged | JLS SE 25#JLS-8.4.3 |
| N-0924 | C-0808 | Method Name | unchanged | Boyarsky 1Z0-829#S-0135; Boyarsky 1Z0-830#S-0119 |
| N-0925 | C-0809 | Method Overloading | unchanged | Mughal 1Z0-829#M829-3.6; Mughal 1Z0-830#M830-P2-3.6 |
| N-0926 | C-0810 | Method Overriding | structured-merge | JLS SE 25#JLS-13.4.24 |
| N-0927 | C-0811 | Method Overriding | unchanged | JVMS SE 25#JVMS-5.4.5 |
| N-0928 | C-0812 | Method Overriding Infinite Calls | unchanged | Boyarsky 1Z0-830#S-0186 |
| N-0929 | C-0813 | Method Reference Expressions | unchanged | JLS SE 25#JLS-15.13 |
| N-0930 | C-0814 | Method Resolution | unchanged | JVMS SE 25#JVMS-5.4.3.3 |
| N-0931 | C-0815 | Method Result | unchanged | JLS SE 25#JLS-8.4.5 |
| N-0932 | C-0816 | Method Result Type | unchanged | JLS SE 25#JLS-13.4.15 |
| N-0933 | C-0817 | Method Selection | unchanged | JVMS SE 25#JVMS-5.4.6 |
| N-0934 | C-0818 | Method Signature | structured-merge | Boyarsky 1Z0-829#S-0137; Boyarsky 1Z0-830#S-0121 |
| N-0935 | C-0818 | Method Signature | structured-merge | JLS SE 25#JLS-8.4.2 |
| N-0936 | C-0819 | Method Throws | unchanged | JLS SE 25#JLS-8.4.6 |
| N-0937 | C-0820 | Methods | unchanged | JVMS SE 25#JVMS-4.6 |
| N-0938 | C-0821 | Micronaut architecture bookmark | unchanged | Engineering scope#ENG-0353 |
| N-0939 | C-0822 | MicroProfile Config | unchanged | Engineering scope#ENG-0313 |
| N-0940 | C-0823 | Migrating an Application | unchanged | Boyarsky 1Z0-829#S-0413; Boyarsky 1Z0-830#S-0372 |
| N-0941 | C-0824 | Migrating to Modules | unchanged | Mughal 1Z0-829#M829-19.12; Mughal 1Z0-830#M830-P2-19.12 |
| N-0942 | C-0825 | mnemonic | unchanged | JVMS SE 25#JVMS-0294 |
| N-0943 | C-0826 | Modifying an ArrayList<E> | unchanged | Mughal 1Z0-829#M829-12.3; Mughal 1Z0-830#M830-P2-12.3 |
| N-0944 | C-0827 | Modifying Loop Variables | unchanged | Boyarsky 1Z0-830#S-0062 |
| N-0945 | C-0828 | Modular-monolith communication | unchanged | Engineering scope#ENG-0179 |
| N-0946 | C-0829 | Module Basics | unchanged | Mughal 1Z0-829#M829-19.3; Mughal 1Z0-830#M830-P2-19.3 |
| N-0947 | C-0830 | Module Declarations | unchanged | JLS SE 25#JLS-7.7 |
| N-0948 | C-0831 | Modules | unchanged | JVMS SE 25#JVMS-3.16 |
| N-0949 | C-0832 | monitorenter | unchanged | JVMS SE 25#JVMS-0427 |
| N-0950 | C-0833 | monitorexit | unchanged | JVMS SE 25#JVMS-0428 |
| N-0951 | C-0834 | More About Describing Modules | unchanged | Boyarsky 1Z0-830#S-0357 |
| N-0952 | C-0835 | More Control Examples | unchanged | JVMS SE 25#JVMS-3.5 |
| N-0953 | C-0836 | More Specific Method Inference | unchanged | JLS SE 25#JLS-18.5.4 |
| N-0954 | C-0837 | Motivation for Virtual Threads | unchanged | Mughal 1Z0-830#M830-P1-3.1 |
| N-0955 | C-0838 | Multi-stage Java builds | unchanged | Engineering scope#ENG-0392 |
| N-0956 | C-0839 | multianewarray | structured-merge | JVMS SE 25#JVMS-0242 |
| N-0957 | C-0839 | multianewarray | structured-merge | JVMS SE 25#JVMS-0429 |
| N-0958 | C-0840 | Multiple Annotations of the Same Interface | unchanged | JLS SE 25#JLS-9.7.5 |
| N-0959 | C-0841 | Multiple “Arrays” in Declarations | unchanged | Boyarsky 1Z0-830#S-0088 |
| N-0960 | C-0842 | Multiplication Operator `*` | unchanged | JLS SE 25#JLS-15.17.1 |
| N-0961 | C-0843 | Multiplicative Operators | unchanged | JLS SE 25#JLS-15.17 |
| N-0962 | C-0844 | MyBatis mapping model bookmark | unchanged | Engineering scope#ENG-0332 |
| N-0963 | C-0845 | Named Modules | unchanged | Boyarsky 1Z0-829#S-0409; Boyarsky 1Z0-830#S-0367 |
| N-0964 | C-0846 | Named Packages | unchanged | JLS SE 25#JLS-7.4.1 |
| N-0965 | C-0847 | Names | unchanged | JVMS SE 25#JVMS-4.2 |
| N-0966 | C-0848 | Names as domain vocabulary | unchanged | Engineering scope#ENG-0089 |
| N-0967 | C-0849 | Naming Conflicts | unchanged | Boyarsky 1Z0-829#S-0016 |
| N-0968 | C-0850 | Narrowing Primitive Conversion | unchanged | JLS SE 25#JLS-5.1.3 |
| N-0969 | C-0851 | Narrowing Reference Conversion | unchanged | JLS SE 25#JLS-5.1.6 |
| N-0970 | C-0852 | Narrowing Reference Conversions at Run Time | unchanged | JLS SE 25#JLS-5.1.6.3 |
| N-0971 | C-0853 | Native-image closed-world assumptions | unchanged | Engineering scope#ENG-0356 |
| N-0972 | C-0854 | Native Method Stacks | unchanged | JVMS SE 25#JVMS-2.5.6 |
| N-0973 | C-0855 | `native` Methods | structured-merge | JLS SE 25#JLS-13.4.18 |
| N-0974 | C-0855 | `native` Methods | structured-merge | JLS SE 25#JLS-8.4.3.4 |
| N-0975 | C-0856 | Nested Loops | unchanged | Boyarsky 1Z0-829#S-0088; Boyarsky 1Z0-830#S-0065 |
| N-0976 | C-0857 | Nested Records are Implicitly static | unchanged | Boyarsky 1Z0-830#S-0234 |
| N-0977 | C-0858 | new | structured-merge | JVMS SE 25#JVMS-0243 |
| N-0978 | C-0858 | new | structured-merge | JVMS SE 25#JVMS-0430 |
| N-0979 | C-0859 | newarray | structured-merge | JVMS SE 25#JVMS-0244 |
| N-0980 | C-0859 | newarray | structured-merge | JVMS SE 25#JVMS-0431 |
| N-0981 | C-0860 | `non-sealed` Classes | unchanged | JLS SE 25#JLS-13.4.2.2 |
| N-0982 | C-0861 | Non-Static Member Classes | unchanged | Mughal 1Z0-829#M829-9.3; Mughal 1Z0-830#M830-P2-9.3 |
| N-0983 | C-0862 | nop | structured-merge | JVMS SE 25#JVMS-0245 |
| N-0984 | C-0862 | nop | structured-merge | JVMS SE 25#JVMS-0432 |
| N-0985 | C-0863 | Normal Annotations | unchanged | JLS SE 25#JLS-9.7.1 |
| N-0986 | C-0864 | Normal Canonical Constructors | unchanged | JLS SE 25#JLS-8.10.4.1 |
| N-0987 | C-0865 | Normal Method Invocation Completion | unchanged | JVMS SE 25#JVMS-2.6.4 |
| N-0988 | C-0866 | Notation | unchanged | JLS SE 25#JLS-1.3 |
| N-0989 | C-0867 | Notation | unchanged | JVMS SE 25#JVMS-1.4 |
| N-0990 | C-0868 | Notification | unchanged | JLS SE 25#JLS-17.2.2 |
| N-0991 | C-0869 | Numeric Conditional Expressions | unchanged | JLS SE 25#JLS-15.25.2 |
| N-0992 | C-0870 | Numeric Contexts | unchanged | JLS SE 25#JLS-5.6 |
| N-0993 | C-0871 | Numeric Promotion | unchanged | Boyarsky 1Z0-829#S-0059; Boyarsky 1Z0-830#S-0021 |
| N-0994 | C-0872 | Object Serialization | unchanged | Mughal 1Z0-829#M829-20.5; Mughal 1Z0-830#M830-P2-20.5 |
| N-0995 | C-0873 | ObjectInputStream | unchanged | Boyarsky 1Z0-829#S-0476 |
| N-0996 | C-0874 | Objects | structured-merge | JLS SE 25#JLS-4.3.1 |
| N-0997 | C-0874 | Objects | structured-merge | Mughal 1Z0-829#M829-1.3; Mughal 1Z0-830#M830-P2-1.3 |
| N-0998 | C-0875 | Obscuring | unchanged | JLS SE 25#JLS-6.4.2 |
| N-0999 | C-0876 | Observability of a Module | unchanged | JLS SE 25#JLS-7.7.6 |
| N-1000 | C-0877 | Obtaining a PreparedStatement | unchanged | Boyarsky 1Z0-829#S-0498 |
| N-1001 | C-0878 | Obtaining Synchronized Collections | unchanged | Boyarsky 1Z0-829#S-0445; Boyarsky 1Z0-830#S-0409 |
| N-1002 | C-0879 | Omitting the permits Clause | unchanged | Boyarsky 1Z0-829#S-0223; Boyarsky 1Z0-830#S-0216 |
| N-1003 | C-0880 | Opening a Package | unchanged | Boyarsky 1Z0-829#S-0392; Boyarsky 1Z0-830#S-0346 |
| N-1004 | C-0881 | OpenTelemetry bookmark | unchanged | Engineering scope#ENG-0388 |
| N-1005 | C-0882 | Operand Stack Management Instructions | unchanged | JVMS SE 25#JVMS-2.11.6 |
| N-1006 | C-0883 | Operand Stacks | unchanged | JVMS SE 25#JVMS-2.6.2 |
| N-1007 | C-0884 | Operating System File Separators | unchanged | Boyarsky 1Z0-830#S-0425 |
| N-1008 | C-0885 | Operations on Directory Entries | unchanged | Mughal 1Z0-829#M829-21.4; Mughal 1Z0-830#M830-P2-21.4 |
| N-1009 | C-0886 | Operations on the Operand Stack | unchanged | JVMS SE 25#JVMS-3.11 |
| N-1010 | C-0887 | Operator Precedence | unchanged | Boyarsky 1Z0-829#S-0053; Boyarsky 1Z0-830#S-0015 |
| N-1011 | C-0888 | Operators | unchanged | JLS SE 25#JLS-3.12 |
| N-1012 | C-0889 | Optional Specifiers | unchanged | Boyarsky 1Z0-829#S-0133; Boyarsky 1Z0-830#S-0117 |
| N-1013 | C-0890 | Orchestrating Tasks with a CyclicBarrier | unchanged | Boyarsky 1Z0-829#S-0441; Boyarsky 1Z0-830#S-0404 |
| N-1014 | C-0891 | Ordering Elements in a Class | unchanged | Boyarsky 1Z0-829#S-0022 |
| N-1015 | C-0892 | Ordering Results | unchanged | Boyarsky 1Z0-830#S-0417 |
| N-1016 | C-0893 | Organization of the Specification | unchanged | JLS SE 25#JLS-1.1 |
| N-1017 | C-0894 | Organization of the Specification | unchanged | JVMS SE 25#JVMS-1.3 |
| N-1018 | C-0895 | Other Expressions | unchanged | JLS SE 25#JLS-16.1.10 |
| N-1019 | C-0896 | Other Expressions of Type `boolean` | unchanged | JLS SE 25#JLS-16.1.7 |
| N-1020 | C-0897 | Other Ways to Create a Path | unchanged | Boyarsky 1Z0-830#S-0427 |
| N-1021 | C-0898 | Overloading | structured-merge | JLS SE 25#JLS-8.4.9 |
| N-1022 | C-0898 | Overloading | structured-merge | JLS SE 25#JLS-9.4.2 |
| N-1023 | C-0899 | Overloading Methods | unchanged | Boyarsky 1Z0-829#S-0166; Boyarsky 1Z0-830#S-0152 |
| N-1024 | C-0810 | Overriding a Method | structured-merge | Boyarsky 1Z0-829#S-0194; Boyarsky 1Z0-830#S-0185 |
| N-1025 | C-0900 | Overriding (by Instance Methods) | structured-merge | JLS SE 25#JLS-8.4.8.1 |
| N-1026 | C-0900 | Overriding (by Instance Methods) | structured-merge | JLS SE 25#JLS-9.4.1.1 |
| N-1027 | C-0901 | Overriding Methods with Exceptions | unchanged | Boyarsky 1Z0-829#S-0344; Boyarsky 1Z0-830#S-0295 |
| N-1028 | C-0902 | Overview of Built-In Functional Interfaces | merge | Mughal 1Z0-829#M829-13.4; Mughal 1Z0-830#M830-P2-13.4 |
| N-1029 | C-0903 | Overview of Module Directives | unchanged | Mughal 1Z0-829#M829-19.4; Mughal 1Z0-830#M830-P2-19.4 |
| N-1030 | C-0904 | Overview of Nested Type Declarations | unchanged | Mughal 1Z0-829#M829-9.1; Mughal 1Z0-830#M830-P2-9.1 |
| N-1031 | C-0905 | Overview of the java.lang Package | unchanged | Mughal 1Z0-829#M829-8.1; Mughal 1Z0-830#M830-P2-8.1 |
| N-1032 | C-0906 | Package Access | unchanged | Boyarsky 1Z0-829#S-0151; Boyarsky 1Z0-830#S-0136 |
| N-1033 | C-0907 | Package Declarations | unchanged | JLS SE 25#JLS-7.4 |
| N-1034 | C-0908 | Package Members | unchanged | JLS SE 25#JLS-7.1 |
| N-1035 | C-0909 | Packages | merge | Boyarsky 1Z0-829#S-0013 |
| N-1036 | C-0909 | Packages | merge | Mughal 1Z0-829#M829-6.3; Mughal 1Z0-830#M830-P2-6.3 |
| N-1037 | C-0910 | Packaging Our First Module | unchanged | Boyarsky 1Z0-829#S-0383; Boyarsky 1Z0-830#S-0336 |
| N-1038 | C-0911 | Parallel Streams | merge | Mughal 1Z0-829#M829-16.9; Mughal 1Z0-830#M830-P2-16.9 |
| N-1039 | C-0912 | Parameter List | unchanged | Boyarsky 1Z0-829#S-0136; Boyarsky 1Z0-830#S-0120 |
| N-1040 | C-0913 | Parameter List Formats | unchanged | Boyarsky 1Z0-830#S-0270 |
| N-1041 | C-0914 | Parameter Passing | unchanged | Mughal 1Z0-829#M829-3.10; Mughal 1Z0-830#M830-P2-3.10 |
| N-1042 | C-0915 | Parameterized Types | unchanged | JLS SE 25#JLS-4.5 |
| N-1043 | C-0916 | Parenthesized Expressions | structured-merge | JLS SE 25#JLS-15.8.5 |
| N-1044 | C-0916 | Parenthesized Expressions | structured-merge | JLS SE 25#JLS-6.3.1.7 |
| N-1045 | C-0917 | Passing an IN Parameter | unchanged | Boyarsky 1Z0-829#S-0508 |
| N-1046 | C-0918 | Passing Data among Methods | unchanged | Boyarsky 1Z0-829#S-0162; Boyarsky 1Z0-830#S-0147 |
| N-1047 | C-0919 | Passing Objects | unchanged | Boyarsky 1Z0-829#S-0163; Boyarsky 1Z0-830#S-0148 |
| N-1048 | C-0920 | Passing Parameters to a Java Program | unchanged | Boyarsky 1Z0-829#S-0011 |
| N-1049 | C-0921 | Pattern Match Operator `instanceof` | unchanged | JLS SE 25#JLS-6.3.1.5 |
| N-1050 | C-0922 | Pattern Matching | unchanged | JLS SE 25#JLS-14.30.2 |
| N-1051 | C-0923 | Patterns | unchanged | JLS SE 25#JLS-14.30 |
| N-1052 | C-0924 | Performing a Defensive Copy | unchanged | Boyarsky 1Z0-829#S-0207; Boyarsky 1Z0-830#S-0200 |
| N-1053 | C-0925 | Performing a Parallel Decomposition | unchanged | Boyarsky 1Z0-829#S-0451; Boyarsky 1Z0-830#S-0416 |
| N-1054 | C-0926 | Permitted Direct Subclasses | unchanged | JLS SE 25#JLS-8.1.6 |
| N-1055 | C-0927 | Phase 1: Identify Matching Arity Methods Applicable by Strict Invocation | unchanged | JLS SE 25#JLS-15.12.2.2 |
| N-1056 | C-0928 | Phase 2: Identify Matching Arity Methods Applicable by Loose Invocation | unchanged | JLS SE 25#JLS-15.12.2.3 |
| N-1057 | C-0929 | Phase 3: Identify Methods Applicable by Variable Arity Invocation | unchanged | JLS SE 25#JLS-15.12.2.4 |
| N-1058 | C-0930 | Picking a Locale | unchanged | Boyarsky 1Z0-829#S-0365; Boyarsky 1Z0-830#S-0317 |
| N-1059 | C-0931 | Picking a Resource Bundle | unchanged | Boyarsky 1Z0-829#S-0371; Boyarsky 1Z0-830#S-0323 |
| N-1060 | C-0932 | Polling with Sleep | unchanged | Boyarsky 1Z0-829#S-0425; Boyarsky 1Z0-830#S-0392 |
| N-1061 | C-0933 | Poly Method Invocation Compatibility | unchanged | JLS SE 25#JLS-18.5.2.1 |
| N-1062 | C-0934 | Polymorphism | unchanged | Mughal 1Z0-829#M829-5.12; Mughal 1Z0-830#M830-P2-5.12 |
| N-1063 | C-0935 | pop | unchanged | JVMS SE 25#JVMS-0433 |
| N-1064 | C-0936 | pop2 | unchanged | JVMS SE 25#JVMS-0434 |
| N-1065 | C-0937 | Possible Outcomes for This Race Condition | unchanged | Boyarsky 1Z0-830#S-0413 |
| N-1066 | C-0938 | Post-deployment verification | unchanged | Engineering scope#ENG-0436 |
| N-1067 | C-0939 | Postfix Decrement Operator `--` | unchanged | JLS SE 25#JLS-15.14.3 |
| N-1068 | C-0940 | Postfix Expressions | unchanged | JLS SE 25#JLS-15.14 |
| N-1069 | C-0941 | Postfix Increment Operator `++` | unchanged | JLS SE 25#JLS-15.14.2 |
| N-1070 | C-0942 | Predefined Annotation Interfaces | unchanged | JLS SE 25#JLS-9.6.4 |
| N-1071 | C-0943 | Predicates | unchanged | Mughal 1Z0-829#M829-13.6; Mughal 1Z0-830#M830-P2-13.6 |
| N-1072 | C-0944 | Prefix Decrement Operator `--` | unchanged | JLS SE 25#JLS-15.15.2 |
| N-1073 | C-0945 | Prefix Increment Operator `++` | unchanged | JLS SE 25#JLS-15.15.1 |
| N-1074 | C-0946 | Preparation | unchanged | JVMS SE 25#JVMS-5.4.2 |
| N-1075 | C-0947 | Preparation of a Class or Interface | unchanged | JLS SE 25#JLS-12.3.2 |
| N-1076 | C-0948 | Preparing for the Exam | merge | Mughal 1Z0-829#M829-A.1 |
| N-1077 | C-0948 | Preparing for the Exam | merge | Mughal 1Z0-830#M830-P2-A.1 |
| N-1078 | C-0949 | Preventing Instantiation of a Class | unchanged | JLS SE 25#JLS-8.8.10 |
| N-1079 | C-0950 | Preview Features | unchanged | JLS SE 25#JLS-1.5 |
| N-1080 | C-0951 | Preview Features | unchanged | JVMS SE 25#JVMS-1.5 |
| N-1081 | C-0952 | Primary Expressions | unchanged | JLS SE 25#JLS-15.8 |
| N-1082 | C-0953 | Primitive Data Types | unchanged | Mughal 1Z0-829#M829-2.2; Mughal 1Z0-830#M830-P2-2.2 |
| N-1083 | C-0954 | Primitives | unchanged | Boyarsky 1Z0-829#S-0168; Boyarsky 1Z0-830#S-0154 |
| N-1084 | C-0955 | Printing an Exception | unchanged | Boyarsky 1Z0-829#S-0345; Boyarsky 1Z0-830#S-0296 |
| N-1085 | C-0956 | Printing Data to the User | unchanged | Boyarsky 1Z0-829#S-0479; Boyarsky 1Z0-830#S-0457 |
| N-1086 | C-0957 | Private Access | unchanged | Boyarsky 1Z0-829#S-0150; Boyarsky 1Z0-830#S-0135 |
| N-1087 | C-0958 | Processing Annotations | unchanged | Mughal 1Z0-829#M829-25.6; Mughal 1Z0-830#M830-P2-25.6 |
| N-1088 | C-0959 | Processing Parallel Reductions | unchanged | Boyarsky 1Z0-829#S-0452; Boyarsky 1Z0-830#S-0418 |
| N-1089 | C-0960 | Processing Query Results | unchanged | Mughal 1Z0-829#M829-24.5; Mughal 1Z0-830#M830-P2-24.5 |
| N-1090 | C-0961 | Program Exit | unchanged | JLS SE 25#JLS-12.8 |
| N-1091 | C-0962 | Program Output | unchanged | Mughal 1Z0-829#M829-1.9; Mughal 1Z0-830#M830-P2-1.9 |
| N-1092 | C-0963 | Properties Files | unchanged | Mughal 1Z0-829#M829-18.2; Mughal 1Z0-830#M830-P2-18.2 |
| N-1093 | C-0964 | Properties of Patterns | unchanged | JLS SE 25#JLS-14.30.3 |
| N-1094 | C-0965 | Protected Access | unchanged | Boyarsky 1Z0-829#S-0152; Boyarsky 1Z0-830#S-0137 |
| N-1095 | C-0966 | Protecting Data with Atomic Classes | unchanged | Boyarsky 1Z0-829#S-0437; Boyarsky 1Z0-830#S-0399 |
| N-1096 | C-0967 | Providing NIO.2 Optional Parameters | unchanged | Boyarsky 1Z0-829#S-0460; Boyarsky 1Z0-830#S-0431 |
| N-1097 | C-0968 | Public Access | unchanged | Boyarsky 1Z0-829#S-0153; Boyarsky 1Z0-830#S-0138 |
| N-1098 | C-0969 | `public` Classes | unchanged | JLS SE 25#JLS-13.4.3 |
| N-1099 | C-0970 | `public` Interfaces | unchanged | JLS SE 25#JLS-13.5.1 |
| N-1100 | C-0971 | Purpose of the Logging API | unchanged | Mughal 1Z0-829#M829-G.1 |
| N-1101 | C-0972 | putfield | structured-merge | JVMS SE 25#JVMS-0247 |
| N-1102 | C-0972 | putfield | structured-merge | JVMS SE 25#JVMS-0435 |
| N-1103 | C-0973 | putstatic | structured-merge | JVMS SE 25#JVMS-0248 |
| N-1104 | C-0973 | putstatic | structured-merge | JVMS SE 25#JVMS-0436 |
| N-1105 | C-0974 | Putting if Absent | unchanged | Boyarsky 1Z0-829#S-0300 |
| N-1106 | C-0975 | Putting It All Together | merge | Boyarsky 1Z0-829#S-0172 |
| N-1107 | C-0976 | Putting It All Together | unchanged | Boyarsky 1Z0-829#S-0317 |
| N-1108 | C-0975 | Putting It All Together | merge | Boyarsky 1Z0-830#S-0158 |
| N-1109 | C-0977 | Putting Together the Pipeline | unchanged | Boyarsky 1Z0-829#S-0327 |
| N-1110 | C-0978 | Qualified Expression Names | unchanged | JLS SE 25#JLS-6.5.6.2 |
| N-1111 | C-0979 | Qualified Package Names | unchanged | JLS SE 25#JLS-6.5.3.2 |
| N-1112 | C-0980 | Qualified PackageOrTypeNames | unchanged | JLS SE 25#JLS-6.5.4.2 |
| N-1113 | C-0981 | Qualified `this` | unchanged | JLS SE 25#JLS-15.8.4 |
| N-1114 | C-0982 | Qualified Type Names | unchanged | JLS SE 25#JLS-6.5.5.2 |
| N-1115 | C-0983 | Quality gates based on risk | unchanged | Engineering scope#ENG-0260 |
| N-1116 | C-0984 | Quarkus architecture bookmark | unchanged | Engineering scope#ENG-0352 |
| N-1117 | C-0985 | Querying an ArrayList<E> | unchanged | Mughal 1Z0-829#M829-12.4; Mughal 1Z0-830#M830-P2-12.4 |
| N-1118 | C-0986 | Queues | unchanged | Mughal 1Z0-829#M829-15.6; Mughal 1Z0-830#M830-P2-15.6 |
| N-1119 | C-0987 | Raw Types | unchanged | JLS SE 25#JLS-4.8 |
| N-1120 | C-0988 | Reachable Objects | unchanged | Mughal 1Z0-829#M829-10.2; Mughal 1Z0-830#M830-P2-10.2 |
| N-1121 | C-0989 | Reading a ResultSet | unchanged | Boyarsky 1Z0-829#S-0503 |
| N-1122 | C-0990 | Reading `final` Fields During Construction | unchanged | JLS SE 25#JLS-17.5.2 |
| N-1123 | C-0991 | Reassigning Pattern Variables | unchanged | Boyarsky 1Z0-830#S-0043 |
| N-1124 | C-0992 | Receiving Arguments | unchanged | JVMS SE 25#JVMS-3.6 |
| N-1125 | C-0993 | Reclassification of Contextually Ambiguous Names | unchanged | JLS SE 25#JLS-6.5.2 |
| N-1126 | C-0994 | Recognizing Exception Classes | unchanged | Boyarsky 1Z0-829#S-0346; Boyarsky 1Z0-830#S-0297 |
| N-1127 | C-0995 | Record Body Declarations | unchanged | JLS SE 25#JLS-8.10.2 |
| N-1128 | C-0996 | Record Classes | structured-merge | JLS SE 25#JLS-8.10 |
| N-1129 | C-0996 | Record Classes | structured-merge | Mughal 1Z0-829#M829-5.14; Mughal 1Z0-830#M830-P2-5.14 |
| N-1130 | C-0997 | Record Components | unchanged | JLS SE 25#JLS-8.10.1 |
| N-1131 | C-0998 | Record Constructor Declarations | unchanged | JLS SE 25#JLS-8.10.4 |
| N-1132 | C-0999 | Record Members | unchanged | JLS SE 25#JLS-8.10.3 |
| N-1133 | C-1000 | Record Pattern Matching with the Enhanced switch Construct | unchanged | Mughal 1Z0-830#M830-P1-1.5 |
| N-1134 | C-1001 | Record Pattern Matching with the instanceof Pattern Match Operator | unchanged | Mughal 1Z0-830#M830-P1-1.4 |
| N-1135 | C-1002 | Record Pattern Type Inference | unchanged | JLS SE 25#JLS-18.5.5 |
| N-1136 | C-1003 | Record Patterns | unchanged | Mughal 1Z0-830#M830-P1-1.3 |
| N-1137 | C-1004 | Redeclaring private Methods | unchanged | Boyarsky 1Z0-829#S-0195; Boyarsky 1Z0-830#S-0187 |
| N-1138 | C-1005 | Reduction | unchanged | JLS SE 25#JLS-18.2 |
| N-1139 | C-1006 | Redundant Imports | unchanged | Boyarsky 1Z0-829#S-0015 |
| N-1140 | C-0154 | Reference Calling the super | merge | Boyarsky 1Z0-830#S-0169 |
| N-1141 | C-1007 | Reference Conditional Expressions | unchanged | JLS SE 25#JLS-15.25.3 |
| N-1142 | C-1008 | Reference Types | structured-merge | Boyarsky 1Z0-829#S-0167; Boyarsky 1Z0-830#S-0153 |
| N-1143 | C-1009 | Reference Value Assignment Conversions | unchanged | Mughal 1Z0-829#M829-5.9; Mughal 1Z0-830#M830-P2-5.9 |
| N-1144 | C-1010 | References | unchanged | JLS SE 25#JLS-1.7 |
| N-1145 | C-1011 | Referencing Nested Subclasses | unchanged | Boyarsky 1Z0-830#S-0217 |
| N-1146 | C-1012 | Referencing Variables from the Lambda Body | unchanged | Boyarsky 1Z0-829#S-0269; Boyarsky 1Z0-830#S-0272 |
| N-1147 | C-1013 | Registering for the Online Proctored Exam | unchanged | Mughal 1Z0-829#M829-A.2 |
| N-1148 | C-1014 | Reifiable Types | unchanged | JLS SE 25#JLS-4.7 |
| N-1149 | C-1015 | Relational Operators | structured-merge | Boyarsky 1Z0-829#S-0067; Boyarsky 1Z0-830#S-0029 |
| N-1150 | C-1015 | Relational Operators | structured-merge | JLS SE 25#JLS-15.20 |
| N-1151 | C-1016 | Remainder Operator `%` | unchanged | JLS SE 25#JLS-15.17.3 |
| N-1152 | C-1017 | Remote call as partial-failure boundary | unchanged | Engineering scope#ENG-0184 |
| N-1153 | C-1018 | Removing Data | unchanged | Boyarsky 1Z0-829#S-0274 |
| N-1154 | C-1019 | Removing with Conditions | unchanged | Boyarsky 1Z0-829#S-0278 |
| N-1155 | C-1020 | Repeatable Annotation Interfaces | unchanged | JLS SE 25#JLS-9.6.3 |
| N-1156 | C-1021 | Replacing Values | unchanged | Boyarsky 1Z0-829#S-0299 |
| N-1157 | C-1022 | Representation of Objects | unchanged | JVMS SE 25#JVMS-2.7 |
| N-1158 | C-1023 | Requirements for Parallel Reduction with collect() | unchanged | Boyarsky 1Z0-830#S-0421 |
| N-1159 | C-1024 | Requirements in Overriding | unchanged | JLS SE 25#JLS-9.4.1.2 |
| N-1160 | C-1025 | Requiring a Module Transitively | unchanged | Boyarsky 1Z0-829#S-0391; Boyarsky 1Z0-830#S-0345 |
| N-1161 | C-1026 | Reserved Opcodes | unchanged | JVMS SE 25#JVMS-6.2 |
| N-1162 | C-1027 | Resolution | unchanged | JLS SE 25#JLS-18.4 |
| N-1163 | C-1028 | Resolution | unchanged | JVMS SE 25#JVMS-5.4.3 |
| N-1164 | C-1029 | Resolution of Symbolic References | unchanged | JLS SE 25#JLS-12.3.3 |
| N-1165 | C-1030 | Restrictions on Field References in Initializers | unchanged | JLS SE 25#JLS-8.3.3 |
| N-1166 | C-1031 | Restrictions on the Use of Preview Features | unchanged | JLS SE 25#JLS-1.5.1 |
| N-1167 | C-1032 | Restrictions on the Use of Preview Features | unchanged | JVMS SE 25#JVMS-1.5.1 |
| N-1168 | C-1033 | ret | unchanged | JVMS SE 25#JVMS-0437 |
| N-1169 | C-1034 | return | structured-merge | JVMS SE 25#JVMS-0249 |
| N-1170 | C-1034 | return | structured-merge | JVMS SE 25#JVMS-0438 |
| N-1171 | C-1035 | Return Type | unchanged | Boyarsky 1Z0-829#S-0134; Boyarsky 1Z0-830#S-0118 |
| N-1172 | C-1036 | Return Value of Assignment Operators | unchanged | Boyarsky 1Z0-829#S-0064; Boyarsky 1Z0-830#S-0026 |
| N-1173 | C-1037 | Returning an Optional | unchanged | Boyarsky 1Z0-829#S-0319; Boyarsky 1Z0-830#S-0284 |
| N-1174 | C-1038 | Returning an OUT Parameter | unchanged | Boyarsky 1Z0-829#S-0509 |
| N-1175 | C-1039 | Returning Objects | unchanged | Boyarsky 1Z0-829#S-0164; Boyarsky 1Z0-830#S-0149 |
| N-1176 | C-1040 | Reusing CyclicBarrier | unchanged | Boyarsky 1Z0-830#S-0405 |
| N-1177 | C-1041 | Review of Key APIs | unchanged | Boyarsky 1Z0-829#S-0488; Boyarsky 1Z0-830#S-0467 |
| N-1178 | C-1042 | Reviewing Access Modifiers | unchanged | Boyarsky 1Z0-829#S-0154; Boyarsky 1Z0-830#S-0139 |
| N-1179 | C-1043 | Reviewing Branching | unchanged | Boyarsky 1Z0-829#S-0094; Boyarsky 1Z0-830#S-0071 |
| N-1180 | C-1044 | Reviewing Collection Types | unchanged | Boyarsky 1Z0-830#S-0281 |
| N-1181 | C-1045 | Reviewing Command-Line Options | unchanged | Boyarsky 1Z0-829#S-0407; Boyarsky 1Z0-830#S-0365 |
| N-1182 | C-1046 | Reviewing Method References | unchanged | Boyarsky 1Z0-829#S-0256; Boyarsky 1Z0-830#S-0258 |
| N-1183 | C-1047 | Reviewing Module Types | unchanged | Boyarsky 1Z0-829#S-0412; Boyarsky 1Z0-830#S-0371 |
| N-1184 | C-1048 | Reviewing Nested Classes | unchanged | Boyarsky 1Z0-829#S-0237; Boyarsky 1Z0-830#S-0237 |
| N-1185 | C-1049 | Reviewing Scope | unchanged | Boyarsky 1Z0-829#S-0046 |
| N-1186 | C-1050 | Reviewing Sealed Class Rules | unchanged | Boyarsky 1Z0-829#S-0225; Boyarsky 1Z0-830#S-0220 |
| N-1187 | C-1051 | Reviewing Thread Concepts | unchanged | Boyarsky 1Z0-830#S-0387 |
| N-1188 | C-1052 | Reviewing Transaction APIs | unchanged | Boyarsky 1Z0-829#S-0516 |
| N-1189 | C-1053 | Rolling deployment | unchanged | Engineering scope#ENG-0430 |
| N-1190 | C-1054 | Rolling upgrade compatibility | unchanged | Engineering scope#ENG-0474 |
| N-1191 | C-1055 | Rounding Numbers | unchanged | Boyarsky 1Z0-829#S-0118; Boyarsky 1Z0-830#S-0098 |
| N-1192 | C-1056 | Rules for Creating a Method with a Varargs Parameter | unchanged | Boyarsky 1Z0-830#S-0130 |
| N-1193 | C-1057 | Running Example: The CD Record Class | unchanged | Mughal 1Z0-829#M829-16.2; Mughal 1Z0-830#M830-P2-16.2 |
| N-1194 | C-1058 | Running Our First Module | unchanged | Boyarsky 1Z0-829#S-0382; Boyarsky 1Z0-830#S-0335 |
| N-1195 | C-1059 | Run-Time Constant Pool | structured-merge | JVMS SE 25#JVMS-2.5.5 |
| N-1196 | C-1060 | Run-Time Data Areas | unchanged | JVMS SE 25#JVMS-2.5 |
| N-1197 | C-1061 | Run-Time Evaluation of Array Access Expressions | unchanged | JLS SE 25#JLS-15.10.4 |
| N-1198 | C-1062 | Run-Time Evaluation of Array Creation Expressions | unchanged | JLS SE 25#JLS-15.10.2 |
| N-1199 | C-1063 | Run-Time Evaluation of Class Instance Creation Expressions | unchanged | JLS SE 25#JLS-15.9.4 |
| N-1200 | C-1064 | Run-Time Evaluation of Lambda Expressions | unchanged | JLS SE 25#JLS-15.27.4 |
| N-1201 | C-1065 | Run-Time Evaluation of Method Invocation | unchanged | JLS SE 25#JLS-15.12.4 |
| N-1202 | C-1066 | Run-Time Evaluation of Method References | unchanged | JLS SE 25#JLS-15.13.3 |
| N-1203 | C-1067 | Run-Time Evaluation of `switch` Expressions | unchanged | JLS SE 25#JLS-15.28.2 |
| N-1204 | C-1068 | Run-Time Handling of an Exception | unchanged | JLS SE 25#JLS-11.3 |
| N-1205 | C-1069 | Runtime Organization for Thread Execution | unchanged | Mughal 1Z0-829#M829-22.2; Mughal 1Z0-830#M830-P2-22.2 |
| N-1206 | C-1070 | RuntimeException Classes | unchanged | Boyarsky 1Z0-829#S-0347; Boyarsky 1Z0-830#S-0298 |
| N-1207 | C-1071 | Safe runtime configuration changes | unchanged | Engineering scope#ENG-0448 |
| N-1208 | C-1072 | saload | structured-merge | JVMS SE 25#JVMS-0250 |
| N-1209 | C-1072 | saload | structured-merge | JVMS SE 25#JVMS-0439 |
| N-1210 | C-1073 | Sample Java Program | unchanged | Mughal 1Z0-829#M829-1.8; Mughal 1Z0-830#M830-P2-1.8 |
| N-1211 | C-1074 | sastore | structured-merge | JVMS SE 25#JVMS-0251 |
| N-1212 | C-1074 | sastore | structured-merge | JVMS SE 25#JVMS-0440 |
| N-1213 | C-1075 | Scalability of Throughput with Virtual Threads | unchanged | Mughal 1Z0-830#M830-P1-3.7 |
| N-1214 | C-1076 | Scheduling Tasks | unchanged | Boyarsky 1Z0-829#S-0432; Boyarsky 1Z0-830#S-0395 |
| N-1215 | C-1077 | Schema ownership | unchanged | Engineering scope#ENG-0180 |
| N-1216 | C-1078 | Scope for Pattern Variables in `case` Labels | unchanged | JLS SE 25#JLS-6.3.3 |
| N-1217 | C-1079 | Scope for Pattern Variables in Expressions | unchanged | JLS SE 25#JLS-6.3.1 |
| N-1218 | C-1080 | Scope for Pattern Variables in Statements | unchanged | JLS SE 25#JLS-6.3.2 |
| N-1219 | C-1081 | Scope of a Declaration | unchanged | JLS SE 25#JLS-6.3 |
| N-1220 | C-1082 | Scope Rules | unchanged | Mughal 1Z0-829#M829-6.6; Mughal 1Z0-830#M830-P2-6.6 |
| N-1221 | C-1083 | `sealed` Classes | unchanged | JLS SE 25#JLS-13.4.2.1 |
| N-1222 | C-1084 | Sealing Classes | unchanged | Boyarsky 1Z0-829#S-0219; Boyarsky 1Z0-830#S-0212 |
| N-1223 | C-1085 | Sealing Interfaces | unchanged | Boyarsky 1Z0-829#S-0224; Boyarsky 1Z0-830#S-0218 |
| N-1224 | C-1086 | Searching | unchanged | Boyarsky 1Z0-829#S-0112; Boyarsky 1Z0-830#S-0092 |
| N-1225 | C-1087 | Searching a Directory | unchanged | Boyarsky 1Z0-829#S-0487; Boyarsky 1Z0-830#S-0465 |
| N-1226 | C-1088 | Searching for Classes on the Class Path | unchanged | Mughal 1Z0-829#M829-6.4; Mughal 1Z0-830#M830-P2-6.4 |
| N-1227 | C-1089 | Security filter-chain bookmark | unchanged | Engineering scope#ENG-0297 |
| N-1228 | C-1090 | Security Manager permanently disabled: legacy migration | unchanged | Engineering scope#ENG-0374 |
| N-1229 | C-1091 | Security Threat Categories | unchanged | Mughal 1Z0-829#M829-26.2; Mughal 1Z0-830#M830-P2-26.2 |
| N-1230 | C-1092 | Selected Standard Annotations | unchanged | Mughal 1Z0-829#M829-25.5; Mughal 1Z0-830#M830-P2-25.5 |
| N-1231 | C-1093 | Selecting a reduce() Method | unchanged | Boyarsky 1Z0-830#S-0420 |
| N-1232 | C-1094 | Selecting Resource Bundle Values | unchanged | Boyarsky 1Z0-829#S-0372; Boyarsky 1Z0-830#S-0324 |
| N-1233 | C-1095 | Selection Statements | unchanged | Mughal 1Z0-829#M829-4.1; Mughal 1Z0-830#M830-P2-4.1 |
| N-1234 | C-1096 | Semantics of `final` Fields | unchanged | JLS SE 25#JLS-17.5.1 |
| N-1235 | C-1097 | Separators | unchanged | JLS SE 25#JLS-3.11 |
| N-1236 | C-1098 | Sequenced Collections | unchanged | Mughal 1Z0-830#M830-P1-2.2 |
| N-1237 | C-1099 | Sequenced Concurrent Collections | unchanged | Mughal 1Z0-830#M830-P1-2.8 |
| N-1238 | C-1100 | Sequenced Concurrent Maps | unchanged | Mughal 1Z0-830#M830-P1-2.9 |
| N-1239 | C-1101 | Sequenced Lists | unchanged | Mughal 1Z0-830#M830-P1-2.3 |
| N-1240 | C-1102 | Sequenced Maps | unchanged | Mughal 1Z0-830#M830-P1-2.6 |
| N-1241 | C-1103 | Sequenced Sets | unchanged | Mughal 1Z0-830#M830-P1-2.4 |
| N-1242 | C-1104 | Serializing Data | unchanged | Boyarsky 1Z0-829#S-0472; Boyarsky 1Z0-830#S-0447 |
| N-1243 | C-1105 | Serializing Records | unchanged | Boyarsky 1Z0-830#S-0452 |
| N-1244 | C-1106 | Service Consumption | unchanged | JLS SE 25#JLS-7.7.3 |
| N-1245 | C-1107 | Service Provision | unchanged | JLS SE 25#JLS-7.7.4 |
| N-1246 | C-1108 | Services | unchanged | Mughal 1Z0-829#M829-19.9; Mughal 1Z0-830#M830-P2-19.9 |
| N-1247 | C-1109 | Sets | unchanged | Mughal 1Z0-829#M829-15.4; Mughal 1Z0-830#M830-P2-15.4 |
| N-1248 | C-1110 | Shadowing | unchanged | JLS SE 25#JLS-6.4.1 |
| N-1249 | C-1111 | Shared Variables | unchanged | JLS SE 25#JLS-17.4.1 |
| N-1250 | C-1112 | Shift Operators | unchanged | JLS SE 25#JLS-15.19 |
| N-1251 | C-1113 | Shortening Code with Pattern Matching | unchanged | Boyarsky 1Z0-829#S-0076; Boyarsky 1Z0-830#S-0042 |
| N-1252 | C-1114 | Shutting Down a Thread Executor | unchanged | Boyarsky 1Z0-829#S-0429; Boyarsky 1Z0-830#S-0394 |
| N-1253 | C-1115 | Signature Polymorphic Methods | unchanged | JVMS SE 25#JVMS-2.9.3 |
| N-1254 | C-1116 | Signatures | unchanged | JVMS SE 25#JVMS-4.7.9.1 |
| N-1255 | C-1117 | Simple Assignment Operator `=` | structured-merge | JLS SE 25#JLS-15.26.1 |
| N-1256 | C-1118 | Simple Expression Names | unchanged | JLS SE 25#JLS-6.5.6.1 |
| N-1257 | C-1119 | Simple Method Names | unchanged | JLS SE 25#JLS-6.5.7.1 |
| N-1258 | C-1120 | Simple Package Names | unchanged | JLS SE 25#JLS-6.5.3.1 |
| N-1259 | C-1121 | Simple PackageOrTypeNames | unchanged | JLS SE 25#JLS-6.5.4.1 |
| N-1260 | C-1122 | Simple Type Names | unchanged | JLS SE 25#JLS-6.5.5.1 |
| N-1261 | C-1123 | Single-Element Annotations | unchanged | JLS SE 25#JLS-9.7.3 |
| N-1262 | C-1124 | Single-Module-Import Declarations | unchanged | JLS SE 25#JLS-7.5.5 |
| N-1263 | C-1125 | Single-Static-Import Declarations | unchanged | JLS SE 25#JLS-7.5.3 |
| N-1264 | C-1126 | Single-Type-Import Declarations | unchanged | JLS SE 25#JLS-7.5.1 |
| N-1265 | C-1127 | sipush | structured-merge | JVMS SE 25#JVMS-0252 |
| N-1266 | C-1127 | sipush | structured-merge | JVMS SE 25#JVMS-0441 |
| N-1267 | C-1128 | Sorting | unchanged | Boyarsky 1Z0-829#S-0111; Boyarsky 1Z0-830#S-0091 |
| N-1268 | C-1129 | Sorting a List | unchanged | Boyarsky 1Z0-829#S-0309 |
| N-1269 | C-1130 | Sorting a Parallel Stream | unchanged | Boyarsky 1Z0-830#S-0419 |
| N-1270 | C-1131 | Sorting Data | unchanged | Boyarsky 1Z0-829#S-0303; Boyarsky 1Z0-830#S-0279 |
| N-1271 | C-1132 | Special Methods | unchanged | JVMS SE 25#JVMS-2.9 |
| N-1272 | C-1133 | Special-Purpose Synchronizers | unchanged | Mughal 1Z0-829#M829-23.5; Mughal 1Z0-830#M830-P2-23.5 |
| N-1273 | C-1134 | Specifying a Locale Category | unchanged | Boyarsky 1Z0-829#S-0368; Boyarsky 1Z0-830#S-0320 |
| N-1274 | C-1135 | Specifying the Subclass Modifier | unchanged | Boyarsky 1Z0-829#S-0222; Boyarsky 1Z0-830#S-0215 |
| N-1275 | C-1136 | Splitting a Big Project into Modules | unchanged | Boyarsky 1Z0-829#S-0417; Boyarsky 1Z0-830#S-0376 |
| N-1276 | C-1137 | Spotting Invalid Declarations | unchanged | Boyarsky 1Z0-829#S-0204; Boyarsky 1Z0-830#S-0196 |
| N-1277 | C-1138 | Spring Core bookmark | unchanged | Engineering scope#ENG-0283 |
| N-1278 | C-1139 | Spring Data boundary | unchanged | Engineering scope#ENG-0296 |
| N-1279 | C-1140 | Statements | structured-merge | JLS SE 25#JLS-14.5 |
| N-1280 | C-1140 | Statements | structured-merge | Mughal 1Z0-829#M829-3.3; Mughal 1Z0-830#M830-P2-3.3 |
| N-1281 | C-1141 | `static` Classes | unchanged | JLS SE 25#JLS-8.1.1.4 |
| N-1282 | C-1142 | Static Constraints | unchanged | JVMS SE 25#JVMS-4.9.1 |
| N-1283 | C-1143 | `static` Fields | structured-merge | JLS SE 25#JLS-13.4.10 |
| N-1284 | C-1143 | `static` Fields | structured-merge | JLS SE 25#JLS-8.3.1.1 |
| N-1285 | C-1144 | Static-Import-on-Demand Declarations | unchanged | JLS SE 25#JLS-7.5.4 |
| N-1286 | C-1145 | static Imports | unchanged | Boyarsky 1Z0-829#S-0161; Boyarsky 1Z0-830#S-0146 |
| N-1287 | C-1146 | Static Initializer Blocks | unchanged | Mughal 1Z0-829#M829-10.7; Mughal 1Z0-830#M830-P2-10.7 |
| N-1288 | C-1147 | static Initializers | structured-merge | Boyarsky 1Z0-829#S-0160; Boyarsky 1Z0-830#S-0145 |
| N-1289 | C-1147 | Static Initializers | structured-merge | JLS SE 25#JLS-13.4.25 |
| N-1290 | C-1147 | Static Initializers | structured-merge | JLS SE 25#JLS-8.7 |
| N-1291 | C-1148 | `static` Interfaces | unchanged | JLS SE 25#JLS-9.1.1.3 |
| N-1292 | C-1149 | Static Local Types | unchanged | Mughal 1Z0-829#M829-9.5; Mughal 1Z0-830#M830-P2-9.5 |
| N-1293 | C-1150 | Static Member Declarations | unchanged | Mughal 1Z0-829#M829-3.8; Mughal 1Z0-830#M830-P2-3.8 |
| N-1294 | C-1151 | Static Member Types | unchanged | Mughal 1Z0-829#M829-9.2; Mughal 1Z0-830#M830-P2-9.2 |
| N-1295 | C-1152 | Static Members | unchanged | Mughal 1Z0-829#M829-1.5; Mughal 1Z0-830#M830-P2-1.5 |
| N-1296 | C-1153 | `static` Methods | structured-merge | JLS SE 25#JLS-13.4.19 |
| N-1297 | C-1153 | `static` Methods | structured-merge | JLS SE 25#JLS-8.4.3.2 |
| N-1298 | C-1154 | static Variable Modifiers | unchanged | Boyarsky 1Z0-829#S-0159; Boyarsky 1Z0-830#S-0144 |
| N-1299 | C-1155 | Stream Basics | unchanged | Mughal 1Z0-829#M829-16.3; Mughal 1Z0-830#M830-P2-16.3 |
| N-1300 | C-1156 | Stream Operations on Directory Entries | unchanged | Mughal 1Z0-829#M829-21.8; Mughal 1Z0-830#M830-P2-21.8 |
| N-1301 | C-1157 | `strictfp` Classes | unchanged | JLS SE 25#JLS-8.1.1.3 |
| N-1302 | C-1158 | `strictfp` Interfaces | unchanged | JLS SE 25#JLS-9.1.1.2 |
| N-1303 | C-1159 | `strictfp` Methods | unchanged | JLS SE 25#JLS-8.4.3.5 |
| N-1304 | C-1160 | String Concatenation Operator `+` | unchanged | JLS SE 25#JLS-15.18.1 |
| N-1305 | C-1161 | String Contexts | unchanged | JLS SE 25#JLS-5.4 |
| N-1306 | C-1162 | String Conversion | unchanged | JLS SE 25#JLS-5.1.11 |
| N-1307 | C-1163 | String Literals | unchanged | JLS SE 25#JLS-3.10.5 |
| N-1308 | C-1164 | Structural Constraints | unchanged | JVMS SE 25#JVMS-4.9.2 |
| N-1309 | C-1165 | Submitting Tasks | unchanged | Boyarsky 1Z0-829#S-0430; Boyarsky 1Z0-830#S-0390 |
| N-1310 | C-1166 | Subsequent Modification of `final` Fields | unchanged | JLS SE 25#JLS-17.5.3 |
| N-1311 | C-1167 | Subtyping | unchanged | JLS SE 25#JLS-4.10 |
| N-1312 | C-1168 | Subtyping among Array Types | unchanged | JLS SE 25#JLS-4.10.3 |
| N-1313 | C-1169 | Subtyping among Primitive Types | unchanged | JLS SE 25#JLS-4.10.1 |
| N-1314 | C-1170 | Subtyping Constraints | unchanged | JLS SE 25#JLS-18.2.3 |
| N-1315 | C-1171 | Summarizing Statistics | unchanged | Boyarsky 1Z0-829#S-0332 |
| N-1316 | C-1172 | Summary | unchanged | Mughal 1Z0-829#M829-G.5 |
| N-1317 | C-1173 | Summary of Java Patterns | unchanged | Mughal 1Z0-830#M830-P1-1.6 |
| N-1318 | C-1174 | Summary of Selected Operations with the JDK Tools | unchanged | Mughal 1Z0-829#M829-19.14; Mughal 1Z0-830#M830-P2-19.14 |
| N-1319 | C-1175 | super() Always Refers to the Most Direct Parent | unchanged | Boyarsky 1Z0-830#S-0177 |
| N-1320 | C-1176 | Superinterfaces | structured-merge | JLS SE 25#JLS-13.5.3 |
| N-1321 | C-1176 | Superinterfaces | structured-merge | JLS SE 25#JLS-8.1.5 |
| N-1322 | C-1177 | Suppliers | unchanged | Mughal 1Z0-829#M829-13.5; Mughal 1Z0-830#M830-P2-13.5 |
| N-1323 | C-1178 | swap | structured-merge | JVMS SE 25#JVMS-0253 |
| N-1324 | C-1178 | swap | structured-merge | JVMS SE 25#JVMS-0442 |
| N-1325 | C-1179 | Switch Blocks | unchanged | JLS SE 25#JLS-14.11.1 |
| N-1326 | C-1180 | `switch` Expressions | structured-merge | JLS SE 25#JLS-15.28 |
| N-1327 | C-1180 | `switch` Expressions | structured-merge | JLS SE 25#JLS-16.1.6 |
| N-1328 | C-1180 | `switch` Expressions | structured-merge | JLS SE 25#JLS-6.3.1.6 |
| N-1329 | C-1181 | `switch` Statements | structured-merge | JLS SE 25#JLS-16.2.9 |
| N-1330 | C-1181 | `switch` Statements | structured-merge | JLS SE 25#JLS-6.3.2.6 |
| N-1331 | C-1182 | Synchronization | unchanged | JLS SE 25#JLS-17.1 |
| N-1332 | C-1183 | Synchronization | structured-merge | JVMS SE 25#JVMS-2.11.10 |
| N-1333 | C-1183 | Synchronization | structured-merge | JVMS SE 25#JVMS-3.14 |
| N-1334 | C-1184 | Synchronization Order | unchanged | JLS SE 25#JLS-17.4.4 |
| N-1335 | C-1185 | `synchronized` Methods | structured-merge | JLS SE 25#JLS-13.4.20 |
| N-1336 | C-1185 | `synchronized` Methods | structured-merge | JLS SE 25#JLS-8.4.3.6 |
| N-1337 | C-1186 | `synchronized` Statements | unchanged | JLS SE 25#JLS-16.2.14 |
| N-1338 | C-1187 | Synchronizing Methods | merge | Boyarsky 1Z0-830#S-0401 |
| N-1339 | C-1187 | Synchronizing on Methods | merge | Boyarsky 1Z0-829#S-0439 |
| N-1340 | C-1188 | Syntactic Classification of a Name According to Context | unchanged | JLS SE 25#JLS-6.5.1 |
| N-1341 | C-1189 | System.exit() | unchanged | Boyarsky 1Z0-830#S-0306 |
| N-1342 | C-1190 | tableswitch | structured-merge | JVMS SE 25#JVMS-0254 |
| N-1343 | C-1190 | tableswitch | structured-merge | JVMS SE 25#JVMS-0443 |
| N-1344 | C-1191 | Terminal Stream Operations | unchanged | Mughal 1Z0-829#M829-16.7; Mughal 1Z0-830#M830-P2-16.7 |
| N-1345 | C-1192 | Test names as behavior specifications | unchanged | Engineering scope#ENG-0202 |
| N-1346 | C-1193 | Testability as architectural consequence | unchanged | Engineering scope#ENG-0154 |
| N-1347 | C-1194 | Testcontainers in CI | unchanged | Engineering scope#ENG-0411 |
| N-1348 | C-1195 | Testing behavior instead of implementation | unchanged | Engineering scope#ENG-0221 |
| N-1349 | C-1196 | Testing Contexts | unchanged | JLS SE 25#JLS-5.7 |
| N-1350 | C-1197 | Testing ports with fakes | unchanged | Engineering scope#ENG-0263 |
| N-1351 | C-1198 | Testing use-case interactors | unchanged | Engineering scope#ENG-0262 |
| N-1352 | C-1199 | Text Blocks | unchanged | JLS SE 25#JLS-3.10.6 |
| N-1353 | C-1200 | The @FunctionalInterface Annotation | unchanged | Boyarsky 1Z0-830#S-0251 |
| N-1354 | C-1201 | The `AnnotationDefault` Attribute | unchanged | JVMS SE 25#JVMS-4.7.22 |
| N-1355 | C-1202 | The Arrays Class | unchanged | Mughal 1Z0-829#M829-15.12; Mughal 1Z0-830#M830-P2-15.12 |
| N-1356 | C-1203 | The `assert` Statement | unchanged | JLS SE 25#JLS-14.10 |
| N-1357 | C-1204 | The basic `for` Statement | unchanged | JLS SE 25#JLS-14.14.1 |
| N-1358 | C-1205 | The Binary String Concatenation Operator + | unchanged | Mughal 1Z0-829#M829-2.9 |
| N-1359 | C-1206 | The `boolean` Type | unchanged | JVMS SE 25#JVMS-2.3.4 |
| N-1360 | C-1207 | The `BootstrapMethods` Attribute | unchanged | JVMS SE 25#JVMS-4.7.23 |
| N-1361 | C-1208 | The break Statement | structured-merge | Boyarsky 1Z0-829#S-0090; Boyarsky 1Z0-830#S-0067 |
| N-1362 | C-1208 | The `break` Statement | structured-merge | JLS SE 25#JLS-14.15 |
| N-1363 | C-1208 | The break Statement | structured-merge | Mughal 1Z0-829#M829-4.11; Mughal 1Z0-830#M830-P2-4.11 |
| N-1364 | C-1209 | The Bytecode Verifier | unchanged | JVMS SE 25#JVMS-4.10.2.2 |
| N-1365 | C-1210 | The Causes of Exceptions | unchanged | JLS SE 25#JLS-11.1.2 |
| N-1366 | C-1211 | The `class` File Format | unchanged | JVMS SE 25#JVMS-2.1 |
| N-1367 | C-1212 | The Class `Object` | unchanged | JLS SE 25#JLS-4.3.2 |
| N-1368 | C-1213 | The Class `String` | unchanged | JLS SE 25#JLS-4.3.3 |
| N-1369 | C-1214 | The `ClassFile` Structure | unchanged | JVMS SE 25#JVMS-4.1 |
| N-1370 | C-1215 | The `Code` Attribute | unchanged | JVMS SE 25#JVMS-4.7.3 |
| N-1371 | C-1216 | The Collections Class | unchanged | Mughal 1Z0-829#M829-15.11; Mughal 1Z0-830#M830-P2-15.11 |
| N-1372 | C-0245 | The Conditional Operator ?: | structured-merge | Mughal 1Z0-829#M829-2.18; Mughal 1Z0-830#M830-P2-2.18 |
| N-1373 | C-1217 | The Console Class | unchanged | Mughal 1Z0-829#M829-20.4; Mughal 1Z0-830#M830-P2-20.4 |
| N-1374 | C-1218 | The Constant Pool | unchanged | JVMS SE 25#JVMS-4.4 |
| N-1375 | C-1219 | The `CONSTANT_Class_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.1 |
| N-1376 | C-1220 | The `CONSTANT_MethodHandle_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.8 |
| N-1377 | C-1221 | The `CONSTANT_MethodType_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.9 |
| N-1378 | C-1222 | The `CONSTANT_Module_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.11 |
| N-1379 | C-1223 | The `CONSTANT_NameAndType_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.6 |
| N-1380 | C-1224 | The `CONSTANT_Package_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.12 |
| N-1381 | C-1225 | The `CONSTANT_String_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.3 |
| N-1382 | C-1226 | The `CONSTANT_Utf8_info` Structure | unchanged | JVMS SE 25#JVMS-4.4.7 |
| N-1383 | C-1227 | The `ConstantValue` Attribute | unchanged | JVMS SE 25#JVMS-4.7.2 |
| N-1384 | C-1228 | The continue Statement | structured-merge | Boyarsky 1Z0-829#S-0091; Boyarsky 1Z0-830#S-0068 |
| N-1385 | C-1228 | The `continue` Statement | structured-merge | JLS SE 25#JLS-14.16 |
| N-1386 | C-1228 | The continue Statement | structured-merge | Mughal 1Z0-829#M829-4.12; Mughal 1Z0-830#M830-P2-4.12 |
| N-1387 | C-0362 | The Default Constructor | structured-merge | Boyarsky 1Z0-829#S-0186; Boyarsky 1Z0-830#S-0172 |
| N-1388 | C-1229 | The `Deprecated` Attribute | unchanged | JVMS SE 25#JVMS-4.7.15 |
| N-1389 | C-1230 | The `do` Statement | unchanged | JLS SE 25#JLS-14.13 |
| N-1390 | C-1231 | The do-while Statement | unchanged | Mughal 1Z0-829#M829-4.6; Mughal 1Z0-830#M830-P2-4.6 |
| N-1391 | C-1232 | The `element_value` structure | unchanged | JVMS SE 25#JVMS-4.7.16.1 |
| N-1392 | C-1233 | The else Statement | unchanged | Boyarsky 1Z0-829#S-0075; Boyarsky 1Z0-830#S-0040 |
| N-1393 | C-1234 | The Empty Statement | unchanged | JLS SE 25#JLS-14.6 |
| N-1394 | C-1235 | The `EnclosingMethod` Attribute | unchanged | JVMS SE 25#JVMS-4.7.7 |
| N-1395 | C-1236 | The enhanced `for` statement | unchanged | JLS SE 25#JLS-14.14.2 |
| N-1396 | C-1237 | The `Exceptions` Attribute | unchanged | JVMS SE 25#JVMS-4.7.5 |
| N-1397 | C-1238 | The Executor Framework | unchanged | Mughal 1Z0-829#M829-23.2; Mughal 1Z0-830#M830-P2-23.2 |
| N-1398 | C-1239 | The for-each Loop | unchanged | Boyarsky 1Z0-829#S-0086; Boyarsky 1Z0-830#S-0063 |
| N-1399 | C-1240 | The for Loop | unchanged | Boyarsky 1Z0-829#S-0085; Boyarsky 1Z0-830#S-0061 |
| N-1400 | C-1241 | The `for` Statement | structured-merge | JLS SE 25#JLS-14.14 |
| N-1401 | C-1241 | The for(;;) Statement | structured-merge | Mughal 1Z0-829#M829-4.7; Mughal 1Z0-830#M830-P2-4.7 |
| N-1402 | C-1241 | The for(:) Statement | structured-merge | Mughal 1Z0-829#M829-4.8; Mughal 1Z0-830#M830-P2-4.8 |
| N-1403 | C-1242 | The Form of a Binary | unchanged | JLS SE 25#JLS-13.1 |
| N-1404 | C-1243 | The if Statement | structured-merge | Boyarsky 1Z0-829#S-0074; Boyarsky 1Z0-830#S-0038 |
| N-1405 | C-1243 | The `if` Statement | structured-merge | JLS SE 25#JLS-14.9 |
| N-1406 | C-1244 | The `if`-`then`-`else` Statement | unchanged | JLS SE 25#JLS-14.9.2 |
| N-1407 | C-1245 | The `if`-`then` Statement | unchanged | JLS SE 25#JLS-14.9.1 |
| N-1408 | C-1246 | The `InnerClasses` Attribute | unchanged | JVMS SE 25#JVMS-4.7.6 |
| N-1409 | C-1247 | The instanceof Operator | structured-merge | Boyarsky 1Z0-829#S-0241; Boyarsky 1Z0-830#S-0241 |
| N-1410 | C-1247 | The `instanceof` Operator | structured-merge | JLS SE 25#JLS-15.20.2 |
| N-1411 | C-1248 | The Java Collections Framework | unchanged | Mughal 1Z0-829#M829-15.1; Mughal 1Z0-830#M830-P2-15.1 |
| N-1412 | C-1249 | The Java Ecosystem | unchanged | Mughal 1Z0-829#M829-1.1; Mughal 1Z0-830#M830-P2-1.1 |
| N-1413 | C-1250 | The Java Virtual Machine | unchanged | JVMS SE 25#JVMS-1.2 |
| N-1414 | C-1251 | The Kinds of Exceptions | unchanged | JLS SE 25#JLS-11.1.1 |
| N-1415 | C-1252 | The Lexical Grammar | unchanged | JLS SE 25#JLS-2.2 |
| N-1416 | C-1253 | The `LineNumberTable` Attribute | unchanged | JVMS SE 25#JVMS-4.7.12 |
| N-1417 | C-1254 | The Loading Process | unchanged | JLS SE 25#JLS-12.2.1 |
| N-1418 | C-1255 | The `LocalVariableTable` Attribute | unchanged | JVMS SE 25#JVMS-4.7.13 |
| N-1419 | C-1256 | The `LocalVariableTypeTable` Attribute | unchanged | JVMS SE 25#JVMS-4.7.14 |
| N-1420 | C-1257 | The main() Method | unchanged | Mughal 1Z0-829#M829-3.12; Mughal 1Z0-830#M830-P2-3.12 |
| N-1421 | C-1258 | The Math Class | unchanged | Mughal 1Z0-829#M829-8.6; Mughal 1Z0-830#M830-P2-8.6 |
| N-1422 | C-1259 | The `MethodParameters` Attribute | unchanged | JVMS SE 25#JVMS-4.7.24 |
| N-1423 | C-1260 | The Modular JDK | unchanged | Mughal 1Z0-829#M829-19.2; Mughal 1Z0-830#M830-P2-19.2 |
| N-1424 | C-1261 | The `Module` Attribute | unchanged | JVMS SE 25#JVMS-4.7.25 |
| N-1425 | C-1262 | The `ModuleMainClass` Attribute | unchanged | JVMS SE 25#JVMS-4.7.27 |
| N-1426 | C-1263 | The `ModulePackages` Attribute | unchanged | JVMS SE 25#JVMS-4.7.26 |
| N-1427 | C-1264 | The Multi- catch Clause | unchanged | Mughal 1Z0-829#M829-7.6; Mughal 1Z0-830#M830-P2-7.6 |
| N-1428 | C-1265 | The `NestHost` Attribute | unchanged | JVMS SE 25#JVMS-4.7.28 |
| N-1429 | C-1266 | The `NestMembers` Attribute | unchanged | JVMS SE 25#JVMS-4.7.29 |
| N-1430 | C-1267 | The Null Literal | unchanged | JLS SE 25#JLS-3.10.8 |
| N-1431 | C-1268 | The Object Class | unchanged | Mughal 1Z0-829#M829-8.2; Mughal 1Z0-830#M830-P2-8.2 |
| N-1432 | C-1269 | The Object Reference super | unchanged | Mughal 1Z0-829#M829-5.2; Mughal 1Z0-830#M830-P2-5.2 |
| N-1433 | C-1270 | The Objects Class | unchanged | Mughal 1Z0-829#M829-14.1; Mughal 1Z0-830#M830-P2-14.1 |
| N-1434 | C-1271 | The Optional Class | unchanged | Mughal 1Z0-829#M829-16.6; Mughal 1Z0-830#M830-P2-16.6 |
| N-1435 | C-1272 | The `pc` Register | unchanged | JVMS SE 25#JVMS-2.5.1 |
| N-1436 | C-1273 | The `PermittedSubclasses` Attribute | unchanged | JVMS SE 25#JVMS-4.7.31 |
| N-1437 | C-1274 | The Process of Verification by Type Inference | structured-merge | JVMS SE 25#JVMS-4.10.2.1 |
| N-1438 | C-1275 | The Questions | unchanged | Mughal 1Z0-829#M829-A.4 |
| N-1439 | C-1276 | The Random Class | unchanged | Mughal 1Z0-829#M829-8.7; Mughal 1Z0-830#M830-P2-8.7 |
| N-1440 | C-1277 | The `Record` Attribute | unchanged | JVMS SE 25#JVMS-4.7.30 |
| N-1441 | C-1278 | The return Statement | structured-merge | Boyarsky 1Z0-829#S-0092; Boyarsky 1Z0-830#S-0069 |
| N-1442 | C-1278 | The `return` Statement | structured-merge | JLS SE 25#JLS-14.17 |
| N-1443 | C-1278 | The return Statement | structured-merge | Mughal 1Z0-829#M829-4.13; Mughal 1Z0-830#M830-P2-4.13 |
| N-1444 | C-1279 | The Role of Exceptions | unchanged | Boyarsky 1Z0-829#S-0340; Boyarsky 1Z0-830#S-0290 |
| N-1445 | C-1059 | The Run-Time Constant Pool | structured-merge | JVMS SE 25#JVMS-5.1 |
| N-1446 | C-1280 | The `RuntimeInvisibleAnnotations` Attribute | unchanged | JVMS SE 25#JVMS-4.7.17 |
| N-1447 | C-1281 | The `RuntimeInvisibleParameterAnnotations` Attribute | unchanged | JVMS SE 25#JVMS-4.7.19 |
| N-1448 | C-1282 | The `RuntimeInvisibleTypeAnnotations` Attribute | unchanged | JVMS SE 25#JVMS-4.7.21 |
| N-1449 | C-1283 | The `RuntimeVisibleAnnotations` Attribute | unchanged | JVMS SE 25#JVMS-4.7.16 |
| N-1450 | C-1284 | The `RuntimeVisibleParameterAnnotations` Attribute | unchanged | JVMS SE 25#JVMS-4.7.18 |
| N-1451 | C-1285 | The `RuntimeVisibleTypeAnnotations` Attribute | unchanged | JVMS SE 25#JVMS-4.7.20 |
| N-1452 | C-1286 | The `Signature` Attribute | unchanged | JVMS SE 25#JVMS-4.7.9 |
| N-1453 | C-1117 | The Simple Assignment Operator = | structured-merge | Mughal 1Z0-829#M829-2.7 |
| N-1454 | C-1287 | The `SourceDebugExtension` Attribute | unchanged | JVMS SE 25#JVMS-4.7.11 |
| N-1455 | C-1288 | The `SourceFile` Attribute | unchanged | JVMS SE 25#JVMS-4.7.10 |
| N-1456 | C-1289 | The `StackMapTable` Attribute | unchanged | JVMS SE 25#JVMS-4.7.4 |
| N-1457 | C-1290 | The String Class | unchanged | Mughal 1Z0-829#M829-8.4; Mughal 1Z0-830#M830-P2-8.4 |
| N-1458 | C-1291 | The String Pool | unchanged | Boyarsky 1Z0-829#S-0106; Boyarsky 1Z0-830#S-0085 |
| N-1459 | C-1292 | The StringBuilder Class | unchanged | Mughal 1Z0-829#M829-8.5; Mughal 1Z0-830#M830-P2-8.5 |
| N-1460 | C-1293 | The Switch Block of a `switch` Expression | unchanged | JLS SE 25#JLS-15.28.1 |
| N-1461 | C-1294 | The Switch Block of a `switch` Statement | unchanged | JLS SE 25#JLS-14.11.2 |
| N-1462 | C-1295 | The switch Expression | merge | Boyarsky 1Z0-829#S-0079 |
| N-1463 | C-1295 | The switch Expression | merge | Mughal 1Z0-829#M829-4.3; Mughal 1Z0-830#M830-P2-4.3 |
| N-1464 | C-1296 | The switch Statement | structured-merge | Boyarsky 1Z0-829#S-0078 |
| N-1465 | C-1296 | The `switch` Statement | structured-merge | JLS SE 25#JLS-14.11 |
| N-1466 | C-1296 | The switch Statement | structured-merge | Mughal 1Z0-829#M829-4.2; Mughal 1Z0-830#M830-P2-4.2 |
| N-1467 | C-1297 | The `synchronized` Statement | unchanged | JLS SE 25#JLS-14.19 |
| N-1468 | C-1298 | The Syntactic Grammar | unchanged | JLS SE 25#JLS-2.3 |
| N-1469 | C-1299 | The `Synthetic` Attribute | unchanged | JVMS SE 25#JVMS-4.7.8 |
| N-1470 | C-1300 | The `target_info` union | unchanged | JVMS SE 25#JVMS-4.7.20.1 |
| N-1471 | C-1301 | The `throw` Statement | structured-merge | JLS SE 25#JLS-14.18 |
| N-1472 | C-1301 | The throw Statement | structured-merge | Mughal 1Z0-829#M829-7.4; Mughal 1Z0-830#M830-P2-7.4 |
| N-1473 | C-1302 | The throws Clause | unchanged | Mughal 1Z0-829#M829-7.5; Mughal 1Z0-830#M830-P2-7.5 |
| N-1474 | C-1303 | The `try` statement | unchanged | JLS SE 25#JLS-14.20 |
| N-1475 | C-1304 | The try -with-resources Statement | unchanged | Mughal 1Z0-829#M829-7.7; Mughal 1Z0-830#M830-P2-7.7 |
| N-1476 | C-1305 | The Type of a Constructor | unchanged | JLS SE 25#JLS-8.8.6 |
| N-1477 | C-1306 | The `type_path` structure | unchanged | JVMS SE 25#JVMS-4.7.20.2 |
| N-1478 | C-1307 | The while Statement | structured-merge | Boyarsky 1Z0-829#S-0081; Boyarsky 1Z0-830#S-0057 |
| N-1479 | C-1307 | The `while` Statement | structured-merge | JLS SE 25#JLS-14.12 |
| N-1480 | C-1307 | The while Statement | structured-merge | Mughal 1Z0-829#M829-4.5; Mughal 1Z0-830#M830-P2-4.5 |
| N-1481 | C-1308 | The Wrapper Classes | unchanged | Mughal 1Z0-829#M829-8.3; Mughal 1Z0-830#M830-P2-8.3 |
| N-1482 | C-1309 | The `yield` Statement | unchanged | JLS SE 25#JLS-14.21 |
| N-1483 | C-1310 | `this` | unchanged | JLS SE 25#JLS-15.8.3 |
| N-1484 | C-1311 | Thread Issues | unchanged | Mughal 1Z0-829#M829-22.5; Mughal 1Z0-830#M830-P2-22.5 |
| N-1485 | C-1312 | Thread Lifecycle | unchanged | Mughal 1Z0-829#M829-22.4; Mughal 1Z0-830#M830-P2-22.4 |
| N-1486 | C-1313 | Throwing an Exception | unchanged | Boyarsky 1Z0-829#S-0342; Boyarsky 1Z0-830#S-0292 |
| N-1487 | C-1314 | Throwing Exceptions | unchanged | JVMS SE 25#JVMS-2.11.9 |
| N-1488 | C-1315 | Timeout budgets across call chains | unchanged | Engineering scope#ENG-0442 |
| N-1489 | C-1316 | Tracing Eligibility | unchanged | Boyarsky 1Z0-829#S-0049 |
| N-1490 | C-1317 | Tracing Scope | unchanged | Boyarsky 1Z0-829#S-0044 |
| N-1491 | C-1318 | Transactions around use cases | unchanged | Engineering scope#ENG-0165 |
| N-1492 | C-1319 | Transfer Statements | unchanged | Mughal 1Z0-829#M829-4.9; Mughal 1Z0-830#M830-P2-4.9 |
| N-1493 | C-1320 | `transient` Fields | structured-merge | JLS SE 25#JLS-13.4.11 |
| N-1494 | C-1320 | `transient` Fields | structured-merge | JLS SE 25#JLS-8.3.1.3 |
| N-1495 | C-1321 | Traversing a Directory Tree | unchanged | Boyarsky 1Z0-829#S-0486; Boyarsky 1Z0-830#S-0464 |
| N-1496 | C-1322 | `try` Statements | unchanged | JLS SE 25#JLS-16.2.15 |
| N-1497 | C-0115 | `try`-with-resources | structured-merge | JLS SE 25#JLS-14.20.3 |
| N-1498 | C-1323 | Type Arguments of Parameterized Types | unchanged | JLS SE 25#JLS-4.5.1 |
| N-1499 | C-1324 | Type Checking Code Streams | unchanged | JVMS SE 25#JVMS-4.10.1.6 |
| N-1500 | C-1325 | Type Checking for `protected` Members | unchanged | JVMS SE 25#JVMS-4.10.1.8 |
| N-1501 | C-1326 | Type Checking Instructions | unchanged | JVMS SE 25#JVMS-4.10.1.9 |
| N-1502 | C-1327 | Type Checking Methods | unchanged | JVMS SE 25#JVMS-4.10.1.5 |
| N-1503 | C-1328 | Type Compatibility Constraints | unchanged | JLS SE 25#JLS-18.2.2 |
| N-1504 | C-1329 | Type Conversion Contexts | unchanged | Mughal 1Z0-829#M829-2.4; Mughal 1Z0-830#M830-P2-2.4 |
| N-1505 | C-1330 | Type Conversion Instructions | unchanged | JVMS SE 25#JVMS-2.11.4 |
| N-1506 | C-1331 | Type Equality Constraints | unchanged | JLS SE 25#JLS-18.2.4 |
| N-1507 | C-1332 | Type Erasure | structured-merge | JLS SE 25#JLS-4.6 |
| N-1508 | C-1332 | Type Erasure | structured-merge | Mughal 1Z0-829#M829-11.11; Mughal 1Z0-830#M830-P2-11.11 |
| N-1509 | C-1333 | Type-Import-on-Demand Declarations | unchanged | JLS SE 25#JLS-7.5.2 |
| N-1510 | C-1334 | Type of a Lambda Expression | unchanged | JLS SE 25#JLS-15.27.3 |
| N-1511 | C-1335 | Type of a Method Reference | unchanged | JLS SE 25#JLS-15.13.2 |
| N-1512 | C-1336 | Type of an Expression | unchanged | JLS SE 25#JLS-15.3 |
| N-1513 | C-1337 | Type Pattern Matching with the Enhanced switch Construct | unchanged | Mughal 1Z0-830#M830-P1-1.2 |
| N-1514 | C-1338 | Type Pattern Matching with the instanceof Pattern Match Operator | unchanged | Mughal 1Z0-830#M830-P1-1.1 |
| N-1515 | C-1339 | Type Projections | unchanged | JLS SE 25#JLS-4.10.5 |
| N-1516 | C-1340 | Type Variables | unchanged | JLS SE 25#JLS-4.4 |
| N-1517 | C-1341 | Types of Operators | unchanged | Boyarsky 1Z0-829#S-0052; Boyarsky 1Z0-830#S-0014 |
| N-1518 | C-1342 | UDP DatagramSocket semantics | unchanged | Engineering scope#ENG-0038 |
| N-1519 | C-1343 | UI boundary bookmark | unchanged | Engineering scope#ENG-0245 |
| N-1520 | C-1344 | UI independence | unchanged | Engineering scope#ENG-0151 |
| N-1521 | C-1345 | Unary Minus Operator `-` | unchanged | JLS SE 25#JLS-15.15.4 |
| N-1522 | C-1346 | Unary Operators | unchanged | JLS SE 25#JLS-15.15 |
| N-1523 | C-1347 | Unary Plus Operator `+` | unchanged | JLS SE 25#JLS-15.15.3 |
| N-1524 | C-1348 | Unboxing Conversion | unchanged | JLS SE 25#JLS-5.1.8 |
| N-1525 | C-1349 | Unchecked Conversion | unchanged | JLS SE 25#JLS-5.1.9 |
| N-1526 | C-1350 | Understanding Arrays | unchanged | Boyarsky 1Z0-829#S-0107; Boyarsky 1Z0-830#S-0086 |
| N-1527 | C-1351 | Understanding Data Types | unchanged | Boyarsky 1Z0-829#S-0028; Boyarsky 1Z0-830#S-0007 |
| N-1528 | C-1352 | Understanding Encapsulation | unchanged | Boyarsky 1Z0-829#S-0227; Boyarsky 1Z0-830#S-0222 |
| N-1529 | C-1353 | Understanding Equality | unchanged | Boyarsky 1Z0-829#S-0104; Boyarsky 1Z0-830#S-0083 |
| N-1530 | C-1354 | Understanding Exception Types | unchanged | Boyarsky 1Z0-829#S-0341; Boyarsky 1Z0-830#S-0291 |
| N-1531 | C-1355 | Understanding Exceptions | unchanged | Boyarsky 1Z0-829#S-0339; Boyarsky 1Z0-830#S-0289 |
| N-1532 | C-1356 | Understanding Garbage Collection | unchanged | Boyarsky 1Z0-829#S-0048 |
| N-1533 | C-1357 | Understanding Inheritance | unchanged | Boyarsky 1Z0-829#S-0174; Boyarsky 1Z0-830#S-0160 |
| N-1534 | C-1358 | Understanding Java Operators | unchanged | Boyarsky 1Z0-829#S-0051; Boyarsky 1Z0-830#S-0013 |
| N-1535 | C-1359 | Understanding Liveness | unchanged | Boyarsky 1Z0-829#S-0447; Boyarsky 1Z0-830#S-0411 |
| N-1536 | C-1360 | Understanding Memory Consistency Errors | unchanged | Boyarsky 1Z0-829#S-0443; Boyarsky 1Z0-830#S-0407 |
| N-1537 | C-1361 | Understanding Polymorphism | unchanged | Boyarsky 1Z0-829#S-0238; Boyarsky 1Z0-830#S-0238 |
| N-1538 | C-1362 | Understanding Record Immutability | unchanged | Boyarsky 1Z0-829#S-0229; Boyarsky 1Z0-830#S-0226 |
| N-1539 | C-1363 | Understanding Suppressed Exceptions | unchanged | Boyarsky 1Z0-829#S-0359; Boyarsky 1Z0-830#S-0311 |
| N-1540 | C-1364 | Understanding the Class Structure | unchanged | Boyarsky 1Z0-829#S-0005; Boyarsky 1Z0-830#S-0003 |
| N-1541 | C-1365 | Understanding the Deserialization Creation Process | unchanged | Boyarsky 1Z0-829#S-0477; Boyarsky 1Z0-830#S-0454 |
| N-1542 | C-1366 | Understanding the Lock Framework | unchanged | Boyarsky 1Z0-829#S-0440; Boyarsky 1Z0-830#S-0402 |
| N-1543 | C-1367 | Understanding the Pipeline Flow | unchanged | Boyarsky 1Z0-829#S-0323 |
| N-1544 | C-1368 | Understanding Thread Concurrency | unchanged | Boyarsky 1Z0-829#S-0421; Boyarsky 1Z0-830#S-0381 |
| N-1545 | C-1369 | Understanding Thread-Safety | unchanged | Boyarsky 1Z0-829#S-0435; Boyarsky 1Z0-830#S-0398 |
| N-1546 | C-1370 | Understanding Type Erasure | unchanged | Boyarsky 1Z0-829#S-0312 |
| N-1547 | C-1371 | Unexpected Failure in Pattern Matching | unchanged | Mughal 1Z0-830#M830-P1-1.8 |
| N-1548 | C-1372 | Unicode | unchanged | JLS SE 25#JLS-3.1 |
| N-1549 | C-1373 | Unicode Escapes | unchanged | JLS SE 25#JLS-3.3 |
| N-1550 | C-1374 | Unnamed Modules | structured-merge | Boyarsky 1Z0-829#S-0411; Boyarsky 1Z0-830#S-0370 |
| N-1551 | C-1374 | Unnamed Modules | structured-merge | JLS SE 25#JLS-7.7.5 |
| N-1552 | C-1375 | Unnamed Packages | unchanged | JLS SE 25#JLS-7.4.2 |
| N-1553 | C-1376 | Unqualified Names | unchanged | JVMS SE 25#JVMS-4.2.2 |
| N-1554 | C-1377 | Unreachable Code | unchanged | Boyarsky 1Z0-829#S-0093; Boyarsky 1Z0-830#S-0070 |
| N-1555 | C-1378 | Unreachable Statements | unchanged | JLS SE 25#JLS-14.22 |
| N-1556 | C-1379 | Updating Multiple Records | unchanged | Boyarsky 1Z0-829#S-0501 |
| N-1557 | C-1380 | Updating Our Example for Multiple Modules | unchanged | Boyarsky 1Z0-829#S-0384; Boyarsky 1Z0-830#S-0337 |
| N-1558 | C-1381 | Updating the Feeding Module | unchanged | Boyarsky 1Z0-829#S-0385; Boyarsky 1Z0-830#S-0338 |
| N-1559 | C-1382 | Uses of Inference | unchanged | JLS SE 25#JLS-18.5 |
| N-1560 | C-1383 | Using a Spliterator | unchanged | Boyarsky 1Z0-829#S-0336 |
| N-1561 | C-1384 | Using Additional Options | unchanged | Boyarsky 1Z0-829#S-0512 |
| N-1562 | C-1385 | Using an Array | unchanged | Boyarsky 1Z0-829#S-0110; Boyarsky 1Z0-830#S-0090 |
| N-1563 | C-1386 | Using Big Numbers | unchanged | Mughal 1Z0-829#M829-8.8; Mughal 1Z0-830#M830-P2-8.8 |
| N-1564 | C-1387 | Using Bind Variables | unchanged | Boyarsky 1Z0-829#S-0505 |
| N-1565 | C-1388 | Using Common Collection APIs | unchanged | Boyarsky 1Z0-829#S-0271; Boyarsky 1Z0-830#S-0274 |
| N-1566 | C-1389 | Using Common Intermediate Operations | unchanged | Boyarsky 1Z0-829#S-0326 |
| N-1567 | C-1390 | Using Common Terminal Operations | unchanged | Boyarsky 1Z0-829#S-0325 |
| N-1568 | C-1391 | Using Concurrent Collections | unchanged | Boyarsky 1Z0-829#S-0442; Boyarsky 1Z0-830#S-0406 |
| N-1569 | C-1392 | Using Convenience Methods on Functional Interfaces | unchanged | Boyarsky 1Z0-829#S-0264; Boyarsky 1Z0-830#S-0266 |
| N-1570 | C-1393 | Using DirectoryStream | unchanged | Boyarsky 1Z0-830#S-0466 |
| N-1571 | C-1394 | Using Enum Values with switch | unchanged | Boyarsky 1Z0-830#S-0049 |
| N-1572 | C-1395 | Using Enums in switch Statements | unchanged | Boyarsky 1Z0-829#S-0217 |
| N-1573 | C-1396 | Using format() with Flags | unchanged | Boyarsky 1Z0-830#S-0076 |
| N-1574 | C-1397 | Using jpackage with Non-Modular Applications | unchanged | Boyarsky 1Z0-830#S-0364 |
| N-1575 | C-1398 | Using Local Variables inside a Lambda Body | unchanged | Boyarsky 1Z0-829#S-0268; Boyarsky 1Z0-830#S-0271 |
| N-1576 | C-1399 | Using Locales | unchanged | Mughal 1Z0-829#M829-18.1; Mughal 1Z0-830#M830-P2-18.1 |
| N-1577 | C-1400 | Using Method References | unchanged | Boyarsky 1Z0-829#S-0251; Boyarsky 1Z0-830#S-0253 |
| N-1578 | C-1401 | Using Methods with Varargs | unchanged | Boyarsky 1Z0-829#S-0114; Boyarsky 1Z0-830#S-0094 |
| N-1579 | C-1402 | Using Module Files with jmod | unchanged | Boyarsky 1Z0-829#S-0405; Boyarsky 1Z0-830#S-0361 |
| N-1580 | C-1403 | Using Optional with Primitive Streams | unchanged | Boyarsky 1Z0-829#S-0331 |
| N-1581 | C-1404 | Using Pattern Matching with Records | unchanged | Boyarsky 1Z0-830#S-0227 |
| N-1582 | C-1405 | Using Pattern Matching with switch | unchanged | Boyarsky 1Z0-830#S-0054 |
| N-1583 | C-1406 | Using Primitive Types | unchanged | Boyarsky 1Z0-829#S-0029 |
| N-1584 | C-1407 | Using Qualified Name for Enum Constants in the switch Construct | unchanged | Mughal 1Z0-830#M830-P1-1.7 |
| N-1585 | C-1008 | Using Reference Types | structured-merge | Boyarsky 1Z0-829#S-0030 |
| N-1586 | C-1408 | Using References of Wildcard Parameterized Types | unchanged | Mughal 1Z0-829#M829-11.5; Mughal 1Z0-830#M830-P2-11.5 |
| N-1587 | C-1409 | Using ServiceLoader | unchanged | Boyarsky 1Z0-830#S-0350 |
| N-1588 | C-1410 | Using Shared Functionality | unchanged | Boyarsky 1Z0-829#S-0458; Boyarsky 1Z0-830#S-0429 |
| N-1589 | C-1411 | Using Streams | unchanged | Boyarsky 1Z0-829#S-0322; Boyarsky 1Z0-830#S-0285 |
| N-1590 | C-1412 | Using the Arrow Operator with switch Statements | unchanged | Boyarsky 1Z0-830#S-0048 |
| N-1591 | C-1413 | Using the Diamond Operator | unchanged | Boyarsky 1Z0-829#S-0272 |
| N-1592 | C-1414 | Using the --jdk-internals Flag | unchanged | Boyarsky 1Z0-829#S-0404; Boyarsky 1Z0-830#S-0360 |
| N-1593 | C-1415 | Using the List Interface | unchanged | Boyarsky 1Z0-829#S-0281; Boyarsky 1Z0-830#S-0275 |
| N-1594 | C-1416 | Using the Map Interface | unchanged | Boyarsky 1Z0-829#S-0293; Boyarsky 1Z0-830#S-0278 |
| N-1595 | C-1417 | Using the Properties Class | unchanged | Boyarsky 1Z0-829#S-0374; Boyarsky 1Z0-830#S-0326 |
| N-1596 | C-1418 | Using the Set Interface | unchanged | Boyarsky 1Z0-829#S-0287; Boyarsky 1Z0-830#S-0276 |
| N-1597 | C-1419 | Using the StringBuilder Class | unchanged | Boyarsky 1Z0-829#S-0100; Boyarsky 1Z0-830#S-0078 |
| N-1598 | C-1420 | Using Thread Builders to Create Virtual Threads | unchanged | Mughal 1Z0-830#M830-P1-3.4 |
| N-1599 | C-1421 | Using Thread Class to Create Virtual Threads | unchanged | Mughal 1Z0-830#M830-P1-3.3 |
| N-1600 | C-1422 | Using Thread Executor Services | unchanged | Mughal 1Z0-830#M830-P1-3.6 |
| N-1601 | C-1423 | Using Thread Factory to Create Threads | unchanged | Mughal 1Z0-830#M830-P1-3.5 |
| N-1602 | C-1424 | Using Varargs with Other Method Parameters | unchanged | Boyarsky 1Z0-829#S-0148; Boyarsky 1Z0-830#S-0133 |
| N-1603 | C-1425 | var Assigning Lambdas to | unchanged | Boyarsky 1Z0-830#S-0248 |
| N-1604 | C-1426 | Varargs | unchanged | Boyarsky 1Z0-829#S-0171; Boyarsky 1Z0-830#S-0157 |
| N-1605 | C-1427 | Variable Arity Methods | unchanged | Mughal 1Z0-829#M829-3.11; Mughal 1Z0-830#M830-P2-3.11 |
| N-1606 | C-1428 | Variable Declarations | unchanged | Mughal 1Z0-829#M829-3.4; Mughal 1Z0-830#M830-P2-3.4 |
| N-1607 | C-1429 | Variables | unchanged | JLS SE 25#JLS-4.12 |
| N-1608 | C-1430 | Variables of Primitive Type | unchanged | JLS SE 25#JLS-4.12.1 |
| N-1609 | C-1431 | Variables of Reference Type | unchanged | JLS SE 25#JLS-4.12.2 |
| N-1610 | C-1432 | Verification | unchanged | JVMS SE 25#JVMS-5.4.1 |
| N-1611 | C-1433 | Verification by Type Checking | unchanged | JVMS SE 25#JVMS-4.10.1 |
| N-1612 | C-1274 | Verification by Type Inference | structured-merge | JVMS SE 25#JVMS-4.10.2 |
| N-1613 | C-1434 | Verification of `class` Files | unchanged | JVMS SE 25#JVMS-4.10 |
| N-1614 | C-1435 | Verification of the Binary Representation | unchanged | JLS SE 25#JLS-12.3.1 |
| N-1615 | C-1436 | Verification Type System | unchanged | JVMS SE 25#JVMS-4.10.1.2 |
| N-1616 | C-1437 | Verifying That the if Statement Evaluates to a Boolean Expression | unchanged | Boyarsky 1Z0-830#S-0041 |
| N-1617 | C-1438 | Virtual Machine Errors | unchanged | JVMS SE 25#JVMS-6.3 |
| N-1618 | C-1439 | Virtual Thread Execution Model | unchanged | Mughal 1Z0-830#M830-P1-3.2 |
| N-1619 | C-1440 | `volatile` Fields | unchanged | JLS SE 25#JLS-8.3.1.4 |
| N-1620 | C-1441 | Wait | unchanged | JLS SE 25#JLS-17.2.1 |
| N-1621 | C-1442 | Waiting for Results | unchanged | Boyarsky 1Z0-829#S-0431; Boyarsky 1Z0-830#S-0391 |
| N-1622 | C-1443 | Watch Semicolons in switch Expressions | unchanged | Boyarsky 1Z0-830#S-0053 |
| N-1623 | C-1444 | Well-Formed Executions | unchanged | JLS SE 25#JLS-17.4.7 |
| N-1624 | C-1445 | What About protected or Package Interface Members? | unchanged | Boyarsky 1Z0-830#S-0208 |
| N-1625 | C-1446 | What About the classpath ? | unchanged | Boyarsky 1Z0-830#S-0334 |
| N-1626 | C-1447 | What Clean Architecture does not prescribe | unchanged | Engineering scope#ENG-0155 |
| N-1627 | C-1448 | When Clean Architecture is excessive | unchanged | Engineering scope#ENG-0183 |
| N-1628 | C-1449 | When Initialization Occurs | unchanged | JLS SE 25#JLS-12.4.1 |
| N-1629 | C-1450 | When Is a switch Expression Not a switch Expression? | unchanged | Boyarsky 1Z0-830#S-0051 |
| N-1630 | C-1451 | When Reference Types Are the Same | unchanged | JLS SE 25#JLS-4.3.4 |
| N-1631 | C-1452 | When rich domain model is unnecessary | unchanged | Engineering scope#ENG-0182 |
| N-1632 | C-1453 | When SOLID creates indirection without value | unchanged | Engineering scope#ENG-0111 |
| N-1633 | C-1454 | Where Annotations May Appear | unchanged | JLS SE 25#JLS-9.7.4 |
| N-1634 | C-1455 | Where Types Are Used | unchanged | JLS SE 25#JLS-4.11 |
| N-1635 | C-1456 | `while` Statements | structured-merge | JLS SE 25#JLS-16.2.10 |
| N-1636 | C-1456 | `while` Statements | structured-merge | JLS SE 25#JLS-6.3.2.3 |
| N-1637 | C-1457 | White Space | unchanged | JLS SE 25#JLS-3.6 |
| N-1638 | C-1458 | Why native serialization is not a new external protocol | unchanged | Engineering scope#ENG-0058 |
| N-1639 | C-1459 | Why the Hippo Program Printed C After AB | unchanged | Boyarsky 1Z0-830#S-0181 |
| N-1640 | C-1460 | wide | structured-merge | JVMS SE 25#JVMS-0255 |
| N-1641 | C-1460 | wide | structured-merge | JVMS SE 25#JVMS-0444 |
| N-1642 | C-1461 | Widening Primitive Conversion | unchanged | JLS SE 25#JLS-5.1.2 |
| N-1643 | C-1462 | Widening Reference Conversion | unchanged | JLS SE 25#JLS-5.1.5 |
| N-1644 | C-1463 | Wildcard Capture | unchanged | Mughal 1Z0-829#M829-11.9; Mughal 1Z0-830#M830-P2-11.9 |
| N-1645 | C-1464 | Wildcards | merge | Boyarsky 1Z0-829#S-0014 |
| N-1646 | C-1464 | Wildcards | merge | Mughal 1Z0-829#M829-11.4; Mughal 1Z0-830#M830-P2-11.4 |
| N-1647 | C-1465 | Word Tearing | unchanged | JLS SE 25#JLS-17.6 |
| N-1648 | C-1466 | Working with a PreparedStatement | unchanged | Boyarsky 1Z0-829#S-0497 |
| N-1649 | C-1467 | Working with Advanced APIs | unchanged | Boyarsky 1Z0-829#S-0483; Boyarsky 1Z0-830#S-0461 |
| N-1650 | C-1468 | Working with Advanced Stream Pipeline Concepts | unchanged | Boyarsky 1Z0-829#S-0333; Boyarsky 1Z0-830#S-0287 |
| N-1651 | C-1469 | Working with an INOUT Parameter | unchanged | Boyarsky 1Z0-829#S-0510 |
| N-1652 | C-1470 | Working with Arrays of Arrays | unchanged | Boyarsky 1Z0-830#S-0095 |
| N-1653 | C-1471 | Working with Binary Arithmetic Operators | unchanged | Boyarsky 1Z0-829#S-0057; Boyarsky 1Z0-830#S-0019 |
| N-1654 | C-0902 | Working with Built-in Functional Interfaces | merge | Boyarsky 1Z0-829#S-0257; Boyarsky 1Z0-830#S-0259 |
| N-1655 | C-1472 | Working with Class Instances | unchanged | JVMS SE 25#JVMS-3.8 |
| N-1656 | C-1473 | Working with Complex Enums | unchanged | Boyarsky 1Z0-830#S-0211 |
| N-1657 | C-1474 | Working with Concurrent Classes | unchanged | Boyarsky 1Z0-829#S-0444; Boyarsky 1Z0-830#S-0408 |
| N-1658 | C-1475 | Working with Daemon Threads | unchanged | Boyarsky 1Z0-830#S-0385 |
| N-1659 | C-1476 | Working with Durations | merge | Boyarsky 1Z0-829#S-0126; Boyarsky 1Z0-830#S-0109 |
| N-1660 | C-1476 | Working with Durations | merge | Mughal 1Z0-829#M829-17.6; Mughal 1Z0-830#M830-P2-17.6 |
| N-1661 | C-1477 | Working with Enums | unchanged | Boyarsky 1Z0-829#S-0215; Boyarsky 1Z0-830#S-0209 |
| N-1662 | C-1478 | Working with Generics | unchanged | Boyarsky 1Z0-829#S-0310; Boyarsky 1Z0-830#S-0282 |
| N-1663 | C-1479 | Working with Instants | merge | Boyarsky 1Z0-829#S-0128; Boyarsky 1Z0-830#S-0112 |
| N-1664 | C-1479 | Working with Instants | merge | Mughal 1Z0-829#M829-17.4; Mughal 1Z0-830#M830-P2-17.4 |
| N-1665 | C-1480 | Working with List Methods | unchanged | Boyarsky 1Z0-829#S-0285 |
| N-1666 | C-1481 | Working with Map Methods | unchanged | Boyarsky 1Z0-829#S-0295 |
| N-1667 | C-1482 | Working with Multidimensional Arrays | unchanged | Boyarsky 1Z0-829#S-0115 |
| N-1668 | C-0911 | Working with Parallel Streams | merge | Boyarsky 1Z0-829#S-0449; Boyarsky 1Z0-830#S-0414 |
| N-1669 | C-1483 | Working with Parameters | unchanged | Boyarsky 1Z0-829#S-0500 |
| N-1670 | C-1484 | Working with Path Objects | unchanged | Mughal 1Z0-829#M829-21.3; Mughal 1Z0-830#M830-P2-21.3 |
| N-1671 | C-1485 | Working with Periods | merge | Boyarsky 1Z0-829#S-0125; Boyarsky 1Z0-830#S-0108 |
| N-1672 | C-1485 | Working with Periods | merge | Mughal 1Z0-829#M829-17.5; Mughal 1Z0-830#M830-P2-17.5 |
| N-1673 | C-1486 | Working with Primitive Streams | unchanged | Boyarsky 1Z0-829#S-0328; Boyarsky 1Z0-830#S-0286 |
| N-1674 | C-1487 | Working with Set Methods | unchanged | Boyarsky 1Z0-829#S-0289 |
| N-1675 | C-1180 | Working with switch Expressions | structured-merge | Boyarsky 1Z0-830#S-0052 |
| N-1676 | C-1181 | Working with switch Statements | structured-merge | Boyarsky 1Z0-830#S-0050 |
| N-1677 | C-1488 | Working with toString() | unchanged | Boyarsky 1Z0-830#S-0082 |
| N-1678 | C-1489 | Working with Varargs | unchanged | Boyarsky 1Z0-829#S-0144; Boyarsky 1Z0-830#S-0128 |
| N-1679 | C-1490 | Working with Variables in Lambdas | unchanged | Boyarsky 1Z0-829#S-0266; Boyarsky 1Z0-830#S-0268 |
| N-1680 | C-1491 | Write-Protected Fields | unchanged | JLS SE 25#JLS-17.5.4 |
| N-1681 | C-1492 | Writing a Local Class | unchanged | Boyarsky 1Z0-829#S-0235; Boyarsky 1Z0-830#S-0235 |
| N-1682 | C-1493 | Writing a main() Method | unchanged | Boyarsky 1Z0-829#S-0009; Boyarsky 1Z0-830#S-0004 |
| N-1683 | C-1494 | Writing Basic SQL Statements | unchanged | Boyarsky 1Z0-829#S-0492 |
| N-1684 | C-1495 | Writing final Methods | unchanged | Boyarsky 1Z0-829#S-0198; Boyarsky 1Z0-830#S-0190 |
| N-1685 | C-1496 | Writing Generic Methods | unchanged | Boyarsky 1Z0-829#S-0314 |
| N-1686 | C-1497 | Writing Log Messages | unchanged | Mughal 1Z0-829#M829-G.3 |
| N-1687 | C-1498 | Writing Simple Lambdas | unchanged | Boyarsky 1Z0-829#S-0245; Boyarsky 1Z0-830#S-0245 |
| N-1688 | C-1499 | Writing Thread-Safe Code | merge | Boyarsky 1Z0-829#S-0434; Boyarsky 1Z0-830#S-0397 |
| N-1689 | C-1499 | Writing Thread-Safe Code | merge | Mughal 1Z0-829#M829-23.4; Mughal 1Z0-830#M830-P2-23.4 |
| N-1690 | C-1500 | Writing while Loops | unchanged | Boyarsky 1Z0-829#S-0080; Boyarsky 1Z0-830#S-0056 |
| N-1691 | C-1501 | XML external entities | unchanged | Engineering scope#ENG-0368 |
