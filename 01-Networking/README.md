# Networking & Connectivity

This module covers the initial network configuration and connectivity verification between all lab assets.

## Logical Topology
![Network Topology](./img/network_topology.svg)

## IP Address Allocation
All systems use static IPv4 addresses within the `10.0.0.0/24` range.

| Host | IP | Role |
| :--- | :--- | :--- |
| **SRV-2025** | 10.0.0.1 | Gateway & Primary DNS |
| **PC-WIN11** | 10.0.0.2 | Domain Workstation |
| **PC-DEBIAN**| 10.0.0.3 | SIEM / Monitoring |
| **PC-KALI** | 10.0.0.10 | Attack Machine |

## Verification Logs
Connectivity was confirmed via ICMP ping between all nodes. Detailed configuration outputs can be found here:
- [SRV-2025 Network Log](./logs/network_config_srv_2025.txt)
- [PC-WIN11 Network Log](./logs/network_config_win11.txt)
- [PC-DEBIAN Network Log](./logs/network_config_debian.txt)
- [PC-KALI Network Log](./logs/betwork_config_kali.txt)

## Troubleshooting
- **Windows Firewall:** Had to enable "File and Printer Sharing (Echo Request - ICMPv4-In)" rule to allow pings.
- **VMware Segments:** All VMs must be set to the same "LAN Segment" to see each other.