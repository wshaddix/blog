# Server-Timing

A response header that names how long each part of one request took, for the caller who received that response.

## Who can see it

- TODO: Say which responses carry the header, and which browser tools show the names and durations.
- TODO: Treat every value in the header as visible to the caller. Leave out anything you would not put in the body.

## Names from middleware

- TODO: Record a named duration around one piece of work, such as authorization or a call this request makes.
- TODO: Keep the names stable so two responses can be compared line by line.

## What to leave out

- TODO: Omit query text, secrets, and internal host names.
- TODO: Send the header in development, or only to a role allowed to see timings. Leave it off for everyone else.

## In the browser tools

- TODO: Show where the named timings sit next to the total time for one response.
- TODO: Start there when the question is "which part was slow" and a full trace is more than you need. The product walkthrough is [Debugging a slow request from the browser](/building-a-saas/12-monitoring-operations/overview#debugging-a-slow-request-from-the-browser).

## Related Topics

- See [Observability](/csharp/aspnet-core/observability/overview)
- See [Building a SaaS: Monitoring](/building-a-saas/12-monitoring-operations/overview)

---

**Next:** [Health Checks](/csharp/aspnet-core/observability/health-checks)
