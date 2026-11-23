# Chapter 12: Monitoring & Operations

Your job isn't done when code ships. Observability keeps your SaaS running smoothly.

## What We'll Cover

- Structured logging with Serilog
- Application Insights integration
- Custom metrics and dashboards
- Alerting strategy
- Incident response
- Performance monitoring

## Logging

## Metrics

### Debugging a slow request from the browser

- TODO: Read the named timings on the slow response before opening a trace.
- TODO: What the header contains, and what it must not, is [Server-Timing](/csharp/aspnet-core/observability/server-timing).

### Model calls per request

- TODO: Record how many model calls one request makes, including every pass of a tool loop. See [A cap on round trips](/csharp/mcp/clients-and-agents#a-cap-on-round-trips).
- TODO: Treat a request that reaches the cap as its own metric.
- TODO: A call whose answer was checked, and one whose answer was rejected, are both part of that count. See [Checking a model's answer](/building-a-saas/06-api-development/overview#checking-a-models-answer).

## Alerting

### Queue age

- TODO: Page when the oldest item has waited longer than you promised, not when the queue is merely long. See [Age of the oldest item](/devops/monitoring/alerting#age-of-the-oldest-item).

## Incident Response

## Health Checks

## OpenTelemetry

### Sampling

- TODO: Keep traces for failures and slow requests. Drop a share of the ordinary traces so exporting them stays within the pipeline's capacity.
- TODO: Head sampling chooses at the start. Tail sampling chooses after the trace ends, which is what lets a failure stay in the sample.

## Sensitive data in logs

## Degraded modes

- TODO: Name what the product still does when a dependency is down.
- TODO: Turn off the feature that failed. Leave the path a tenant needs in order to work.

## Cache health

- TODO: Watch hit rate, eviction rate, and the latency of a miss. A process that is up can still be a cache that never hits.
- TODO: A cache that stays full by dropping the keys you just warmed is out of room.

## Related Topics

- See [DevOps: Monitoring](/devops/monitoring/logging)
- See [Observability](/csharp/aspnet-core/observability/overview)
- See [Health checks](/csharp/aspnet-core/observability/health-checks)
- See [Sensitive data in logs](/csharp/security/sensitive-data-in-logs)
- See [Failure and degradation](/fundamentals/distributed-systems/failure-and-degradation)
- See [Caching](/fundamentals/distributed-systems/caching)

---

**Congratulations!** You've built a production-ready SaaS application. Continue to [Career Development](/career-development/overview) to learn how to grow as an engineer and leader.
