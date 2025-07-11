# Glossary

- [Domain-Driven Design (DDD)](DomainDrivenDesign.md)




## Business domain
This the primary industry that your company/organization operates in.


## Project / Sub-domain / Bounded Context
[Bounded context - Martin Fowler](https://martinfowler.com/bliki/BoundedContext.html)

[DDD Bounded Contexts & Subdomains - video](https://www.youtube.com/watch?v=NvBsEnDgA4o)

A part of the software where particualr terms, rules and definitions apply consistantly.


## Actions / Commands / Events
[Events vs Commands: What's the difference? - video](https://www.youtube.com/watch?v=vS7sCJ1uezY)

### Command/Action
Represents decisions, actions or intent. They can be initiated by an actor or from an automated process. During process EventStorming usually, the word "Action" usually fits better with stakeholders than command because it is easier to grasp.


## Event sourcing
[Event Sourcing Explained - video](https://www.youtube.com/watch?v=yFjzGRb8NOk)


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


## Pull request
Is an amendment or addition you want to make in a document.


---
[Edit this page](https://github.com/saascade/platform.saascade.com/edit/main/Hub/Glossary/README.md)

[How to contribute to the docs](../../General/HowToContribute/README.md)



<!-- MS Clarity. We use this so that we know what people need help with, otherwise we'd be wasting a lot of time just guessing. --> 
<script type="text/javascript"> (function(c,l,a,r,i,t,y){ c[a]=c[a]||function(){(c[a].q=c[a].q||[]).push(arguments)}; t=l.createElement(r);t.async=1;t.src="https://www.clarity.ms/tag/"+i;  y=l.getElementsByTagName(r)[0];y.parentNode.insertBefore(t,y); })(window, document, "clarity", "script", "sdby7q18rz"); </script>
