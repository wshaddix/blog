---
title: Overview
order: 1
---

# Databases

Databases are the backbone of most applications. Understanding how to design, query, and optimize databases is essential for any software engineer.

## What's Covered

### Relational Databases

Traditional SQL databases with structured schemas:

- [SQL Fundamentals](/databases/relational/sql-fundamentals) - The language of relational databases
- [Database Design](/databases/relational/database-design) - Normalization, relationships, constraints
- [SQL Server](/databases/relational/sql-server/overview) - Microsoft's enterprise database

### NoSQL Databases

Alternative data models for specific use cases:

- [Document Databases](/databases/nosql/overview) - MongoDB, CosmosDB
- [Key-Value Stores](/databases/nosql/overview) - Redis, caching
- [When to Use NoSQL](/databases/nosql/overview) - Picking the right tool

### Data Modeling

Designing data structures that serve your application:

- [Entity Relationships](/databases/data-modeling/overview) - One-to-many, many-to-many
- [Normalization](/databases/data-modeling/overview) - Reducing redundancy
- [Denormalization](/databases/data-modeling/overview) - When to break the rules

## SQL vs NoSQL

| Aspect | SQL | NoSQL |
|--------|-----|-------|
| Schema | Fixed, defined upfront | Flexible, schema-on-read |
| Relationships | Strong, foreign keys | Weak or embedded |
| Transactions | ACID guaranteed | Varies (BASE often) |
| Scaling | Vertical primarily | Horizontal primarily |
| Query language | SQL (standardized) | Varies by database |
| Best for | Complex queries, transactions | High scale, flexible data |

## Learning Path

1. Start with [SQL Fundamentals](/databases/relational/sql-fundamentals) - essential for any engineer
2. Learn [Database Design](/databases/relational/database-design) - structure data correctly
3. Understand [Entity Framework](/csharp/entity-framework/getting-started) - ORM for C#
4. Apply in [Building a SaaS](/building-a-saas/07-data-layer/overview) - real-world implementation

---

*Start with [SQL Fundamentals](/databases/relational/sql-fundamentals) - you'll use SQL everywhere.*
