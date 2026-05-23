# Environment Strategy

Status: Draft

Environment topology:

DEV
AXS-DISTAI-DEV

TEST
AXS-DISTAI-TST

PROD
AXS-DISTAI-PRD

CLEAN INSTALL
AXS-DISTAI-CLEAN

DEMO
AXS-DISTAI-DEMO

Purpose:

DEV:
Build and experimentation

TEST:
Managed solution validation

PROD:
Release candidate and AppSource packaging

CLEAN:
Simulate customer installation

DEMO:
Scripted showcase environment

Rules:

- No work in default solution
- No direct production edits
- Managed solution promotion only
- Customer-install validation mandatory

## Dedicated Environment Provisioning Findings

Environment creation:

Verified

Dataverse creation:

Verified

Security group assignment:

Supported

Dynamics 365 apps:

Supported

Sample data:

Optional

Pay-as-you-go with Azure:

Disabled

Decision:

Create dedicated environments only.

Planned environments:

- AXS-DISTAI-DEV
- AXS-DISTAI-TST
- AXS-DISTAI-PRD
- AXS-DISTAI-CLEAN
- AXS-DISTAI-DEMO

Future DEV environment settings:

Dataverse:
Enabled

Dynamics apps:
Enabled

Sample data:
No