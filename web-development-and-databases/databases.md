# Learning Guide: Databases

- [Learning Guide: Databases](#learning-guide-databases)
  - [Introduction](#introduction)
  - [Key Concepts](#key-concepts)
  - [Types of Databases](#types-of-databases)
    - [Relational Databases](#relational-databases)
    - [NoSQL Databases](#nosql-databases)
  - [Popular Database Systems](#popular-database-systems)
    - [MySQL](#mysql)
    - [PostgreSQL](#postgresql)
    - [MongoDB](#mongodb)
  - [Database Management](#database-management)
    - [CRUD Operations](#crud-operations)
    - [Database Design](#database-design)
  - [Transactions and ACID Properties](#transactions-and-acid-properties)
  - [Database Security](#database-security)
  - [Scaling and Replication](#scaling-and-replication)
  - [Summary](#summary)

## Introduction

Databases are crucial for storing, managing, and retrieving structured or unstructured data efficiently. Understanding different database types, their management, and best practices is essential for backend developers and data engineers.

## Key Concepts

- **Database**: An organized collection of data.
- **DBMS (Database Management System)**: Software for managing databases.
- **SQL (Structured Query Language)**: Language for managing relational databases.
- **ACID Properties**: Properties that ensure database transactions are processed reliably.
- **Scaling**: Increasing database capacity to handle more data or users.
- **Replication**: Creating copies of a database to improve availability and fault tolerance.

## Types of Databases

### Relational Databases

Relational databases store data in tables with predefined schema and relationships between tables.

- **Examples**: MySQL, PostgreSQL, SQL Server.
- **Use Cases**: Applications requiring structured data with complex relationships.

### NoSQL Databases

NoSQL databases store data in a schema-less manner, allowing flexibility and scalability.

- **Examples**: MongoDB, Cassandra, Redis.
- **Use Cases**: Big data, real-time web applications, unstructured data storage.

## Popular Database Systems

### MySQL

MySQL is a widely used open-source relational database management system.

```sql
-- Example of creating a table in MySQL
CREATE TABLE users (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(50) NOT NULL,
    email VARCHAR(100) NOT NULL UNIQUE,
    password VARCHAR(255) NOT NULL
);
```

### PostgreSQL

PostgreSQL is a powerful, open-source object-relational database system.

```sql
-- Example of creating a table in PostgreSQL
CREATE TABLE products (
    id SERIAL PRIMARY KEY,
    name VARCHAR(100) NOT NULL,
    price NUMERIC(10, 2) NOT NULL
);
```

### MongoDB

MongoDB is a popular NoSQL document-oriented database.

```javascript
// Example of inserting a document in MongoDB
db.users.insertOne({
    username: "john_doe",
    email: "john@example.com",
    age: 30
});
```

## Database Management

### CRUD Operations

CRUD (Create, Read, Update, Delete) operations are fundamental for interacting with databases.

- **Create**: Inserting new data into a database.
- **Read**: Retrieving data based on specified criteria.
- **Update**: Modifying existing data.
- **Delete**: Removing data from the database.

### Database Design

Designing databases involves creating efficient schemas, defining relationships, and optimizing queries for performance.

## Transactions and ACID Properties

Transactions ensure data integrity by following ACID properties:

- **Atomicity**: All operations in a transaction complete successfully or none.
- **Consistency**: Data remains consistent before and after transaction execution.
- **Isolation**: Transactions are isolated from each other until completed.
- **Durability**: Changes made by committed transactions are permanent.

## Database Security

Implement security measures like authentication, authorization, encryption, and auditing to protect database assets from unauthorized access or attacks.

## Scaling and Replication

Scale databases horizontally (adding more servers) or vertically (upgrading hardware) to handle increased workload and ensure high availability.

## Summary

Databases are critical for storing and managing data in applications. Relational databases like MySQL and PostgreSQL offer structured data management, while NoSQL databases like MongoDB provide flexibility for unstructured data. Understanding database types, management, transactions, security, and scaling is essential for building robust and efficient applications.
