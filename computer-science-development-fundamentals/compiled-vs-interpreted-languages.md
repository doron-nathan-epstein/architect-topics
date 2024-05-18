# Compiled vs Interpreted Languages

Compiled and interpreted languages represent two different approaches to translating and executing code written by programmers. Here’s an overview of each, along with their key differences, advantages, and disadvantages:

## Compiled Languages

| Aspect              | Description                                                                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| **Definition**      | Source code is translated into machine code by a compiler. The resulting machine code can be executed directly by the computer's hardware.           |
| **Examples**        | C, C++, Rust, Go                                                                                                                                     |
| **Process**         | 1. Write source code. <br> 2. Compile source code into machine code (executable file). <br> 3. Execute machine code.                                     |
| **Advantages**      | - High performance due to direct execution of machine code.<br>- Optimizations performed by the compiler.<br>- No runtime overhead.                 |
| **Disadvantages**   | - Compilation can be time-consuming.<br>- Machine code is platform-dependent.<br>- Debugging can be complex.                                        |

## Interpreted Languages

| Aspect              | Description                                                                                                                             |
|---------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **Definition**      | Source code is executed line-by-line by an interpreter at runtime, translating it into machine code on the fly.                         |
| **Examples**        | Python, JavaScript, Ruby, PHP                                                                                                           |
| **Process**         | 1. Write source code.<br>2. Interpreter reads and executes source code line-by-line.                                                    |
| **Advantages**      | - High portability across different platforms.<br>- Easier debugging due to immediate error handling.<br>- Support for interactive execution environments (REPLs). |
| **Disadvantages**   | - Slower performance due to runtime translation.<br>- Added runtime overhead from the interpreter.<br>- Source code cannot run without the interpreter. |

### Mixed Approaches

| Language | Description                                                                                                                            |
|----------|----------------------------------------------------------------------------------------------------------------------------------------|
| **Java** | Source code is compiled into bytecode by the Java compiler. The JVM then interprets or just-in-time compiles the bytecode at runtime.   |
| **Python**| Source code is often compiled into bytecode, which is then interpreted by the Python interpreter.                                      |

This table format provides a clear and concise comparison between compiled and interpreted languages, highlighting their definitions, processes, advantages, and disadvantages.
