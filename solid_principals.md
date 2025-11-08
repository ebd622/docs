# SOLID principals
The SOLID principles (generl in OOP) are a set of five design principles intended to make software designs more understandable, flexible, and maintainable. Here's a breakdown of each principle:
## S — Single Responsibility Principle (SRP)
A class should have only one reason to change, meaning it should have only one job or responsibility.

* ✅ Good: A class that handles only user authentication.
* ❌ Bad: A class that handles authentication, logging, and database access.

This makes code easier to test and maintain.

## O — Open/Closed Principle (OCP)
Software entities (classes, modules, functions) should be open for extension but closed for modification.

* ✅ Good: You can add new behavior by extending a class or implementing an interface.
* ❌ Bad: You have to modify existing code to add new behavior.

This encourages the use of inheritance and polymorphism.

## L — Liskov Substitution Principle (LSP)
Objects of a superclass should be replaceable with objects of its subclasses without breaking the application.

* ✅ Good: A subclass correctly overrides methods and maintains expected behavior.
* ❌ Bad: A subclass changes behavior in a way that violates the expectations of the superclass.

This ensures correct inheritance.

## I — Interface Segregation Principle (ISP)
Clients should not be forced to depend on interfaces they do not use.

* ✅ Good: Many small, specific interfaces.
* ❌ Bad: One large interface with many unrelated methods.

This promotes clean and focused interfaces.

## D — Dependency Inversion Principle (DIP)
High-level modules should not depend on low-level modules. Both should depend on abstractions.

* ✅ Good: Use interfaces or abstract classes to decouple components.
* ❌ Bad: High-level logic directly depends on low-level implementation details.

This principle is key to dependency injection and inversion of control.
