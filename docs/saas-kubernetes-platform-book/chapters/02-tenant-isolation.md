# Chapter 2: Tenant Isolation Models

Tenant isolation is the most important architectural choice in a multi-tenant SaaS platform. It determines security boundaries, cost, operations, compliance posture, and customer confidence.

## Namespace per Tenant

Each tenant receives a Kubernetes namespace, scoped secrets, resource quotas, role bindings, network policies, and tenant-specific configuration.

### Best For

- Free trials
- Small and medium businesses
- High tenant counts
- Lower cost tiers

### Benefits

- Efficient resource usage
- Fast provisioning
- Easier cluster operations
- Lower cost

### Risks

- Weaker isolation than dedicated clusters
- Policy mistakes can create cross-tenant exposure
- Shared cluster failures can affect many tenants

## Cluster per Tenant

Each tenant receives a dedicated Kubernetes cluster and usually dedicated supporting infrastructure.

### Best For

- Enterprise tenants
- Regulated industries
- Bring-your-own-cloud deployments
- Strict blast-radius requirements

### Benefits

- Strong isolation
- Independent upgrade windows
- Clearer audit boundary
- Easier tenant-level disaster recovery

### Risks

- Higher cost
- More cluster lifecycle complexity
- Requires mature automation

## Cloud Account, Subscription, or Project per Tenant

Each tenant receives a dedicated AWS account, Azure subscription, or Google Cloud project.

### Benefits

- Strong billing isolation
- Strong IAM and audit boundary
- Cleaner offboarding
- Easier customer-specific compliance reporting

## Recommended Tiering Model

| Tenant Tier | Isolation Model |
| --- | --- |
| Trial | Shared cluster, namespace per tenant |
| Standard | Namespace per tenant, dedicated data boundary |
| Business | Namespace or small cluster per tenant |
| Enterprise | Dedicated cluster and dedicated data |
| Regulated | Dedicated cloud account/project/subscription and cluster |

## Data Isolation Patterns

- Database per tenant: strong isolation and easier restore.
- Schema per tenant: efficient and manageable for many tenants.
- Cluster per tenant database: strongest model for enterprise and regulated customers.

Tenant isolation should be tested continuously with automated security and integration tests.
