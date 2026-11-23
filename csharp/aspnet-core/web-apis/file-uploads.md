# File Uploads

The API can accept the bytes, or the client can write them straight to storage and tell the API when they have landed.

## Buffered files and a streamed body

- TODO: A form file buffers the upload in the process. Streaming the body does not.
- TODO: Stream when holding the whole file would pressure memory. Buffer only a small file.

## Limits

- TODO: Set a ceiling on the server, on the form, and on the endpoint. The smallest one is the one that applies.
- TODO: A ceiling that follows the caller's plan belongs with the other plan limits.

## Straight to storage

- TODO: Issue a short-lived URL that can write one object. The API never reads those bytes.
- TODO: The URL expires, and it can write only the path it was minted for.

## Knowing the upload finished

- TODO: Mark the object present when storage reports it, or when the client calls back with the name you issued.
- TODO: A URL that was issued and never used leaves no row. Do not mark the file ready from the URL alone.

## Type, extension, and quarantine

- TODO: Accept only the content types and extensions this endpoint named.
- TODO: Keep a new object off the public path until a scan has accepted it.

## A path per tenant

- TODO: Put the tenant in the storage path so one tenant cannot address another's object.
- TODO: How this product stores tenant files is [Tenant attachments](/building-a-saas/06-api-development/overview#tenant-attachments).

## Related Topics

- See [Routing and model binding](/csharp/aspnet-core/web-apis/routing-and-binding)
- See [Blob Storage](/devops/azure/blob-storage)
- See [Building a SaaS: API Development](/building-a-saas/06-api-development/overview)

---

**Next:** [Routing and Model Binding](/csharp/aspnet-core/web-apis/routing-and-binding)
