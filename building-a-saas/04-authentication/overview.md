---
title: Overview
order: 1
---

# Chapter 4: Authentication

Security is non-negotiable. We'll implement robust authentication that's also user-friendly.

## What We'll Cover

- ASP.NET Core Identity setup
- JWT token authentication
- Refresh token flow
- Password policies and hashing
- Email verification
- Password reset
- (Optional) MFA

## Authentication Flow

<!-- TODO: Registration, login, token refresh -->

## ASP.NET Identity Setup

<!-- TODO: Configuration, custom user class -->

## JWT Implementation

<!-- TODO: Token generation, validation, claims -->

## Key strength

- TODO: Generate the signing key as long random material and store it with the other secrets.
- TODO: Rotate it on a plan, and accept the previous key until the longest access token has expired.

## Readable payload

- TODO: The access token carries the user id, the tenant id, and the permissions.
- TODO: Assume the holder of the token, and any proxy along the way, can read those claims.

## Immediate revocation

- TODO: Logout revokes the refresh token and clears the cookie.
- TODO: The access token stays valid until it expires. Keep that lifetime short, and check a denylist when a token has to die early.

### A token version per user

- TODO: Keep a version number on the user row and put it in the access token.
- TODO: Removing a user from a tenant or changing their role raises it, so the old token stops working before it expires. See [A version number per user](/csharp/aspnet-core/authentication/jwt#a-version-number-per-user).

## Refresh Tokens

<!-- TODO: Why, implementation, rotation -->

## Security Considerations

<!-- TODO: Password hashing, token storage, HTTPS -->

## Passkeys and machine-to-machine authentication

<!-- TODO: Passkeys, device-bound sessions, and service-to-service calls -->

## Token expiry and the clock

<!-- TODO: Expiry that tests can control -->

## Permission-based authorization

<!-- TODO: Named permissions on the caller, enforced with a policy -->

## Reviewing authorization changes

- TODO: A change to who can do what gets a second reviewer, even when the diff is small. See [Changes that need a second reviewer](/sdlc/code-review#changes-that-need-a-second-reviewer).

## Moving tenants to a new identity provider

- TODO: Accept a token from the current provider and from the new one until every tenant has moved.
- TODO: Record which provider a tenant uses, and send that tenant to the new provider on its turn.
- TODO: Remove the old scheme after the last tenant has signed in with the new one.

## Related Topics

- See [ASP.NET Core: Authentication](/csharp/aspnet-core/authentication/overview)
- See [JWT bearer](/csharp/aspnet-core/authentication/jwt)
- See [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)
- See [Modern authentication](/csharp/aspnet-core/authentication/modern-auth)
- See [Permission-based authorization](/csharp/aspnet-core/authorization/permissions)

---

**Next:** [Chapter 5: Multi-Tenancy](/building-a-saas/05-multi-tenancy/overview)
