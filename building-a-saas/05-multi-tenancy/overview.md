---
title: Overview
order: 1
---

# Chapter 5: Multi-Tenancy

Multi-tenancy allows one application to serve many customers with isolated data.

## What We'll Cover

- Multi-tenancy strategies
- Tenant identification
- Data isolation with EF Core
- Tenant-specific configuration
- Cross-tenant operations (admin)

## Multi-Tenancy Strategies

| Strategy | Isolation | Complexity | Cost |
|----------|-----------|------------|------|
| Shared database, shared schema | Low | Low | Low |
| Shared database, separate schema | Medium | Medium | Medium |
| Separate database | High | High | High |

We'll use **shared database with row-level filtering** - good balance for most SaaS apps.

## Tenant Identification

<!-- TODO: Subdomain, header, claim-based -->

## Data Isolation

<!-- TODO: Global query filters, TenantId on entities -->

## EF Core Implementation

<!-- TODO: ITenantProvider, SaveChanges override -->

## Contextual options

<!-- TODO: Tenant settings through named options, selected for the current tenant -->

## The cross-tenant admin list

- TODO: An operator lists tenants across the product. The query is not limited to one tenant, and a tenant user does not get this page.
- TODO: Show one page of rows. The API returns the next page with a keyset cursor. See [Keyset pagination](/building-a-saas/06-api-development/overview#keyset-pagination).
- TODO: Render that page with the grid in [Data grids](/csharp/aspnet-core/blazor/data-grids).

## Related Topics

- See [Databases: Data Modeling](/databases/data-modeling/overview)
- See [Entity Framework: Querying](/csharp/entity-framework/querying)
- See [Configuration and options](/csharp/platform/configuration-and-options)
- See [Data grids](/csharp/aspnet-core/blazor/data-grids)

---

**Next:** [Chapter 6: API Development](/building-a-saas/06-api-development/overview)
