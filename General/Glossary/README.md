# Glossary

## Business domain
This the primary industry that your company/organization operates in.


## Project / Bounded Context
...


## Aggregate
An Aggregate is by far the hardest thing to explain in Domain-Driven Design (DDD), with the following statement being the original/official definition:
"An Aggregate is a cluster of associated objects that we treat as a unit for the purpose of data changes. 
Each Aggregate has a root and a boundary.
The boundary defines what is inside the aggregate.
The root is a single, specific Entity contained in the Aggregate." - Eric Eveans: Domain-Driven Design


In basic terms an agggregate is a unit of consistency and concurrency that carries some kind of identity and data.
When you define an Aggreagte using our workflow designer, you are actually defining the root of the Aggregate.
To keep things simple you can kind of think of it in the same way as an Entity, in that it has it's own identity and associated data - and we'll take care of the rest for you.
So for example if you we're modelling a Bank, some of the Aggregate roots would be things like 'Customer' or 'Bank Account', with each instance of those having it's own identity and data. In this case a Customer would perhaps have an Address, but we can decide to model that as just a value object / property of a Customer instead of a completely seperate Aggregate, because it doesn't really have any reason to change outside of the context of a specific customer and should probably be kept consistant with other changes to a specific customer.

## Environment
...

## Pull request
Is an amendment or addition you want to make in a document.


---
[Edit this page](https://github.com/saascade/platform.saascade.com/edit/main/General/Glossary/README.md)

[How to contribute to the docs](../HowToContribute/README.md)
