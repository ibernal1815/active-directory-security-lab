# Security Controls & Hardening

**Status:** Planning Phase

## Telemetry & Logging
Visibility is the primary goal of this lab. Native Windows Event logs are augmented to provide deep visibility into process creation, network connections, and PowerShell execution.

* **Sysmon:** Deployed to all endpoints using a modified version of [SwiftOnSecurity / Olaf Hartong] configurations.
* **PowerShell Logging:** 
  * Script Block Logging: **[TODO: Status]**
  * Module Logging: **[TODO: Status]**
  * Transcription: **[TODO: Status]**

## Group Policy Objects (GPOs)
The following key security policies are planned for deployment:

1. **LAPS (Local Administrator Password Solution):** Randomize local `Administrator` passwords across all workstations.
2. **Endpoint Hardening:** Disable LLMNR/NBT-NS to prevent network poisoning attacks.
3. **Windows Defender / ASR:** Enforce Attack Surface Reduction rules (e.g., block Office applications from creating child processes).
4. **Log Forwarding:** Configure WinRM and Windows Event Forwarding (WEF) subscriptions to centralize logs.

## Privilege Management
* SMB Signing enforced across the domain.
* Tiered administration enforced (Tier-0 admins cannot log into Tier-2 workstations).
* RDP access restricted strictly to administrative subnets and jump servers.
