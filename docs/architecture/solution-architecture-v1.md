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

## Component Inventory

### User surfaces

- Dynamics 365 Sales
- Copilot Studio embedded experience
- Microsoft Teams approval cards


### Data layer

Standard Dataverse entities:

- Lead
- Account
- Contact
- Product
- Price List
- Activity
- System User
- Team


AXSource custom entities:

- Distributor Partner
- Branch Territory
- Qualification History
- Channel Classification


### Automation layer

Power Automate:

- Lead qualification trigger
- Channel conflict workflow
- Credit eligibility workflow
- Human approval workflow
- Draft email workflow


### AI layer

Copilot Studio:

- Distribution qualification instructions
- BANT+ framework
- Confidence scoring
- Public web grounding


### ALM layer

GitHub

GitHub Actions

Managed solution deployment