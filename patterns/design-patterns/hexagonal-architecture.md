# Hexagonal Architecture

![Hexagonal Architecture](https://miro.medium.com/v2/resize:fit:720/format:webp/1*NfFzI7Z-E3ypn8ahESbDzw.png)

## Definition

Hexagonal architecture is an architectural pattern for building software systems that are testable, decoupled, flexible, and maintainable. Hexagonal architecture is a pattern that helps you shift the main focus to the business domain while spending less time on the technical aspects of it.

## Notes

- Hexagonal architecture is a general-purpose architectural style that aims to create decoupled software.
- This architectural style is also known as Ports and Adapters, and that’s because Ports and Adapters are the main properties of this pattern.
- The key idea is to separate core business logic from external concerns such as databases, web frameworks, message queues, and so on, in a way that the application itself is not dependent on any particular technology.
- The general rule of thumb is that nothing comes in, and nothing goes out without going through the ports.

## Advantages vs Disadvantages

| Advantages | Disadvantages |
| ---------- | ------------- |
| Testability | Debugging |
| Flexibility | Indirection |
| Technology Agnostic | Translaton |
| Deferring Decisions | Steep Learning Curve |
| Focus on the Business Domain | |

## Sources

- <https://cardoai.com/what-is-hexagonal-architecture-should-you-use-it/>
- <https://medium.com/ssense-tech/hexagonal-architecture-there-are-always-two-sides-to-every-story-bc0780ed7d9c>
- <https://netflixtechblog.com/ready-for-changes-with-hexagonal-architecture-b315ec967749>