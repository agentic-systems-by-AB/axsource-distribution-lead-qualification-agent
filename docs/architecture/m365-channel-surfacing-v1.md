# Microsoft 365 and Channel Surfacing v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

Design principles:

- Seller workflow first
- Surface inside existing tools
- Human approval before external action
- Minimize context switching
- Dynamics remains primary system of engagement

Primary user channels:

- Dynamics 365 Sales
- Microsoft Teams
- Copilot Studio embedded experience

Future channels:

- Microsoft 365 Copilot
- Outlook surfaces
- Additional Copilot integrations

## Primary User Experience Flows

Dynamics 365 Sales

Purpose:

Primary seller workspace


User experience:

- View qualification results
- View confidence score
- View qualification narrative
- View routing recommendations
- Review suggested next actions


Microsoft Teams

Purpose:

Approval and notification surface


User experience:

- Approval adaptive cards
- Qualification notifications
- Follow-up reminders


Copilot Studio Embedded Experience

Purpose:

Interactive qualification assistant


User experience:

- Ask qualification questions
- Request explanations
- Review BANT+ evaluation
- Request lead analysis


Rule:

Dynamics remains the system of engagement.

## Dynamics 365 Sales Surfacing

Primary location:

Lead form


Embedded components:

- Qualification summary
- Confidence score
- Qualification narrative
- Recommended branch
- Recommended owner
- Conflict indicators
- Credit findings
- Seller recommendations


Supporting components:

- Qualification History subgrid
- Related Tasks subgrid
- Approval status section


Future candidates:

- Sales workspace dashboard
- Seller manager dashboard


Rule:

Seller should not leave Lead workspace to review qualification output.

## Microsoft Teams Surfacing

Primary purpose:

Approval and seller notification channel


Teams artifacts:

Adaptive cards:

- Qualification approval request
- Qualification completed notification
- Missing information request
- Follow-up reminder


Adaptive card contents:

- Lead name
- Company
- Qualification score
- Confidence score
- Recommended owner
- Recommended branch
- Conflict findings
- Approval actions


Available actions:

Approve

Reject

Request more information


Rule:

Teams actions execute workflow responses only.

No business logic executes inside Teams.

## Microsoft First-Party Agent Coexistence

Microsoft baseline:

Sales Qualification Agent

Status:

Generally Available


AXSource positioning:

Distribution-specialized extension


Microsoft responsibilities:

- Generic lead qualification
- General enrichment
- Standard qualification workflows


AXSource responsibilities:

- Distribution-specific BANT+
- Branch routing
- Partner conflict detection
- Credit eligibility checks
- Channel classification
- Distribution-specific recommendations


Coexistence rule:

AXSource augments Microsoft qualification behavior.

AXSource does not replace first-party Sales agents.


Future compatibility:

Sales Opportunity Agent

Sales Research Agent

Sales Close Agent

## Future Surface Roadmap

v1:

- Dynamics 365 Sales
- Teams approvals
- Copilot Studio embedded experience


v1.x:

- Sales workspace dashboard
- Manager dashboard
- Outlook draft review experience


v2:

- Microsoft 365 Copilot integration
- Opportunity Agent handoff
- ERP-aware experiences
- Cross-agent workflow experiences


Rule:

New surfaces should reduce seller effort, not create duplicate workflows.