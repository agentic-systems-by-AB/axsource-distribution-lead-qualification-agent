# Power Platform Components v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

Design principles:

- Environment-variable driven
- Connection-reference driven
- No hardcoded tenant values
- Human approval before external action
- Managed solution compatible
- Customer tenant execution only

Component categories:

- Power Automate flows
- Environment variables
- Connection references
- Dataverse interactions
- Approval orchestration

## Power Automate Flow Inventory

Flow 1

Name:

Lead Qualification Trigger

Trigger:

Lead create or update

Purpose:

Start qualification orchestration


Flow 2

Name:

Channel Conflict Review

Trigger:

Qualification execution

Purpose:

Detect conflicts and agreements


Flow 3

Name:

Credit Eligibility Review

Trigger:

Qualification execution

Purpose:

Evaluate internal customer credit indicators


Flow 4

Name:

Approval Workflow

Trigger:

Agent recommendation requiring approval

Purpose:

Request seller confirmation


Flow 5

Name:

Draft Outreach Workflow

Trigger:

Approved recommendation

Purpose:

Generate seller-reviewed outreach draft


Flow 6

Name:

Qualification Audit Workflow

Trigger:

Qualification completion

Purpose:

Persist qualification artifacts