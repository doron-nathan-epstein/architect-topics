# Architect Topical Knowledge Requirements <!-- omit in toc -->

- [Context](#context)
- [Topics](#topics)
  - [High Availability](#high-availability)
  - [Security](#security)
  - [Testing](#testing)
  - [Performance](#performance)
  - [Operating Systems](#operating-systems)
  - [Architecture Patterns](#architecture-patterns)
  - [Analysis](#analysis)
  - [Project Work Styles](#project-work-styles)
  - [Design Patterns](#design-patterns)
  - [Computer Science and Development Fundamentals](#computer-science-and-development-fundamentals)
  - [APIs](#apis)
  - [DevOps](#devops)
  - [Infrastructure and Hardware](#infrastructure-and-hardware)
  - [Containers](#containers)
  - [Kubernetes](#kubernetes)
  - [Artificial Intelligence](#artificial-intelligence)
- [Blogs](#blogs)
  - [Santosh Pai](#santosh-pai)
  - [Arslan Ahmad](#arslan-ahmad)

## Context

## Topics

### High Availability

- [ ] [Applications](./high-availablity/applications.md)
- [ ] [Databases](./high-availablity/databases.md)

### Security

- [x] [Hashing](./security/hashing.md)
- [ ] [Encryption](./security/encryption.md)
- [ ] [JWT's](./security/jwt.md)
- [x] [Certificates](./security/certificates.md)
- [ ] [Symmetric and Asymmetric encryption](./security/symmetric-vs-asymmetric-encryption.md)

### Testing

- [ ] [The test pyramid](./testing/test-pyramid.md)
- [ ] [Kinds of tests, techniques for each](./testing/test-techniques.md)

### Performance

- [ ] [Threads](./performance/threads.md)
- [ ] [How async/await works](./performance/async-await.md)

### Operating Systems

- [ ] [Virtual Memory](./operating-systems/virtual-memory.md)
- [ ] [Mutual Exclusion](./operating-systems/mutual-exclusion.md)

### Architecture Patterns

- [x] [N-Tier](./architecture-patterns/n-tier.md)
- [x] [Event Driven](./architecture-patterns/event-driven.md)
- [x] [Monolith](./architecture-patterns/monolith.md)
- [x] [IDesign](./architecture-patterns/idesign.md)

### Analysis

- [ ] [Capturing requirements](./analysis/capturing-requirements.md)
- [ ] [UML use-cases and activity diagrams](./analysis/uml.md)

### Project Work Styles

- [ ] [Waterfall](./project-work-styles/waterfall.md)
- [ ] [Agile methods](./project-work-styles/agile.md)
- [ ] [SCRUM vs. Kanban](./project-work-styles/scrum-vs-kanban.md)
- [ ] [#noestimates](./project-work-styles/no-estimates.md)

### Design Patterns

- [x] [Gang of Four](./design-patterns/gang-of-four.md)
- [x] [Hexagonal Architecture](./design-patterns/hexagonal-architecture.md)
- [x] [Clean Architecture](./design-patterns/clean-architecture.md)
- [ ] [UML](./design-patterns/uml.md)

### Computer Science and Development Fundamentals

- [ ] [Values vs Reference Types](./computer-science-development-fundamentals/value-vs-reference-types.md)
- [ ] [O(n) notation](./computer-science-development-fundamentals/o-notation.md)
- [ ] [Collection Data Structures](./computer-science-development-fundamentals/collection-data-structure.md)
- [ ] [Bitwise operators](./computer-science-development-fundamentals/bitwise-operators.md)
- [ ] [Unicode and Character Encoding](./computer-science-development-fundamentals/unicode-character-encoding.md)
- [ ] [Protocols and Serialization](./computer-science-development-fundamentals/protocols-and-serialization.md)
- [x] [TCP vs. UDP](./computer-science-development-fundamentals/tcp-vs-udp.md)
- [ ] [Mutual Exclusion Primitives](./computer-science-development-fundamentals/mutual-exlusion-primitives.md)
- [ ] [CAP Theorem](./computer-science-development-fundamentals/cap-theorem.md)
- [ ] [Eventual Consistency](./computer-science-development-fundamentals/eventual-consistency.md)
- [ ] [Saga Pattern](./computer-science-development-fundamentals/saga-pattern.md)
- [ ] [N Phase Commit](./computer-science-development-fundamentals/n-phase-commit.md)
- [ ] [Optimistic Locking](./computer-science-development-fundamentals/optimistic-locking.md)
- [ ] [Compiled vs. Interpreted languages](./computer-science-development-fundamentals/compiled-vs-interpreted-languages.md)
- [ ] [Runtimes and Intermediate-languages (e.g. JAVA, .NET)](./computer-science-development-fundamentals/runtimes-and-intermediate-languages.md)

### APIs

- [ ] [RPC vs. REST](./apis/rpc-vs-rest.md)
- [ ] [Idempotent behaviour](./apis/idempotent-behaviour.md)
- [ ] [Documenting APIs and IDL](./apis/documenting-apis-and-idl.md)

### DevOps

- [ ] [Pipelines](./devops/pipelines.md)
- [ ] [PR's and everything-as-code](./devops/prs-and-everything-as-code.md)
- [ ] [Automated tests](./devops/automated-tests.md)
- [ ] [Linters and Code Quality Tools](./devops/linters-and-code-quality-tools.md)
- [ ] [Observability](./devops/observability.md)

### Infrastructure and Hardware

- [ ] [How do firewalls work?](./infrastructure-and-hardware/firewalls.md)
- [ ] [How do virtual machines work?](./infrastructure-and-hardware/virtual-machines.md)
- [ ] [How do SANs work?](./infrastructure-and-hardware/sans.md)
- [ ] [Memory access times](./infrastructure-and-hardware/memory-access-times.md)
- [ ] [32-bit and 64-bit instruction sets](./infrastructure-and-hardware/32bit-and-64bit-instruction-sets.md)
- [ ] [Caches and False Cache-line Invalidation](./infrastructure-and-hardware/caches-and-false-cacheline-invalidation.md)

### Containers

- [ ] [Fundamentals](./containers/fundamentals.md)
- [ ] [Linux on Windows](./containers/linux-on-windows.md)
- [ ] [Repositories and Tagging](./containers/repositories-and-tagging.md)

### Kubernetes

- [ ] [Architecture - K8s components](./kubernetes/architecture-k8s-components.md)
- [ ] [Kinds of Resources](./kubernetes/kinds-of-resources.md)
- [ ] [Health Checks](./kubernetes/health-checks.md)
- [ ] [Helm](./kubernetes/helm.md)

### Artificial Intelligence

- [ ] [Machine Learning](./artificial-intelligence/machine-learning.md)
- [ ] [Deep Learning](./artificial-intelligence/deep-learning.md)
- [ ] [Neural Networks](./artificial-intelligence/neural-networks.md)
- [ ] [Training and Labelling](./artificial-intelligence/training-and-labelling.md)
- [ ] [ML.NET](./artificial-intelligence/ml-net.md)

## Blogs

### Santosh Pai

- [12 factor Microservice applications — on Kubernetes](https://itnext.io/12-factor-microservice-applications-on-kubernetes-db913008b018)
- [Isolating and Managing Dependencies in 12-factor Microservice Applications — with Kubernetes](https://itnext.io/isolating-and-managing-dependencies-in-12-factor-microservice-applications-with-kubernetes-988638f8bc6d)

### Arslan Ahmad

- [12 Microservices Patterns I Wish I Knew Before the System Design Interview](https://levelup.gitconnected.com/12-microservices-pattern-i-wish-i-knew-before-the-system-design-interview-5c35919f16a2)
- [I Wish I Knew These 10 Software Architectural Styles Before the Interview](https://levelup.gitconnected.com/i-wish-i-knew-these-10-software-architectural-styles-before-the-interview-b08d8224433f)