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