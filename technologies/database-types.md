# Database Types

![Database Types](https://unihost.com/blog/wp-content/uploads/2021/11/657.png)

## RDBMS

A relational database is a (most commonly digital) database based on the relational model of data, as proposed by E. F. Codd in 1970. A system used to maintain relational databases is a relational database management system (RDBMS). Many relational database systems are equipped with the option of using SQL (Structured Query Language) for querying and updating the database.

### SQL

Structured Query Language (SQL) is a domain-specific language used in programming and designed for managing data held in a relational database management system (RDBMS), or for stream processing in a relational data stream management system (RDSMS). It is particularly useful in handling structured data, i.e., data incorporating relations among entities and variables.

## NoSQL

NoSQL (originally referring to "non-SQL" or "non-relational") is an approach to database design that focuses on providing a mechanism for storage and retrieval of data that is modeled in means other than the tabular relations used in relational databases. Instead of the typical tabular structure of a relational database, NoSQL databases house data within one data structure. Since this non-relational database design does not require a schema, it offers rapid scalability to manage large and typically unstructured data sets. NoSQL systems are also sometimes called "Not only SQL" to emphasize that they may support SQL-like query languages or sit alongside SQL databases in polyglot-persistent architectures.

## Graph DB

A graph database (GDB) is a database that uses graph structures for semantic queries with nodes, edges, and properties to represent and store data. A key concept of the system is the graph (or edge or relationship). The graph relates the data items in the store to a collection of nodes and edges, the edges representing the relationships between the nodes. The relationships allow data in the store to be linked together directly and, in many cases, retrieved with one operation. Graph databases hold the relationships between data as a priority. Querying relationships is fast because they are perpetually stored in the database. Relationships can be intuitively visualized using graph databases, making them useful for heavily inter-connected data.

## Time Series DB

A time series database (TSDB) is a software system that is optimized for storing and serving time series through associated pairs of time(s) and value(s). In some fields, time series may be called profiles, curves, traces or trends. Several early time series databases are associated with industrial applications which could efficiently store measured values from sensory equipment (also referred to as data historians), but now are used in support of a much wider range of applications.

## Database Types Comparison

|   | Relational Database Management System (RDBMS) | NoSQL Databases | Graph Databases | Time Series Databases (TSDBs) |
| - | --------------------------------------------- | --------------- | --------------- | ------------ |
| **Table Structure** |RDBMS databases store data in tables with a fixed schema. Each table has predefined columns, and each row contains specific data that adheres to the column definitions | NoSQL databases use various data models like document-based, key-value, column-family, and wide-column stores, each with its own structure. They typically do not enforce a fixed schema. | Graph databases organize data as nodes (entities) and edges (relationships), not in tables. Nodes and edges can have properties, but the data structure is inherently graph-based. | TSDBs are optimized for storing and querying time-stamped data. They typically use a table-like structure with a timestamp column and one or more value columns. Each row represents a data point recorded at a specific timestamp. |
| **Data Relationships** | RDBMS databases use tables and define relationships between them through foreign keys. These relationships enforce referential integrity. | NoSQL databases often avoid complex relationships between tables and favor denormalized data or embedding related data within documents or records. | Graph databases excel at modeling and traversing complex relationships between data points, making them ideal for scenarios where understanding connections is crucial. | TSDBs are specialized for handling time-ordered data and may not have the complex relationships found in RDBMS or graph databases. |
| **Query Language** | SQL (Structured Query Language) is used to perform complex queries and join data from multiple tables. | Query languages vary depending on the NoSQL database type, but they are generally less expressive and powerful than SQL for complex joins and transactions. | Graph databases typically have their query languages (e.g., Cypher for Neo4j). These languages are optimized for graph traversals and pattern matching. | TSDBs often provide specialized query languages or extensions of SQL to efficiently query and aggregate time-series data. Common operations include time-based filtering, aggregation over time intervals, and downsampling. |
| **Use Cases** | Well-suited for structured data with clear relationships, such as financial records, inventory management, and traditional business applications. | Suitable for unstructured or semi-structured data, high scalability, and applications where flexibility and speed of development are crucial, such as web and mobile apps, real-time analytics, and content management systems. | Best suited for scenarios where data relationships are the primary focus, such as social networks, recommendation engines, fraud detection, and network analysis. |  Ideal for applications that involve collecting and analyzing time-stamped data, such as IoT sensor data, monitoring and observability, financial market data, and performance metrics tracking. |

## Sources

- <https://en.wikipedia.org/wiki/Relational_database>
- <https://en.wikipedia.org/wiki/SQL>
- <https://en.wikipedia.org/wiki/NoSQL>
- <https://en.wikipedia.org/wiki/Graph_database>
- <https://en.wikipedia.org/wiki/Time_series_database>
- <https://chat.openai.com/>
