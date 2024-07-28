# Learning Guide: CAP Theorem

- [Learning Guide: CAP Theorem](#learning-guide-cap-theorem)
  - [Introduction](#introduction)
  - [Key Concepts](#key-concepts)
  - [Understanding CAP Theorem](#understanding-cap-theorem)
  - [Examples](#examples)
    - [Example 1: Consistent and Partition Tolerant (CP)](#example-1-consistent-and-partition-tolerant-cp)
    - [Example 2: Available and Partition Tolerant (AP)](#example-2-available-and-partition-tolerant-ap)
    - [Example 3: Consistent and Available (CA)](#example-3-consistent-and-available-ca)
  - [Implications of CAP Theorem](#implications-of-cap-theorem)
  - [Summary](#summary)

## Introduction

The CAP Theorem is a fundamental principle in distributed systems that describes the trade-offs between consistency, availability, and partition tolerance. Understanding CAP Theorem helps in designing and evaluating distributed systems.

## Key Concepts

- **Consistency (C)**: Every read receives the most recent write or an error.
- **Availability (A)**: Every request (read or write) receives a response (without a guarantee that it contains the most recent write).
- **Partition Tolerance (P)**: The system continues to operate despite an arbitrary number of messages being dropped or delayed by the network.

## Understanding CAP Theorem

CAP Theorem, proposed by Eric Brewer, states that in a distributed data store, it is impossible to simultaneously provide all three of the following guarantees:

1. **Consistency**: All nodes see the same data at the same time.
2. **Availability**: Every request receives a response, regardless of the success or failure of the request.
3. **Partition Tolerance**: The system continues to operate, even if there is a partition (network failure) that divides the nodes into multiple groups that cannot communicate with each other.

In the presence of a network partition, a distributed system has to choose between consistency and availability.

## Examples

### Example 1: Consistent and Partition Tolerant (CP)

In a CP system, the system ensures that all nodes see the same data, but some requests might be denied to maintain this consistency during a partition.

```plaintext
Example: HBase, MongoDB (configured for consistency)
```

### Example 2: Available and Partition Tolerant (AP)

In an AP system, the system ensures that every request receives a response, but the data might not be consistent across all nodes during a partition.

```plaintext
Example: Couchbase, Cassandra, DynamoDB
```

### Example 3: Consistent and Available (CA)

In a CA system, the system ensures that all nodes see the same data and every request receives a response, but this is only possible in the absence of network partitions.

```plaintext
Example: Traditional relational databases like MySQL (not distributed)
```

## Implications of CAP Theorem

| **Aspect**         | **Consistency (C)**                    | **Availability (A)**                     | **Partition Tolerance (P)**             |
|--------------------|----------------------------------------|------------------------------------------|------------------------------------------|
| **Trade-offs**     | Ensuring data consistency at all nodes | Ensuring every request gets a response   | System continues to function despite network failures |
| **System Design**  | Systems must deny some requests during partition to remain consistent | Systems must allow inconsistent data to be available | Systems must operate with potential data inconsistency or unavailability |

## Summary

The CAP Theorem highlights the trade-offs involved in designing distributed systems. While it is impossible to achieve consistency, availability, and partition tolerance simultaneously, understanding these trade-offs allows for better system design and decision-making based on the specific requirements and constraints of the application.
