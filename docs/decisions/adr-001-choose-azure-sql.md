# ADR-001: Choose Azure SQL as the primary data store

## Status

Accepted

## Context

The system requires strong consistency, relational data, transactional guarantees, and reporting capabilities.

## Decision

Use Azure SQL (General Purpose, Zone Redundant) as the primary data store.

## Alternatives Considered

### Cosmos DB

- Pros: Global distribution, low latency
- Cons: Overkill for relational data; complex modeling

### Table Storage

- Pros: Cheap and simple
- Cons: No relational integrity, limited querying

## Consequences

- Faster development with mature relational tooling
- Supports complex queries like “timeline for incident”
