# Chapter 6: Security Architecture

Security must be embedded into templates, pipelines, runtime controls, and operating procedures.

## Identity and Access

Use centralized identity providers such as Okta, Auth0, Microsoft Entra ID, Keycloak, Ping Identity, or IAM Identity Center.

Support:

- OAuth 2.0
- OpenID Connect
- SAML for enterprise customers
- SCIM for user provisioning
- RBAC and ABAC
- Tenant-aware authorization

## Kubernetes Security

Enforce:

- Least-privilege RBAC
- Namespace-scoped roles
- Dedicated service accounts per workload
- No default cluster-admin access
- Break-glass access with approval and audit logs
- Pod Security Standards
- Non-root containers
- Dropped Linux capabilities
- Read-only root filesystems where possible

## Secrets Management

Use HashiCorp Vault, AWS Secrets Manager, Azure Key Vault, Google Secret Manager, Doppler, 1Password Secrets Automation, SOPS, or Sealed Secrets.

Integrate through:

- External Secrets Operator
- Secrets Store CSI Driver
- Vault Agent Injector
- Vault CSI Provider

## Workload Identity

Prefer short-lived workload identity over static credentials.

- AWS: IRSA or EKS Pod Identity
- Azure: Azure Workload Identity
- Google Cloud: GKE Workload Identity

## Policy as Code

Use Kyverno, Open Policy Agent Gatekeeper, Conftest, Checkov, tfsec, Terrascan, or Datree to enforce controls.

Policies should require:

- Approved registries
- No `latest` tags
- Image signatures
- Resource limits
- Probes
- Network policies
- Restricted security contexts

## Supply Chain Security

Every production artifact should include:

- SBOM
- Vulnerability scan
- Signature
- Provenance
- Immutable digest reference

Useful tools include Syft, Grype, Trivy, Cosign, Sigstore, SLSA, and in-toto.
