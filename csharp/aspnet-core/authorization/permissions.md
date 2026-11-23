# Permission-Based Authorization

A permission names one action the caller may perform.

## Permissions and roles

## Where the permission lives

## A policy per permission

### Names

### Several permissions on one endpoint

## On the endpoint

## One row

## Cached decisions and revocation

- TODO: Decide how old an allow or a deny is allowed to be before it is wrong.
- TODO: Drop the cached decision on every instance when a permission changes, or read the store on each request when that lag is not acceptable.
- TODO: Work that runs after the request has ended is [Acting on a user's behalf later](/csharp/aspnet-core/web-apis/background-services#acting-on-a-users-behalf-later). The product side is [Cached authorization decisions](/building-a-saas/04-authentication/overview#cached-authorization-decisions).

## Practical Examples

- See [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview) - Permission checks beside sign-in

## Related Topics

- See [Authorization](/csharp/aspnet-core/authorization/overview)
- See [Resource-based authorization](/csharp/aspnet-core/authorization/resource-based)
- See [Authentication and authorization](/fundamentals/security/authentication-and-authorization)

---

**Next:** [Resource-Based Authorization](/csharp/aspnet-core/authorization/resource-based)
