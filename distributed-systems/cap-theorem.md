# CAP Theorem

![CAP Theorem](https://miro.medium.com/v2/resize:fit:850/1*Br1FrvKnK3hU6Xl_LbDkwg.png)

## Definition

The CAP theorem, originally introduced as the CAP principle, explains the trade-offs involved in designing distributed systems with replicated data. It states that it's impossible to simultaneously achieve all three of the following properties in a distributed system with data replication: Consistency, Availability, and Partition Tolerance.

![CAP Theorem Triangle](https://www.mysoftkey.com/wp-content/uploads/2016/09/cap-theorem-triangle.png)

### Consistency

Consistency ensures that all nodes in a distributed system have the same copies of a replicated data item visible for various transactions. It guarantees that every node returns the same, most recent, and successful write. Consistency in the CAP theorem typically refers to sequential consistency, a strong form of consistency.

### Availability

Availability ensures that every read or write request for a data item is processed successfully or receives a response indicating that the operation cannot be completed. In other words, every non-failing node responds to read and write requests promptly, ensuring the system remains accessible to clients.

### Partition Tolerance

Partition tolerance enables the system to continue operating even if network partitions occur, dividing nodes into separate groups that can only communicate within each group. Despite network partitions, the system maintains its consistency guarantees and gracefully recovers when partitions heal.

## Notes

- **CA (Consistency and Availability)**: Prioritizes availability over consistency, possibly responding with stale data. Example databases include Cassandra, CouchDB, Riak, and Voldemort.
  
- **AP (Availability and Partition Tolerance)**: Prioritizes availability over consistency and can respond with stale data. Designed to operate reliably in the face of network partitions. Example databases include Amazon DynamoDB and Google Cloud Spanner.

- **CP (Consistency and Partition Tolerance)**: Prioritizes consistency over availability and responds with the latest updated data. Designed to operate reliably even in the face of network partitions. Example databases include Apache HBase, MongoDB, and Redis.

*Note: Database behavior may vary based on configuration and usage.*

## Sources

- [GeeksforGeeks: The CAP Theorem in DBMS](https://www.geeksforgeeks.org/the-cap-theorem-in-dbms/)
- [MySoftKey: Understanding of CAP Theorem](https://www.mysoftkey.com/architecture/understanding-of-cap-theorem/)