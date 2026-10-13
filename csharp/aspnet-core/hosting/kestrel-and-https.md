---
title: Kestrel and HTTPS
order: 10
---

# Kestrel and HTTPS

Kestrel is the server. In production it usually sits behind a reverse proxy that terminates TLS.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Kestrel

What it serves, and the limits you set.

## HTTPS in development

The developer certificate.

## A reverse proxy

Forwarded headers, the original scheme, and the original client address.

## YARP load balancing

<!-- TODO: A .NET reverse proxy in front of the app, and how it spreads requests -->

## HSTS

Telling a browser to stay on HTTPS.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Transport and headers](/csharp/security/transport-and-headers)
- [Azure App Service](/devops/azure/app-service)

---

**Next:** [Transport and Headers](/csharp/security/transport-and-headers)
