# Raw SQL

LINQ is the default. SQL is for a query LINQ cannot express, or a procedure the database already owns.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## FromSql and ExecuteSql

A query that still tracks, and a command that does not.

## Parameters

Always a parameter. Never a concatenated value.

## Stored procedures

When the procedure is the contract.

## Interceptors

Logging SQL, and setting session state, without editing every query.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Querying](/csharp/entity-framework/querying)

---

**Next:** [Testing Entity Framework](/csharp/entity-framework/testing)
