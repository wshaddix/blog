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

## Related Topics

- See [Databases: Data Modeling](/databases/data-modeling/overview)
- See [Entity Framework: Querying](/csharp/entity-framework/querying)

---

**Next:** [Chapter 6: API Development](/building-a-saas/06-api-development/overview)
