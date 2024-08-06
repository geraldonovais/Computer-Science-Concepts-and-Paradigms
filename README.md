# Computer Science: Concepts and Paradigms
Concepts, Paradigms and Design Patterns in Computer Science to develop higher quality code

# The four pillars of Object Oriented Programming

## Abstraction

Abstraction involves hiding complex implementation details and showing only the essential features of an object. It allows you to focus on interactions at a higher level, without needing to understand the intricate details of how something works.

**Benefits**: 
* It simplifies the interaction with objects by providing a clear, **_simplified interface_** and reducing the complexity of the code.
* It helps in managing and working with complex systems by breaking them down into more manageable parts.

## Encapsulation

Encapsulation is the principle of bundling the data (attributes) and the methods (functions) that operate on the data into a single unit or class. It also involves restricting direct access to some of the object's components, which can help prevent unintended interference and misuse.

**Benefits**: 
* It promotes **_modularity and separation of concerns_**, making code easier to manage, understand, and maintain.
* It hides the internal state of an object and only exposes a controlled interface for interaction.

## Inheritance

Inheritance is a mechanism where a new class (child or subclass) inherits attributes and methods from an existing class (parent or superclass). This allows the child class to reuse code from the parent class and extend or override functionality as needed.

**Benefits**: 
* Inheritance promotes **_code reuse_**, making it easier to create and maintain complex systems.
* It also helps establish a natural hierarchy and relationship between classes, making it easier to model real-world scenarios.

## Polymorphism

Polymorphism allows objects of different classes to be treated as objects of a common superclass. It enables a single function or method to work in different ways depending on the object or data it is operating on. There are two main types: method overriding (runtime polymorphism) and method overloading (compile-time polymorphism).

**Benefits**:
* **_Flexibility and extensibility_** by adding new classes without modifying existing code.
* Simplifies code by using a common interface for different data types.
* Improves code readability and maintainability.

**In Summary**

* **_Abstraction_** promotes a simple commom interface for a class of objects. 
* **_Encapsulation_** promotes modularity and separation of concerns.
* **_Inheritance_** makes code reuse easier
* **_Polymorphism_** promotes flexibility and extensibility.

# Relationship Between Abstraction and Coupling

## Abstraction
Abstraction in OOP refers to the concept of hiding the complex implementation details of an object and exposing only the essential features. It allows a programmer to interact with an object using a simplified interface without needing to understand its internal workings.

## Coupling
Coupling refers to the degree of dependence between different components or classes in a system. Low coupling means that classes or components are independent and changes in one have minimal impact on others. High coupling means that classes or components are tightly dependent on each other.

## Reducing Coupling through Abstraction

* Encapsulation: Abstraction helps reduce coupling by encapsulating data and behavior within a class. When you use well-defined interfaces or abstract classes, the concrete implementation details are hidden, which minimizes the direct dependencies between classes. For example, if class A interacts with class B through an interface or an abstract class, A does not need to know the specifics of B’s implementation.

* Interfaces and Abstract Classes: By programming to an interface rather than a concrete implementation, you reduce the dependency between components. This means that if class B changes, class A might not need to be modified as long as B still adheres to the same interface.

## Maintaining Abstraction and Low Coupling

* Modularity: Abstraction supports modular design by allowing different parts of a system to be developed, tested, and maintained independently. When classes are designed with high levels of abstraction, their interactions are managed through well-defined interfaces, reducing the risk of changes in one module affecting others.

* Flexibility and Extensibility: High levels of abstraction contribute to flexibility and ease of extension. Since abstract classes or interfaces define expected behaviors without dictating specific implementations, new implementations can be added with minimal changes to the existing codebase.

> In summary, abstraction and coupling are closely related in OOP. Proper use of abstraction can significantly reduce coupling, leading to more modular, flexible, and maintainable code. 

# Dependecy Injection

Dependency injection is a programming technique to manage dependencies between classes or components. It involves providing an object with its dependencies, rather than the object creating them itself. This pattern promotes loose coupling and enhances the testability, maintainability, and flexibility of code. Dependency injection makes implicit dependencies explicit and helps solve the following problems:

* How can a class be independent from the creation of the objects it depends on?
* How can an application, and the objects it uses support different configurations?

## How Dependency Injection Works

**Dependencies**: These are the objects or services that a class needs to perform its functions. For example, a class that manages user authentication might need a database connection as a dependency.

**Injection**: Instead of a class instantiating its dependencies directly, they are "injected" into the class from the outside, typically through constructors, setters, or interfaces.

## Types of Dependency Injection

**1. Constructor Injection:**

Dependencies are provided through the class's constructor.  

<details>
    
<summary>Example in PHP:</summary>

```php
class Database {
    // Database connection logic
}

class UserService {
    private $database;

    public function __construct(Database $database) {
        $this->database = $database;
    }

    // Methods that use the database dependency
}

// Usage
$database = new Database();
$userService = new UserService($database);
```
</details>

**2. Setter Injection:**

Dependencies are provided through setter methods.  
Example in PHP:

<details>
    
<summary>Example in PHP:</summary>

```php
class Database {
    // Database connection logic
}

class UserService {
    private $database;

    public function setDatabase(Database $database) {
        $this->database = $database;
    }

    // Methods that use the database dependency
}

// Usage
$database = new Database();
$userService = new UserService();
$userService->setDatabase($database);
```
</details>
    
## Benefits of Dependency Injection

* Loose Coupling: Classes are not tightly bound to their dependencies, making them easier to change or replace.
* Improved Testability: Dependencies can be easily mocked or stubbed during unit testing.
* Flexibility: Makes it easier to swap out implementations of dependencies without modifying the dependent class.
* Maintainability: Code is more modular and easier to maintain or extend over time.
    
# Solid Principles

## Single Responsibility

## Liskov Substitution

This priciple stands that If S is a subtype of T, then objects of type T in a program may be replaced with objects of type S without altering any of the desirable properties of that program.

In practical software development it defines that objects of a superclass could be replaceable with objects of its subclasses without breaking the application.
