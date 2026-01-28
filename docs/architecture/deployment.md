# Deployment Architecture

## Azure Resources

- Azure App Service (Web + API)
- Azure Functions (Durable)
- Azure Service Bus (Premium)
- Azure SQL with zone redundancy
- Azure Communication Services
- Azure Key Vault
- Azure Front Door + WAF
- Application Insights + Log Analytics

## Environments

- dev
- test
- prod

## IaC Strategy

All infrastructure deployed via Bicep:

- App Service plan
- Function app
- Service Bus namespace/queues
- SQL server & database
- Key Vault + secrets
- Front Door routes
- Diagnostic settings
