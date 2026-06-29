# Chapter 12: Compliance, Governance, and Operations

Enterprise SaaS platforms need repeatable controls, evidence, support workflows, billing, and operational visibility.

## Compliance Targets

Common targets include SOC 2, ISO 27001, HIPAA, PCI DSS, GDPR, CCPA, FedRAMP, FINRA, SEC, and HITRUST.

## Governance Tools

Use Drata, Vanta, Secureframe, Sprinto, Wiz, Orca, Lacework, Prisma Cloud, Snyk, Aqua, or Sysdig Secure.

## Audit Logging

Audit logs should capture:

- User login and failed login
- Permission changes
- Tenant creation and deletion
- Data export
- Admin access
- Billing changes
- API key creation
- Secret rotation
- Infrastructure changes
- Production access
- Support impersonation

Audit logs should be tamper-resistant, encrypted, retained according to policy, queryable by tenant, and exportable for enterprise customers.

## Backup and Disaster Recovery

Use Velero, Kasten K10, pgBackRest, WAL-G, Restic, Kopia, or cloud-native backup services.

Each tenant should have:

- Automated backups
- Encrypted backups
- Retention policy
- Point-in-time recovery where needed
- Restore testing
- Cross-region replication for high tiers
- Tenant-specific restore workflow

## Cost Management

Use Kubecost, OpenCost, CloudHealth, CloudZero, Vantage, AWS Cost Explorer, Azure Cost Management, Google Cloud Billing, and Infracost.

Track cost per tenant, service, cluster, region, and environment.

## Support Operations

Support tools such as Zendesk, Intercom, Freshdesk, Salesforce Service Cloud, Linear, Jira Service Management, and HubSpot should integrate with tenant metadata and health dashboards.

Support access must be audited, time-bound, approved for sensitive tenants, least-privilege, and tenant-scoped.
