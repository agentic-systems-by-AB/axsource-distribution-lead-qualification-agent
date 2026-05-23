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


## GitHub Actions Pipeline Design

Pipeline 1

Name:

solution-export.yml

Purpose:

Export unmanaged solution from DEV


Pipeline 2

Name:

solution-unpack.yml

Purpose:

Unpack solution into source control


Pipeline 3

Name:

solution-checker.yml

Purpose:

Run Power Platform Solution Checker


Pipeline 4

Name:

managed-build.yml

Purpose:

Create managed solution package


Pipeline 5

Name:

import-test.yml

Purpose:

Import managed solution into TEST


Pipeline 6

Name:

import-clean.yml

Purpose:

Import managed solution into CLEAN


Pipeline 7

Name:

release-package.yml

Purpose:

Create AppSource release artifacts


Rule:

Pipeline execution uses service principal authentication only.