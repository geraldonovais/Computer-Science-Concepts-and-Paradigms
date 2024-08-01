# Computer Science: Concepts and Paradigms
Concepts, Paradigms and Design Patterns in Computer Science to develop higher quality code

# The four pillars of Object Oriented Programming

## Abstraction

Abstraction involves hiding complex implementation details and showing only the essential features of an object. It allows you to focus on interactions at a higher level, without needing to understand the intricate details of how something works.

**Benefits**: 
* It simplifies the interaction with objects by providing a clear, _simplified interface_ and reducing the complexity of the code.
* It helps in managing and working with complex systems by breaking them down into more manageable parts.
## Encapsulation

Encapsulation is the principle of bundling the data (attributes) and the methods (functions) that operate on the data into a single unit or class. It also involves restricting direct access to some of the object's components, which can help prevent unintended interference and misuse.

**Benefits**: 
* It promotes _modularity and separation of concerns_, making code easier to manage, understand, and maintain.
* It hides the internal state of an object and only exposes a controlled interface for interaction.

## Inheritance

Inheritance is a mechanism where a new class (child or subclass) inherits attributes and methods from an existing class (parent or superclass). This allows the child class to reuse code from the parent class and extend or override functionality as needed.

**Benefits**: 
* Inheritance promotes code reuse, making it easier to create and maintain complex systems.
* It also helps establish a natural hierarchy and relationship between classes, making it easier to model real-world scenarios.

## Polymorphism

Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables a single function or method to work in different ways depending on the object or data it is operating on. There are two main types: method overriding (runtime polymorphism) and method overloading (compile-time polymorphism).

**Benefits**:
* Flexibility and extensibility by adding new classes without modifying existing code.
* Simplifies code by using a common interface for different data types.
* Improves code readability and maintainability.

# Solid Principles

## Single Responsibility

## Liskov Substitution

This priciple stands that If S is a subtype of T, then objects of type T in a program may be replaced with objects of type S without altering any of the desirable properties of that program.

In practical software development it defines that objects of a superclass could be replaceable with objects of its subclasses without breaking the application.
