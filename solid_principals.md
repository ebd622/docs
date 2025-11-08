# SOLID principals
The SOLID principles (generl in OOP) are a set of five design principles intended to make software designs more understandable, flexible, and maintainable. Here's a breakdown of each principle:
## S — Single Responsibility Principle (SRP)
A class should have only one reason to change, meaning it should have only one job or responsibility.

✅ Good: A class that handles only user authentication.
❌ Bad: A class that handles authentication, logging, and database access.

This makes code easier to test and maintain.

## O — Open/Closed Principle (OCP)
Software entities (classes, modules, functions) should be open for extension but closed for modification.

* ✅ Good: You can add new behavior by extending a class or implementing an interface.
* ❌ Bad: You have to modify existing code to add new behavior.

This encourages the use of inheritance and polymorphism.
