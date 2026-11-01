# Pagination, Filtering, and Sorting

List endpoints return a page, not a table.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Page shape

Offset or a continuation token, plus a total when it is cheap.

## Filtering

A fixed set of query fields. Not a query language from the client.

## Totals instead of rows

A client that walks every page to draw a count is asking for a summary.

- TODO: Spot the client that pages through the whole collection only to count rows or fill a chart.
- TODO: Offer a summary endpoint that takes a date range and a bucket size and returns the count in each bucket.
- TODO: Apply the filter before the grouping, so the database scans the requested range.
- TODO: Group with EF Core on a date part, and read the SQL that was generated for that query.
- TODO: Cache a bucket after it closes. The current bucket is the one that still changes.
- TODO: Cap the range and the number of buckets, and say in the response when the result was cut short. The per-tenant form of this endpoint is [Usage summaries](/building-a-saas/06-api-development/overview#usage-summaries).

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
