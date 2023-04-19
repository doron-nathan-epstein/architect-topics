# iDesign Methodology

## Definition
A system with no clear architecture is doomed to become a legacy system after enough changes in the requirements over time.

## Functional decomposition - wrong way
- A method of analysis that dissects a complex process in order to examine its individual elements. A function, in this context, is a task in a larger process whereby decomposition breaks down that process into smaller, easier to comprehend units.

### Advantages vs Disadvantages
| Advantages | Disadvantages |
| ---------- | ------------- |
| Simplifies complex systems | Time consumption |
| Promotes reusability in the systems | Limitation in flexibility |
| Enhancing communication between stakeholders | Risk of oversimplification |
| | Lack of integration |
| | Dependence on domain expertise |

## Volatility based decomposition - right way
- Identifies areas of potential change and encapsulates those into services or system building blocks. You then implement the required behavior as the interaction between the encapsulated areas of volatility.
- The motivation for volatility-based decomposition is simplicity itself: any change is encapsulated, containing the effect on the system.
- Should be used for applications that:
  - Has requirements that change often.
  - Will be maintained for many years even decades.
  - Where the system is dependent on 3rd parties or sub systems.
  - The development time is open ended.
  - Requires a level of security between the front end and the back end.
  - Requires the ability to isolate use cases.

### Advantages vs Disadvantages
| Advantages | Disadvantages |
| ---------- | ------------- |
| Encapsulates the use case. One use case will not affect another. No bugs due to someone working in another part of the system | The decomposition is not easy or quick |
| The design encapsulates change | Requires a skilled architect |
| Implementing variations of use cases / requirements are quick to do | Takes longer to implement |
| Each component can be isolated and tested | Development cost is high |
| Troubleshooting of performance issues are easy due to the components based design | Requires developers to follow a implementation pattern |
| Speed of delivery goes up as the system matures and more components are build that can be re-used | Slow to deliver any features in the beginning |
| Cloud cost can be managed as the only load baring components can be isolated and scaled | Requires service contracts to be documented. Documentation will not only need to cover the inputs and outputs but also the internal behavior of the services |
| Attempts to control the amount of traffic to and from the client | | 
| As the development order of components and the dependencies are known upfront it can be used for accurate project planning and costing | |
| Results in a very stable system | | 

## Sources
- https://medium.com/nmc-techblog/software-architecture-with-the-idesign-method-63716a8329ec
- https://www.investopedia.com/terms/f/functional-decomposition.asp#:~:text=our%20editorial%20policies-,What%20Is%20Functional%20Decomposition%3F,smaller%2C%20easier%20to%20comprehend%20units
- https://www.baeldung.com/cs/functional-decomposition
- http://www.waynecliffordbarker.co.za/2019/03/23/volatility-based-decomposition-for-microservices/