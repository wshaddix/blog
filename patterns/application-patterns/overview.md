---
title: Overview
---


# Patterns from Martin Fowler's *Patterns of Enterprise Application Architecture*

Below is a bullet list of patterns from Martin Fowler's book *Patterns of Enterprise Application Architecture* (2002). Each pattern includes its name and a brief description of its purpose, based on the book's catalog of solutions for common enterprise application challenges.[](https://martinfowler.com/eaaCatalog/)

- **Active Record**: Encapsulates database access by integrating data and behavior into a single object, where each object corresponds to a database row, simplifying CRUD operations. 
- **Association Table Mapping**: Maps an association between two objects to a database table, enabling flexible relationships like many-to-many links in relational databases.
- **Class Table Inheritance**: Represents a class hierarchy in a database by creating a table for each class, with shared data in a parent table, supporting inheritance in object-oriented designs.
- **Coarse-Grained Lock**: Locks a group of related objects as a single unit to prevent concurrent modifications, simplifying concurrency control in complex data structures.
- **Concrete Table Inheritance**: Maps each class in a hierarchy to its own database table containing all fields, simplifying queries but potentially duplicating data.
- **Data Mapper**: Separates domain objects from database access logic by using a mapper class to handle data transfer, decoupling the object model from the database schema.
- **Data Transfer Object**: Packages data into a single object to reduce the number of method calls across system boundaries, improving performance in distributed systems.
- **Dependent Mapping**: Delegates the mapping of an object’s fields to another object (e.g., a parent object), reducing redundancy in mapping logic for related objects.
- **Domain Model**: Organizes business logic into a rich object model with behavior and data, enabling complex domain logic while keeping it independent of persistence.
- **Embedded Value**: Stores a small, dependent object’s data directly within its parent’s table, simplifying storage for simple value objects without needing separate tables.
- **Foreign Key Mapping**: Uses foreign keys in a database to represent relationships between objects, enabling navigation and maintaining referential integrity.
- **Front Controller**: Centralizes request handling through a single controller to manage web requests, ensuring consistent processing and reducing duplication in web applications.
- **Gateway**: Encapsulates access to an external system or resource (e.g., a database or service) through a simple interface, simplifying interaction and isolating external dependencies.
- **Identity Field**: Adds a unique field (e.g., a primary key) to an object to map it to a database record, ensuring consistent identification across layers.
- **Identity Map**: Maintains a cache of objects by their identity to ensure each database record is loaded only once, preventing duplicate objects and improving performance.
- **Implicit Lock**: Manages concurrency by automatically applying locks during transactions, simplifying locking logic for developers but potentially reducing flexibility.
- **Inheritance Mappers**: Uses separate mapper classes for each class in an inheritance hierarchy to handle persistence, supporting complex object hierarchies.
- **Layer Supertype**: Provides a common superclass for all objects in a layer to share common behavior, reducing duplication across similar objects in a layer.
- **Lazy Load**: Delays loading of an object’s data until it’s needed, improving performance by reducing unnecessary database queries.
- **Metadata Mapping**: Stores mapping information (e.g., between objects and database tables) in metadata, enabling flexible and configurable persistence logic.
- **Model View Controller**: Separates application concerns into models (data and logic), views (UI), and controllers (input handling), improving modularity and testability.
- **Money**: Represents monetary values with a specific currency and handles arithmetic and rounding, ensuring accurate financial calculations.
- **Optimistic Offline Lock**: Allows concurrent access to data by checking for conflicts only at commit time, improving performance in low-conflict scenarios.
- **Page Controller**: Handles web requests for a specific page or action with a dedicated controller, simplifying handling for straightforward web applications.
- **Plugin**: Enables dynamic loading of components or modules at runtime, improving extensibility and configurability of applications.
- **Query Object**: Encapsulates a database query as an object, allowing complex queries to be built and reused while keeping persistence logic separate.
- **Record Set**: Represents tabular data (e.g., query results) as an in-memory structure, providing a flexible way to manipulate data in applications.
- **Registry**: Provides a central point to access commonly used objects or services, simplifying access and reducing coupling across the system.
- **Remote Facade**: Exposes a coarse-grained interface to hide the complexity of a fine-grained object model, improving performance in distributed systems.
- **Repository**: Centralizes data access logic for a domain type, providing a collection-like interface to query and manage domain objects.
- **Row Data Gateway**: Represents a single database row as an object with fields and access methods, simplifying data access for simple applications.
- **Separated Interface**: Defines an interface in a separate package from its implementation to reduce coupling and allow multiple implementations.
- **Serialized LOB**: Stores a large object (LOB), like a complex object graph, as a serialized blob in a database, simplifying storage of complex data.
- **Service Layer**: Centralizes business logic into a distinct layer that coordinates operations across domain objects, improving maintainability and modularity.
- **Service Stub**: Replaces an external service with a simplified version for testing or development, isolating the system from external dependencies.
- **Session State**: Manages user session data (e.g., in web applications) to maintain state between requests, supporting user-specific interactions.
- **Single Table Inheritance**: Maps an entire class hierarchy to a single database table with all fields, simplifying database structure but potentially complicating queries.
- **Special Case**: Uses a specific object to handle edge cases (e.g., null or default behavior), reducing conditional logic in the codebase.
- **Table Data Gateway**: Provides a single object to handle all database operations for a table, simplifying data access for straightforward applications.
- **Table Module**: Organizes business logic around database tables, with one module per table, suitable for simpler applications with table-centric logic.
- **Template View**: Renders dynamic content by embedding logic in a presentation template, balancing simplicity and flexibility for web applications.
- **Transaction Script**: Organizes business logic as a single procedure or script for each use case, suitable for simple applications with minimal complexity.
- **Transform View**: Processes data into a specific format (e.g., HTML or XML) using a transformation pipeline, useful for rendering complex outputs.
- **Two-Step View**: Separates view rendering into two stages—logic to structure data and a template to format it—improving reusability in presentation logic.
- **Unit of Work**: Tracks changes to objects during a transaction and commits them to the database as a single unit, simplifying persistence and ensuring consistency.
- **Value Object**: Represents a small, immutable object with no identity (e.g., a date or money amount), simplifying data handling and ensuring consistency.
