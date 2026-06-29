# Chapter 4: Infrastructure as Code and GitOps

Infrastructure as Code and GitOps create a controlled, auditable delivery model for both platform and tenant environments.

## Infrastructure as Code

Use Terraform, OpenTofu, Pulumi, or Crossplane to provision:

- Cloud accounts, subscriptions, and projects
- Virtual networks and subnets
- Kubernetes clusters
- Databases
- Object storage
- DNS
- IAM
- KMS keys
- Observability resources
- Backup policies

## Terraform and OpenTofu

Terraform and OpenTofu are strong defaults for cross-cloud infrastructure. Terragrunt can help compose reusable modules and tenant stacks.

## Pulumi

Pulumi is useful when infrastructure logic benefits from general-purpose programming languages such as TypeScript, Python, Go, C#, or Java.

## Crossplane

Crossplane is useful when Kubernetes should become the platform control plane for cloud infrastructure. It supports self-service compositions for tenant resources.

## GitOps

Use Argo CD or Flux CD to reconcile desired state from Git into Kubernetes clusters.

Recommended structure:

```text
platform/
  infrastructure/
  clusters/
  policies/
apps/
  api/
  worker/
  web/
tenants/
  tenant-a/
  tenant-b/
```

## Packaging

Use Helm for parameterized releases, Kustomize for overlays, and ApplicationSets for fleet-style tenant deployments.

## Pull Request Controls

Require:

- Code review
- CODEOWNERS
- Automated tests
- Security scanning
- Policy checks
- Signed artifacts for sensitive changes
