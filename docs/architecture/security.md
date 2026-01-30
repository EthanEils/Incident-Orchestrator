# Security Model

## Zero Trust Principles

- No public SQL endpoints (private endpoints only)
- App Service + Functions use Managed Identity
- Key Vault stores all secrets
- RBAC-defined access to operational APIs

## Identity & Access

- Entra ID for SSO
- App Roles:
  - Incident.Admin
  - Incident.Commander
  - Incident.Responder
  - Incident.Viewer

## Data Protection

- SQL TDE + optional CMK (customer-managed key)
- Audit logs immutable and append-only
- Secrets rotated on schedule

## Network Security

- Front Door → App Service (private backend)
- Private endpoints for SQL, Service Bus, Key Vault
- NSGs controlling subnet flow
