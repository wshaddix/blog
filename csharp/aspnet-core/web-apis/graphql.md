---
title: GraphQL
order: 102
---

# GraphQL

An API where the caller names the fields it wants, and the server resolves each one.

## When the client shapes the query

Letting the caller pick fields removes a one-off endpoint, and it also hides how expensive the query is.

- TODO: Say when one screen's mix of fields is a better fit than a separate endpoint for that screen.
- TODO: Say when that freedom makes the contract harder to version and the cost harder to see.

## Nested queries and N+1

A field that loads its own children can issue one lookup for every parent row.

- TODO: Show a nested selection whose query count follows the length of the list.
- TODO: Explain why that count is a property of the resolvers, separate from how small the schema looks.

## Batching lookups

A data loader gathers the keys requested in one pass and loads them in a single round trip.

- TODO: Describe a loader that collects ids from sibling fields and fetches them together.
- TODO: Keep that batch inside one request. A loader that lives longer can mix two callers' keys.

## Depth, complexity, and cost

A query can be turned away before any resolver runs when it is too deep, too wide, or too expensive.

- TODO: Set a maximum depth, a complexity score, and a cost budget on the query.
- TODO: Reject a query that crosses a limit, and return an error that names which limit it was.

## Caching and authorization per field

A field can have its own cache entry and its own rule for who may see it.

- TODO: Cache a field from the arguments that change its result, and skip the cache when this caller must not see the value.
- TODO: Authorize the field itself. A check on the outer query is not a check on every field inside it.

## Beside REST and gRPC

A resource endpoint, a client-shaped query, and a contract-first call serve different callers in the same .NET service.

- TODO: Compare the three on contract stability, on how a client asks for less data, and on the hosting each one needs.
- TODO: This product's choice is recorded in [Why not GraphQL](/building-a-saas/06-api-development/overview#why-not-graphql).

## Related Topics

- See [gRPC](/csharp/aspnet-core/web-apis/grpc)
- See [Minimal APIs and controllers](/csharp/aspnet-core/web-apis/minimal-apis-and-controllers)
- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview)

---

**Next:** [gRPC](/csharp/aspnet-core/web-apis/grpc)
