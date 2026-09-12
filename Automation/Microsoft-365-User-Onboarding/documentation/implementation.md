# Implementation Notes

> Source code is private. This describes the approach at a high level only.

## Onboarding Script

- Triggered when a new user account is created.
- Assigns the user to a pre-defined Microsoft 365 security group tied to their role.
- Group membership drives SharePoint access automatically — no manual permission steps.

## Template Deployment Script

- Packaged and deployed via Microsoft Intune to the user's device.
- Detects the default/blank Word and PowerPoint templates and replaces them with the organisation's versions, pulled from a central SharePoint location.
- Runs as part of standard endpoint provisioning, requiring no manual technician action on the device itself.

## Testing Approach

- Validated against a small group of test accounts before rollout.
- Checked group assignment, SharePoint access, and template deployment independently before confirming end-to-end behaviour.
- Rolled out gradually to production users after validation.
