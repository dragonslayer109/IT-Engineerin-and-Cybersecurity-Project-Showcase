# Microsoft 365 User Onboarding & Office Template Automation

## Overview

This project automates multiple stages of the Microsoft 365 user onboarding process using PowerShell, Microsoft 365, SharePoint Online and Microsoft Intune.

The solution was designed to reduce manual configuration during user onboarding while ensuring that new users receive the appropriate SharePoint access and standardised Microsoft Office templates.

The automation combines identity and access management, SharePoint permissions, endpoint management and PowerShell automation into a single onboarding workflow.

---

## Objectives

The primary objectives of the solution were to:

- Reduce manual steps during user onboarding
- Standardise SharePoint access for new users
- Automatically provide users with the resources required for their role
- Ensure corporate Microsoft Word and PowerPoint templates are deployed consistently
- Reduce the possibility of configuration errors
- Improve the overall consistency and efficiency of the onboarding process

---

## Solution Overview

The onboarding process follows the workflow below:

New User
↓
PowerShell User Onboarding
↓
User Added to Appropriate Microsoft 365 Group
↓
Group-Based SharePoint Access
↓
SharePoint Resources Available to User
↓
Resources Synchronise to User's PC
↓
Microsoft Intune Deployment
↓
Office Templates Configured
↓
User Ready to Work

---

## Technologies Used

| Technology | Purpose |
|---|---|
| PowerShell | User onboarding and automation |
| Microsoft 365 | Identity and collaboration platform |
| Microsoft Entra ID | User and group management |
| SharePoint Online | Document storage and access management |
| Microsoft Intune | Endpoint configuration and script deployment |
| Microsoft Word | Corporate document templates |
| Microsoft PowerPoint | Corporate presentation templates |

---

## Key Components

### 1. User Onboarding Automation

PowerShell is used to automate the initial onboarding process.

The script adds the new user to the appropriate Microsoft 365 group based on the required access.

This removes the need to manually configure individual user access where group-based access can be used instead.

---

### 2. Group-Based SharePoint Access

The Microsoft 365 group is associated with the required SharePoint resources.

Once the user is added to the appropriate group, the required SharePoint access is automatically inherited.

This provides a more scalable and manageable approach to access management compared with manually assigning permissions to individual users.

---

### 3. SharePoint Synchronisation

The required SharePoint resources are made available on the user's workstation through synchronisation.

This allows users to access the required company resources directly from their workstation without requiring additional manual configuration during onboarding.

---

### 4. Intune Template Deployment

Microsoft Intune is used to deploy a PowerShell script to the user's workstation.

The script configures the default Microsoft Word and PowerPoint templates so that users receive the approved corporate templates.

This ensures that newly onboarded users begin working with the correct standardised templates without requiring manual configuration.

---

## Automation Workflow

```text
                    ┌─────────────────┐
                    │    New User     │
                    └────────┬────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ PowerShell Onboarding│
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ Microsoft 365 Group  │
                  │    Assignment        │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │   SharePoint Access  │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │ SharePoint Sync to   │
                  │      Workstation     │
                  └──────────┬───────────┘
                             │
                             ▼
                  ┌──────────────────────┐
                  │    Microsoft Intune  │
                  │    Script Deployment │
                  └──────────┬───────────┘
                             │
                             ▼
              ┌──────────────────────────────┐
              │ Word & PowerPoint Templates  │
              │       Automatically Set       │
              └──────────────────────────────┘
