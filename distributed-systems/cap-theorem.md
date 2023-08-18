# CAP Theorem

![CAP Theorem](https://miro.medium.com/v2/resize:fit:850/1*Br1FrvKnK3hU6Xl_LbDkwg.png)

## Definition

The CAP theorem, originally introduced as the CAP principle, can be used to explain some of the competing requirements in a distributed system with replication. It is a tool used to make system designers aware of the trade-offs while designing networked shared-data systems. 

The three letters in CAP refer to three desirable properties of distributed systems with replicated data: consistency (among replicated copies), availability (of the system for read and write operations) and partition tolerance (in the face of the nodes in the system being partitioned by a network fault). 

The CAP theorem states that it is not possible to guarantee all three of the desirable properties – consistency, availability, and partition tolerance at the same time in a distributed system with data replication. 

![](https://www.mysoftkey.com/wp-content/uploads/2016/09/cap-theorem-1.png)

### Consistency

Consistency means that the nodes will have the same copies of a replicated data item visible for various transactions. A guarantee that every node in a distributed cluster returns the same, most recent and a successful write. Consistency refers to every client having the same view of the data. There are various types of consistency models. Consistency in CAP refers to sequential consistency, a very strong form of consistency. 

### Availability 

Availability means that each read or write request for a data item will either be processed successfully or will receive a message that the operation cannot be completed. Every non-failing node returns a response for all the read and write requests in a reasonable amount of time. The key word here is “every”. In simple terms, every node (on either side of a network partition) must be able to respond in a reasonable amount of time. 
 
### Partition Tolerance

Partition tolerance means that the system can continue operating even if the network connecting the nodes has a fault that results in two or more partitions, where the nodes in each partition can only communicate among each other. That means, the system continues to function and upholds its consistency guarantees in spite of network partitions. Network partitions are a fact of life. Distributed systems guaranteeing partition tolerance can gracefully recover from partitions once the partition heals. 

## Notes

* CA (Consistency and Availability) - The system prioritizes availability over consistency and can respond with possibly stale data.

  `Example databases: Cassandra, CouchDB, Riak, Voldemort.`

* AP (Availability and Partition Tolerance) - The system prioritizes availability over consistency and can respond with possibly stale data. The system can be distributed across multiple nodes and is designed to operate reliably even in the face of network partitions.
  
  `Example databases: Amazon DynamoDB, Google Cloud Spanner.`

* CP (Consistency and Partition Tolerance) - The system prioritizes consistency over availability and responds with the latest updated data.
The system can be distributed across multiple nodes and is designed to operate reliably even in the face of network partitions.

  `Example databases: Apache HBase, MongoDB, Redis.`

* It’s important to note that these database systems may have different configurations and settings that can change their behavior with           respect to consistency, availability, and partition tolerance. Therefore, the exact behavior of a database system may depend on its            configuration and usage. For example, Neo4j, a graph database, the CAP theorem still applies. Neo4j prioritizes consistency and partition tolerance over availability, which means that in the event of a network partition or failure, Neo4j will sacrifice availability to maintain consistency.

![](https://www.mysoftkey.com/wp-content/uploads/2016/09/cap-theorem-triangle.png)


## Sources

- <https://www.geeksforgeeks.org/the-cap-theorem-in-dbms/>
- <https://www.mysoftkey.com/architecture/understanding-of-cap-theorem/>