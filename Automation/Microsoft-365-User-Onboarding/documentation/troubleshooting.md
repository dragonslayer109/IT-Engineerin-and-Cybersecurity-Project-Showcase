# Troubleshooting & Lessons Learned

A few things worth noting from building and running this in production:

- **Sync timing matters.** SharePoint/OneDrive sync isn't instant — the workflow accounts for a short delay before checking that content has landed on the device.
- **Group propagation delay.** Microsoft 365 group membership can take a few minutes to propagate; scripts that assume instant access can fail intermittently if run too early.
- **Template locking.** If Word/PowerPoint is already open when the deployment script runs, template replacement can fail silently — the script checks for this before proceeding.
- **Keep validation manual.** Automating the setup steps was straightforward; deliberately keeping a human validation step at the end caught edge cases that would have been costly to fully automate.

## What I'd Improve Next

- Add automated logging/reporting so onboarding status is visible without checking each device manually.
- Extend group-based access to cover a wider range of role-specific SharePoint sites.
