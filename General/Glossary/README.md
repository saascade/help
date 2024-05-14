# Glossary

## Domain-Driven Design (DDD)
[Wikipedia](https://en.wikipedia.org/wiki/Domain-driven_design)

[DDD Building Blocks - video](https://www.youtube.com/watch?v=xFl-QQZJFTA)

[Domain Driven Design: What You Need To Know - video](https://www.youtube.com/watch?v=4rhzdZIDX_k)
 

To oversimplify things, Domain-Driven Design is the recommended approach for creating Enterprise-grade software applications.
This is because it allows the structure and lanaguage in the code to match what is actually used in the business - making it much easier to reason about complex (or even simple) software systems. It's about creating a language that is shared between domain/business experts and technical experts. We then use that shared language to model the business in a user-friendly, but technically complete way - reducing a lot of the risk, while also speeding up the software development.



When you are trying to build complex software it is extremely important that everyone is on the same page!
The software itself should represent the business and it should be clear from the code how the business functions. 
Software development is difficult enough without the business and engineering using different names for the same thing.

This is where Domain Driven Design (DDD) comes in, which was made popular by Eric Evans in his 2003 book Domain Driven Design: Tackling Complexity in the Heart of Software.


The SaaScade platform takes things further by providing tools to easily do the modelling, generate the code and manage the resulting software systems - effectively eliminating or reducing a lot of the risk and complexity of trying to do this manually.



## Business domain
This the primary industry that your company/organization operates in.


## Project / Sub-domain / Bounded Context
[Bounded context - Martin Fowler](https://martinfowler.com/bliki/BoundedContext.html)

[DDD Bounded Contexts & Subdomains - video](https://www.youtube.com/watch?v=NvBsEnDgA4o)

A part of the software where particualr terms, rules and definitions apply consistantly.


## Aggregate
An Aggregate is by far the hardest thing to explain in Domain-Driven Design (DDD), with the following statement being the original/official definition:
"An Aggregate is a cluster of associated objects that we treat as a unit for the purpose of data changes. 
Each Aggregate has a root and a boundary.
The boundary defines what is inside the aggregate.
The root is a single, specific Entity contained in the Aggregate." - Eric Eveans: Domain-Driven Design


In basic terms an agggregate is a unit of consistency and concurrency that carries some kind of identity and data.

When you model an Aggreagte using our workflow designer, what you see directly on the diagram is actually the root of the Aggregate, with it's accociated value objects hidden within.
To keep things simple you can kind of think of it in the same way as an Entity, in that it has it's own identity and associated data - and we'll take care of the rest for you.
So for example if you we're modelling a Bank, some of the Aggregate roots would be things like 'Customer' or 'Bank Account', with each instance of those having it's own identity (Aggregate ID) and data. In this case a Customer (as in a unique person) would perhaps have an Address, but we can decide to model the Address as just a value object / property of a Customer instead of a completely seperate Aggregate, because it doesn't really have any reason to change outside of the context of a specific customer and should probably be kept consistant with other changes to that specific customer.


## Policy
A policy is a reaction that says “whenever X happens, we do Y”, eventually ending up with in the flow between a Domain Event and a Command/action. A policy can be an automated process or manual. 


## Environment
A software development environment (SDE) is the collection of hardware and software tools a system developer uses to build software systems.

When you are developing software, you probably don’t want your users to see every messy part of your application creation process. In order to make sure you control what people see and when they have access to it, development teams use environments to create “stages” of the app which they consider good for releasing.

Each environment has its own unique purpose. There are different standards of environments which are used in the industry, although almost every process starts at the ‘development’ (or shortened to just 'dev') stage and ends with ‘production’. Different organisations all have their own purposes and policies which dictate when and how each environment is used.

## Commands / Action & Events
[Events vs Commands: What's the difference? - video](https://www.youtube.com/watch?v=vS7sCJ1uezY)

## Event sourcing
[Event Sourcing Explained - video](https://www.youtube.com/watch?v=yFjzGRb8NOk)


## Pull request
Is an amendment or addition you want to make in a document.


---
[Edit this page](https://github.com/saascade/platform.saascade.com/edit/main/General/Glossary/README.md)

[How to contribute to the docs](../HowToContribute/README.md)
