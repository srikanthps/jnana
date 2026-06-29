# Chapter 10: Multi-Cloud and Portability

Multi-cloud support requires a clear platform contract and deliberate abstraction. The goal is portability where it matters, not denial that cloud providers differ.

## Portable Layers

Use:

- Kubernetes for compute
- OpenTelemetry for telemetry
- Terraform/OpenTofu, Pulumi, or Crossplane for infrastructure
- S3-compatible object storage where practical
- PostgreSQL-compatible databases where practical
- External Secrets Operator for secrets abstraction
- Gateway API or service mesh for traffic management
- CloudEvents for event payloads

## Cloud-Specific Implementations

Build provider modules for AWS, Azure, and Google Cloud behind a common tenant contract.

Example:

```yaml
tenant:
  cloud: gcp
  region: us-central1
  isolation: dedicated-project
  database: cloud-sql-postgres
  storage: dedicated-bucket
```

## Multi-Cloud Tooling

Useful tools include Terraform, OpenTofu, Pulumi, Crossplane, Rancher, Anthos, Azure Arc, OpenShift, VMware Tanzu, Cilium, Istio, and Backstage.

## Avoiding Lock-In

Avoid embedding cloud-specific APIs directly in business logic. Prefer adapters, event abstractions, workload identity, and portable observability standards.
