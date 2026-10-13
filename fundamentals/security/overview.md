# Security Concepts

The failures a feature developer meets, before any framework. The C# pages show how ASP.NET Core implements the controls.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Secrets

Passwords, connection strings, and API keys stay out of source control.

## Injection

Untrusted input treated as code: SQL, commands, and HTML.

## Cross-site scripting

Untrusted content rendered as markup.

## Cross-site request forgery

A browser sending a cookie the user did not mean to send.

## Broken access control

Knowing who the caller is, and still failing to check what they may touch.

## Transport

Why plaintext HTTP is not enough once a token or a cookie is on the wire.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Authentication and authorization](/fundamentals/security/authentication-and-authorization)
- [C# security](/csharp/security/overview)

---

**Next:** [Authentication and authorization](/fundamentals/security/authentication-and-authorization)
