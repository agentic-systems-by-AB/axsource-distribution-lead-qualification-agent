# Telemetry and Analytics v1

Status: Draft

Product:

AXSource Distribution Lead Qualification Agent

Telemetry principles:

- Customer-owned telemetry
- No centralized AXSource telemetry
- Support-focused diagnostics
- Business outcome visibility
- Low operational overhead
- Privacy-first analytics

Telemetry categories:

- Copilot analytics
- Qualification telemetry
- Workflow telemetry
- Business KPIs
- Support diagnostics

## Copilot Studio Analytics

Primary analytics source:

Copilot Studio analytics dashboard


Metrics:

- Agent sessions
- Active users
- Topic usage
- Prompt usage
- Completion rate
- Escalation rate
- Approval request count
- Confidence distribution


Purpose:

Measure agent usage and adoption


Ownership:

Customer tenant


Rule:

AXSource does not receive analytics automatically.

## Qualification Telemetry

Qualification metrics:

- Qualification executions
- Qualification completion rate
- Qualification score distribution
- Confidence score distribution
- Branch recommendation frequency
- Channel classification distribution
- Conflict detection count
- Credit eligibility outcomes


Persisted sources:

- axs_QualificationHistory
- Dataverse audit data


Purpose:

Measure qualification behavior and recommendation patterns


Rule:

Telemetry must support explainability and troubleshooting.