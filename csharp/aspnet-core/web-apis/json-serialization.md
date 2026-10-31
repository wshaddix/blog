# JSON Serialization

How an ASP.NET Core API turns a request body into an object and an object into a response.

## Where bodies are read and written

The framework reads the body and writes the result around the handler, on both minimal APIs and controllers.

- TODO: Name the points where a request body is read and a result is written.
- TODO: Say what the handler receives after that read, and what it returns before the write.

## Configuring options once

Naming, nulls, and converters belong to one options object that every endpoint shares.

- TODO: Set those options in one place, and show an endpoint that inherits them.
- TODO: Say what drifts when a second endpoint builds its own options. See [One set of JSON options](/building-a-saas/06-api-development/overview#one-set-of-json-options).

## Source-generated contexts

A source-generated context lists the types the serializer may touch, which is what AOT and a faster startup need.

- TODO: Show a context generated for the request and response types this API uses.
- TODO: Contrast that with finding the same types by reflection at startup.

## Streaming a large body

A large payload does not have to sit in memory as one document before the first item is handled.

- TODO: Read the body through a PipeReader and take items as they arrive, instead of buffering the whole payload.
- TODO: Contrast that with a bound parameter, which is the whole document before the handler runs. See [Large request bodies](/csharp/aspnet-core/web-apis/routing-and-binding#large-request-bodies).

## Another serializer

The framework serializer can be replaced, and the replacement brings its own costs.

- TODO: Show where a different serializer is registered, and which behaviors you give up or take on.
- TODO: Include the contract, source generation, and the work of keeping one set of options.

## Measure before switching

A number on the bodies this API actually sends is the reason to change serializers.

- TODO: Compare the current serializer and the candidate with BenchmarkDotNet on representative payloads.
- TODO: Record those numbers next to the decision to switch or to stay.

## Related Topics

- See [Routing and model binding](/csharp/aspnet-core/web-apis/routing-and-binding)
- See [Files, streams, and JSON](/csharp/language-basics/files-streams-and-json)
- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview)

---

**Next:** [Minimal APIs and Controllers](/csharp/aspnet-core/web-apis/minimal-apis-and-controllers)
