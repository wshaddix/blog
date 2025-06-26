---
order: 1005
---

The "Gang of Four" design patterns, from the book *Design Patterns: Elements of Reusable Object-Oriented Software* by Erich Gamma, Richard Helm, Ralph Johnson, and John Vlissides, are 23 classic software design patterns. They are categorized into three groups: Creational, Structural, and Behavioral. Below is a bullet list with each pattern's category, name, and a brief description of its purpose.

### Creational Patterns
- **[Abstract Factory](/patterns/coding-patterns/creational-patterns/abstract-factory-pattern.md)**: Provides an interface for creating families of related or dependent objects without specifying their concrete classes.
- **[Builder](/patterns/coding-patterns/creational-patterns/builder-pattern.md)**: Separates the construction of a complex object from its representation, allowing the same construction process to create different representations.
- **[Factory Method](/patterns/coding-patterns/creational-patterns/factory-method-pattern.md)**: Defines an interface for creating an object, but lets subclasses decide which class to instantiate.
- **[Prototype](/patterns/coding-patterns/creational-patterns/prototype-pattern.md)**: Creates new objects by copying an existing object, known as the prototype, to avoid the overhead of initializing from scratch.
- **[Singleton](/patterns/coding-patterns/creational-patterns/singleton-pattern.md)**: Ensures a class has only one instance and provides a global point of access to it.

### Structural Patterns
- **Adapter**: Converts the interface of a class into another interface that a client expects, enabling incompatible classes to work together.
- **Bridge**: Decouples an abstraction from its implementation so that the two can vary independently.
- **Composite**: Composes objects into tree structures to represent part-whole hierarchies, allowing clients to treat individual objects and compositions uniformly.
- **Decorator**: Dynamically adds responsibilities to objects in a flexible and reusable way without modifying their code.
- **Facade**: Provides a simplified interface to a complex subsystem, making it easier to use.
- **Flyweight**: Shares fine-grained objects to reduce memory usage and improve performance when dealing with large numbers of similar objects.
- **Proxy**: Controls access to an object by acting as a surrogate or placeholder, often to add functionality like lazy loading or access control.

### Behavioral Patterns
- **Chain of Responsibility**: Passes a request along a chain of handlers, allowing each handler to process it or pass it to the next handler.
- **Command**: Encapsulates a request as an object, allowing parameterization of clients with queues, logs, or undoable operations.
- **Interpreter**: Defines a representation for a language's grammar and an interpreter to process expressions in that language.
- **Iterator**: Provides a way to access elements of a collection sequentially without exposing its underlying representation.
- **Mediator**: Defines an object that encapsulates how a set of objects interact, promoting loose coupling by preventing direct references.
- **Memento**: Captures and externalizes an object's internal state so that it can be restored later without violating encapsulation.
- **Observer**: Defines a one-to-many dependency where objects are notified and updated automatically when one object changes state.
- **State**: Allows an object to change its behavior when its internal state changes, appearing as if it changes its class.
- **Strategy**: Defines a family of algorithms, encapsulates each one, and makes them interchangeable, letting the client choose the algorithm at runtime.
- **Template Method**: Defines the skeleton of an algorithm in a method, deferring some steps to subclasses to customize behavior.
- **Visitor**: Separates an algorithm from an object structure by moving the operations to a visitor object, allowing new operations without modifying the structure.

