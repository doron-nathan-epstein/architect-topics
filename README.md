# Architect Topical Knowledge Requirements <!-- omit in toc -->

- [Introduction](#introduction)
- [Purpose](#purpose)
- [Learning Path for Software Architect Interview](#learning-path-for-software-architect-interview)
  - [1. Foundation in Programming](#1-foundation-in-programming)
  - [2. Software Development Skills](#2-software-development-skills)
  - [3. Advanced Programming and Design](#3-advanced-programming-and-design)
  - [4. Web Development and Databases](#4-web-development-and-databases)
  - [5. Software Architecture Fundamentals](#5-software-architecture-fundamentals)
  - [6. Cloud and Infrastructure](#6-cloud-and-infrastructure)
  - [7. Security](#7-security)
  - [8. Computer Science Fundamentals](#8-computer-science-fundamentals)
  - [9. Distributed Systems](#9-distributed-systems)
  - [10. Performance Optimization](#10-performance-optimization)
  - [11. API Design](#11-api-design)
  - [12. Infrastructure and Hardware](#12-infrastructure-and-hardware)
  - [13. Technologies](#13-technologies)
  - [14. DevOps](#14-devops)
  - [15. Containers and Kubernetes](#15-containers-and-kubernetes)
- [How to Use This Repository](#how-to-use-this-repository)
- [Contribution](#contribution)

## Introduction

Welcome to the Software Architecture Learning Path repository! This repository is designed to help you prepare for a
software architect interview or to simply enhance your knowledge in software architecture. Whether you're a seasoned developer looking to transition into an architecture role or a current architect aiming to sharpen your skills, this repository provides a structured and comprehensive learning journey.

## Purpose

The purpose of this repository is to organize and present key topics and concepts that are crucial for a software architect. It includes a well-structured learning path covering various aspects of software architecture, design patterns, computer science fundamentals, security, distributed systems, performance optimization, API design, infrastructure, technologies, containers, DevOps, and more. By following this path, you'll gain a deeper understanding of the principles, practices, and technologies that underpin modern software architecture.

## Learning Path for Software Architect Interview

### 1. Foundation in Programming

- [Learn Programming Languages](./foundation-in-programming/learn-programming-languages.md)
- Data Structures and Algorithms
  - [Collection Data Structures](./foundation-in-programming/data-structures-and-algorithms/collection-data-structures.md)
  - [O(n) notation](./foundation-in-programming/data-structures-and-algorithms/o-notation.md)

### 2. Software Development Skills

- [Version Control Systems](./software-development-skills/version-control-systems.md)
- [Software Development Methodologies](./software-development-skills/software-development-methodologies.md)
- [Testing](./software-development-skills/testing.md)
- Programming Paradigms
  - [Compiled vs. Interpreted languages](./software-development-skills/programming-paradigms/compiled-vs-interpreted-languages.md)
  - [Runtimes and Intermediate-languages (e.g., JAVA, .NET)](./software-development-skills/programming-paradigms/compiled-vs-interpreted-languages.md)

### 3. Advanced Programming and Design

- [Object-Oriented Design](./advanced-programming-and-design/object-oriented-design.md)
- Design Patterns
  - [Classical Design Patterns (Gang of Four)](./advanced-programming-and-design/design-patterns/classical-design-patterns.md)

### 4. Web Development and Databases

- [Frontend Development](./web-development-and-databases/frontend-development.md)
- [Backend Development](./web-development-and-databases/backend-development.md)
- [Databases](./web-development-and-databases/databases.md)

### 5. Software Architecture Fundamentals

- Architecture Patterns
  - [Monolithic Architecture (Monolith)](./software-architecture-fundamentals/architecture-patterns/monolithic-architecture.md)
  - [Layered Architecture (N-Tier)](./software-architecture-fundamentals/architecture-patterns/layered-architecture.md)
  - [Event-Driven Architecture (Event Driven)](./software-architecture-fundamentals/architecture-patterns/event-driven-architecture.md)
  - [Hexagonal Architecture](./software-architecture-fundamentals/architecture-patterns/hexagonal-architecture.md)
  - [Clean Architecture](./software-architecture-fundamentals/architecture-patterns/clean-architecture.md)
  - [IDesign Method](./software-architecture-fundamentals/architecture-patterns/idesign-method.md)
- Principles and Best Practices
  - [SOLID Principles](./software-architecture-fundamentals/principles-and-best-practices/solid-principles.md)
  - [DRY, KISS, YAGNI](./software-architecture-fundamentals/principles-and-best-practices/dry-kiss-yagni.md)

### 6. Cloud and Infrastructure

- Cloud Platforms
  - [Compute Services (EC2, Lambda, etc.)](./cloud-and-infrastructure/cloud-platforms/compute-services.md )
  - [Storage Services (S3, Azure Blob Storage)](./cloud-and-infrastructure/cloud-platforms/storage-services.md)
  - [Networking (VPC, Load Balancers)](./cloud-and-infrastructure/cloud-platforms/networking.md)
- Containerization and Orchestration
  - [Containers (Fundamentals, Linux on Windows, Repositories and Tagging)](./cloud-and-infrastructure/containerization-and-orchestration/containers.md)
  - [Kubernetes (Architecture - K8s components, Health Checks, Helm)](./cloud-and-infrastructure/containerization-and-orchestration/kubernetes.md)
- [Infrastructure as Code (IaC)](./cloud-and-infrastructure/infrustructure-as-code.md)

### 7. Security

- Fundamentals
  - [Certificates](./security/fundamentals/certificates.md)
  - [Encryption](./security/fundamentals/encryption.md)
  - [Hashing](./security/fundamentals/hashing.md)
  - [JWTs](./security/fundamentals/jwts.md)
  - [Secure Coding Practices](./security/fundamentals/secure-coding-practices.md)
  - [Access Control Models (RBAC, ABAC)](./security/fundamentals/access-control-models.md)

### 8. Computer Science Fundamentals

- Concurrency
  - [Deadlocks](./computer-science-fundamentals/concurrency/deadlocks.md)
  - [Mutual Exclusion](./computer-science-fundamentals/concurrency/mutual-exclusion.md)
  - [Mutual Exclusion Primitives](./computer-science-fundamentals/concurrency/mutual-exclusion-primitives.md)
  - [Optimistic Locking](./computer-science-fundamentals/concurrency/optimistic-locking.md)
  - [Concurrency Models (Threads, Actors)](./computer-science-fundamentals/concurrency/concurrency-models.md)
- Networking and Protocols
  - [TCP vs. UDP](./computer-science-fundamentals/networking-and-protocols/tcp-vs-udp.md)
  - [Protocols and Serialization](./computer-science-fundamentals/networking-and-protocols/protocols-and-serialization.md)
  - [HTTP/HTTPS](./computer-science-fundamentals/networking-and-protocols/http-https.md)
  - [WebSockets](./computer-science-fundamentals/networking-and-protocols/websockets.md)
- Memory Management
  - [Virtual Memory](./computer-science-fundamentals/memory-management/virtual-memory.md)
  - [Memory Access Times](./computer-science-fundamentals/memory-management/memory-access-times.md)
  - [Garbage Collection](./computer-science-fundamentals/memory-management/garbage-collection.md)
- Character Encoding
  - [Unicode and Character Encoding](./computer-science-fundamentals/character-encoding/unicode-and-character-encoding.md)
  - [ASCII](./computer-science-fundamentals/character-encoding/ascii.md)
- Type Systems
  - [Values vs. Reference Types](./computer-science-fundamentals/type-systems/values-vs-reference-types.md)
  - [Strong vs. Weak Typing](./computer-science-fundamentals/type-systems/strong-vs-weak-typing)
  - [Static vs. Dynamic Typing](./computer-science-fundamentals/type-systems/static-vs-dynamic-typing)

### 9. Distributed Systems

- Theoretical Foundations
  - [CAP Theorem](./distributed-systems/theoretical-foundations/cap-theorem.md)
  - [ACID vs. BASE](./distributed-systems/theoretical-foundations/acid-vs-base.md)
- Consistency Models
  - [Eventual Consistency](./distributed-systems/consistency-models/eventual-consistency.md)
  - [Strong Consistency](./distributed-systems/consistency-models/strong-consistency.md)
  - [Causal Consistency](./distributed-systems/consistency-models/causal-consistency.md)
- High Availability
  - [Load Balancing](./distributed-systems/high-availability/load-balancing.md)
  - [Failover Strategies](./distributed-systems/high-availability/failover-strategies.md)
- Data Consistency Protocols
  - [N Phase Commit](./distributed-systems/data-consistency-protocols/n-phase-commit.md)
  - [Two-Phase Commit](./distributed-systems/data-consistency-protocols/two-phase-commit.md)
- Communication Models
  - [Event Queue vs. Message Queue](./distributed-systems/communication-models/event-queue-vs-message-queue.md)
  - [Publish/Subscribe](./distributed-systems/communication-models/publish-subscribe.md)
- Transaction Management
  - [Saga Pattern](./distributed-systems/transaction-management/saga-pattern.md)
  - [TCC (Try-Confirm/Cancel)](./distributed-systems/transaction-management/tcc.md)

### 10. Performance Optimization

- Asynchronous Programming
  - How async/await works
  - Event Loop
  - Promises/Futures
- Low-Level Performance
  - Bitwise operators
  - Assembly Language Basics
  - CPU Caching

### 11. API Design

- API Documentation
  - Documenting APIs and IDL
  - OpenAPI/Swagger
- API Behavior
  - Idempotent Behaviour
  - Statelessness
- API Protocols
  - RPC vs. REST
  - GraphQL

### 12. Infrastructure and Hardware

- Caching
  - Caches and False Cache-line Invalidation
  - In-Memory Caching (Redis, Memcached)
- Instruction Sets
  - 32-bit and 64-bit instruction sets
  - ARM vs. x86
- Firewalls
  - How do firewalls work?
  - Types of Firewalls (Packet-filtering, Proxy, Stateful Inspection)
- Storage Area Networks (SANs)
  - How do SANs work?
  - NAS vs. SAN
- Virtual Machines
  - How do virtual machines work?
  - Hypervisors (Type 1 vs. Type 2)

### 13. Technologies

- Message Brokers
  - Kafka
  - RabbitMQ
  - ActiveMQ
- Artificial Intelligence
  - Deep Learning
  - Machine Learning
  - ML.NET
  - Neural Networks
  - Training and Labeling
  - Natural Language Processing (NLP)

### 14. DevOps

- Code Quality and Tools
  - Linters and Code Quality Tools
  - Static Code Analysis
- Observability
  - Logging
  - Monitoring
  - Tracing
- CI/CD Pipelines
  - Pipelines, PR's, and everything-as-code
  - Deployment Strategies (Blue/Green, Canary)
- Agile Methods and Analysis
  - Agile methods (SCRUM vs. Kanban, #noestimates)
  - Capturing requirements
  - UML use-cases and activity diagrams
  - Waterfall
- Testing
  - Automated tests
  - The test pyramid
  - Kinds of tests, techniques for each

### 15. Containers and Kubernetes

- Containers
  - Fundamentals
  - Linux on Windows
  - Repositories and Tagging
  - Container Orchestration
- Kubernetes
  - Architecture - K8s components
  - Health Checks
  - Helm
  - StatefulSets vs. Deployments

## How to Use This Repository

1. Start with the basics: Begin with fundamental concepts in computer science to build a strong foundation.
2. Progress through architecture patterns: Understand different architectural styles and their use cases.
3. Deepen your knowledge in design patterns: Study classical design patterns and their applications.
4. Explore advanced topics: Dive into distributed systems, performance optimization, and security.
5. Practical applications: Learn about technologies, containers, Kubernetes, and DevOps practices.
6. Prepare for interviews: Use the provided interview notes and mock questions to get ready for your software architect interviews.

## Contribution

Feel free to contribute by submitting pull requests for additional topics, improvements, or corrections. This repository aims to be a collaborative learning resource for aspiring software architects.
