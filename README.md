# Architect Topical Knowledge Requirements <!-- omit in toc -->

- [Introduction](#introduction)
- [Purpose](#purpose)
- [Learning Path for Software Architect Interview](#learning-path-for-software-architect-interview)
  - [1. Architecture Patterns](#1-architecture-patterns)
  - [2. Design Patterns](#2-design-patterns)
  - [3. Computer Science Fundamentals](#3-computer-science-fundamentals)
  - [4. Security](#4-security)
  - [5. Distributed Systems](#5-distributed-systems)
  - [6. Performance](#6-performance)
  - [7. API Design](#7-api-design)
  - [8. Infrastructure and Hardware](#8-infrastructure-and-hardware)
  - [9. Technologies](#9-technologies)
  - [10. Containers and Kubernetes](#10-containers-and-kubernetes)
  - [11. DevOps](#11-devops)
- [Potential Missing Topics](#potential-missing-topics)
  - [Advanced Architecture Patterns](#advanced-architecture-patterns)
  - [Software Development Principles](#software-development-principles)
  - [Advanced Computer Science Topics](#advanced-computer-science-topics)
  - [DevOps Practices](#devops-practices)
  - [Cloud Computing](#cloud-computing)
  - [Security](#security)
  - [Data Engineering](#data-engineering)
  - [Emerging Technologies](#emerging-technologies)
  - [Miscellaneous](#miscellaneous)
- [Blogs](#blogs)
  - [Santosh Pai](#santosh-pai)
  - [Arslan Ahmad](#arslan-ahmad)
- [Books](#books)
- [How to Use This Repository](#how-to-use-this-repository)
- [Contribution](#contribution)

## Introduction

Welcome to the Software Architecture Learning Path repository! This repository is designed to help you prepare for a 
software architect interview or to simply enhance your knowledge in software architecture. Whether you're a seasoned developer looking to transition into an architecture role or a current architect aiming to sharpen your skills, this repository provides a structured and comprehensive learning journey.

## Purpose

The purpose of this repository is to organize and present key topics and concepts that are crucial for a software architect. It includes a well-structured learning path covering various aspects of software architecture, design patterns, computer science fundamentals, security, distributed systems, performance optimization, API design, infrastructure, technologies, containers, DevOps, and more. By following this path, you'll gain a deeper understanding of the principles, practices, and technologies that underpin modern software architecture.

## Learning Path for Software Architect Interview

### 1. Architecture Patterns

- **Monolithic Architecture**
  - [x] [Monolith](./architecture-patterns/monolith.md)
- **Layered Architecture**
  - [x] [N-Tier](./architecture-patterns/n-tier.md)
- **Event-Driven Architecture**
  - [x] [Event Driven](.//event-driven.md)
- **Hexagonal Architecture**
  - [x] [Hexagonal Architecture](./architecture-patterns/hexagonal-architecture.md)
- **Clean Architecture**
  - [x] [Clean Architecture](./architecture-patterns/clean-architecture.md)
- **IDesign Method**
  - [x] [IDesign](./architecture-patterns/idesign.md)
- **Architectural Interview Preparation**
  - [x] [Interview Notes](./architecture-patterns/interview-notes.md)

### 2. Design Patterns

- **Classical Design Patterns**
  - [x] [Gang of Four](./design-patterns/gang-of-four.md)

### 3. Computer Science Fundamentals

- **Algorithm Complexity**
  - [x] [O(n) notation](./computer-science-development-fundamentals/o-notation.md)
- **Concurrency**
  - [x] [Mutual Exclusion](./operating-systems/mutual-exclusion.md)
  - [x] [Mutual Exclusion Primitives](./computer-science-development-fundamentals/mutual-exclusion-primitives.md)
  - [x] [Optimistic Locking](./computer-science-development-fundamentals/optimistic-locking.md)
- **Data Structures**
  - [x] [Collection Data Structures](./computer-science-development-fundamentals/collection-data-structures.md)
- **Programming Paradigms**
  - [x] [Compiled vs. Interpreted languages](./computer-science-development-fundamentals/compiled-vs-interpreted-languages.md)
  - [x] [Runtimes and Intermediate-languages (e.g. JAVA, .NET)](./computer-science-development-fundamentals/runtimes-and-intermediate-languages.md)
- **Networking and Protocols**
  - [x] [TCP vs. UDP](./computer-science-development-fundamentals/tcp-vs-udp.md)
  - [x] [Protocols and Serialization](./computer-science-development-fundamentals/protocols-and-serialization.md)
- **Memory Management**
  - [x] [Virtual Memory](./computer-science-development-fundamentals/virtual-memory.md)
- **Character Encoding**
  - [x] [Unicode and Character Encoding](./computer-science-development-fundamentals/unicode-character-encoding.md)
- **Type Systems**
  - [x] [Values vs Reference Types](./computer-science-development-fundamentals/value-vs-reference-types.md)

### 4. Security

- **Fundamentals**
  - [x] [Certificates](./security/certificates.md)
  - [x] [Encryption](./security/encryption.md)
  - [x] [Hashing](./security/hashing.md)
  - [x] [JWT's](./security/jwt.md)

### 5. Distributed Systems

- **Theoretical Foundations**
  - [x] [CAP Theorem](./distributed-systems/cap-theorem.md)
- **Consistency Models**
  - [x] [Eventual Consistency](./distributed-systems/eventual-consistency.md)
- **High Availability**
  - [x] [High Availability](./distributed-systems/high-availability.md)
- **Data Consistency Protocols**
  - [x] [N Phase Commit](./distributed-systems/n-phase-commit.md)
- **Communication Models**
  - [x] [Event Queue vs Message Queue](./distributed-systems/event-queue-vs-message-queue.md)
- **Transaction Management**
  - [x] [Saga Pattern](./distributed-systems/saga-pattern.md)

### 6. Performance

- **Asynchronous Programming**
  - [ ] [How async/await works](./performance/async-await.md)
- **Low-Level Performance**
  - [x] [Bitwise operators](./performance/bitwise-operators.md)

### 7. API Design

- **API Documentation**
  - [x] [Documenting APIs and IDL](./api-design/documenting-apis-and-idl.md)
- **API Behavior**
  - [x] [Idempotent Behaviour](./api-design/idempotent-behaviour.md)
- **API Protocols**
  - [x] [RPC vs. REST](./api-design/rpc-vs-rest.md)

### 8. Infrastructure and Hardware

- **Caching**
  - [x] [Caches and False Cache-line Invalidation](./infrastructure-and-hardware/caches-and-false-cacheline-invalidation.md)
- **Instruction Sets**
  - [ ] [32-bit and 64-bit instruction sets](./infrastructure-and-hardware/32bit-and-64bit-instruction-sets.md)
- **Firewalls**
  - [ ] [How do firewalls work?](./infrastructure-and-hardware/firewalls.md)
- **Memory Access**
  - [ ] [Memory access times](./infrastructure-and-hardware/memory-access-times.md)
- **Storage Area Networks (SANs)**
  - [ ] [How do SANs work?](./infrastructure-and-hardware/sans.md)
- **Virtual Machines**
  - [ ] [How do virtual machines work?](./infrastructure-and-hardware/virtual-machines.md)

### 9. Technologies

- **Databases**
  - [x] [Database Types](/.technologies/database-types.md)
- **Message Brokers**
  - [x] [Kafka](./technologies/kafka.md)
  - [x] [RabbitMQ](./technologies/rabbitmq.md)
- **Artificial Intelligence**
  - [x] [Deep Learning](./technologies/artificial-intelligence/deep-learning.md)
  - [ ] [Machine Learning](./technologies/artificial-intelligence/machine-learning.md)
  - [ ] [ML.NET](./technologies/artificial-intelligence/ml-net.md)
  - [ ] [Neural Networks](./technologies/artificial-intelligence/neural-networks.md)
  - [ ] [Training and Labelling](./technologies/artificial-intelligence/training-and-labelling.md)

### 10. Containers and Kubernetes

- **Containers**
  - [ ] [Fundamentals](./containers-kubernetes/containers/fundamentals.md)
  - [ ] [Linux on Windows](./containers-kubernetes/containers/linux-on-windows.md)
  - [ ] [Repositories and Tagging](./containers-kubernetes/containers/repositories-and-tagging.md)
- **Kubernetes**
  - [ ] [Architecture - K8s components](./containers-kubernetes/kubernetes/architecture-k8s-components.md)
  - [ ] [Health Checks](./containers-kubernetes/kubernetes/health-checks.md)
  - [ ] [Helm](./containers-kubernetes/kubernetes/helm.md)

### 11. DevOps

- **Code Quality and Tools**
  - [ ] [Linters and Code Quality Tools](./devops/linters-and-code-quality-tools.md)
- **Observability**
  - [ ] [Observability](./devops/observability.md)
- **CI/CD Pipelines**
  - [ ] [Pipelines](./devops/pipelines.md)
  - [ ] [PR's and everything-as-code](./devops/prs-and-everything-as-code.md)
- **Agile Methods and Analysis**
  - [ ] [Agile methods](./devops/analysis/agile.md)
  - [ ] [Capturing requirements](./devops/analysis/capturing-requirements.md)
  - [ ] [#noestimates](./devops/analysis//no-estimates.md)
  - [ ] [SCRUM vs. Kanban](./devops/analysis//scrum-vs-kanban.md)
  - [ ] [UML use-cases and activity diagrams](./devops/analysis/uml.md)
  - [ ] [Waterfall](./devops/analysis/waterfall.md)
- **Testing**
  - [ ] [Automated tests](./devops/testing/automated-tests.md)
  - [ ] [The test pyramid](./devops/testing/test-pyramid.md)
  - [ ] [Kinds of tests, techniques for each](./devops/testing/test-techniques.md)

## Potential Missing Topics

### Advanced Architecture Patterns

- Microservices
- Service-Oriented Architecture (SOA)
- Serverless Architecture

### Software Development Principles

- SOLID Principles
- Domain-Driven Design (DDD)
- Test-Driven Development (TDD)
- Continuous Integration/Continuous Deployment (CI/CD)

### Advanced Computer Science Topics

- Graph Algorithms
- Dynamic Programming
- Distributed Algorithms
- Computational Complexity

### DevOps Practices

- Infrastructure as Code (IaC)
- Continuous Monitoring
- Containerization (Docker, Kubernetes)
- Configuration Management (Ansible, Chef, Puppet)

### Cloud Computing

- Cloud Architecture Patterns
- Cloud Security
- Hybrid and Multi-Cloud Strategies
- Cloud Service Models (IaaS, PaaS, SaaS)

### Security

- OAuth and OpenID Connect
- Secure Coding Practices
- Network Security
- Penetration Testing

### Data Engineering

- ETL (Extract, Transform, Load) Processes
- Data Warehousing
- Big Data Technologies (Hadoop, Spark)
- Data Lake Architecture

### Emerging Technologies

- Blockchain
- Edge Computing
- Quantum Computing
- Internet of Things (IoT)

### Miscellaneous

- Software Project Management
- Risk Management
- Legal and Ethical Issues in Software Development
- Communication Skills for Architects

## Blogs

### Santosh Pai

- [12 factor Microservice applications — on Kubernetes](https://itnext.io/12-factor-microservice-applications-on-kubernetes-db913008b018)
- [Isolating and Managing Dependencies in 12-factor Microservice Applications — with Kubernetes](https://itnext.io/isolating-and-managing-dependencies-in-12-factor-microservice-applications-with-kubernetes-988638f8bc6d)

### Arslan Ahmad

- [12 Microservices Patterns I Wish I Knew Before the System Design Interview](https://levelup.gitconnected.com/12-microservices-pattern-i-wish-i-knew-before-the-system-design-interview-5c35919f16a2)
- [I Wish I Knew These 10 Software Architectural Styles Before the Interview](https://levelup.gitconnected.com/i-wish-i-knew-these-10-software-architectural-styles-before-the-interview-b08d8224433f)

## Books

- Designing Data-Intensive Applications - Martin Kleppmann
  - [PDF](https://github.com/ms2ag16/Books/blob/master/Designing%20Data-Intensive%20Applications%20-%20Martin%20Kleppmann.pdf)
  - [Learning Notes](https://github.com/keyvanakbary/learning-notes/blob/master/books/designing-data-intensive-applications.md)

## How to Use This Repository

1. Start with the basics: Begin with fundamental concepts in computer science to build a strong foundation.
2. Progress through architecture patterns: Understand different architectural styles and their use cases.
3. Deepen your knowledge in design patterns: Study classical design patterns and their applications.
4. Explore advanced topics: Dive into distributed systems, performance optimization, and security.
5. Practical applications: Learn about technologies, containers, Kubernetes, and DevOps practices.
6. Prepare for interviews: Use the provided interview notes and mock questions to get ready for your software architect interviews.

## Contribution

Feel free to contribute by submitting pull requests for additional topics, improvements, or corrections. This repository aims to be a collaborative learning resource for aspiring software architects.
