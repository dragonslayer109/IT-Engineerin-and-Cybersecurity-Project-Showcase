# Microsoft 365 User Onboarding & Office Template Automation

> Part of the [IT Engineering & Cybersecurity Project Showcase](https://github.com/dragonslayer109/IT-Engineerin-and-Cybersecurity-Project-Showcase)

## Overview

This project is an end-to-end Microsoft 365 user onboarding automation workflow, built to reduce repetitive administrative work, improve consistency, and simplify the provisioning of new users.

The solution uses **PowerShell**, **Microsoft 365**, **SharePoint**, **Microsoft Entra ID**, and **Microsoft Intune** to automate several stages of onboarding — from assigning the right access through to configuring Microsoft Office templates on the user's workstation.

It was developed from a real-world IT support and administration workflow and is documented here as a sanitised portfolio project, to demonstrate practical experience with Microsoft 365 administration, automation, endpoint management, identity, and process improvement.

---

## Objectives

- Reduce repetitive Microsoft 365 administration
- Improve consistency when provisioning new users
- Reduce the possibility of configuration errors
- Automate SharePoint access through group membership
- Ensure required SharePoint content is available to the user
- Automatically deploy the required Word and PowerPoint templates
- Reduce the amount of technician time required per onboarding
- Create a repeatable, scalable onboarding process
- Demonstrate practical PowerShell automation in a Microsoft 365 environment

---

## Solution Overview

```
New User
   │
   ▼
PowerShell Onboarding Script
   │
   ▼
Microsoft 365 Group Assignment
   │
   ▼
Group-Based SharePoint Access
   │
   ▼
SharePoint / OneDrive Sync to User's PC
   │
   ▼
Microsoft Intune Deployment
   │
   ▼
Office Template Configuration (Word & PowerPoint)
   │
   ▼
Technician Validation
```

The automation removes a number of repetitive configuration steps that would otherwise need to be performed manually for every new user.

---

## Technologies Used

| Technology | Purpose |
|---|---|
| PowerShell | User onboarding and automation |
| Microsoft 365 | Identity, licensing and productivity services |
| Microsoft Entra ID | Identity and group-based access |
| SharePoint Online | Centralised storage and access to templates |
| Microsoft Intune | Endpoint configuration and script deployment |
| Microsoft Word | Corporate document templates |
| Microsoft PowerPoint | Corporate presentation templates |
| OneDrive | Synchronisation of user and SharePoint content |

---

## How It Works

### 1. User Onboarding
PowerShell automates the initial onboarding process and assigns the new user to the appropriate Microsoft 365 group — providing the required access without the technician manually configuring individual SharePoint permissions.

### 2. Group-Based SharePoint Access
The user's group membership grants access to the required SharePoint resources, creating a consistent access model and removing the need to configure permissions per user.

### 3. SharePoint & OneDrive Synchronisation
Once access is established, the required SharePoint content syncs to the user's workstation, giving them the centralised resources needed for their role.

### 4. Intune Template Deployment
Microsoft Intune deploys a PowerShell-based configuration script to the user's workstation, replacing the standard/blank Word and PowerPoint templates with the organisation's required templates stored in SharePoint — removing another manual step from onboarding.

### 5. Technician Validation
The repetitive configuration is automated, but a human validation stage remains. The technician still:

- Completes account creation
- Assigns licences
- Signs the user into Windows, Entra ID and Microsoft 365
- Completes initial Office configuration
- Tests Word and PowerPoint
- Confirms SharePoint and OneDrive functionality
- Troubleshoots any unexpected issues

---

## Before vs. After

### Manual Process (Before Automation)

The complete onboarding workflow could involve:

- Creating the user
- Assigning licences
- Configuring permissions
- Setting up the workstation
- Signing into Microsoft 365
- Configuring OneDrive
- Configuring SharePoint
- Synchronising required content
- Uploading and configuring templates
- Testing the environment
- Troubleshooting configuration issues

For a medium-complexity Microsoft 365 environment, this is estimated at **~3 hours per user**, depending on the environment and issues encountered.

### Automated Process (After Automation)

| Remaining Task | Typical Time |
|---|---|
| Create user account | 5–10 min |
| Assign licences | 5–10 min |
| Windows / Entra ID / M365 sign-in & initial setup | 5–10 min |
| First-time Office / M365 setup | 1–5 min |
| Test Word / PowerPoint / SharePoint / OneDrive | 1–5 min |
| Troubleshooting / unexpected issues | 5–10+ min |
| **Estimated remaining hands-on time** | **~35–40 min** |

Using the midpoint of these estimates, remaining technician involvement is approximately **36 minutes per user**.

### Estimated Impact

| | Before | After |
|---|---|---|
| Time per user | ~3 hours | ~35–40 min |

**Estimated time saved: ~2 hours 20–25 minutes per user (~78–81% reduction in hands-on onboarding time).**

> These figures are estimates based on the workflow described above and should be validated against actual onboarding measurements once sufficient production data is available.

---

## Business Value

**Reduced technician time** — a significant share of repetitive onboarding work runs automatically, freeing technicians for higher-value support and engineering tasks.

**Improved consistency** — a repeatable, automated process reduces the risk of users ending up with different configurations due to manual variation.

**Fewer configuration errors** — group-based access and scripted configuration cut down on manual permission and setup steps.

**Faster user readiness** — users reach a usable, consistently configured Microsoft 365 environment with less technician intervention.

**Scalability** — the workflow can be reused as onboarding volume grows, without a proportional increase in manual administrative effort.

### Example Time Savings at Scale

| Users | Estimated Manual Time | Estimated Post-Automation Time | Estimated Time Saved |
|---|---|---|---|
| 25 | 75 hrs | ~15 hrs | ~60 hrs |
| 50 | 150 hrs | ~30 hrs | ~120 hrs |
| 100 | 300 hrs | ~60 hrs | ~240 hrs |
| 200 | 600 hrs | ~120 hrs | ~480 hrs |

> Illustrative figures, based on the estimated ~3-hour manual workflow and ~36-minute post-automation workflow above.