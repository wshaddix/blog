---
title: Resource-Based Authorization
order: 10
---

# Resource-Based Authorization

The question is not only whether the caller is an editor. It is whether they may edit this row.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The resource

The entity, or the tenant it belongs to.

## Requirements and handlers

A requirement, a handler, and the resource passed in.

## Tenancy

A caller with a valid token for tenant A reading tenant B's id.

## Where it runs

After the entity is loaded, before it is changed.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Building a SaaS: Multi-Tenancy](/building-a-saas/05-multi-tenancy/overview)

---

**Next:** [Authorization](/csharp/aspnet-core/authorization/overview)
