# Known Issues

Version: 1.0.0

Current Status

No blocking production issues identified.

Resolved During v1 Development

## 1. Tool parameter drift

Issue

Copilot orchestration incorrectly mapped values across tools.

Examples:

LeadId = Qualified

QualificationOutcome = Not Required

Resolution

Input descriptions hardened.

Tool contracts standardized.

---

## 2. Dataverse Choice conversion failures

Issue

Choice fields expected Integer values while tools returned labels.

Examples:

Qualified

Not Required

Resolution

Added explicit conversion mappings.

---

## 3. Routing recommendation contract drift

Issue

Narrative responses replaced structured routing outputs.

Resolution

Routing outputs constrained to approved values.

---

## 4. Confidence score remained static

Issue

Risk evaluation logic always returned Low.

Resolution

Signal analysis updated to generate ReviewRisk.

---

## 5. User prompt interruptions

Issue

Agent requested values already available from prior tools.

Examples:

BranchTerritory

QualificationScore

Resolution

Tool descriptions and orchestration instructions hardened.