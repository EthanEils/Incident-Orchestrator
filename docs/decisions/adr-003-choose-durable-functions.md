# ADR-003: Choose Durable Functions for escalation workflows

## Status

Accepted

## Context

Escalation requires timers, external events, fan-Out/in, human-in-loop orchestration.

## Decision

Use Durable Functions orchestrators + activities.

## Consequences

- Excellent fit for ACK workflows
- Vendor lock-in, but highly productive and Azure-native
