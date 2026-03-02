Interpreters and Compilers
# Interpreter
- Execute line-by-line, translating and running each statement in real-time without creating an intermediate file
- Detects Errors during runtime, stopping at the first error encountered
	- Advantage: Immediate feedback during development
	- Disadvantage: Errors in later code may go unnoticed until execution
- No seperate translation phase, execution is slower due to realtime translation
- Highly portable - code runs on any platform with intepreter installed
- Use-case: rapid development, scripting, testing; Ideal for dynamic environments like web scripting or interactive shells
### Steps
- Initiate execution - run
- Lexical Analysis - converts source code - keywords,  identifirers, operators into tokens
- Syntax analysis - token stream is parsed to check if it adheres to programming rules
- Semantic analysis - semantic errors such as type mismatches and undeclared variables
- Code Generation - parsed code (currently looking at) is translated to bytecode, and is then executed.
- bytecode is kinda a lower-level platform independent representation of the source code,  specific to interpreter.
- execution - Executes bytecode instruction one at a time
----
# Compiler
Translates entire source ode into machine code or bytecode before execution, producing an executable file
- eg. C++ compiler generates an .exe file from source code

Error detection: detects errors during compilation, prventing execution unill all errors are fixed
- Advantage catches errors across entire program
- Disadvantage requires recompilation after fixes, slowing development, does not catch runtime errors
Portability - less portable; compiled executables are platform-specific unless targeting a virt. machine

Translation time requires a compilation phase, but execution is faster
- Use-Cases: Performance-critical applications, large-scale software, and systems requiring optimized execution​
    
- Example: C for operating system kernels or game engines
### Steps
same as above until semantic analysis
- Optimisation - compiler optimises the code, imrpoving performance without change in functionality, may involve reordering instructions, eliminating redudant code & optimising data storage
- The optimised code is translated into machine code, generating an executable binary file specific to the target platfiorm
--
- execution - seperate step initiated by the user after  compilation
---
# Bytecode interpreters
combines interpreter and compiler
Intermediate representation used by compilers
For portability across platforms
Executed by virtual machines, which interpret or JIT-compile bytecode to machine code
Lower level than normal code but not as low as machine code
### Example
Java virt machine
- each computer needs to have java virtuam machine 
- once program is writeen, java program is compiled to create Java Byte Code
- when program is run, code is interpreted by Java Virtual machine
- Java Byte Code can be transfrerred to any computer that has a JVM installed
---
# Just-In-Time JIT compiler
- Combines interpreter and compiler traits​
- Compiles code at runtime into machine code for faster execution​
- Example: Java's JVM uses JIT to compile bytecode dynamically, improving performance
-