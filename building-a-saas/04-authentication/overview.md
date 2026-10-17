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

## ASP.NET Identity Setup

## JWT Implementation

## Key strength

- TODO: Generate the signing key as long random material and store it with the other secrets.
- TODO: Rotate it on a plan, and accept the previous key until the longest access token has expired.

## Readable payload

- TODO: The access token carries the user id, the tenant id, and the permissions.
- TODO: Assume the holder of the token, and any proxy along the way, can read those claims.

## Immediate revocation

- TODO: Logout revokes the refresh token and clears the cookie.
- TODO: The access token stays valid until it expires. Keep that lifetime short, and check a denylist when a token has to die early.

## Refresh Tokens

## Security Considerations

## Passkeys and machine-to-machine authentication

## Token expiry and the clock

## Permission-based authorization

## Related Topics

- See [ASP.NET Core: Authentication](/csharp/aspnet-core/authentication/overview)
- See [JWT bearer](/csharp/aspnet-core/authentication/jwt)
- See [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)
- See [Modern authentication](/csharp/aspnet-core/authentication/modern-auth)
- See [Permission-based authorization](/csharp/aspnet-core/authorization/permissions)

---

**Next:** [Chapter 5: Multi-Tenancy](/building-a-saas/05-multi-tenancy/overview)
