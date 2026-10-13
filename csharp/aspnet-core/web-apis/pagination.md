# Pagination, Filtering, and Sorting

List endpoints return a page, not a table.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Page shape

Offset or a continuation token, plus a total when it is cheap.

## Filtering

A fixed set of query fields. Not a query language from the client.

## Sorting

An allow-list of fields.

## Stability

A sort that does not skip or repeat rows when data changes underneath.

## Entity Framework

The query stays `IQueryable` until the page is applied.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Querying](/csharp/entity-framework/querying)

---

**Next:** [Background Services](/csharp/aspnet-core/web-apis/background-services)
