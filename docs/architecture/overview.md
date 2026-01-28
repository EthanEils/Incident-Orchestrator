# Architecture Overview

This system is composed of four primary areas:

1. **Web/UI Layer**  
   Blazor Server or Razor/React frontend authenticated with Entra ID.

2. **API Layer**  
   ASP.NET Core REST API secured via Entra ID, issuing commands and queries.

3. **Workflow Orchestration Layer**  
   Azure Durable Functions implementing paging and escalation logic.

4. **Messaging & Notification Layer**  
   Azure Service Bus + Azure Communication Services + Microsoft Graph (Teams).

5. **Persistence Layer**  
   Azure SQL for relational storage + optional long-term event archiving.

See `/docs/architecture/diagrams` for diagrams.
