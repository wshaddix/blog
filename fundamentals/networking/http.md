---
title: HTTP and the Web
order: 1
---

# HTTP and the Web

How a request moves from a browser or an `HttpClient` to a server and back. Read this before building an API.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Names and addresses

DNS, IP addresses, ports, and the parts of a URL.

## TCP and TLS

Connections, certificates, and why HTTPS is the default.

## The request

Method, path, query, headers, and body.

## The response

Status codes, headers, and body. Which codes mean retry, and which mean the caller was wrong.

## Idempotency and safety

Which methods can be repeated, and which change state.

## Caching headers

Cache-Control, ETag, and what a client may reuse.

## HTTP/2 and HTTP/3

- TODO: HTTP/2 carries many streams on one connection. gRPC requires it.
- TODO: HTTP/3 runs over QUIC. Clients and middleboxes still need a fallback.
- TODO: The application contract is the choice. Which HTTP version carries it is a hosting decision.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Security concepts](/fundamentals/security/overview)
- [gRPC](/csharp/aspnet-core/web-apis/grpc)

---

**Next:** [Security concepts](/fundamentals/security/overview)
