# Chapter 3 (Part 2)

## Modules

Modules are an important factor in domain driven design - creating Modules that are well designed and cohesive is a large step towards writing clear and maintainable code. The parts of a Module should attempt to follow the idea of *[functional cohesion][1]*. Ensure you are considering how tightly coupled the Modules are with themselves and the rest of the application. A low level of coupling is something to work towards; this can also make the move to microservies much easier at a later date if so desired. An important piece of advice the author recommends is to 

>the Modules names that become part of the Ubiquitous Language. Modules and their names should reflect insight into the domain.

For examples of tight versus loose coupling, think of the API of a bank. If the banks software is written for only one front end or client (in the programming sense, not the business sense), then we can consider the backend and frontend of that API *tightly coupled*. Now the bank has decided to let customers pull their own data about their accounts - this will require a redesign of the API of the backend in order to allow connections from different users, not just the single integrated front end. We can now say the system is *loosely coupled*. 

## Aggregates, Factories, and Repositories

The last three parts of Chapter 3 cover the life cycle of domain objects. Objects in your application will be created, used throughout the application, and then destroyed when they are no longer needed. These three concepts help to establish some of the aspects of that cycle. Aggregates are 

>a group of associated objects which are considered as one unit with regard to data changes.

Each Aggregate has exactly one root. The root of the Aggregate is an Entity; the Entity is the only publicly accessible object of the Aggreggate. Internal objects inside the Aggregate





[1]: <https://softwareengineering.stackexchange.com/questions/402593/concept-of-functional-cohesion> "Stack Exchange post about functional cohesion in software"