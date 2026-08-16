# 05 - Azure Virtual Machines

## Overview

This lab focused on deploying and administering **Azure Virtual Machines (VMs)**.

The goal was to gain hands-on experience creating virtual machines, configuring compute, storage, networking, availability, secure connectivity, scaling, and ongoing VM administration.

---

## Objectives

- Create an Azure Virtual Machine
- Review VM sizing options
- Configure OS and data disks
- Configure VM networking
- Connect securely using Azure Bastion
- Understand availability concepts
- Resize an existing VM
- Attach additional disks
- Review Virtual Machine Scale Sets
- Practice VM deployment with PowerShell

---

## Azure Services & Tools Used

- Azure Virtual Machines
- Azure Portal
- Azure PowerShell
- Managed Disks
- Premium SSD
- Virtual Networks
- Network Interfaces
- Azure Bastion
- Availability Sets
- Virtual Machine Scale Sets (VMSS)

---

## Tasks Completed

### Virtual Machine Deployment

Worked through the VM creation process and reviewed the major configuration areas involved in an Azure deployment.

Configuration areas included:

- Subscription and resource group
- VM name
- Azure region
- Availability options
- Image
- VM size
- Administrator account
- Inbound connectivity
- Disk configuration
- Networking
- Management settings
- Advanced options

---

### VM Sizing

Reviewed Azure VM sizes and how CPU, memory, disk, and workload requirements affect VM selection.

This reinforced that VM sizing is both a performance and cost decision.

---

### Managed Disks

Reviewed VM disk options and the role of managed disks in Azure.

Topics included:

- OS disks
- Data disks
- Standard and Premium storage options
- Attaching additional disks

Premium SSD was reviewed as an option for workloads requiring higher disk performance.

---

### Networking

Reviewed the network resources associated with a VM, including:

- Virtual network
- Subnet
- Network interface
- IP configuration
- Inbound connectivity

This reinforced that VM connectivity depends on multiple Azure networking components rather than the VM alone.

---

### Azure Bastion

Reviewed and practiced the use of **Azure Bastion** for secure VM connectivity.

Azure Bastion allows administrators to connect to virtual machines without exposing the VM through a public IP address.

This is useful for reducing direct internet exposure of administrative protocols such as RDP and SSH.

---

### Availability

Reviewed Azure VM availability concepts, including:

- Availability Sets
- Fault Domains
- Update Domains

#### Fault Domains

Distribute VMs across separate physical infrastructure to reduce the impact of hardware or rack-level failure.

#### Update Domains

Separate VMs into logical groups so planned platform maintenance does not affect all instances at the same time.

This reinforced that availability design requires planning for both unplanned hardware failure and planned maintenance.

---

### VM Resizing

Practiced reviewing and changing VM size.

VM resizing allows administrators to adjust compute capacity as workload requirements change.

Considerations include:

- Regional size availability
- Cost
- Workload requirements
- Potential restart or downtime

---

### Additional Data Disks

Reviewed the process of attaching additional managed disks to a VM.

This separates application or data storage from the operating system disk and allows storage capacity to be expanded independently.

---

### Virtual Machine Scale Sets

Reviewed **Virtual Machine Scale Sets (VMSS)** and how they support groups of similar VMs.

VMSS can be used to:

- Deploy multiple VM instances
- Support application scalability
- Automatically increase or decrease instance count
- Improve availability for distributed workloads

The lab reinforced the difference between manually scaling infrastructure and configuring automatic scaling behavior.

---

### PowerShell VM Administration

Reviewed VM deployment and management through Azure PowerShell.

Using PowerShell reinforced how infrastructure tasks can be made more consistent and repeatable than manual portal-only deployment.

---

## Verification

VM-related configurations were verified by reviewing:

- VM deployment status
- Selected VM size
- Disk configuration
- Network configuration
- Bastion connectivity options
- Availability configuration
- Attached disks
- Scale set options

---

## Key Takeaways

- Azure VM deployment requires coordination between compute, storage, and networking.
- VM size should match workload and cost requirements.
- Managed disks simplify VM storage administration.
- Azure Bastion provides secure remote access without requiring a VM public IP.
- Fault Domains protect against physical infrastructure failure.
- Update Domains reduce impact during planned maintenance.
- VM resizing allows compute capacity to change over time.
- Data disks allow storage to scale separately from the OS disk.
- VM Scale Sets support scalable groups of VM instances.
- PowerShell provides a repeatable way to deploy and manage Azure VMs.

---

## Evidence

Supporting files can be stored in:

```text
05-Azure-Virtual-Machines/
├── README.md
├── scripts/
└── screenshots/
```

Future additions may include:

- VM deployment screenshots
- Disk configuration
- Network configuration
- Bastion setup
- Availability settings
- Resize operation
- Additional disk attachment
- VM Scale Set configuration
- PowerShell VM deployment commands

---

[← Back to Azure Home Lab Portfolio](../README.md)
