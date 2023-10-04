# Event Driven Architecture

## Definition

An event-driven architecture uses events to trigger and communicate between decoupled services and is common in modern applications built with microservices.

## Notes

- An event is a change in state, or an update, like an item being placed in a shopping cart on an e-commerce website. Events can either carry the state (the item purchased, its price, and a delivery address) or events can be identifiers (a notification that an order was shipped).
- Event-driven architectures have three key components:
  - Producers
  - Routers
  - Consumers
- When to use this architecture
  - Multiple subsystems must process the same events.
  - Real-time processing with minimum time lag.
  - Complex event processing, such as pattern matching or aggregation over time windows.
  - High volume and high velocity of data, such as IoT.

## Advantages vs Disadvantages

| Advantages | Disadvantages |
| ---------- | ------------- |
| Loose coupling | Duplicated events |
| Fault tolerance | Error handling and troubleshooting |
| Reduced technical debt | Naming convention confusion |
| | Lack of clear workflow order |

## RabbitMQ vs Kafaka

| Topic | RabbitMQ | Kafka |
| ----- | -------- | ----- |
| **Performance** | 4K-10K messages per second | 1 million messages per second |
| **Message Retention** | Acknowledgment based | Policy-based (e.g., 30 days) |
| **Data Type** | Transactional | Operational |
| **Consumer Mode** | Smart broker/dumb consumer | Dumb broker/smart consumer |
| **Topology** | Exchange type: Direct, Fan out, Topic, Header-based | Publish/subscribe based |
| **Payload Size** | No constraints | Default 1MB limit |
| **Usage Cases** | Simple use cases | Massive data/high throughput cases |

- Data Flow
  - RabbitMQ uses a distinct, bounded data flow. Messages are created and sent by the producer and received by the consumer. Apache Kafka uses an unbounded data flow, with the key-value pairs continuously streaming to the assigned topic.
- Data Usage
  - RabbitMQ is best for transactional data, such as order formation and placement, and user requests. Kafka works best with operational data like process operations, auditing and logging statistics, and system activity.
- Messaging
  - RabbitMQ sends messages to users. These messages are removed from the queue once they are processed and acknowledged. Kafka is a log. It uses continuous messages, which stay in the queue until the retention time expires.
- Design Model
  - RabbitMQ employs the smart broker/dumb consumer model. The broker consistently delivers messages to consumers and keeps track of their status. Kafka uses the dumb broker/smart consumer model. Kafka doesn’t monitor the messages each user has read. Rather, it retains unread messages only, preserving all messages for a set amount of time. Consumers must monitor their position in each log.
- Topology
  - RabbitMQ uses the exchange queue topology — sending messages to an exchange where they are in turn routed to various queue bindings for the consumer’s use. Kafka employs the publish/subscribe topology, sending messages across the stream to the correct topics, and then consumed by users in the different authorized groups.
- Architecture Differences
  - When choosing between Apache Kafka and RabbitMQ, the internal operations and fundamental design can be important considerations.
  - The components of RabbitMQ’s Architecture consist of the following:
    - Queue: It is in charge of keeping track of messages that have been received and may have configuration data that specifies what it can do with a message.
    - Exchange: An exchange receives messages sent to RabbitMQ and determines where they should be forwarded. Exchanges define the routing strategies that are used for messages, most frequently by examining the data characteristics that are transmitted with the message or included inside its attributes.
    - Producer: Produces messages and sends them to a broker server (publishes). A payload and a label are the two components of a message. The user's desired data to convey is the payload. The label specifies who should receive a copy of the message and describes the payload.
    - Consumer: It subscribes to a queue and is connected to a broker server.
    - Broker: Applications can exchange information and communicate with one another through a broker.
    - Binding: It tells an exchange which queues to distribute messages. Additionally, the binding will instruct the exchange to filter which messages it is permitted to add to a queue for specific exchange types.
  - Kafka’s architecture is designed using the following components:
    - Mirror Maker: One of the most crucial elements of Kafka is replication, which makes sure that messages are published and consumed even in the event that the broker encounters a problem.
    - ZooKeeper: Acts as a liaison between the consumers and the Kafka broker. It maintains coordination data such as configuration, location, and status details.
    - Producer: Producers push or publish messages to a Kafka topic created on a Kafka broker. Producers also have the option of sending messages to a broker in a synchronous or asynchronous manner.
    - Consumers: Individuals who subscribe to a Kafka topic and pull messages from it. Kafka By default, consumers store messages in ZooKeeper. However, Kafka also allows data to be stored in additional storage platforms used by programs for online transaction processing (OLTP).
    - Broker: Acts as a Kafka server, or broker. The number of partitions for each message is defined in accordance with the order in which the messages are stored by the broker.
- Scalability and Redundancy
  - RabbitMQ uses a round-robin queue to repeat messages. To boost throughput and balance the load, the messages are divided among the queues. Additionally, it enables numerous consumers to read messages from various queues at once.
  - Scalability and redundancy are provided by Kafka partitions. The partition was duplicated across numerous brokers. In the event that one of the brokers fails, the customer can still be served by another broker.
  - If we store all of the partitions in one broker, our dependence on that broker will grow, which is hazardous and increases the likelihood that it will fail. Additionally, distributing the partitions will vastly improve throughput.
- Message Deletion
  - To be unqueued, RabbitMQ delivers a successful acknowledgment via the consumer.
  - The messages are returned to the queue on negative ACK and saved to the consumer on positive ACK.
  - While Kafka uses a retention time, any messages that were retained based on that period are erased once it has passed.
- Message Consumption
  - A message must be delivered to the customer by one of RabbitMQ's brokers, and these messages are transmitted in batches.
  - Kafka Consumers read a message from the broker and keep the queue counter offset trackable. As soon as the message is read, the offset is increased.
- Message Priority
  - Messages can be given priority with the help of a priority queue in RabbitMQ.
  - In Kafka, all messages have the same priority, which cannot be altered.

## Sources

- <https://aws.amazon.com/event-driven-architecture/#:~:text=What%20is%20an%20Event%2DDriven,modern%20applications%20built%20with%20microservices>.
- <https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/event-driven>
- <https://www.techtarget.com/searchapparchitecture/tip/Event-driven-architecture-pros-and-cons-Is-EDA-worth-it>
- <https://www.simplilearn.com/kafka-vs-rabbitmq-article>
