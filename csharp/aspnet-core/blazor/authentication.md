# Blazor Authentication

A Blazor app in the browser uses the cookie scheme. It does not store a JWT where script can read it.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## AuthorizeView

What a signed-in user sees, and what everyone else sees.

## The authentication state

Where the principal comes from in each render mode.

## Challenges

A redirect to sign in, and the return URL.

## Calling an API

The app's own server attaches the credential. The component does not.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Cookie authentication](/csharp/aspnet-core/authentication/cookies)
- [Choosing a scheme](/csharp/aspnet-core/authentication/choosing-a-scheme)

---

**Next:** [Calling the API](/csharp/aspnet-core/blazor/calling-the-api)
