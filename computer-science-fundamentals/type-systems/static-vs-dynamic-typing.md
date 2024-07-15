# Learning Guide: Static vs. Dynamic Typing

- [Learning Guide: Static vs. Dynamic Typing](#learning-guide-static-vs-dynamic-typing)
  - [Introduction](#introduction)
  - [Key Concepts](#key-concepts)
  - [Static Typing](#static-typing)
    - [Example:](#example)
  - [Dynamic Typing](#dynamic-typing)
    - [Example:](#example-1)
  - [Comparison of Static and Dynamic Typing](#comparison-of-static-and-dynamic-typing)
  - [Examples in C#](#examples-in-c)
    - [Static Typing Example](#static-typing-example)
    - [Dynamic Typing Example (Using Dynamic)](#dynamic-typing-example-using-dynamic)
  - [Advantages and Disadvantages](#advantages-and-disadvantages)
    - [Advantages of Static Typing](#advantages-of-static-typing)
    - [Disadvantages of Static Typing](#disadvantages-of-static-typing)
    - [Advantages of Dynamic Typing](#advantages-of-dynamic-typing)
    - [Disadvantages of Dynamic Typing](#disadvantages-of-dynamic-typing)
  - [Summary](#summary)

## Introduction

Static and dynamic typing are concepts that refer to when types are checked in a programming language. Understanding these concepts is important for writing safe and efficient code.

## Key Concepts

- **Static Typing**: Types are checked at compile-time, meaning the variable types are known before the program runs.
- **Dynamic Typing**: Types are checked at run-time, allowing variables to change types during execution.

## Static Typing

In statically typed languages, variable types are explicitly declared, and type checking occurs at compile-time. This leads to fewer type-related errors at runtime.

### Example:

In C#, variable types must be declared explicitly:

```csharp
int number = 5; // number is of type int
```

## Dynamic Typing

In dynamically typed languages, variables can hold values of any type, and type checking happens at runtime. This flexibility can make the code easier to write but may lead to type-related errors.

### Example:

In Python, variables can change types easily:

```python
number = 5      # number is an integer
number = "five" # now number is a string
```

## Comparison of Static and Dynamic Typing

| **Aspect**          | **Static Typing**                       | **Dynamic Typing**                     |
|---------------------|-----------------------------------------|----------------------------------------|
| **Type Checking**    | At compile-time                          | At run-time                            |
| **Type Declaration** | Required (explicitly declared)          | Not required (implicit)               |
| **Performance**      | Generally faster due to compile-time checks | May be slower due to run-time checks  |
| **Error Detection**  | Errors caught early during compilation   | Errors may only appear at run-time     |

## Examples in C#

### Static Typing Example

```csharp
string greeting = "Hello, World!";
int number = 10; 
// This will cause a compile-time error if types are mismatched
// greeting = number; // Uncommenting this line will cause an error
```

### Dynamic Typing Example (Using Dynamic)

C# also supports a `dynamic` type that allows for dynamic typing:

```csharp
dynamic variable = 5; // variable is an int
variable = "Now I'm a string"; // variable can change to a string
Console.WriteLine(variable); // Output: Now I'm a string
```

## Advantages and Disadvantages

### Advantages of Static Typing

- **Type Safety**: Errors related to type mismatches are caught early.
- **Performance**: Can be optimized by the compiler.

### Disadvantages of Static Typing

- **Verbosity**: Requires more explicit declarations.
- **Less Flexibility**: Types must be defined upfront.

### Advantages of Dynamic Typing

- **Flexibility**: Easier to write and modify code on the fly.
- **Conciseness**: Less boilerplate code is required.

### Disadvantages of Dynamic Typing

- **Potential for Errors**: Type errors may not be discovered until run-time.
- **Performance Overhead**: Checking types at run-time can slow down execution.

## Summary

Static and dynamic typing represent different approaches to type handling in programming languages. Static typing promotes safety and performance through early type checking, while dynamic typing offers flexibility and ease of coding. The choice between them depends on the specific requirements of your project and coding style.
