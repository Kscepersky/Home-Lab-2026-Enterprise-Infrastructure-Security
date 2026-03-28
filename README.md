# Home Lab 2026: Enterprise Infrastructure & Security
> A full-scale enterprise lab environment designed for hands-on experience in Active Directory administration, SOC operations, and penetration testing.

---

## Network Architecture (Topology)
*Built on VMware Workstation Pro using isolated LAN segments to mimic a corporate environment.*

![Home Lab Logical Topology](./01-Networking/img/network_topology.svg)

- **Internal LAN (Segment):** `10.0.0.0/24` (Fully isolated for security testing)
- **Domain Name:** `homelab.local` (Local Domain)
- **Host System:** AMD Ryzen 7 5700X | 32GB RAM

---

## Lab Inventory

| Machine | OS | Role | Specs |
| :--- | :--- | :--- | :--- |
| **SRV-2025** | Windows Server 2025 Datacenter | Domain Controller | 4 vCPU / 4GB RAM |
| **PC-WIN11** | Windows 11 Pro | Client Endpoint (Workstation) | 4 vCPU / 8GB RAM |
| **PC-DEBIAN** | Debian 13 | Monitoring & SIEM (Wazuh/ELK) | 2 vCPU / 4GB RAM |
| **PC-KALI** | Kali Linux | Attack Machine (Penetration Testing) | 2 vCPU / 4GB RAM |

---

## Project Goals

### 🔵 Blue Team (Defensive)
- [ ] **Active Directory Hardening:** Implementing Group Policy Objects (GPO), password policies, and OU structures.
- [ ] **Centralized Logging:** Forwarding Windows Event Logs to a centralized SIEM (Debian).
- [ ] **Detection Engineering:** Monitoring for brute-force attempts, lateral movement, and unauthorized AD changes.

### 🔴 Red Team (Offensive)
- [ ] **Network Reconnaissance:** Service discovery and mapping using Nmap and BloodHound.
- [ ] **AD Exploitation:** Simulating LLMNR Poisoning, Kerberoasting, and Privilege Escalation.
- [ ] **Post-Exploitation:** Testing persistence mechanisms and data exfiltration techniques.

---

## Project Modules

Detailed documentation for each phase of the lab can be found in the respective directories:

* **[1: Networking & Connectivity](./01-Networking/)** – *IP addressing, Topology, and verification.*
* **[2: Active Directory & Domain Services](./02-Active_Directory/)** – *Domain Controller setup, OU structure, and GPO.*
* **[3: Security Operations (SOC)](./03-Security-Operations/)** – *Wazuh SIEM installation and log ingestion.*

## Repository Structure

```text
/
├── 01-Networking/           # Interface configs, DHCP scopes, VLAN mapping
├── 02-Active-Directory/      # GPO documentation, OU structure, PS scripts
├── 03-Security-Operations/   # SIEM setup, detection rules, log analysis
├── 04-Pentesting-Reports/    # Write-ups for simulated attacks and mitigations
└── scripts/                  # Custom PowerShell (.ps1) and Bash (.sh) automation