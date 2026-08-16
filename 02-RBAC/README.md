# 02 - Azure Role-Based Access Control (RBAC)

## Overview

This lab focused on **Azure Role-Based Access Control (RBAC)** and how permissions are assigned to users, groups, and identities across Azure resources.

The goal was to build hands-on experience with Azure authorization, understand role scope and inheritance, and practice assigning built-in roles using both the Azure portal and PowerShell.

---

## Objectives

- Understand how Azure RBAC controls authorization
- Review built-in Azure roles
- Assign roles at different scopes
- Understand subscription, resource group, and resource scope
- Practice least-privilege access
- Assign RBAC roles using PowerShell
- Interpret effective access and inherited permissions

---

## Azure Services & Tools Used

- Azure Role-Based Access Control (RBAC)
- Azure Portal
- Azure PowerShell
- Azure Resource Groups
- Azure Storage
- Microsoft Entra ID

---

## Tasks Completed

### RBAC Fundamentals

Reviewed how Azure RBAC determines what an authenticated identity is allowed to do within Azure.

A role assignment combines three components:

```text
Security Principal
      +
Role Definition
      +
Scope
      =
Role Assignment
```

This reinforced the difference between authentication and authorization:

- **Microsoft Entra ID** confirms identity.
- **Azure RBAC** controls access to Azure resources.

---

### Built-In Roles

Worked with common built-in Azure roles and reviewed the permissions associated with each.

Examples included:

- Reader
- Contributor
- Owner
- Storage Blob Data Reader

The lab reinforced that broad roles should only be used when required.

---

### Scope and Inheritance

Reviewed the Azure scope hierarchy:

```text
Management Group
      ↓
Subscription
      ↓
Resource Group
      ↓
Resource
```

Role assignments made at a higher scope can be inherited by lower-level resources.

This became especially important during testing because inherited permissions can affect the results of access-control labs.

---

### PowerShell Role Assignments

Used Azure PowerShell to assign permissions at the **resource group scope**.

Hands-on work included assigning roles such as:

- Storage Blob Data Reader
- Contributor

This provided experience performing access-control tasks outside of the Azure portal.

---

## Troubleshooting / Key Observation

During access testing, an identity with a lower-level read role was still able to perform write actions.

### Cause

The account already had **Owner** permissions inherited from a higher scope.

### Learning

A lower-level role assignment does not remove broader permissions inherited from another scope.

When troubleshooting Azure RBAC, effective access must be evaluated across **all applicable role assignments**, not just the role being tested.

---

## Least Privilege

A major focus of this lab was applying the principle of least privilege.

Examples:

- Use **Reader** when modification is unnecessary.
- Use data-plane roles such as **Storage Blob Data Reader** for specific storage access.
- Avoid assigning **Owner** or **Contributor** when a narrower role will meet the requirement.
- Assign roles at the lowest appropriate scope.

---

## Verification

Role assignments were verified by reviewing:

- Assigned role
- Security principal
- Assignment scope
- Inherited permissions
- Effective access behavior

PowerShell and Azure portal results were compared to confirm the role assignments were applied.

---

## Key Takeaways

- Azure RBAC controls authorization to Azure resources.
- Role assignments consist of a principal, role definition, and scope.
- Permissions can be inherited from higher scopes.
- Effective permissions may include multiple role assignments.
- Broad inherited permissions can affect lab testing.
- Least privilege should guide both role selection and assignment scope.
- PowerShell provides a repeatable way to manage Azure access.

---

## Evidence

Supporting files can be stored in:

```text
02-RBAC/
├── README.md
├── scripts/
└── screenshots/
```

Future additions may include:

- PowerShell role-assignment commands
- Role assignment screenshots
- Access-control verification
- Effective-access examples

---

[← Back to Azure Home Lab Portfolio](../README.md)
