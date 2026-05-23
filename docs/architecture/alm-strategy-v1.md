# ALM Strategy v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

ALM principles:

- Solution-aware development only
- No work in Default Solution
- Managed environments only
- Managed solution promotion only
- GitHub is source of truth
- No production edits
- Environment-variable driven
- Connection-reference driven
- Quarterly release cadence
- Patch solutions for hotfixes only

Environment topology:

DEV

↓

TEST

↓

PROD

↓

AppSource


## Environment Definitions

AXS-DISTAI-DEV

Purpose:

Builder development environment

Characteristics:

- unmanaged development
- experimentation allowed
- Environment Maker access
- sample data permitted


AXS-DISTAI-TST

Purpose:

Validation and integration testing

Characteristics:

- managed solution imports
- regression validation
- release candidate testing


AXS-DISTAI-PRD

Purpose:

Internal production validation

Characteristics:

- production configuration
- managed solution only
- no direct edits


AXS-DISTAI-CLEAN

Purpose:

Customer install simulation

Characteristics:

- empty baseline
- no manual fixes allowed
- validates package integrity


AXS-DISTAI-DEMO

Purpose:

Demo and showcase environment

Characteristics:

- scripted demonstrations
- sample distributor data
- demo scenarios


## Git Branching Strategy

Primary branches:

main

Purpose:

Production-ready state


develop

Purpose:

Active development


Feature branches:

feature/<name>


Examples:

feature/qualification-history

feature/approval-flow

feature/copilot-topics


Release branches:

release/<version>


Examples:

release/v1.0.0


Hotfix branches:

hotfix/<version>


Examples:

hotfix/v1.0.1


Rules:

- Protect main branch
- Pull requests required into main
- No direct commits to main
- Squash merge feature branches
- One feature per branch