---
title: Change Tracking
order: 70
---

# Change Tracking

A context remembers the entities it loaded. That memory is how `SaveChanges` knows what to write.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## Tracked and untracked

`AsNoTracking` for a read that will not be saved.

## States

Added, Modified, Deleted, and Unchanged.

## Updates

Load and edit, versus attaching a graph the client sent.

## Identity resolution

Two loads of the same key return the same instance inside one context.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [DbContext](/csharp/entity-framework/dbcontext)

---

**Next:** [Migrations](/csharp/entity-framework/migrations)
