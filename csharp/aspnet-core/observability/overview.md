---
title: Observability
order: 20
---

# Observability

Logs, metrics, and traces from the running API. Alerting and the operational response live in the DevOps monitoring pages.

*This page is an outline. The sections will be filled in over time, including a C# sample where the topic has one.*

## The three signals

A log says what happened. A metric says how often. A trace says where the time went.

## OpenTelemetry

One pipeline for all three, and an exporter per environment.

### Wiring in ASP.NET Core

<!-- TODO -->

### Auto versus manual instrumentation

<!-- TODO: ActivitySource and Meter -->

### Exporters

<!-- TODO: OTLP to Application Insights or the Aspire dashboard -->

### Tenant id on a span

<!-- TODO -->

### A slow 200

<!-- TODO: Find the time in a trace when the status code is success -->

### Sampling

- TODO: Head sampling keeps or drops a trace when it starts. Tail sampling decides after the trace finishes, so a failed or slow trace can be kept while ordinary ones are dropped.
- TODO: Keep enough failing traces to investigate, and drop enough of the rest that the exporter can keep up.

## Correlation

A trace id on the request, the log, and the downstream call.

## What to measure

Request rate, latency, and error rate, plus the dependencies you call.

## ILogger

Application logs join the same pipeline. The logging page covers the API.

## Code example

A short C# sample will go here. A sample longer than about 30 lines will live in a companion `.cs` file next to this page.

## Related

- [Logging](/csharp/platform/logging)
- [Health checks](/csharp/aspnet-core/observability/health-checks)
- [DevOps monitoring](/devops/monitoring/logging)
- [Building a SaaS: Monitoring](/building-a-saas/12-monitoring-operations/overview)

---

**Next:** [Health Checks](/csharp/aspnet-core/observability/health-checks)
