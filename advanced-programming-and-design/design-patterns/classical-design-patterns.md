# Learning Guide: Classical Design Patterns (Gang of Four)

- [Learning Guide: Classical Design Patterns (Gang of Four)](#learning-guide-classical-design-patterns-gang-of-four)
  - [Introduction](#introduction)
  - [Design Patterns Overview](#design-patterns-overview)
  - [Creational Patterns](#creational-patterns)
  - [Structural Patterns](#structural-patterns)
  - [Behavioral Patterns](#behavioral-patterns)
  - [Summary](#summary)

## Introduction

The Gang of Four (GoF) design patterns provide solutions to common software design problems. They are categorized into creational, structural, and behavioral patterns.

## Design Patterns Overview

| **Pattern Category** | **Patterns**                                     |
|----------------------|--------------------------------------------------|
| **Creational**       | Singleton, Factory Method, Abstract Factory, Builder, Prototype |
| **Structural**       | Adapter, Decorator, Composite, Facade, Flyweight, Proxy, Bridge |
| **Behavioral**       | Observer, Strategy, Command, Iterator, Mediator, Memento, State, Visitor, Template Method, Chain of Responsibility, Interpreter |

## Creational Patterns

1. **Singleton**: Ensures a class has only one instance and provides a global point of access to it. Use when a single instance of a class is required across the application.

2. **Factory Method**: Defines an interface for creating objects but allows subclasses to alter the type of objects that will be created. Use for decoupling object creation from its implementation.

3. **Abstract Factory**: Provides an interface for creating families of related or dependent objects without specifying their concrete classes. Use when the system needs to be independent of how its objects are created.

4. **Builder**: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations. Use for constructing complex objects with many optional parts.

5. **Prototype**: Creates new objects by copying an existing object, known as the prototype. Use when creating an instance is more expensive than copying an existing one.

## Structural Patterns

1. **Adapter**: Allows incompatible interfaces to work together. Use when you need to integrate classes with incompatible interfaces.

2. **Decorator**: Adds new functionality to objects dynamically without altering their structure. Use for extending an object's behavior without modifying its code.

3. **Composite**: Composes objects into tree structures to represent part-whole hierarchies. Use to treat individual objects and compositions uniformly.

4. **Facade**: Provides a simplified interface to a complex system. Use when you want to simplify the interface of a complex subsystem.

5. **Flyweight**: Reduces the cost of creating and manipulating a large number of similar objects. Use when you need to minimize memory usage by sharing common parts of state across multiple objects.

6. **Proxy**: Provides a surrogate or placeholder for another object to control access to it. Use when you need to control access to an object.

7. **Bridge**: Decouples an abstraction from its implementation so that the two can vary independently. Use when you want to separate abstraction from implementation.

## Behavioral Patterns

1. **Observer**: Defines a one-to-many dependency between objects, so that when one object changes state, all its dependents are notified. Use for implementing distributed event-handling systems.

2. **Strategy**: Defines a family of algorithms, encapsulates each one, and makes them interchangeable. Use when you need to select an algorithm at runtime.

3. **Command**: Encapsulates a request as an object, thereby allowing for parameterization of clients with queues, requests, and operations. Use for implementing undo/redo operations.

4. **Iterator**: Provides a way to access the elements of an aggregate object sequentially without exposing its underlying representation. Use when you need to iterate over a collection without exposing its structure.

5. **Mediator**: Defines an object that encapsulates how a set of objects interact. Use to reduce the complexity of communication between multiple objects or classes.

6. **Memento**: Captures and externalizes an object’s internal state so that it can be restored later. Use for implementing undo mechanisms.

7. **State**: Allows an object to alter its behavior when its internal state changes. Use when an object must change its behavior at runtime depending on its state.

8. **Visitor**: Represents an operation to be performed on the elements of an object structure, allowing you to define a new operation without changing the classes of the elements on which it operates. Use when you need to perform operations on object structures without modifying the structures.

9. **Template Method**: Defines the skeleton of an algorithm in an operation, deferring some steps to subclasses. Use to implement the invariant parts of an algorithm once and let subclasses implement the behavior.

10. **Chain of Responsibility**: Passes a request along a chain of handlers. Upon receiving a request, each handler decides either to process the request or to pass it to the next handler in the chain. Use when you want to decouple the sender and receiver of a request.

11. **Interpreter**: Implements an expression interface to interpret a particular context. Use for building interpreters for simple languages or expressions.

## Summary

The Gang of Four design patterns offer robust, reusable solutions for common design problems, making code more maintainable and flexible. Understanding and applying these patterns can greatly enhance software design.