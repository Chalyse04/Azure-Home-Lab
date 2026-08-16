# 03 - Azure Governance & Policy

## Overview

This lab focused on **Azure governance** and the tools administrators use to organize, protect, control, and standardize Azure resources.

The goal was to gain hands-on experience with subscriptions, resource groups, tags, resource locks, Azure Policy, and management groups while understanding how governance controls are applied at scale.

---

## Objectives

- Review subscription-level administration
- Work with resource groups
- Apply and manage tags
- Configure resource locks
- Understand Azure Policy
- Assign policy at the appropriate scope
- Review resource movement between resource groups
- Understand management groups
- Practice governance tasks with PowerShell

---

## Azure Services & Tools Used

- Azure Portal
- Azure PowerShell
- Azure Policy
- Resource Groups
- Resource Locks
- Tags
- Subscriptions
- Management Groups
- Cost Management

---

## Tasks Completed

### Subscription Administration

Reviewed the Azure subscription dashboard and how subscriptions provide a boundary for:

- Billing
- Resource organization
- Access control
- Policy assignment
- Cost management

This reinforced the relationship between subscriptions, resource groups, and individual Azure resources.

---

### Cost Management

Reviewed Azure Cost Management features and how administrators can monitor spending and resource consumption.

This reinforced that Azure administration includes both technical configuration and cost awareness.

---

### Resource Locks

Worked with Azure resource locks to protect important resources from accidental changes.

Reviewed the two primary lock types:

- **CanNotDelete** — prevents deletion
- **ReadOnly** — prevents changes and deletion

The lab reinforced that locks can be inherited by child resources depending on where they are applied.

---

### Tags

Used tags to organize Azure resources with metadata.

Common tagging use cases include:

- Environment
- Department
- Owner
- Application
- Cost center

Tags support governance, reporting, organization, and cost tracking.

---

### Azure Policy

Worked with Azure Policy to understand how organizations enforce standards across Azure environments.

Policy can be used to:

- Audit configurations
- Deny noncompliant deployments
- Require specific settings
- Enforce organizational standards

The lab included applying policy and reviewing how policy scope affects the resources evaluated.

---

### PowerShell Governance Tasks

Used PowerShell during governance exercises when portal-based configuration was limited or when command-line practice provided a more repeatable administration method.

This reinforced the value of automation for governance at scale.

---

### Moving Azure Resources

Reviewed resource movement between resource groups and the considerations administrators should validate before moving resources.

This reinforced that Azure resources are organized logically through subscriptions and resource groups, while dependencies can affect whether a move is supported.

---

### Management Groups

Reviewed management groups and how they allow governance to be applied above the subscription level.

Hierarchy example:

```text
Management Group
      ↓
Subscriptions
      ↓
Resource Groups
      ↓
Resources
```

Management groups are especially useful in larger organizations that operate multiple Azure subscriptions.

---

## Governance Concepts Reinforced

### Azure Policy vs Azure RBAC

These services solve different problems:

```text
Azure RBAC
Who can perform an action?

Azure Policy
What configurations are allowed?
```

RBAC manages **authorization**, while Policy manages **resource compliance and standards**.

---

## Verification

Governance configurations were reviewed through the Azure portal and PowerShell by validating:

- Policy assignment and scope
- Resource lock configuration
- Tag assignments
- Subscription organization
- Resource group placement
- Management hierarchy concepts

---

## Key Takeaways

- Azure governance helps organizations manage resources consistently and safely.
- Resource locks protect against accidental modification or deletion.
- Tags improve organization, reporting, and cost tracking.
- Azure Policy enforces or audits resource configuration standards.
- RBAC and Policy serve different governance purposes.
- Management groups allow governance across multiple subscriptions.
- PowerShell makes governance tasks more repeatable.

---

## Evidence

Supporting files can be stored in:

```text
03-Azure-Governance/
├── README.md
├── scripts/
└── screenshots/
```

Future additions may include:

- Azure Policy screenshots
- PowerShell policy commands
- Resource lock examples
- Tag configuration
- Subscription and management group screenshots

---

[← Back to Azure Home Lab Portfolio](../README.md)
