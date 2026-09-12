# Architecture

## Components

| Component | Role |
|---|---|
| PowerShell | Orchestrates onboarding and Intune deployment scripts |
| Microsoft Entra ID | Identity and group-based access control |
| SharePoint Online | Central store for corporate templates and resources |
| Microsoft Intune | Deploys endpoint configuration script |
| OneDrive | Syncs SharePoint content to the user's device |

## Flow

See [`diagrams/onboarding-workflow.png`](../diagrams/onboarding-workflow.png) for the full visual.

1. New user is created in Microsoft 365.
2. PowerShell assigns the user to the relevant security group.
3. Group membership grants SharePoint access — no manual per-user permissions.
4. SharePoint/OneDrive content syncs to the user's PC.
5. Intune pushes a configuration script to the endpoint.
6. The script replaces default Word/PowerPoint templates with the organisation's SharePoint-hosted versions.
7. Technician performs final validation (licensing, sign-in, quick functional checks).

## Design Choices

- **Group-based access over individual permissions** — reduces manual configuration and permission drift.
- **Intune for template deployment** — keeps template management centralised in SharePoint rather than baked into images or manual copy/paste.
- **Human validation retained** — automation removes repetitive setup, not the final quality check.
