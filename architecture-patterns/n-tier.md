# N-Tier Architecture

## Definition
N-tier architecture is also called multi-tier architecture because the software is engineered to have the processing, data management, and presentation functions physically and logically separated.  That means that these different functions are hosted on several machines or clusters, ensuring that services are provided without resources being shared and, as such, these services are delivered at top capacity.  The “N” in the name n-tier architecture refers to any number from 1.

## Notes
- Tiers are physically separated, running on separate machines. A tier can call to another tier directly, or use asynchronous messaging (message queue). Although each layer might be hosted in its own tier, that's not required. Several layers might be hosted on the same tier. Physically separating the tiers improves scalability and resiliency, but also adds latency from the additional network communication.

- A traditional three-tier application has a presentation tier, a middle tier, and a database tier. The middle tier is optional. More complex applications can have more than three tiers.

- An N-tier application can have a closed layer architecture or an open layer architecture:
  - In a closed layer architecture, a layer can only call the next layer immediately down.
  - In an open layer architecture, a layer can call any of the layers below it.

- A closed layer architecture limits the dependencies between layers. However, it might create unnecessary network traffic, if one layer simply passes requests along to the next layer.

- Common N-Tier Architectures:
  - 3-Tier architecture
    - Presentation layer - Handles user interactions with the application.
    - Business Logic layer - Accepts the data from the application layer, validates it as per business logic and passes it to the data layer.
    - Data Access layer - Receives the data from the business layer and performs the necessary operation on the database.
  - 2-Tier architecture
    - In this architecture, the presentation layer runs on the client and communicates with a data store. There is no business logic layer or immediate layer between client and server.
  - Single Tier or 1-Tier architecture
    - It is the simplest one as it is equivalent to running the application on a personal computer. All of the required components for an application to run are on a single application or server.

## Advantages vs Disadvantages
| Advantages | Disadvantages |
| ---------- | ------------- |
| Scalability | Increase in Effort |
| Data Integrity | Increase in Complexity |
| Reusability | Performance |
| Reduced Distribution | Cost |
| Improved Security |
| Improved Availability |

## Sources
- https://stackify.com/n-tier-architecture/
- https://learn.microsoft.com/en-us/azure/architecture/guide/architecture-styles/n-tier
- https://www.guru99.com/n-tier-architecture-system-concepts-tips.html
- https://dev.to/karanpratapsingh/system-design-n-tier-architecture-4j82