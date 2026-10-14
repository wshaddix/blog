---
title: Permission-Based Authorization
order: 30
---

# Permission-Based Authorization

A permission names one action the caller may perform.

## Permissions and roles

<!-- TODO: A permission names one action. A role groups the people who hold a set of permissions -->

## Where the permission lives

<!-- TODO: A claim on the principal, a row in the store, and how a request sees the current set -->

## A policy per permission

<!-- TODO: One requirement and handler that accept the permission name -->

### Names

<!-- TODO: A stable list owned by the API, such as invoices:read -->

### Several permissions on one endpoint

<!-- TODO: Require every permission in a set, or any permission in a set -->

## On the endpoint

<!-- TODO: Require the policy in endpoint metadata. The handler remains the place that enforces it -->

## One row

<!-- TODO: The permission allows the action. Resource-based authorization decides whether this entity is in scope -->

## Practical Examples

- See [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview) - Permission checks beside sign-in

## Related Topics

- See [Authorization](/csharp/aspnet-core/authorization/overview)
- See [Resource-based authorization](/csharp/aspnet-core/authorization/resource-based)
- See [Authentication and authorization](/fundamentals/security/authentication-and-authorization)

---

**Next:** [Resource-Based Authorization](/csharp/aspnet-core/authorization/resource-based)
