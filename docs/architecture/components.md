# Component Architecture

## Web UI

- Blazor Server or Blazor WebAssembly.
- Provides incident dashboard, ACK buttons, timelines.

## API

- ASP.NET Core API.
- Commands: CreateIncident, AcknowledgeIncident, ResolveIncident.
- Queries: GetIncident, GetTimeline, GetOnCall.

## Orchestration (Durable Functions)

- `IncidentEscalation_Orchestrator`
- Activities:
  - NotifyActivity
  - RecordAckActivity
  - EscalateActivity
  - AppendTimelineActivity

## Messaging

- Service Bus queues for:
  - incident-created
  - notification-events
  - audit-events

## Notifications

- Azure Communication Services (SMS, email)
- Teams bot via Microsoft Graph

## Data

- Azure SQL with:
  - Incidents
  - TimelineEvents
  - Schedules
  - EscalationPolicies
  - Users
