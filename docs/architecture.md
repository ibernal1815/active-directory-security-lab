# System Architecture

**Status:** Planning Phase

## Overview
This document outlines the high-level architecture of the Active Directory Security Lab. The environment is fully virtualized and designed to simulate a typical corporate infrastructure with a focus on centralized authentication, endpoint management, and security telemetry.

## System Inventory

| Hostname | Role | OS Version | Primary Services | Status |
| :--- | :--- | :--- | :--- | :--- |
| `[TODO: DC01]` | Domain Controller | Windows Server 2022 | AD DS, DNS, GPO | Planned |
| `[TODO: WKSTN01]` | Client Endpoint | Windows 11 Enterprise | Sysmon, Forwarder | Planned |
| `[TODO: WKSTN02]` | Client Endpoint | Windows 10 Enterprise | Sysmon, Forwarder | Planned |

## Architecture Diagram
*(A visual topology diagram mapping the virtual switch, domain controller, and endpoints will be added here once the environment is finalized).*

**[TODO: Insert architecture diagram image]**

## Hypervisor Configuration
* **Platform:** [TODO: e.g., Hyper-V, VMware Workstation, VirtualBox]
* **Resource Allocation:** 
  * DC: [TODO: e.g., 2 vCPU, 4GB RAM]
  * Endpoints: [TODO: e.g., 2 vCPU, 4GB RAM each]
