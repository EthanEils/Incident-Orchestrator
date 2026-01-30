# Project Goals

## Functional Goals

- Support full incident lifecycle: creation → paging → acknowledgement → escalation → resolution.
- Provide on-call schedules, rotations, overrides, and time-zone aware handoff logic.
- Support multi-channel paging: Email, SMS, Teams, Push.
- Provide durable, reliable escalation using Azure Durable Functions.
- Persist incidents, timelines, acknowledgements, and schedules in Azure SQL.
- Integrate with Microsoft Entra ID for SSO and RBAC.
- Provide a Web UI + API for operational visibility and control.
- Generate audit logs suitable for compliance review.

## Non-Functional Goals

- High availability via Azure PaaS services.
- Zero Trust security posture.
- HA/DR strategy aligned with Azure region pairing.
- Observability: logs, metrics, distributed traces.
- Infrastructure-as-Code (Bicep).
- CI/CD via GitHub Actions.
- Scalable messaging and workflow orchestration.

## Out of Scope (for v1)

- Full mobile application (optional later)
- Real-time analytics dashboards (planned for v2)
- Support for non-Microsoft identity providers
