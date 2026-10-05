# Network Design & IP Allocation

**Status:** Planning Phase

## Network Topology
To prevent lab traffic (especially malware/attack simulations) from bleeding into the home network, the lab operates on an isolated virtual switch with NAT configured exclusively for required outbound internet access (e.g., downloading Sysmon or Windows Updates).

## IP Addressing Scheme

| Subnet / VLAN | Network Address | Gateway | Purpose |
| :--- | :--- | :--- | :--- |
| **Lab-Mgmt** | `[TODO: e.g., 10.0.0.0/24]` | `[TODO: 10.0.0.1]` | Core infrastructure and endpoints |

## Static IP Assignments

* **Domain Controller (`[TODO: DC01]`):** `[TODO: 10.0.0.10]`
* **DNS Server:** Primary DNS for all endpoints points directly to `[TODO: DC01]`.

## Firewall & Routing
**[Planned Section]**
* Windows Defender Firewall configurations via GPO.
* Rules allowing WinRM, RDP, and Event Forwarding exclusively from administrative IP ranges.
