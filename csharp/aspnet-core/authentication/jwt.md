---
title: JWT Bearer
order: 160
---

# JWT Bearer

A JSON Web Token is a signed set of claims. The API checks the signature, the issuer, the audience, and the expiry.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Claims

Subject, name, roles, and a tenant id.

## Signing

A key, an algorithm, and who holds the private material.

## Validation

Issuer, audience, lifetime, and clock skew.

## Where a browser must not put it

Local storage is readable by script. See choosing a scheme.

## Passing the token

An Authorization header. Nothing else.

## Key strength

- TODO: Sign with a key made of long random bytes, and store it with the other secrets.
- TODO: An HMAC secret has to be at least as long as the hash. Prefer an asymmetric key when more than one service validates the token.

## Readable payload

- TODO: The payload is base64url. Anyone who can see the token can read the claims.
- TODO: Put an id, a role, and an expiry in the claims. Keep secrets out of them.

## Immediate revocation

- TODO: An access token stays valid until it expires. Deleting the copy on the client does not tell the API.
- TODO: Keep that lifetime short, and revoke the refresh token on logout.
- TODO: Reject an access token early only when the API checks a denylist on each request.

### A version number per user

- TODO: Store a version number on the user, and copy it into a claim when a token is issued.
- TODO: Raise the number on logout everywhere, a password change, or a role change. Every older token now fails.
- TODO: The check is one lookup per request. Cache it briefly, and decide how many seconds of delay you accept.
- TODO: A version per user ends all of that user's sessions at once. A denylist of token ids ends one.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Refresh tokens](/csharp/aspnet-core/authentication/refresh-tokens)
- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)
- [Building a SaaS: Authentication](/building-a-saas/04-authentication/overview)

---

**Next:** [Refresh Tokens](/csharp/aspnet-core/authentication/refresh-tokens)
