# Kafka

## Definition

Apache Kafka is a distributed event store and stream-processing platform. It is an open-source system developed by the Apache Software Foundation written in Java and Scala. The project aims to provide a unified, high-throughput, low-latency platform for handling real-time data feeds. Kafka can connect to external systems (for data import/export) via Kafka Connect, and provides the Kafka Streams libraries for stream processing applications. Kafka uses a binary TCP-based protocol that is optimized for efficiency and relies on a "message set" abstraction that naturally groups messages together to reduce the overhead of the network roundtrip. This "leads to larger network packets, larger sequential disk operations, contiguous memory blocks [...] which allows Kafka to turn a bursty stream of random message writes into linear writes."

## Concepts

### Message

A message is the atomic unit of data for Kafka. Let’s say that you are building a log monitoring system, and you push each log record into Kafka, your log message is a JSON that has this structure.

When you push this JSON into Kafka you are actually pushing 1 message. Kafka saves this JSON as a byte array, and that byte array is a message for Kafka. This is that atomic unit, a JSON having two keys “level” and “message”. But it does not mean you can’t push anything else into Kafka, you can push String, Integer, a JSON of different schema, and everything else, but we generally push different types of messages into different topics (we will get to know what is a topic soon).

Messages might have an associated “Key” which is nothing but some metadata, which is used to determine the destination partition (will know soon as well) for a message.

### Topic

Topics, as the name suggests, are the logical categories of messages in Kafka, a stream of the same type of data. Going back to our previous example of the logging system, let’s say our system generates application logs, ingress logs, and database logs and pushes them to Kafka for other services to consume. Now, these three types of logs can be logically be divided into three topics, appLogs, ingressLogs, and dbLogs. We can create these three topics in Kafka, whenever there’s an app log message, we push it to appLogs topic and for database logs, we push it to the dbLogs topic. This way we have logical segregation between messages, sort of like having different tables for holding different types of data.

### Partitions

Partition is analogous to shard in the database and is the core concept behind Kafka’s scaling capabilities. Let’s say that our system becomes really popular and hence there are millions of log messages per second. So now the node on which appLogs topic is present, is unable to hold all the data that is coming in. We initially solve this by adding more storage to our node i.e. vertical scaling. But as we all know vertical scaling has its limit, once that threshold is reached we need to horizontally scale, which means we need to add more nodes and split the data between the nodes. When we split data of a topic into multiple streams, we call all of those smaller streams the “Partition” of that topic.

![Source: Kafka The Definitive Guide](https://miro.medium.com/v2/resize:fit:720/format:webp/1*pG3veZFlunxKRl9LlFhu-g.png)

This image depicts the idea of partitions, where a single topic has 4 partitions, and all of them hold a different set of data. The blocks you see here are the different messages in that partition. Let’s imagine the topic to be an array, now due to memory constraint we have split the single array into 4 different smaller arrays. And when we write a new message to a topic, the relevant partition is selected and then that message is added at the end of the array.

An offset for a message is the index of the array for that message. The numbers on the blocks in this picture denote the Offset, the first block is at the 0th offset and the last block would on the (n-1)th offset. The performance of the system also depends on the ways you set up partitions, we will look into that later in the article. (Please note that on Kafka it is not going to be an actual array but a symbolic one)

## Producer / Consumer

### Producer

- You can send messages in 3 ways to Kafka.
  - Fire and forget.
  - Synchronous send.
  - Asynchronous send.
- All of them have their performance vs consistency pitfalls.
- You can configure characteristics of acknowledgment on the producer as well.
  - ACK 0: Don’t wait for an ack |FASTEST
  - ACK 1: Consider sent when leader broker received the message |FASTER
  - ACK All: Consider sent when all replicas received the message |FAST
- You can compress and batch messages on producer before sending to broker.
  - It gives high throughput and lowers disk usage but raises CPU usage.
- Avro Serializer/ Deserializer
  - If you use Avro as the serializer/ deserializer instead of normal JSON, you will have to declare your schema upfront but this gives better performance and saves storage.

### Consumer

- Poll loop
  - Kafka consumer constantly polls data from the broker and it’s no the other way round.
- You can configure partition assignment strategy
  - Range: Consumer gets consecutive partitions
  - Round Robin: Self-explanatory
  - Sticky: Tries to create minimum impact while rebalancing keeping most of the assignment as is
  - Cooperative sticky: Sticky but allows cooperative rebalancing
- Batch size
  - We can configure how many records and how much data is returned per poll call.
- Commit offset
  - On message read we can update the offset position for the consumer, this is called committing the offset. Auto commit can be enabled or the application can commit the offset explicitly. This can be done both synchronously and asynchronously.

## Components and Description Cheatsheet

| Component | Description |
| --------- | ----------- |
| Topics | A stream of messages belonging to a particular category is called a topic. Data is stored in topics. Topics are split into partitions. For each topic, Kafka keeps a mini-mum of one partition. Each such partition contains messages in an immutable ordered sequence. A partition is implemented as a set of segment files of equal sizes. |
| Partition | Topics may have many partitions, so it can handle an arbitrary amount of data. |
| Partition offset | Each partitioned message has a unique sequence id called as offset. |
| Replicas of partition | Replicas are nothing but backups of a partition. Replicas are never read or write data. They are used to prevent data loss. |
| Brokers | Brokers are simple system responsible for maintaining the published data. Each broker may have zero or more partitions per topic. Assume, if there are N partitions in a topic and N number of brokers, each broker will have one partition. Assume if there are N partitions in a topic and more than N brokers (n + m), the first N broker will have one partition and the next M broker will not have any partition for that particular topic. Assume if there are N partitions in a topic and less than N brokers (n-m), each broker will have one or more partition sharing among them. This scenario is not recommended due to unequal load distribution among the broker. |
| Kafka Cluster | Kafka’s having more than one broker are called as Kafka cluster. A Kafka cluster can be expanded without downtime. These clusters are used to manage the persistence and replication of message data. |
| Producers | Producers are the publisher of messages to one or more Kafka topics. Producers send data to Kafka brokers. Every time a producer publishes a message to a broker, the broker simply appends the message to the last segment file. Actually, the message will be appended to a partition. Producer can also send messages to a partition of their choice. |
| Consumers | Consumers read data from brokers. Consumers subscribes to one or more topics and consume published messages by pulling data from the brokers. |
| Leader | Leader is the node responsible for all reads and writes for the given partition. Every partition has one server acting as a leader. |
| Follower | Node which follows leader instructions are called as follower. If the leader fails, one of the follower will automatically become the new leader. A follower acts as normal consumer, pulls messages and up-dates its own data store. |

## Sources

- <https://en.wikipedia.org/wiki/Apache_Kafka>
- <https://medium.com/inspiredbrilliance/kafka-basics-and-core-concepts-5fd7a68c3193>
- <https://www.tutorialspoint.com/apache_kafka/apache_kafka_fundamentals.htm>
