# Domain Driven Design

## Origins

- Invented before Agile and Microservices
- See [Domain Driven Design Distilled](https://www.amazon.com/Domain-Driven-Design-Distilled-Vaughn-Vernon/dp/0134434420) by Vaughn Vernon
- Also see [Domain-Driven Design: Tackling Complexity in the Heart of Software](https://www.amazon.com/Domain-Driven-Design-Tackling-Complexity-Software/dp/0321125215) written by Eric Evans in 2003 on the subject

## Philosophy

- Four parts
    - Collaborative
    - Models environment in 1:1 fashion, to be flexible to domain change
    - Incremental - small changes with learning
    - Domain influences the system, which in turn influences the Domain
- Inspect and adapt

## Approach

- Use microservices to implement DDD
- Microservices should be no bigger than what You can hold in your head.
- Modeled around business concepts
- Independent deployability
- Services are decentralized

## Concepts

- Bounded context - naturally occuring in boundaries of business
    - What are the responsibilities of people working in that context?
- Model the proper communication boundaries between contexts
- Entity does one thing in a specfic context
- An aggregate is a collection of entities spoken to in a single portal
- Ubiquitious language is a shared language in a context
- The language of one context can be different from another
    - The language uses nouns and verbs
    - Language is used in the code
- Actors (people) and Roles (tasks) are used in the context
- Entities are named after roles, not actors
- Every entity in DDD should be associated with only one context'
- Everything stays context specific
- An event happens at the business level that people care about
    - Past tense
    - Has already occured
- Events cause actions to happen
- Policy determines how the event plays out - it is a business rule

# Execution

- Orchestration - one entity tells what the other to do
    - Declarative systems have a tight coupling to the data they use
    - A difficult problem to solve when microservices fail at communicating
- Choreography - reactive systems
    - Reactive systems solves the tght coupling of the events
    - Resolves coupling between upstream and downstream systems
    - Pub/sub model - subscribers are unknown to the publishers
    - Typically uses a messaging system like Kafka/RabbitMQ/ZeroMQ
- [Event Storming](https://en.wikipedia.org/wiki/Event_storming) is used to design new systems
    - Collaborate with technical and business
    - Stories are important
    - Maps events through a system over time
    - Uses many different sticky notes to model actions, events, policies, human activities
    - Includes red stickies that highlight questions about the system
    - Stack events vertically denotes parallel tasks

## Event Storming Seqeunce

- Start with events first, place as many on the board first
    - Example: Cart Purchased
- Then the activity flow: create the human activities and external activities
    - Example: Request Payment
- Then fill in the entities, or how is doing the work
    - Example: Sales Clerk
- Then on each entity sticky, place the context that entity or aggregate works on
    - Example: Order Processing
- Then draw out the *context map*, that hghlights the relations between the entities/contexts
    - Example: Store -> Finance -> Order Processing are bounded contexts
    - Creates the big picture and illustrates the bounded contexts
- Finally create a *entity map* that hoghlights the CRC cards (Classes, Responsibility, Collaborators)
    - Highlights relationships
    - Example: Sales Clerk CRC card
