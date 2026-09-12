# IT Engineering & Cybersecurity Project Showcase

## Microsoft 365 User Onboarding & Office Template Automation

### Overview

This project demonstrates an end-to-end Microsoft 365 user onboarding automation workflow designed to reduce repetitive administrative work, improve consistency, and simplify the provisioning of new users.

The solution uses PowerShell, Microsoft 365, SharePoint, Microsoft Entra ID, and Microsoft Intune to automate several stages of the onboarding process, from assigning the appropriate access through to configuring Microsoft Office templates on the user's workstation.

The project was developed from a real-world IT support and administration workflow and has been documented as a sanitised portfolio project to demonstrate practical experience with Microsoft 365 administration, automation, endpoint management, identity, and process improvement.

---

## Objectives

The primary objectives of the automation are to:

- Reduce repetitive Microsoft 365 administration
- Improve consistency when provisioning new users
- Reduce the possibility of configuration errors
- Automate SharePoint access through group membership
- Ensure required SharePoint content is available to the user
- Automatically deploy the required Microsoft Word and PowerPoint templates
- Reduce the amount of technician time required for each onboarding
- Create a repeatable and scalable onboarding process
- Demonstrate practical PowerShell automation in a Microsoft 365 environment

---

## Solution Overview

The onboarding workflow combines several Microsoft technologies into a single process:

```text
New User
   │
   ▼
PowerShell Onboarding
   │
   ├── Microsoft 365 User
   │
   └── Group Assignment
          │
          ▼
   SharePoint Access
          │
          ▼
   SharePoint Sync
          │
          ▼
   User's PC
          │
          ▼
   Microsoft Intune
          │
          ▼
   Office Template Deployment
          │
          ├── Microsoft Word
          │
          └── Microsoft PowerPoint
          │
          ▼
   Technician Validation

   The automation removes a number of repetitive configuration steps that would otherwise need to be performed manually for every new user.

Technologies Used
Technology	Purpose
PowerShell	User onboarding and automation
Microsoft 365	Identity, licensing and productivity services
Microsoft Entra ID	Identity and group-based access
SharePoint Online	Centralised storage and access to templates
Microsoft Intune	Endpoint configuration and script deployment
Microsoft Word	Corporate document templates
Microsoft PowerPoint	Corporate presentation templates
OneDrive	Synchronisation of user and SharePoint content
Automated Workflow
1. User Onboarding

PowerShell is used to automate the initial onboarding process and assign the new user to the appropriate Microsoft 365 group.

The group provides the required access without requiring the technician to manually configure individual SharePoint permissions.

2. Group-Based SharePoint Access

The user's group membership provides access to the required SharePoint resources.

This creates a more consistent access model and reduces the need for technicians to manually configure permissions for each individual user.

3. SharePoint and OneDrive Synchronisation

Once access has been established, the required SharePoint content can be synchronised to the user's workstation.

This provides the user with access to the centralised resources required for their role.

4. Intune Template Deployment

Microsoft Intune is used to deploy a PowerShell-based configuration script to the user's workstation.

The script replaces the relevant standard and blank Microsoft Word and PowerPoint templates with the organisation's required templates stored within SharePoint.

This removes another manual configuration step from the onboarding process.

5. Validation

Although the repetitive configuration has been automated, the technician still performs final validation.

The remaining process includes:

Completing the required account creation
Assigning licences
Signing into Windows, Entra ID and Microsoft 365
Completing initial Office configuration
Testing Word and PowerPoint
Confirming SharePoint and OneDrive functionality
Troubleshooting unexpected issues

This approach maintains a human validation stage while removing much of the repetitive provisioning work.

Before vs After

One of the primary benefits of the project is the reduction in hands-on technician time.

Manual Process

Before automation, the complete onboarding workflow could involve:

Creating the user
Assigning licences
Configuring permissions
Setting up the workstation
Signing into Microsoft 365
Configuring OneDrive
Configuring SharePoint
Synchronising required content
Uploading and configuring templates
Testing the environment
Troubleshooting configuration issues

For a medium-complexity Microsoft 365 environment, this workflow is estimated at approximately 3 hours per user, depending on the environment and issues encountered.

Automated Process

After implementing the automation, the remaining technician work is approximately:

Remaining Task	Typical Time
Create user account	5–10 min
Assign licences	5–10 min
Windows/Entra/M365 sign-in & initial setup	5–10 min
First-time Office/M365 setup	1–5 min
Test Word/PowerPoint/SharePoint/OneDrive	1–5 min
Troubleshooting / unexpected issues	5–10+ min
Estimated remaining hands-on time	~35–40 min

Using the midpoint of these estimates, the remaining technician involvement is approximately 36 minutes per user.

Estimated Impact

Using approximately 3 hours before automation and 35–40 minutes after automation:

Estimated time saved: approximately 2 hours 20 minutes – 2 hours 25 minutes per user.

This represents an estimated 78–81% reduction in hands-on onboarding time.

These figures are estimates based on the workflow and should be validated against actual onboarding measurements when sufficient production data is available.

Business Value

The automation provides several operational benefits.

Reduced Technician Time

A significant portion of repetitive onboarding work is performed automatically, allowing technicians to spend more time on higher-value support and engineering tasks.

Improved Consistency

Using a repeatable automated process reduces the likelihood of users receiving different configurations due to manual variations.

Reduced Configuration Errors

Group-based access and scripted configuration reduce the number of manual permission and configuration steps.

Faster User Readiness

Users can reach a usable and consistently configured Microsoft 365 environment with less technician intervention.

Scalability

The automated workflow can be reused as the number of onboardings increases without requiring a proportional increase in manual administrative effort.

Example Time Savings
Users	Estimated Manual Time	Estimated Post-Automation Time	Estimated Time Saved
25	75 hrs	~15 hrs	~60 hrs
50	150 hrs	~30 hrs	~120 hrs
100	300 hrs	~60 hrs	~240 hrs
200	600 hrs	~120 hrs	~480 hrs

These figures are illustrative and are based on the estimated 3-hour manual workflow and approximately 36-minute post-automation workflow.