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

## Sources

- <https://aws.amazon.com/event-driven-architecture/#:~:text=What%20is%20an%20Event%2DDriven,modern%20applications%20built%20with%20microservices>.
- <https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/event-driven>
- <https://www.techtarget.com/searchapparchitecture/tip/Event-driven-architecture-pros-and-cons-Is-EDA-worth-it>
