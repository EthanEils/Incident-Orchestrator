# ADR-002: Choose Azure Service Bus for messaging

## Status

Accepted

## Context

Notification workflows need durability, retries, poison queues, and decoupling.

## Decision

Use Azure Service Bus Premium for inter-service messaging.

## Alternatives

- Event Grid: pub/sub only, no ordering, no retries
- Storage Queues: lacks advanced features

## Consequences

- Reliable workflows
- Higher cost but justified for operational stability
