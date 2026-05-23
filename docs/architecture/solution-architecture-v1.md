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

## End-to-End Flow

Step 1

Lead created or updated in Dynamics 365 Sales


Step 2

Power Automate trigger executes


Step 3

Copilot Studio agent retrieves:

- Lead
- Account
- Contact
- Product
- Price List
- Territory context


Step 4

Public web grounding enriches context


Step 5

Agent executes:

Distribution BANT+

Scoring

Channel classification

Branch recommendation

Confidence evaluation


Step 6

Agent writes:

- qualification narrative
- confidence score
- recommendation
- qualification history


Step 7

Human approval required


Step 8

Approved actions execute:

- draft email
- task creation
- follow-up activities

## Trust Boundaries

Customer tenant owns:

- Dataverse data
- Dynamics 365 Sales records
- Copilot execution
- Power Automate execution
- DLP policies
- telemetry
- approvals
- credentials


AXSource owns:

- managed solution
- packaging
- product IP
- AppSource publishing


AXSource does NOT host:

- customer data
- AI memory
- enrichment databases
- external APIs
- centralized telemetry
- customer prompts


Trust model:

Customer-tenant execution only

## Deployment Topology

Development:

AXS-DISTAI-DEV


Testing:

AXS-DISTAI-TST


Production:

AXS-DISTAI-PRD


Customer Install Validation:

AXS-DISTAI-CLEAN


Demo:

AXS-DISTAI-DEMO


Deployment model:

Managed solution only


Promotion path:

DEV

↓

TEST

↓

PROD

↓

AppSource package


Validation rule:

Every release must install successfully into CLEAN with zero manual configuration fixes.

## External Dependency Policy

Approved v1 dependencies:

- Dataverse
- Dynamics 365 Sales
- Copilot Studio
- Power Automate
- Microsoft Teams
- Public web grounding


Explicitly excluded:

- ERP integrations
- Azure-hosted APIs
- Customer-managed AI endpoints
- SharePoint knowledge
- External product information systems
- Third-party credit bureau APIs
- Custom connectors
- AXSource-hosted services


Future candidates:

v2

- Dynamics 365 Finance and Supply Chain
- SAP
- Oracle
- Infor
- Epicor


Rule:

No external dependency becomes a runtime requirement in v1.