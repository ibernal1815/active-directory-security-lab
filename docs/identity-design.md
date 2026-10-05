# Identity & Access Management Design

**Status:** Planning Phase

## Domain Configuration
* **Domain FQDN:** `[TODO: e.g., corp.local or ad.yourdomain.com]`
* **NetBIOS Name:** `[TODO: e.g., CORP]`
* **Functional Level:** Windows Server 2016+

## Organizational Unit (OU) Hierarchy
The directory structure avoids default containers and implements a custom hierarchy to allow granular Group Policy application and delegation of control.

    [Domain Root]
    │
    ├── Administration (Tier 0)
    │   ├── Admins
    │   ├── Service Accounts
    │   └── Tier 0 Servers
    │
    ├── Departments (Tier 2)
    │   ├── IT
    │   ├── Engineering
    │   ├── Finance
    │   ├── Human Resources
    │   └── Sales
    │
    └── Devices
        ├── Workstations
        └── Servers

## Role-Based Access Control (RBAC)
User access is strictly managed via Security Groups rather than direct assignment. 

* **Domain Admins:** Strictly limited to `[TODO: specify 1-2 accounts]`. Used only for Tier-0 tasks.
* **Standard Users:** All employees (including IT staff) utilize standard unprivileged accounts for daily workstation use.
* **Department Groups:** E.g., `GG-Finance-Users`, `GG-HR-Users` used for file share and resource access.

## Naming Conventions
* **Users:** `[FirstInitial][LastName]` (e.g., `jsmith`)
* **Admin Accounts:** `admin-[FirstInitial][LastName]` (e.g., `admin-jsmith`)
* **Service Accounts:** `svc_[ServiceName]`
