# Chapter 7: Observability, Logging, and Reliability

Observability turns a multi-tenant platform from a black box into an operable system.

## Metrics

Use Prometheus, Thanos, Cortex, Mimir, VictoriaMetrics, Datadog, New Relic, Dynatrace, CloudWatch, Azure Monitor, or Google Cloud Monitoring.

Track:

- Latency
- Error rate
- Throughput
- Saturation
- Queue depth
- Tenant-level usage
- Database performance
- Kubernetes health
- Deployment health
- SLO burn rate

## Logs

Use Loki, OpenSearch, Elasticsearch, Splunk, Datadog Logs, New Relic Logs, CloudWatch Logs, Google Cloud Logging, or Azure Monitor Logs.

Collectors include Fluent Bit, Fluentd, Vector, and OpenTelemetry Collector.

Logs should be structured and include:

- Tenant ID
- Request ID
- Trace ID
- User ID when appropriate
- Service name
- Version
- Region
- Cloud

Secrets and personally identifiable information must be redacted.

## Traces

Use OpenTelemetry with Jaeger, Tempo, Zipkin, Honeycomb, Datadog APM, New Relic APM, or Lightstep.

Trace context should propagate across HTTP, gRPC, events, and background jobs.

## SLOs

Define SLOs per platform, service, region, tenant, and critical customer journey.

Example SLOs:

- API availability of 99.9%
- p95 API latency below 300 milliseconds
- Tenant provisioning below 30 minutes
- RPO below 15 minutes
- RTO below 1 hour

Use burn-rate alerting rather than noisy threshold-only alerts.

## Incident Response

Use PagerDuty, Opsgenie, Grafana OnCall, Rootly, FireHydrant, incident.io, or Statuspage.

Runbooks should exist for provisioning failures, deployment rollback, database incidents, certificate expiration, logging outage, and tenant restore.
