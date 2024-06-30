# Learning Guide: SOLID Principles

- [Learning Guide: SOLID Principles](#learning-guide-solid-principles)
  - [Introduction](#introduction)
  - [Single Responsibility Principle (SRP)](#single-responsibility-principle-srp)
  - [Open/Closed Principle (OCP)](#openclosed-principle-ocp)
  - [Liskov Substitution Principle (LSP)](#liskov-substitution-principle-lsp)
  - [Interface Segregation Principle (ISP)](#interface-segregation-principle-isp)
  - [Dependency Inversion Principle (DIP)](#dependency-inversion-principle-dip)
  - [Benefits](#benefits)
  - [Summary](#summary)

## Introduction

The SOLID principles are a set of five design principles that help software developers design more understandable, flexible, and maintainable systems. They were introduced by Robert C. Martin (Uncle Bob) to promote good object-oriented design practices.

## Single Responsibility Principle (SRP)

A class should have only one reason to change. It states that a class should have only one job or responsibility and should encapsulate that responsibility. This principle helps in ensuring that each class is focused on a single task, making it easier to understand, maintain, and modify.

```csharp
public class ProductService
{
    public void AddProduct(Product product)
    {
        // Add product to database
    }

    public void UpdateProduct(Product product)
    {
        // Update product in database
    }

    public void DeleteProduct(Product product)
    {
        // Delete product from database
    }
}
```

## Open/Closed Principle (OCP)

Software entities (classes, modules, functions, etc.) should be open for extension but closed for modification. This principle encourages developers to design modules that can be easily extended with new functionality without modifying existing code. This promotes reusability and minimizes the risk of introducing bugs in existing code.

```csharp
public abstract class Shape
{
    public abstract double Area();
}

public class Circle : Shape
{
    public double Radius { get; set; }

    public override double Area()
    {
        return Math.PI * Radius * Radius;
    }
}

public class Rectangle : Shape
{
    public double Width { get; set; }
    public double Height { get; set; }

    public override double Area()
    {
        return Width * Height;
    }
}
```

## Liskov Substitution Principle (LSP)

Subtypes must be substitutable for their base types without altering the correctness of the program. In other words, derived classes should be able to replace their base classes without affecting the functionality expected from the base class. This principle ensures that inheritance hierarchies are designed in a way that maintains logical consistency and avoids unexpected behavior.

```csharp
public class Rectangle
{
    public virtual double Width { get; set; }
    public virtual double Height { get; set; }

    public double Area()
    {
        return Width * Height;
    }
}

public class Square : Rectangle
{
    private double _side;

    public override double Width
    {
        get => _side;
        set
        {
            _side = value;
            Height = value;
        }
    }

    public override double Height
    {
        get => _side;
        set
        {
            _side = value;
            Width = value;
        }
    }
}
```

## Interface Segregation Principle (ISP)

Clients should not be forced to depend on interfaces they do not use. This principle emphasizes creating smaller and more specific interfaces that are tailored to the exact requirements of clients. By segregating interfaces based on client requirements, developers can avoid creating monolithic interfaces that require clients to implement unnecessary methods.

```csharp
public interface IWorker
{
    void Work();
}

public interface IEater
{
    void Eat();
}

public class Worker : IWorker
{
    public void Work()
    {
        // Implement work logic
    }
}

public class SuperWorker : IWorker, IEater
{
    public void Work()
    {
        // Implement work logic
    }

    public void Eat()
    {
        // Implement eat logic
    }
}
```

## Dependency Inversion Principle (DIP)

High-level modules should not depend on low-level modules. Both should depend on abstractions (e.g., interfaces). Abstractions should not depend on details. Details should depend on abstractions. This principle encourages decoupling between high-level and low-level modules by introducing abstractions that both modules depend on. This promotes flexibility, testability, and easier maintenance.

```csharp
public interface ILogger
{
    void Log(string message);
}

public class DatabaseLogger : ILogger
{
    public void Log(string message)
    {
        // Log message to database
    }
}

public class FileLogger : ILogger
{
    public void Log(string message)
    {
        // Log message to file
    }
}

public class UserService
{
    private readonly ILogger _logger;

    public UserService(ILogger logger)
    {
        _logger = logger;
    }

    public void RegisterUser(string username)
    {
        // Register user logic

        _logger.Log($"User '{username}' registered.");
    }
}
```

## Benefits

- **Modularity**: Facilitates easier maintenance and modification of code.
- **Flexibility**: Promotes code reuse and extensibility.
- **Readability**: Enhances code readability and understanding.
- **Scalability**: Supports the development of scalable and robust software systems.
- **Testability**: Improves testability and reduces the risk of introducing bugs.

## Summary

The SOLID principles provide a foundation for designing software that is maintainable, scalable, and adaptable. By adhering to these principles, developers can create well-structured and efficient code that meets current and future business requirements.
