---
title: Data Grids
order: 45
---

# Data Grids

A grid shows one page of rows. The API chooses which page, and the component renders it.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The grid

- TODO: Use the built-in `QuickGrid` component. It renders columns and the items for the current page.
- TODO: The component does not own the query. The page loads a page of results and hands them to the grid.

## Columns

- TODO: A property column shows one field. A template column is for a link, a status, or any cell that is not a single field.
- TODO: Mark a column sortable only when the API can order by that field.

## Sorting and filtering

- TODO: A new sort or filter goes back to the API with the request, and the view returns to the first page.
- TODO: The allow-list of sort fields lives on the list endpoint, beside the other query fields.

## One page at a time

- TODO: Ask for the page the user is on, and pass the sort and the filter with that request. Do not load every row and then skip to the page in memory.
- TODO: When the list can grow, such as the tenants an operator reviews, continue with a keyset cursor. See [Keyset pagination](/building-a-saas/06-api-development/overview#keyset-pagination).

## Practical Examples

- See [Building a SaaS: Multi-Tenancy](/building-a-saas/05-multi-tenancy/overview#the-cross-tenant-admin-list) - The cross-tenant admin list

## Related Topics

- See [Components and routing](/csharp/aspnet-core/blazor/components-and-routing)
- See [Calling the API](/csharp/aspnet-core/blazor/calling-the-api)
- See [Pagination, filtering, and sorting](/csharp/aspnet-core/web-apis/pagination)
- See [Querying](/csharp/entity-framework/querying#offset-versus-keyset)

---

**Next:** [Forms and Validation](/csharp/aspnet-core/blazor/forms-and-validation)
