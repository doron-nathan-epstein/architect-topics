# Saga Pattern

![Saga Pattern](https://miro.medium.com/v2/resize:fit:720/format:webp/0*OZEToHT0UrRMytrJ.png)

## Definition

The saga pattern is a failure management pattern that helps establish consistency in distributed applications, and coordinates transactions between multiple microservices to maintain data consistency.

## Notes

* The saga design pattern is provide to manage data consistency across microservices in distributed transaction cases. Basically, saga patterns offers to create a set of transactions that update microservices sequentially,
and publish events to trigger the next transaction for the next microservices.
* If one of the step is failed, than saga patterns trigger to rollback transactions which is basically do reverse operations with publishing rollback events to previous microservices.
* The SAGA pattern is especially useful in distributed systems, where multiple microservices need to coordinate their actions. In the context of distributed transactions, the SAGA pattern can help ensure that the overall transaction is either completed successfully, or is rolled back to its initial state if any individual microservice encounters an error.
* The saga pattern provides transaction management with using a sequence of local transactions of microservices. Every microservices has its own database and it can able to manage local transaction in atomic way with strict consistency.

## Choreography-based saga

![Choreography-based saga](https://microservices.io/i/sagas/Create_Order_Saga.png)

An e-commerce application that uses this approach would create an order using a choreography-based saga that consists of the following steps:

1. The Order Service receives the POST /orders request and creates an Order in a PENDING state
2. It then emits an Order Created event
3. The Customer Service’s event handler attempts to reserve credit
4. It then emits an event indicating the outcome
5. The OrderService’s event handler either approves or rejects the Order

## Orchestration-based saga

![Orchestration-based saga](https://microservices.io/i/sagas/Create_Order_Saga_Orchestration.png)

An e-commerce application that uses this approach would create an order using an orchestration-based saga that consists of the following steps:

1. The Order Service receives the POST /orders request and creates the Create Order saga orchestrator
2. The saga orchestrator creates an Order in the PENDING state
3. It then sends a Reserve Credit command to the Customer Service
4. The Customer Service attempts to reserve credit
5. It then sends back a reply message indicating the outcome
6. The saga orchestrator either approves or rejects the Order

## Resulting context

This pattern has the following benefits:
* It enables an application to maintain data consistency across multiple services without using distributed transactions

This solution has the following drawbacks:
* The programming model is more complex. For example, a developer must design compensating transactions that explicitly undo changes made earlier in a saga.

There are also the following issues to address:
* In order to be reliable, a service must atomically update its database and publish a message/event. It cannot use the traditional mechanism of a distributed transaction that spans the database and the message broker. Instead, it must use one of the patterns listed below.
* A client that initiates the saga, which an asynchronous flow, using a synchronous request (e.g. HTTP POST /orders) needs to be able to determine its outcome. There are several options, each with different trade-offs:
  * The service sends back a response once the saga completes, e.g. once it receives an OrderApproved or OrderRejected event.
  * The service sends back a response (e.g. containing the orderID) after initiating the saga and the client periodically polls (e.g. GET /orders/{orderID}) to determine the outcome
  * The service sends back a response (e.g. containing the orderID) after initiating the saga, and then sends an event (e.g. websocket, web hook, etc) to the client once the saga completes.

## Advantages & Disadvantages
| Advantages | Disadvantages |
|------------|---------------|
|Provides better fault tolerance: With SAGA, if one step fails, the entire process can be rolled back or compensated without affecting other steps.	 |Increased complexity: Implementing SAGA requires additional coding and architecture to handle compensation and rollback steps. |
| Simplifies error handling: SAGA provides a clear and standardized way to handle errors and compensations, making it easier to debug and maintain.	|Limited support: Not all frameworks or platforms support SAGA out of the box, which can make implementation more difficult. |
| Allows for asynchronous processing: SAGA can support asynchronous processing, allowing for greater concurrency and performance. |	Requires careful design: The SAGA pattern requires careful design to ensure that the compensations and rollbacks are implemented correctly and can handle all possible failure scenarios. |
| Supports distributed transactions: SAGA can handle transactions across multiple services or databases, allowing for more scalable and distributed architectures. | Increased latency: SAGA may result in additional latency due to the need to coordinate between different services or databases. |

## Sources

- <https://docs.aws.amazon.com/prescriptive-guidance/latest/modernization-data-persistence/saga-pattern.html>
- <https://microservices.io/patterns/data/saga.html>
- <https://medium.com/design-microservices-architecture-with-patterns/saga-pattern-for-microservices-distributed-transactions-7e95d0613345>
- <https://www.geeksforgeeks.org/saga-design-pattern/>