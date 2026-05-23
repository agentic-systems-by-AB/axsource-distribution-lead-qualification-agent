# Solution Architecture v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

Architecture principles:

- Multi-tenant ISV design from day one
- Customer-tenant execution only
- No AXSource-hosted services
- Human approval before external action
- Managed-solution deployment only
- Configuration through environment variables
- Connection references only
- Dataverse as authoritative source
- Public web grounding as supplementary context

Core components planned:

- Copilot Studio agent
- Dataverse
- Dynamics 365 Sales entities
- AXSource custom tables
- Power Automate orchestration
- Teams approval surfaces
- GitHub-based ALM