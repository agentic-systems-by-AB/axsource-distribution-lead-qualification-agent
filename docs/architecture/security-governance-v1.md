# Security Governance v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

Security principles:

- Least privilege
- Customer tenant ownership
- Human approval before external action
- No AXSource-hosted customer data
- Dataverse as authoritative source
- Shared master data protected
- Customer-controlled governance
- Responsible AI first

Security categories:

- Dataverse security
- Business units
- DLP
- Responsible AI
- Audit logging
- Compliance controls

## Dataverse Security Roles

Role 1

Name:

AXS Distribution Seller


Purpose:

End-user seller access


Permissions:

Read:

- Lead
- Qualification History
- Activities

Create:

- Tasks
- Notes

No direct configuration access


Role 2

Name:

AXS Distribution Manager


Purpose:

Sales manager oversight


Permissions:

Seller permissions plus:

- approval actions
- qualification review
- reporting access


Role 3

Name:

AXS Distribution Administrator


Purpose:

System administration


Permissions:

- environment configuration
- connection references
- environment variables
- qualification settings


Role 4

Name:

AXS Distribution Agent Service Role


Purpose:

Agent execution identity


Permissions:

- qualification writes
- qualification history create/update
- activity creation

Restrictions:

No Account ownership changes

No Contact ownership changes

No Opportunity creation

## Business Unit Strategy

Business Unit model:

Customer-controlled


Recommended structure:

Corporate

↓

Region

↓

Branch


Ownership model:

Lead ownership:

Seller or team owned


Branch routing:

Team ownership supported


Qualification history:

Parented to Lead


Routing model:

Branch territory records determine recommended ownership


Rule:

AXSource solution should not create Business Units automatically.


Rule:

Respect customer organizational hierarchy.

## Data Loss Prevention Strategy

Default DLP posture:

Restrictive by default


Business connector group:

- Microsoft Dataverse
- Microsoft Teams
- Office 365 Outlook
- Approvals
- Microsoft Copilot Studio


Blocked connector group:

- HTTP
- Custom connectors
- Dropbox
- Google Drive
- Twitter/X
- Facebook
- Consumer connectors


Rules:

No custom connector dependency in v1

No anonymous outbound connections

No personal connector usage


Governance rule:

Customer administrators retain ownership of DLP policies.