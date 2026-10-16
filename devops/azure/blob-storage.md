# Blob Storage

Object storage for files the database should not hold.

## What goes in a blob

- TODO: Store the bytes in a container. Store the blob name, content type, and owner in the database.
- TODO: The database row is the source of "who may read this." The blob is the bytes.

## Conditional writes

- TODO: Send a condition so a write succeeds only when the blob is absent, or only when the ETag still matches.
- TODO: A retry that loses the race must not replace the object another request already stored.

## BlobCreated is at-least-once

- TODO: A BlobCreated event can arrive more than once, and it can arrive late.
- TODO: The handler keys off the blob identity and treats a second delivery as the same event.

## Practical Examples

- See [Building a SaaS: Data Layer](/building-a-saas/07-data-layer/overview) - File storage for a tenant

## Related Topics

- See [Azure overview](/devops/azure/overview)
- See [Azure Functions](/devops/azure/functions)
- See [Outbox and the idempotent consumer](/patterns/integration-patterns/outbox-and-idempotent-consumer)

---

**Next:** [Monitoring](/devops/monitoring/logging)
