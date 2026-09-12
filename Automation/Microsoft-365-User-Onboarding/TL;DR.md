# Microsoft 365 User Onboarding & Office Template Automation

> Part of the [IT Engineering & Cybersecurity Project Showcase](https://github.com/dragonslayer109/IT-Engineerin-and-Cybersecurity-Project-Showcase)

An end-to-end Microsoft 365 onboarding automation that cuts new-user setup time by an estimated **~80%**, using PowerShell, Entra ID, SharePoint, and Intune.

Built from a real-world production workflow and documented here as a sanitised portfolio project. **Source code is private** — happy to walk through it in an interview.

---

## The Problem

Manually onboarding a new Microsoft 365 user — permissions, SharePoint access, workstation sync, Office templates — took roughly **3 hours** of hands-on technician time per user, with configuration steps easy to miss or apply inconsistently.

## The Solution

A PowerShell-driven workflow that automates the repetitive parts of onboarding end-to-end:

```
New User → M365 Group Assignment → SharePoint Access (group-based)
   → SharePoint/OneDrive Sync → Intune Deployment
   → Word/PowerPoint Templates Configured → Technician Validation
```

**Tech stack:** PowerShell · Microsoft 365 · Entra ID · SharePoint Online · Microsoft Intune

Access is granted through group membership rather than manual per-user permissions, and Intune pushes a script that swaps in the correct Word/PowerPoint templates automatically — so a new user lands on a fully configured, correctly permissioned machine with far less manual setup.

A technician still validates the account at the end (licensing, sign-in, quick functionality checks), but the bulk of the repetitive configuration work is gone.

## Impact

| | Before | After |
|---|---|---|
| Technician time per user | ~3 hours | ~35–40 min |
| **Time saved** | | **~80% reduction** |

At scale, that's roughly **240 hours saved per 100 onboardings** — time technicians can put toward higher-value support and engineering work instead of repetitive setup.

*Figures are estimates based on the workflow above, pending validation against production data.*

## Why It Matters

- **Consistency** — every user gets the same configuration, every time
- **Fewer errors** — group-based access removes manual permission mistakes
- **Scalable** — handles 10 onboardings or 200 without added technician effort

---

## TL;DR

Built a PowerShell + Microsoft 365 automation that takes new-user onboarding from ~3 hours to ~35 minutes (~80% faster) by automating group-based SharePoint access and Intune-deployed Office templates. Source is private; happy to demo/discuss in an interview.
