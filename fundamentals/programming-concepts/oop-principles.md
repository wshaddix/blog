---
title: OOP Principles
order: 1
---

# Object-Oriented Programming Principles

Object-oriented programming (OOP) organizes code around objects that contain data and behavior. These principles help you write maintainable, flexible code.

## The Four Pillars of OOP

### 1. Encapsulation

**What:** Bundling data and methods that operate on that data, hiding internal details.

**Why:** Protects internal state, reduces coupling, enables change without breaking clients.

**How:**
- Make fields private
- Expose behavior through public methods
- Use properties for controlled access

### 2. Abstraction

**What:** Exposing only essential features while hiding implementation details.

**Why:** Simplifies complexity, defines clear contracts, enables interchangeable implementations.

**How:**
- Define interfaces for contracts
- Use abstract classes for partial implementations
- Hide "how" behind "what"

### 3. Inheritance

**What:** Creating new classes based on existing ones, inheriting their properties and methods.

**Why:** Code reuse, establishing hierarchies, polymorphic behavior.

**How:**
- Use sparingly - prefer composition
- Follow Liskov Substitution Principle
- Keep inheritance hierarchies shallow

### 4. Polymorphism

**What:** Objects of different types responding to the same interface in different ways.

**Why:** Write generic code that works with multiple types, enable extensibility.

**How:**
- Override virtual methods
- Implement interfaces
- Use generics

## SOLID Principles

### S - Single Responsibility Principle (SRP)

> A class should have only one reason to change.

**Bad:** A `UserService` that handles authentication, database access, and email sending.

**Good:** Separate `AuthService`, `UserRepository`, and `EmailService`.

### O - Open/Closed Principle (OCP)

> Software entities should be open for extension, closed for modification.

**Bad:** Adding new behavior by modifying existing code with if/switch statements.

**Good:** Adding new behavior by creating new classes that implement existing interfaces.

### L - Liskov Substitution Principle (LSP)

> Subtypes must be substitutable for their base types.

**Bad:** A `Square` class extending `Rectangle` that breaks when you set width/height independently.

**Good:** Design inheritance hierarchies where subclasses truly are specialized versions of the parent.

### I - Interface Segregation Principle (ISP)

> Clients should not be forced to depend on interfaces they don't use.

**Bad:** One `IRepository` with 50 methods, forcing simple implementations to throw `NotImplementedException`.

**Good:** Small, focused interfaces like `IReadRepository`, `IWriteRepository`.

### D - Dependency Inversion Principle (DIP)

> High-level modules should not depend on low-level modules. Both should depend on abstractions.

**Bad:** `OrderService` directly instantiates `SqlOrderRepository`.

**Good:** `OrderService` depends on `IOrderRepository`, injected via constructor.

## Other Important Principles

### DRY - Don't Repeat Yourself

Duplication leads to inconsistency. Extract common code into reusable units.

*But:* Don't over-abstract - some duplication is okay if the code serves different purposes.

### KISS - Keep It Simple, Stupid

The simplest solution that works is usually the best. Complexity should be justified.

### YAGNI - You Aren't Gonna Need It

Don't build features or abstractions until you actually need them.

### Composition Over Inheritance

Prefer combining simple objects over complex inheritance hierarchies.

**Why:**
- Inheritance is static; composition is dynamic
- Inheritance creates tight coupling
- Multiple inheritance is problematic

## When Principles Conflict

Principles are guidelines, not laws. They sometimes conflict:

- **DRY vs YAGNI**: Don't create abstractions prematurely just to avoid duplication
- **SRP vs KISS**: Too many tiny classes can add complexity
- **OCP vs YAGNI**: Don't add extension points until you need them

Use judgment. The goal is maintainable code, not principle compliance.

## Practical Examples in C#

- See [Classes and Objects](/csharp/language-basics/classes) for OOP in C#
- See [ASP.NET Core](/csharp/aspnet-core/web-apis/overview) for Dependency Injection in practice
- See [Design Patterns](/patterns/coding-patterns/overview) for OOP patterns

## Practice Exercises

<!-- TODO: Add exercises -->

---

**Next:** [Functional Concepts](/fundamentals/programming-concepts/functional-concepts) - A different paradigm
