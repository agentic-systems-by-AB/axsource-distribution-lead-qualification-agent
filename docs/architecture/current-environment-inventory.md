# Current Environment Inventory

Status: Draft

Observed environments:

Sales Trial
Type: Trial

AX5D365AI2026
Type: Sandbox

axt2-sandbox
Type: Sandbox

AX/AGPL_CRM2023
Type: Production

AXSource (default)
Type: Default


Step 0 findings:

Power Platform access:
Verified

Environment creation:
Verified

Dataverse creation:
Verified

Copilot Studio access:
Verified


Pending:

Determine whether existing environments can be reused or whether dedicated ISV environments should be created:

AXS-DISTAI-DEV
AXS-DISTAI-TST
AXS-DISTAI-PRD
AXS-DISTAI-CLEAN
AXS-DISTAI-DEMO

## Managed Environment Findings

Environment reviewed:

AX5D365AI2026

Findings:

Managed Environment:
No

Security Group:
Not assigned

Auditing:
Disabled

Decision:

Do not reuse existing AX environments for ISV product development.

Create dedicated environments for:

- AXS-DISTAI-DEV
- AXS-DISTAI-TST
- AXS-DISTAI-PRD
- AXS-DISTAI-CLEAN
- AXS-DISTAI-DEMO

## Copilot Studio Findings

Environment visibility verified.

Supported environments visible:

- Sales Trial
- axt2-sandbox
- AX5D365AI2026
- AX/AGPL_CRM2023

Default environment:

- AXSource (default)

Decision:

Do not use the default environment for product development.

Dedicated ISV environments remain required.