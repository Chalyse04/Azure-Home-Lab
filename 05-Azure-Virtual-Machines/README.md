# Azure Virtual Machines

## Project Summary

This lab focused on deploying and administering **Azure Virtual Machines (VMs)** and the supporting compute, storage, networking, availability, and connectivity components required to operate virtual workloads in Azure.

The project covered VM creation, sizing, managed disks, networking, Azure Bastion, Availability Sets, Fault Domains, Update Domains, VM resizing, additional data disks, Virtual Machine Scale Sets (VMSS), and Azure PowerShell.

The lab reinforced how multiple Azure services work together to provide a secure and scalable virtual-machine environment.

---

## Scenario

An organization needs to deploy virtual servers in Azure while maintaining secure administrative access, appropriate performance, storage flexibility, and availability.

As the Azure administrator, I was responsible for deploying and reviewing the virtual-machine environment, selecting appropriate compute and disk options, configuring connectivity, evaluating availability protections, and reviewing scaling options for future workload growth.

The environment needed to support the following requirements:

- Deploy an Azure virtual machine.
- Select compute resources appropriate for the workload.
- Configure OS and data storage.
- Review the virtual network components supporting the VM.
- Provide secure administrative connectivity without requiring direct public exposure.
- Understand protections against hardware failure and planned maintenance.
- Resize VM compute resources as requirements change.
- Add storage independently from the OS disk.
- Review horizontal scaling using Virtual Machine Scale Sets.
- Practice VM administration through Azure PowerShell.

---

## Workflow

### 1. Created the Azure Virtual Machine

Worked through the Azure VM deployment process and configured the major deployment options, including:

- Subscription and resource group.
- VM name.
- Azure region.
- Availability options.
- Operating system image.
- VM size.
- Administrator credentials.
- Inbound connectivity.
- Disk configuration.
- Networking.
- Management settings.
- Advanced options.

**Result:** Deployed and reviewed the core components required to provision an Azure virtual machine.

---

### 2. Reviewed VM Sizing

Reviewed Azure VM size options and evaluated how the following factors affect VM selection:

- CPU.
- Memory.
- Disk requirements.
- Workload type.
- Cost.

**Result:** Reinforced that VM sizing should balance workload performance with Azure consumption cost.

---

### 3. Configured and Reviewed Managed Disks

Reviewed the storage architecture used by Azure VMs, including:

- OS disks.
- Data disks.
- Standard storage.
- Premium SSD.

Evaluated **Premium SSD** for workloads requiring higher IOPS and lower storage latency.

**Result:** Demonstrated how VM storage can be selected based on workload-performance requirements.

---

### 4. Reviewed VM Networking

Reviewed the network components associated with the VM, including:

- Virtual network.
- Subnet.
- Network interface.
- IP configuration.
- Inbound connectivity.

**Result:** Demonstrated that Azure VM connectivity depends on supporting virtual-network resources rather than only the VM configuration itself.

---

### 5. Used Azure Bastion for Secure Connectivity

Reviewed and practiced **Azure Bastion** as a secure administrative connection method.

Azure Bastion allows RDP or SSH connectivity to an Azure VM without requiring the VM to have a directly exposed public IP address.

**Result:** Demonstrated a secure remote-administration method that reduces direct internet exposure.

---

### 6. Reviewed Availability Sets

Reviewed Azure Availability Sets and how VMs can be distributed across **Fault Domains** and **Update Domains**.

#### Fault Domains

Protect against physical infrastructure or rack-level failures by distributing VM instances across separate hardware groupings.

#### Update Domains

Reduce the impact of planned Azure platform maintenance by separating VMs into logical maintenance groups.

**Result:** Distinguished protections for unplanned physical failure from protections used during planned platform maintenance.

---

### 7. Resized the Virtual Machine

Reviewed and practiced changing the VM size to adjust available compute capacity.

Evaluated considerations including:

- Regional size availability.
- Workload needs.
- Cost.
- Possible restart or downtime.

**Result:** Demonstrated how VM compute resources can be adjusted after deployment.

---

### 8. Added an Additional Data Disk

Reviewed the process for attaching an additional managed disk to the VM.

Separated data-storage requirements from the operating-system disk so capacity could be expanded independently.

**Result:** Demonstrated a scalable approach to VM storage administration.

---

### 9. Reviewed Virtual Machine Scale Sets

Reviewed **Virtual Machine Scale Sets (VMSS)** and how multiple VM instances can be managed as a scalable group.

Evaluated VMSS capabilities including:

- Deploying multiple similar VM instances.
- Increasing or decreasing instance count.
- Automatic scaling.
- Supporting distributed application workloads.

**Result:** Distinguished vertical VM resizing from horizontal scaling across multiple VM instances.

---

### 10. Reviewed Azure PowerShell VM Administration

Reviewed virtual-machine deployment and management through Azure PowerShell.

This demonstrated how scripting can make infrastructure deployment more consistent and repeatable than relying only on manual portal configuration.

**Result:** Added automation concepts to the VM administration workflow.

---

### 11. Verified the VM Configuration

Validated the VM-related work by reviewing:

- VM deployment status.
- Selected VM size.
- Managed disk configuration.
- Network configuration.
- Bastion connectivity options.
- Availability configuration.
- Additional data disks.
- VM Scale Set options.

**Result:** Confirmed the major compute, storage, network, availability, connectivity, and scaling components used in the lab.

---

## Workflow Summary

```text
Create Azure VM
      ↓
Select VM Size
      ↓
Configure Managed Disks
      ↓
Review VM Networking
      ↓
Connect with Azure Bastion
      ↓
Review Fault & Update Domains
      ↓
Resize VM
      ↓
Attach Data Disk
      ↓
Review VM Scale Sets
      ↓
Review PowerShell Administration
      ↓
Verify VM Configuration
```

---

## Skills Demonstrated

- Azure Virtual Machines
- VM deployment
- VM sizing
- Managed Disks
- Premium SSD
- Virtual Networks
- Subnets
- Network Interfaces
- Azure Bastion
- Availability Sets
- Fault Domains
- Update Domains
- VM resizing
- Additional data disks
- Virtual Machine Scale Sets
- Autoscaling concepts
- Azure PowerShell
- Infrastructure verification

---

## Project Outcome

The lab demonstrated how Azure virtual machines are deployed and administered as part of a broader infrastructure solution that includes compute, storage, networking, availability, secure connectivity, and scaling.

By completing the workflow, I gained hands-on experience deploying and reviewing Azure VMs, selecting performance options, using Bastion for secure connectivity, evaluating availability protections, resizing compute resources, expanding disk capacity, reviewing VM Scale Sets, and applying PowerShell concepts to repeatable infrastructure administration.

---

[← Back to Azure Home Lab Portfolio](../README.md)