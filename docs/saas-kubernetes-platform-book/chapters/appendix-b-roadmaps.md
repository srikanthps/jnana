# Appendix B: MVP and Enterprise Roadmaps

## Minimum Viable Platform

Start with:

- One managed Kubernetes provider
- Terraform or OpenTofu
- Helm and Kustomize
- Argo CD
- GitHub Actions or GitLab CI
- Namespace per tenant
- Database per tenant or schema per tenant
- External Secrets Operator
- cert-manager
- ExternalDNS
- NGINX Ingress or Gateway API
- Prometheus
- Grafana
- Loki
- OpenTelemetry
- Trivy
- Kyverno
- Backstage service catalog
- Tenant provisioning workflow

## MVP Must-Haves

- Tenant ID propagated everywhere
- Tenant isolation tests
- GitOps deployment
- Automated tenant creation
- Centralized logs
- Metrics and alerts
- Secret management
- Backups
- Security scanning
- Infrastructure templates

## Enterprise Additions

Add:

- Cluster per tenant
- Cloud account, subscription, or project per tenant
- Multi-cloud support
- Service mesh
- Tenant-specific encryption keys
- Customer-managed keys
- Tenant-specific dashboards
- Tenant-specific restore
- Bring-your-own-cloud support
- Advanced compliance automation
- AI incident assistant
- Cost allocation
- Runtime threat detection
- Multi-region failover
- Progressive delivery by tenant tier

## Suggested Delivery Phases

### Phase 1: Foundation

Build Kubernetes, IaC, GitOps, secrets, logging, metrics, and basic tenant provisioning.

### Phase 2: Security and Reliability

Add policy-as-code, supply-chain security, backups, SLOs, alerting, and tenant isolation testing.

### Phase 3: Platform Self-Service

Add Backstage, tenant factory workflows, golden path templates, preview environments, and cost reporting.

### Phase 4: Enterprise Readiness

Add dedicated tenant infrastructure, compliance automation, customer-managed keys, support tooling, and audit exports.

### Phase 5: Multi-Cloud and AI Operations

Add provider modules for multiple clouds, AI-assisted operations, tenant health summarization, and cross-cloud deployment patterns.
