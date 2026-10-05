# Active Directory Security Lab

**Project Status:** Active Development (Phase 1: Architecture & Planning)

## Project Overview
A professional, heavily monitored Active Directory home lab built to demonstrate practical skills in identity and access management (IAM), Windows security, PowerShell automation, and detection engineering. This repository tracks the full lifecycle of an enterprise environment: from automated deployment and hardening, through execution of simulated attack vectors, to forensic investigation and remediation.

**Lifecycle Phases:** `Build → Configure → Secure → Attack → Detect → Investigate → Remediate`

## Objectives
* Architect and deploy a realistic Windows Active Directory environment.
* Automate user, group, and organizational unit (OU) provisioning via PowerShell.
* Implement robust logging and telemetry using Sysmon and native Windows Event Forwarding.
* Simulate common adversary tactics (e.g., Password Spraying, Lateral Movement).
* Develop and document SIEM/EDR detections using Sigma rules and Event Log queries.

## Architecture
**[TODO: Insert link to network diagram once created]**

## Lab Environment
The lab infrastructure relies on virtualization to simulate a standard corporate environment:
* **Domain Controller (1):** Windows Server (AD DS, DNS, GPO)
* **Client Endpoints (2):** Windows 10/11 Enterprise
* **Telemetry & Logging:** Sysmon, Windows Event Logs
* **Hypervisor:** [TODO: Specify your hypervisor, e.g., Hyper-V / VirtualBox]

## Active Directory Design
The fictional organization consists of the following departments, each with distinct group policies and access controls:
* IT (Domain Admins, Helpdesk)
* Engineering
* Finance
* Human Resources
* Sales

*For detailed OU mapping and GPO strategies, see [Identity Design](docs/identity-design.md).*

## Security Controls
**[Planned Section]**
* Sysmon configuration mappings
* Group Policy Objects (LAPS, AppLocker, Attack Surface Reduction)
* Tiered administration model implementation

## PowerShell Automation
**[Planned Section]**
Custom scripts used to build and tear down the environment rapidly. Scripts will handle bulk user creation from CSVs, group nesting, and permission auditing.

## Attack Scenarios
**[Planned Section]**
1. Password Spraying (`attacks/01-password-spraying`)
2. Account Compromise (`attacks/02-account-compromise`)
3. Privilege Escalation (`attacks/03-privilege-escalation`)
4. Lateral Movement (`attacks/04-lateral-movement`)
5. Persistence (`attacks/05-persistence`)

## Detection Engineering & Incident Investigations
**[Planned Section]**
Corresponding to the attack scenarios, this section will contain event log queries, Sigma rules, and structured forensic investigations of the simulated breaches.

## Skills Demonstrated
* Active Directory Administration & IAM
* Windows Security Hardening & GPO Management
* PowerShell Scripting & Automation
* Telemetry Generation (Sysmon)
* Threat Hunting & Detection Engineering
* Incident Response & DFIR Documentation

## Repository Structure
[TODO: Generate automated tree output once repository is populated]

## Reproducing the Lab
**[Planned Section]**
Instructions for cloning this repository, modifying the `.csv` configuration files, and running the PowerShell build scripts to recreate the environment locally.
