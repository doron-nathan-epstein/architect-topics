# Interview Notes

## How to answer in a System Design Interview

1. For a Read-Heavy System - Consider using a Cache.
2. For a Write-Heavy System - Use Message Queues for async processing
3. For a Low Latency Requirement - Consider using a Cache and CDN.
4. Need Atomicity, Consistency, Isolation, Durability (ACID) Compliant DB - Go for RDBMS/SQL Database.
5. Have unstructured data - Go for NoSQL Database.
6. Have Complex Data (Videos, Images, Files) - Go for Blob/Object storage.
7. Complex Pre-computation - Use Message Queue & Cache.
8. High-Volume Data Search - Consider search index, tries or search engine.
9. Scaling SQL Database - Implement Database Sharding.
10. High Availability, Performance, & Throughput - Use a Load Balancer.
11. Global Data Delivery - Consider using a CDN.
12. Graph Data (data with nodes, edges, and relationships) - Utilize Graph Database.
13. Scaling Various Components - Implement Horizontal Scaling.
14. High-Performing Database Queries - Use Database Indexes.
15. Bulk Job Processing - Consider Batch Processing & Message Queues.
16. Server Load Management & Preventing DOS Attacks- Use a Rate Limiter.
17. Microservices Architecture - Use an API Gateway.
18. For Single Point of Failure - Implement Redundancy.
19. For Fault-Tolerance and Durability - Implement Data Replication.
20. For User-to-User fast communication - Use Websockets.
21. Failure Detection in Distributed Systems - Implement a Heartbeat.
22. Data Integrity - Use Checksum Algorithm.
23. Efficient Server Scaling - Implement Consistent Hashing.
24. Decentralized Data Transfer - Consider Gossip Protocol.
25. Location-Based Functionality - Use Quadtree, Geohash, etc.
26. Avoid Specific Technology Names - Use generic terms.
27. High Availability and Consistency Trade-Off - Eventual Consistency.
28. For IP resolution & Domain Name Query - Mention DNS (Domain Name System).
29. Handling Large Data in Network Requests - Implement Pagination.
30. Cache Eviction Policy - Preferred is LRU (Least Recently Used) Cache.
31. For System Observability - Consider implement Monitoring and alerting.
32. For Security - Consider ACL (Access Control Lists) and security groups.
33. For Global availability - Consider multi-region deployment.

## Cheat Sheet

![Microservices Best Practices](https://media.licdn.com/dms/image/D4E22AQGeby-gjYmZ2g/feedshare-shrink_800/0/1692251333350?e=1695859200&v=beta&t=ayvQAdRZfUbzgYZWYEmh50OjrN21RdoFeCA0dI-Oo18)

![API Architectures](https://media.licdn.com/dms/image/D4D22AQFJL505waXWMQ/feedshare-shrink_2048_1536/0/1692406577598?e=1695859200&v=beta&t=0YgNipGEyTqbhk5rsWBlw6zVndr53l6hKfNR2uW_giU)

## Sources

- <https://www.linkedin.com/posts/dinesh-varyani_systemdesign-interview-microservices-activity-7101067190350622720-mkbD/?utm_source=share&utm_medium=member_android>
