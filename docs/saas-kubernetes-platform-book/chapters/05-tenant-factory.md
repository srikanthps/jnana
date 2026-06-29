# Chapter 5: Tenant Factory and Provisioning

The tenant factory is the automated system that converts an approved tenant request into running, secure, observable infrastructure.

## Responsibilities

A tenant factory should provision:

- Cloud account, subscription, or project if required
- Network boundaries
- Kubernetes namespace or cluster
- Databases and schemas
- Object storage
- Cache and message queues
- DNS records
- TLS certificates
- Secrets and workload identities
- GitOps application definitions
- Observability dashboards and alerts
- Backup policies
- Billing and metering metadata
- Smoke tests

## Workflow Engine Options

Use durable workflows for provisioning because tenant creation is long-running and failure-prone.

Good options include:

- Temporal
- Argo Workflows
- GitHub Actions
- GitLab CI
- AWS Step Functions
- Azure Durable Functions
- Google Workflows

## Self-Service Portal

Backstage, Port, Humanitec, Cortex, or OpsLevel can provide a user-facing portal for approved tenant creation.

## Tenant Definition Contract

Example tenant contract:

```yaml
tenant:
  id: example-customer
  tier: enterprise
  cloud: aws
  region: us-east-1
  isolation: dedicated-cluster
  database: dedicated
  storage: dedicated-bucket
  compliance:
    - soc2
    - hipaa
  observability: dedicated-dashboards
```

## Provisioning Checklist

- Validate tenant request.
- Create infrastructure from templates.
- Register tenant metadata.
- Deploy applications through GitOps.
- Run smoke tests.
- Enable monitoring and alerts.
- Notify support, billing, and customer success systems.
