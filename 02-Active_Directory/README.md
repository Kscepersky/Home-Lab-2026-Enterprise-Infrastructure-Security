# Module 02: Active Directory Infrastructure & Identity Management

## Project Overview
The goal of this module was to design and implement a professional **Active Directory Domain Services (AD DS)** environment on Windows Server 2025 Datacenter. Moving away from a flat "default" structure, I implemented a hierarchical **Organizational Unit (OU)** model. This approach enables granular Group Policy (GPO) application, streamlined Role-Based Access Control (RBAC), and enhanced security management.

---

## Logical Architecture (OU Structure)
The structure was designed to reflect a real-world corporate environment, ensuring a clear separation between administrative assets and standard end-user objects.

```text
[HOMELAB.LOCAL] (Root)
└── 📂 SRV-2025 (Main Container)
    ├── 📂 ADMINS (Tier 0 - High-Privileged Accounts)
    ├── 📂 IT-DEPT (Technical Staff - Helpdesk & Admins)
    ├── 📂 HR-DEPT (Standard Users - High-Risk Phishing Group)
    ├── 📂 WORKSTATIONS (Computer Objects for Client Machines)
    └── 📂 GROUPS (Security & Distribution Groups)