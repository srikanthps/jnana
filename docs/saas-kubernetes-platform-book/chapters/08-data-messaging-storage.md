# Chapter 8: Data, Messaging, and Storage

Tenant data boundaries shape security, reliability, cost, support, and compliance.

## Relational Databases

Common choices include PostgreSQL, MySQL, MariaDB, SQL Server, Aurora PostgreSQL, AlloyDB, Cloud SQL, Azure Database for PostgreSQL, CockroachDB, and YugabyteDB.

## NoSQL and Search

Options include DynamoDB, Cosmos DB, MongoDB Atlas, Firestore, Cassandra, ScyllaDB, OpenSearch, Elasticsearch, Meilisearch, Typesense, and Algolia.

## Cache

Use Redis, Valkey, or Memcached. Enterprise tenants may require dedicated cache instances.

## Messaging

Use Kafka, Redpanda, Pulsar, NATS, RabbitMQ, AWS SQS/SNS, EventBridge, Azure Service Bus, Event Grid, or Google Pub/Sub.

Every event should include tenant context and idempotency metadata.

## Object Storage

Use Amazon S3, Azure Blob Storage, Google Cloud Storage, MinIO, Cloudflare R2, or other S3-compatible storage.

Patterns:

- Bucket per tenant for strong isolation
- Prefix per tenant for lower cost
- Tenant-specific encryption keys for sensitive workloads

## Data Migrations

Use Flyway, Liquibase, Prisma Migrate, Alembic, Rails migrations, Django migrations, Atlas, or Sqitch.

Migration requirements:

- Per-tenant migration tracking
- Backward-compatible changes
- Tenant-by-tenant rollout
- Preflight validation
- Backup before risky changes
- Tested rollback or recovery path
