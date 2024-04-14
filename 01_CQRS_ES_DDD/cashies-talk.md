# Talk

### Patterns

- Command Query Request Segregation (CQRS)
- Event Sourcing (ES)
- Domain Driven Design (DDD)

--

### Command Query Request Segregation

Separate the read and write side of your application. Each side can now be optimize based on its unique characteristics. 

- Read side should never cause side effects or state changes
- Allows for different read side data models (UI, Search, Reporting)
- Allows for independent scale of read and writes
- Allows for different technology (write to SQL, read from DocumentDB)

--

### Command Query Request Segregation

Common Terms

- Command - instructions to change the system (have side effects)
- Query - requests to read from the system (have no side effects)

--

### Command Query Request Segregation

![Simplified CQRS diagram](./images/CQRS.svg)

--

### Event Sourcing

Represent your application state changes as a series of ordered events. Read the events to replay the state changes and produce the current application state.

- Allows replaying the events into different data models
- Naturally creates an audit trail (each event contains who/what/why)
- Allows point-in-time queries
- Debugging state changes is easier

--

### Event Sourcing

Common Terms

- Event - representation of a state change
- Event Stream - ordered list of events
- Projection - events replayed into a data model
- Temporal Query - replay events up to a point-in-time

--

### Event Sourcing

![Simplified ES diagram](./images/ES.svg)

--

### Domain Driven Design

Represent the core problem domain of your application as a well-defined and expressive domain model. Specific contexts within the domain are segregated to allow each to specialize.

- Requires common language between developers and business users
- Aimed at improving software quality by more closely aligning with the business
- Domain models encapsulate the data and behavior for a given context

--

### Domain Driven Design

Common Terms

- Bounded Context - logical boundaries between domain models
- Entity - data where the ID matters
- Value Object - data where the value matters
- Aggregate - collection of Entities and Value Objects
- Aggregate Root - the top node in an object tree; entry point
- Domain Event - meaningful business change in the system
- Repository - retrieve and store domain models
- Factories - control the creation of domain models
- Services - business logic that doesn't fit into any single Entity or Aggregate
- Ubiquitous Language - common language between developers and business users

--

### Domain Driven Design

![Simplified DDD Flow diagram](./images/DDD_Flow.svg)

--

### Domain Driven Design

![Simplified DDD Logical diagram](./images/DDD_Logical.svg)

--

### Domain Driven Design

![Simplified DDD Context diagram](./images/DDD_Contexts.svg)

--

### Mix and Match

Any combination of these patterns are possible.

--

### Mix and Match

<!-- CQRS + ES -->

--

### Mix and Match

<!-- CQRS + DDD -->

--

### Mix and Match

<!-- DDD + ES -->

--

### Mix and Match

<!-- CQRS + ES + DDD -->

--

### 

What other patterns do you want covered in the future?

--