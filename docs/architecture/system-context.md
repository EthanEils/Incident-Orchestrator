# System Context

```mermaid
flowchart LR
    User((On-Call User))
    Admin((Admin / Commander))
    Monitor((Monitoring System))
    Web(Web UI)
    API(API)
    DF(Durable Functions)
    SB(Service Bus)
    SQL[(Azure SQL)]
    ACS(Azure Communication Services)
    Teams(Microsoft Teams)
    Graph(Microsoft Graph)
    AAD(Entra ID)

    User --> Web
    Admin --> Web
    Web --> AAD
    Web --> API
    API --> SB
    SB --> DF
    DF --> ACS
    DF --> Teams
    Teams --> Graph
    API --> SQL
```

The platform interacts with:

- Users: On-call engineers, dispatchers, responders
- External Systems: Monitoring tools posting incidents
- Microsoft Graph: Teams messages, Adaptive Cards
- ACS: SMS, email notifications
- Azure SQL: Persistence layer
