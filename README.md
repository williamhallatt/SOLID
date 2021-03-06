# An Introduction to S.O.L.I.D.

## Firstly, What is S.O.L.I.D.?

SOLID is an acronym for the 5 principles of Object Orientated Design, created by Robert Martin (Uncle Bob). It stands for:

* Single Responsibility Principle
* Open-Closed Principle
* Liskov Substitution Principle
* Interface Segregation Principle
* Dependancy Inversion Principle

## Why Follow These Principles?

As a software developer, your goal should be to create code that is loosely coupled, highly cohesive, strongly encapsulated, reusable and easy to maintain. Following the SOLID principles helps you reach these goals.

> In essence, high cohesion means keeping parts of a code base that are related to each other in a single place. Low coupling, at the same time, is about separating unrelated parts of the code base as much as possible.

-- *Vladimir Khorikov* ([Cohesion and Coupling: the difference](http://enterprisecraftsmanship.com/2015/09/02/cohesion-coupling-difference/))

## Single Responsibility Principle

> A class should have one and only one reason to change, meaning that a class should have only one responsibility.

When a class has multiple responsibilities, the likelihood that it will need to be changed increases. Each time a class is modified the risk of introducing bugs grows. By concentrating on a single responsibility, this risk is limited.

[View SRP code problem](1_SRP_code_problem.md)

## Open-closed Principle

> Objects or entities should be open for extension, but closed for modification.

The "closed" part of the rule states that once a module has been developed and tested, the code should only be adjusted to correct bugs. 

The "open" part says that you should be able to extend existing code in order to introduce new functionality.

[View OCP code problem](2_OCP_code_problem.md)

## Liskov Substitution Principle

> Code that uses a base class must be able to substitute a subclass without knowing it.

The principle is named after Barbara Liskov, and originally stated "Let q(x) be a property provable about objects of x of type T. Then q(y) should be provable for objects y of type S where S is a subtype of T".

If you create a class with a dependency of a given type, you should be able to provide an object of that type or any of its subclasses **without introducing unexpected results** and **without the dependent class knowing the actual type** of the provided dependency. 

If the type of the dependency must be checked so that behaviour can be modified according to type, or if subtypes generated unexpected rules or side effects, the code may become more complex, rigid and fragile.

[View LSP code problem](3_LSP_code_problem.md)

## Interface Segregation Principle

> A client should never be forced to implement an interface that it doesn’t use or clients shouldn’t be forced to depend on methods they do not use.

Often when you create a class with a large number of methods and properties, the class is used by other types that only require access to one or two members. The classes are more tightly coupled as the number of members they are aware of grows. When you follow the ISP, large classes implement multiple smaller interfaces that group functions according to their usage.

[View ISP code problem](4_ISP_code_problem.md)

## Dependancy Inversion Principle

> Entities must depend on abstractions not on concretions. It states that the high level module must not depend on the low level module, but they should depend on abstractions.

The DIP primarily relates to the concept of layering within applications, where lower level modules deal with very detailed functions and higher level modules use lower level classes to achieve larger tasks. 

The principle specifies that where dependencies exist between classes, they should be defined using abstractions, such as interfaces, rather than by referencing classes directly. This reduces fragility caused by changes in low level modules introducing bugs in the higher layers. The DIP is often met with the use of dependency injection.

[View DIP code problem](5_DIP_code_problem.md)

## References and Further Reading

- [Cohesion and Coupling: the difference](http://enterprisecraftsmanship.com/2015/09/02/cohesion-coupling-difference/)

- [S.O.L.I.D. Software Development, One Step at a Time](http://www.codemag.com/article/1001061)

- [The SOLID Principles](http://www.blackwasp.co.uk/SOLID.aspx)
