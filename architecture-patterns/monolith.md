# Monolithic Architecture

## Definition
A monolithic architecture is a traditional model of a software program, which is built as a unified unit that is self-contained and independent from other applications.

## Notes
- Monolith means composed all in one piece. The Monolithic application describes a single-tiered software application in which different components combined into a single program from a single platform. Components can be:
  - Authorization — responsible for authorizing a user
  - Presentation — responsible for handling HTTP requests and responding with either HTML or JSON/XML (for web services APIs).
  - Business logic — the application’s business logic.
  - Database layer — data access objects responsible for accessing the database.
  - Application integration — integration with other services (e.g. via messaging or REST API). Or integration with any other Data sources.
  - Notification module — responsible for sending email notifications whenever needed.

## Advantages vs Disadvantages
| Advantages | Disadvantages |
| ---------- | ------------- |
| Simplicity of development | Slow speed of development |
| Simplicity of debugging | High code coupling |
| Simplicity of testing | Code ownership cannot be used |
| Simplicity of deployment | Testing becomes harder |
| Simplicity of application evolution | Performance issues |
| Cross-cutting concerns and customizations are used only once | The cost of infrastructure |
| Simplicity in onboarding new team members | Legacy technologies |
| Low cost on early stages of the application | Lack of flexibility |
| | Problems with deployment |

## Sources
- https://www.atlassian.com/microservices/microservices-architecture/microservices-vs-monolith#:~:text=A%20monolithic%20architecture%20is%20a,monolith%20architecture%20for%20software%20design.
- https://datamify.com/architecture/how-to-understand-monolithic-architecture/
- https://medium.com/koderlabs/introduction-to-monolithic-architecture-and-microservices-architecture-b211a5955c63