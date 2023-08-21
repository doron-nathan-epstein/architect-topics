# Event Queue vs Message Queue

![Event Queue vs Message Queue](https://eda-visuals.boyney.io/images/message-queue-vs-event-broker.png)

## Event vs Message

| Event | Message |
|-------|---------|
| Has no recipient, is just put in some place (where others can listen and maybe react to it) | Has a clear, addressable recipient |
| Is a pure statement that something happened, with no intention of notifying anyone. The producer doesn't care who listens to those events and he doesn't need to know. ("xyz happened.") | Is usually sent with the intention to let the recipient know or make him do something ("Do xyz!") |
| Is always asynchronous | Can be synchronous or asynchronous |

## Event Queue

An event queue is a data structure used in computer programming to manage and process events in an asynchronous, non-blocking way. It is typically used in event-driven programming, where an application responds to user input or system events by executing a sequence of code known as an event handler.

## Message Queue

A message queue is a form of asynchronous service-to-service communication used in serverless and microservices architectures. Messages are stored on the queue until they are processed and deleted. Each message is processed only once, by a single consumer. Message queues can be used to decouple heavyweight processing, to buffer or batch work, and to smooth spiky workloads.

## What's the difference between message queues and event queues?

- If the elements in your queue have a clear recipient -> `it's a message queue`
- If the elements in your queue are sent with the intention to make that recipient do something -> `it's a message queue`
- Else -> `it's an event queue`

## Sources

- <https://redis.com/glossary/event-queue>
- <https://aws.amazon.com/message-queue>
- <https://stackoverflow.com/questions/22713303/difference-between-event-queue-and-message-queue>
