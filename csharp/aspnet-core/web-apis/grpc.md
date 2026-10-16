# gRPC

A contract-first RPC API that runs on HTTP/2.

## The contract

- TODO: A `.proto` file names the service, the methods, and the message fields.
- TODO: Generate the server and client stubs from that file. Do not hand-write a parallel shape.

## On HTTP/2

- TODO: gRPC needs HTTP/2. Confirm the host, the proxy, and the client all allow it.
- TODO: JSON over HTTP stays the public API unless an internal client needs this contract.

## A call from ASP.NET Core

- TODO: Map the generated service and register the client with a typed address.
- TODO: Metadata carries the tenant, the caller, and the trace. Do not hide those in the message body.

## Deadlines

- TODO: Set a deadline on the call. A missing deadline waits until the connection fails.
- TODO: Honor cancellation so a dropped caller does not keep the handler running.

## Practical Examples

- See [Building a SaaS: Architecture Decisions](/building-a-saas/02-architecture-decisions/overview) - When an internal client would use gRPC

## Related Topics

- See [HTTP and the Web](/fundamentals/networking/http)
- See [Minimal APIs and controllers](/csharp/aspnet-core/web-apis/minimal-apis-and-controllers)
- See [HTTP clients](/csharp/platform/http-clients)

---

**Next:** [SignalR](/csharp/aspnet-core/web-apis/signalr)
