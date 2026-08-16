# 04 - Azure Storage

## Overview

This lab focused on **Azure Storage** and the core services, security controls, redundancy options, access methods, and lifecycle features used to manage cloud-based data.

The goal was to gain hands-on experience creating and configuring storage resources, managing blob and file data, testing authorization methods, and troubleshooting storage access.

---

## Objectives

- Create and configure an Azure Storage account
- Understand storage redundancy options
- Review access tiers
- Configure storage networking and data protection
- Work with blob containers
- Work with Azure Files
- Compare Access Keys, SAS, and Microsoft Entra authorization
- Use lifecycle management
- Review object replication
- Practice AzCopy and storage management tools
- Create and review file share snapshots

---

## Azure Services & Tools Used

- Azure Storage Accounts
- Blob Storage
- Azure Files
- Azure Queues
- Azure Tables
- Azure Portal
- Azure RBAC
- Shared Access Signatures (SAS)
- Access Keys
- Microsoft Entra ID
- Lifecycle Management
- Object Replication
- AzCopy
- Storage Browser / Storage Explorer
- File Share Snapshots

---

## Tasks Completed

### Storage Account Configuration

Created and reviewed an Azure Storage account and explored configuration areas including:

- Redundancy
- Performance
- Networking
- Data protection
- Encryption
- Access configuration

This reinforced that a storage account is the top-level resource used to host multiple Azure Storage services.

---

### Blob Storage

Worked with Azure Blob Storage and created a container named:

```text
finance-reports
```

Uploaded a file to the container and verified that the object was available in storage.

This provided hands-on experience working with object storage in Azure.

---

### Anonymous Access Troubleshooting

During the blob-storage lab, the anonymous-access option was initially unavailable.

### Cause

Anonymous access had to be enabled at the **storage account level** before it could be configured for an individual container.

### Resolution

Enabled the required account-level setting and then continued with the container configuration.

### Learning

Azure features often have both account-level and resource-level dependencies. When a setting is unavailable, upstream configuration should be checked before assuming there is a portal issue.

---

### Storage Authentication

Compared multiple Azure Storage authorization methods.

#### Access Keys

Provide broad access to the storage account and should be protected carefully.

#### Shared Access Signatures (SAS)

Provide temporary, scoped access to storage resources.

A SAS is useful when access should be:

- Limited to a specific resource
- Limited to specific permissions
- Limited by an expiration time

#### Microsoft Entra ID / Azure RBAC

Provides identity-based access without sharing storage account keys.

This is generally preferred for employees and managed identities when supported.

---

### RBAC Testing

Tested storage access with Azure RBAC.

An important observation was that a more restrictive storage role did not appear to prevent write operations because the testing account also inherited **Owner** permissions from a higher scope.

This reinforced the importance of evaluating effective RBAC permissions when testing storage authorization.

---

### Lifecycle Management

Reviewed lifecycle management rules that can automatically move or delete blob data based on conditions such as age.

Use cases include:

- Moving older blobs to cooler tiers
- Archiving infrequently accessed data
- Automatically deleting expired content

---

### Object Replication

Reviewed object replication and how block blobs can be asynchronously copied between storage accounts.

This reinforced the distinction between:

- **Lifecycle Management** — manages data over time
- **Object Replication** — copies data between storage accounts

---

### AzCopy

Reviewed AzCopy as a command-line utility for transferring data to and from Azure Storage.

AzCopy is useful for:

- Large file transfers
- Scripted data movement
- Bulk migration
- Automation

---

### Azure Files and Snapshots

Worked with Azure Files concepts and reviewed file-share snapshots.

Snapshots provide a point-in-time copy of a file share and can support recovery from accidental changes or deletion.

---

## Storage Tool Selection

Different tools are appropriate for different scenarios:

```text
Temporary external access
→ SAS

Employee identity-based access
→ Microsoft Entra ID + RBAC

Full storage account access
→ Access Keys (use carefully)

Bulk command-line transfer
→ AzCopy

Interactive storage management
→ Storage Explorer / Storage Browser
```

---

## Verification

Storage configurations were verified by:

- Reviewing storage account settings
- Creating the `finance-reports` blob container
- Uploading data successfully
- Testing authentication methods
- Reviewing RBAC behavior
- Validating storage feature settings
- Reviewing lifecycle and replication options

---

## Key Takeaways

- Azure Storage supports multiple data services under one storage account.
- Authorization method should match the access requirement.
- SAS is useful for temporary, scoped access.
- Microsoft Entra ID and RBAC provide identity-based authorization.
- Access Keys provide broad access and should be protected.
- Higher-scope RBAC assignments can affect storage permission testing.
- Lifecycle Management automates data aging.
- Object Replication copies block blobs between storage accounts.
- AzCopy is useful for bulk data movement.
- Account-level settings can control whether lower-level features are available.

---

## Evidence

Supporting files can be stored in:

```text
04-Azure-Storage/
├── README.md
├── scripts/
└── screenshots/
```

Future additions may include:

- Storage account configuration screenshots
- `finance-reports` container
- Blob upload verification
- SAS configuration examples
- RBAC testing
- Lifecycle management rules
- Object replication settings
- File share snapshots

---

[← Back to Azure Home Lab Portfolio](../README.md)
