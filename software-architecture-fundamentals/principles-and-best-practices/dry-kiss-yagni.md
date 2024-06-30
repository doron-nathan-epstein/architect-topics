# Learning Guide: DRY, KISS, YAGNI

- [Learning Guide: DRY, KISS, YAGNI](#learning-guide-dry-kiss-yagni)
  - [Introduction](#introduction)
  - [DRY: Don't Repeat Yourself](#dry-dont-repeat-yourself)
  - [KISS: Keep It Simple, Stupid](#kiss-keep-it-simple-stupid)
  - [YAGNI: You Aren't Gonna Need It](#yagni-you-arent-gonna-need-it)
  - [Benefits](#benefits)
  - [Summary](#summary)

## Introduction

DRY, KISS, and YAGNI are three important principles in software development that guide developers toward writing better code that is more maintainable, understandable, and efficient.

## DRY: Don't Repeat Yourself

The DRY principle states that every piece of knowledge or logic within a system should have a single, unambiguous representation. This means that duplication in code (e.g., repeated code snippets) should be avoided by abstracting common functionality into reusable components.

```csharp
// Without DRY
public class UserService
{
    public void RegisterUser(string username)
    {
        // Validation logic
        if (string.IsNullOrEmpty(username))
        {
            throw new ArgumentException("Username cannot be empty.");
        }

        // Business logic
        // Register user logic

        // Logging
        Console.WriteLine($"User '{username}' registered.");
    }

    public void DeleteUser(string username)
    {
        // Validation logic
        if (string.IsNullOrEmpty(username))
        {
            throw new ArgumentException("Username cannot be empty.");
        }

        // Business logic
        // Delete user logic

        // Logging
        Console.WriteLine($"User '{username}' deleted.");
    }
}

// With DRY
public class UserService
{
    private void ValidateUsername(string username)
    {
        if (string.IsNullOrEmpty(username))
        {
            throw new ArgumentException("Username cannot be empty.");
        }
    }

    public void RegisterUser(string username)
    {
        ValidateUsername(username);

        // Business logic
        // Register user logic

        LogUserAction(username, "registered");
    }

    public void DeleteUser(string username)
    {
        ValidateUsername(username);

        // Business logic
        // Delete user logic

        LogUserAction(username, "deleted");
    }

    private void LogUserAction(string username, string action)
    {
        Console.WriteLine($"User '{username}' {action}.");
    }
}
```

## KISS: Keep It Simple, Stupid

The KISS principle advocates for simplicity in design and implementation. It suggests that systems should be designed and implemented in the simplest way possible without sacrificing clarity and functionality. Complex solutions should be avoided unless absolutely necessary.

```csharp
// Complex solution without KISS
public class ComplexCalculator
{
    public double CalculateSquareRoot(double number)
    {
        // Complex logic to calculate square root
    }
}

// Simple solution with KISS
public class SimpleCalculator
{
    public double SquareRoot(double number)
    {
        return Math.Sqrt(number);
    }
}
```

## YAGNI: You Aren't Gonna Need It

YAGNI advises developers not to implement features or functionality until they are actually needed by the current requirements. This principle discourages speculative coding or adding features that are anticipated but not currently necessary. By adhering to YAGNI, developers can avoid unnecessary complexity and focus on delivering essential functionality.

```csharp
// Implementing unnecessary feature without YAGNI
public class UnnecessaryFeature
{
    public void CalculateTax(decimal amount)
    {
        // Unnecessary tax calculation logic
    }
}

// Implementing necessary feature with YAGNI
public class NecessaryFeature
{
    // No unnecessary tax calculation logic until needed
}
```

## Benefits

- **Code Quality**: Improves code readability, maintainability, and scalability.
- **Efficiency**: Reduces development time by avoiding redundant or unnecessary work.
- **Clarity**: Enhances understanding of code and reduces the chance of introducing bugs.
- **Flexibility**: Allows for easier adaptation to changing requirements and future enhancements.

## Summary

DRY, KISS, and YAGNI are foundational principles that help developers write cleaner, more maintainable, and efficient code. By applying these principles, developers can create software that is easier to understand, modify, and extend, leading to better overall software quality and developer productivity.
