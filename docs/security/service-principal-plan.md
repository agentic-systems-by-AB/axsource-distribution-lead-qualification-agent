# Service Principal Plan

Status: Pending

Dependency:

P-001 Microsoft admin access partially unavailable

Planned service principal:

axs-distai-pipeline-sp

Purpose:

- GitHub Actions authentication
- Power Platform pipeline execution
- Solution export/import
- Solution Checker execution

Preferred authentication:

OIDC

Fallback:

Client secret

Planned permissions:

Power Platform:

- Environment Maker (DEV)
- System Administrator (DEV)
- Deployment Pipeline Admin

Notes:

Do not use personal credentials for automation.