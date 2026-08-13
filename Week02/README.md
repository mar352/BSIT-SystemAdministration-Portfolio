# Enterprise IT Infrastructure Plan — ABC Startup Solutions

> **Course:** ITEP 414 – System Administration and Maintenance  
> **Module:** Week 2 Individual Portfolio Project  
> **Institution:** Laguna State Polytechnic University  
> **Instructor:** Mr. John Randolf M. Peñaredondo, MIT  
> **Author:** BSIT Student / Junior System Administrator  

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Learning Objectives](#learning-objectives)
3. [Company Scenario & Profile](#company-scenario--profile)
4. [Enterprise Hardware Inventory Summary](#enterprise-hardware-inventory-summary)
5. [Enterprise Software Inventory Summary](#enterprise-software-inventory-summary)
6. [Enterprise Network Infrastructure & Diagram](#enterprise-network-infrastructure--diagram)
7. [System Administration Roles & Collaboration](#system-administration-roles--collaboration)
8. [Infrastructure Recommendations](#infrastructure-recommendations)
9. [Technologies Used](#technologies-used)
10. [Challenges Encountered](#challenges-encountered)
11. [Personal Reflection](#personal-reflection)
12. [References](#references)

---

## Project Overview
Every successful IT infrastructure begins with comprehensive planning. Before purchasing hardware, deploying servers, configuring networking gear, or provisioning cloud resources, a System Administrator must assess business requirements and architect a secure, scalable, and cost-effective infrastructure.

This project presents a complete **Enterprise IT Infrastructure Plan** created for **ABC Startup Solutions**, a newly established software development company with 20 employees operating on a single office floor. Designed from scratch, this plan covers company profiling, hardware/software/network inventories, network topology design, system administration roles analysis, technical recommendations, and personal reflection.

---

## Learning Objectives
Upon completion of this portfolio project, the student demonstrates:
* **Knowledge:**
  * Understanding the core roles and responsibilities of System Administrators, Network Administrators, Helpdesk Technicians, and Cloud Administrators.
  * Identifying key hardware, software, and networking requirements for an enterprise startup environment.
  * Comprehending the significance of structured IT documentation and proactive infrastructure planning.
* **Skills:**
  * Analyzing organizational IT requirements across departmental workflows.
  * Preparing technical enterprise hardware, software, and network inventory matrices.
  * Designing an enterprise network topology using standard icons and logical segmentation.
  * Formulating professional technical documentation in Markdown format.
* **Attitude:**
  * Demonstrating professionalism, attention to detail, technical communication, and analytical thinking.

---

## Company Scenario & Profile

### Overview
**ABC Startup Solutions** is a newly established software development enterprise specializing in custom web applications, enterprise software solutions, and cloud-native backend services.

* **Company Name:** ABC Startup Solutions Inc.
* **Nature of Business:** Software Development & IT Consulting
* **Office Location:** 5th Floor, East Tower, Greenfield IT Park, Santa Rosa City, Laguna, Philippines
* **Company Vision:** To become a premier provider of scalable, high-performance web and cloud enterprise solutions across Southeast Asia.
* **Company Mission:** To empower businesses through modern, secure, and user-centric software applications built on reliable cloud and modern web technologies.

### Organizational Structure & Employee Distribution
The startup operates with **20 full-time employees** distributed across four functional departments:

| Department | Employee Count | Primary Responsibilities | Key System Needs |
| :--- | :---: | :--- | :--- |
| **Information Technology** | 5 | Software development, DevOps, QA testing, and internal sysadmin tasks | High-performance workstations, dual monitors, Docker/VirtualBox, Git, CI/CD tools, server access |
| **Human Resources** | 4 | Recruitment, employee relations, payroll support, records management | Standard laptops, productivity software, secure access to HRIS and cloud storage |
| **Finance** | 5 | Accounting, billing, payroll, financial auditing, tax reporting | Secure workstations, spreadsheet tools, dedicated NAS storage, restricted network access |
| **Sales & Marketing** | 6 | Client acquisition, lead generation, digital marketing, account management | Portable laptops, softphone tools, CRM access, high-speed Wi-Fi |
| **TOTAL** | **20** | — | — |

---

## Enterprise Hardware Inventory Summary

Below is the complete hardware specification designed to meet operational demands, redundancy, and future expansion.

| Asset ID | Hardware Description | Specifications | Qty | Department | Business Purpose & Justification |
| :--- | :--- | :--- | :---: | :--- | :--- |
| `HW-DESK-01` | Workstation Desktop | Intel Core i7-13700, 32GB DDR5 RAM, 1TB NVMe SSD, Nvidia RTX 3060 | 5 | IT | High-compute development, local containerization, software compilation. |
| `HW-DESK-02` | Standard Desktop | Intel Core i5-13400, 16GB DDR4 RAM, 512GB NVMe SSD | 5 | Finance | Financial modeling, multi-sheet spreadsheets, data accounting software. |
| `HW-LAP-01` | Enterprise Laptop | Lenovo ThinkPad L14 Gen 4 (i5-1335U, 16GB RAM, 512GB SSD) | 4 | Human Resources | Portability for recruitment interviews, confidential HR management, meetings. |
| `HW-LAP-02` | Mobile Business Laptop | Lenovo ThinkPad L14 Gen 4 (i5-1335U, 16GB RAM, 512GB SSD) | 6 | Sales & Marketing | Client pitches, remote presentations, field sales, flexible desk arrangements. |
| `HW-SRV-01` | Rackmount On-Prem Server | Dell PowerEdge R450 (Xeon Silver 4310, 64GB ECC RAM, 4x2TB SAS HDD RAID 10) | 1 | Server Room (IT) | Local Active Directory/Domain Controller, DNS, DHCP, file server, local Git mirror. |
| `HW-NAS-01` | Network Attached Storage | Synology DiskStation DS923+ (4x4TB NAS HDDs in RAID 5) | 1 | Server Room (IT) | Centralized automated backup target for local files, database dumps, system snapshots. |
| `HW-MON-01` | Dual 27" 4K Monitors | Dell P2723QE 27" UHD IPS Monitors | 10 | IT (2 per employee) | Multi-screen setup for coding, debugging, monitoring logs simultaneously. |
| `HW-MON-02` | Single 24" FHD Monitor | Dell P2422H 24" FHD IPS Monitor | 5 | Finance | Ergonomic screen space for financial reporting and split-screen documentation. |
| `HW-RTR-01` | Enterprise Router | Cisco Integrated Services Router ISR 1100 (1G WAN/LAN) | 1 | IT Server Room | Border gateway router connecting ISP fiber line to internal firewall and LAN. |
| `HW-SW-01` | Managed PoE+ Switch | Cisco Catalyst 2960-X 48-Port Gigabit PoE+ Switch | 1 | IT Server Room | Central core switch providing wired connections, VLAN segmentation, PoE for APs. |
| `HW-WAP-01` | Wireless Access Point | Ubiquiti UniFi 6 Pro (Wi-Fi 6, Dual-Band PoE) | 2 | Office Floor / Common Area | High-density wireless coverage for laptop users, mobile devices, and guests. |
| `HW-PRN-01` | Multifunction Network Printer | HP LaserJet Enterprise MFP M528dn | 1 | Common Area (Admin) | Centralized secure network printing, scanning, and document copying. |
| `HW-UPS-01` | Smart Rackmount UPS | APC Smart-UPS X 3000VA Rackmount 2U (120V) | 1 | Server Room (IT) | Clean power delivery and battery backup for server, NAS, switch, router during power outages. |
| `HW-BKP-01` | External Rugged Hard Drive | SanDisk Professional G-DRIVE ArmorATD 4TB | 2 | IT Admin / Offsite | Offline air-gapped physical backup destination for critical weekly backups. |

---

## Enterprise Software Inventory Summary

| Software | Version | License Type | Primary Purpose & Technical Role |
| :--- | :--- | :--- | :--- |
| **Windows 11 Pro** | 22H2 / 23H2 | Commercial Volume License | OS for client desktop/laptop workstations; supports Active Directory domain join and BitLocker encryption. |
| **Ubuntu Server** | 24.04 LTS | Open Source (Free GPL) | Enterprise Linux OS for primary server, local infrastructure services, web server testing, and containers. |
| **Microsoft 365 Business** | Enterprise | Subscription (Per User/Mo) | Corporate communication suite (Outlook, Teams, Word, Excel, OneDrive) across all 20 employees. |
| **Visual Studio Code** | Latest Stable | Open Source / Free | Standard Integrated Development Environment (IDE) for IT software developers. |
| **Git** | 2.x | Open Source (Free) | Distributed version control system installed across developer machines. |
| **GitHub Desktop** | Latest | Open Source / Free | Graphical user interface for Git repository management and workflow efficiency. |
| **VirtualBox** | 7.0.x | Open Source (GPL v3 / PUEL) | Local virtualization software for running isolated test virtual machines (VMs). |
| **Google Chrome** | Latest Stable | Freeware | Primary enterprise web browser configured with central security policies. |
| **Microsoft Defender for Business** | Endpoint Edition | Subscription License | Enterprise Endpoint Protection (EDR), real-time antivirus, firewall management, and threat response. |
| **AnyDesk** | Enterprise | Commercial License | Secure remote desktop administration software for IT Helpdesk support. |
| **7-Zip** | 24.0x | Open Source (GNU LGPL) | High-compression utility for archiving log files, documentation, and data backups. |

---

## Enterprise Network Infrastructure & Diagram

### Network Architecture Highlights
* **Border Security:** The incoming ISP fiber connection terminates at the **ISP Modem**, which connects to a **Cisco ISR Router** and **Fortinet FortiGate Firewall**.
* **VLAN Segmentation:** The 48-port managed switch enforces logical isolation:
  * `VLAN 10`: IT Department (`192.168.10.0/24`)
  * `VLAN 20`: Human Resources (`192.168.20.0/24`)
  * `VLAN 30`: Finance Department (`192.168.30.0/24`)
  * `VLAN 40`: Sales & Marketing (`192.168.40.0/24`)
  * `VLAN 50`: Servers & NAS (`192.168.50.0/24`)
  * `VLAN 99`: Guest Wi-Fi (`172.16.99.0/24` - Internet access only)
* **Wireless Access:** Ubiquiti UniFi 6 APs powered via PoE providing seamless roaming across office space.

### Embedded Network Diagram
```
                          [ Internet Connection ]
                                     |
                             [ ISP Fiber Modem ]
                                     |
                        [ Cisco ISR Router (1100) ]
                                     |
                       [ Next-Gen Firewall (FortiGate) ]
                                     |
          +--------------------------+--------------------------+
          |                                                     |
  [ Dell PowerEdge Server ]                             [ Synology NAS Storage ]
   (Active Directory/DNS)                                  (Backup Target)
          |                                                     |
          +--------------------------+--------------------------+
                                     |
                     [ Cisco Catalyst 48-Port PoE+ Switch ]
                                     |
       +-----------------+-----------+-----------+-----------------+
       |                 |                       |                 |
 [ IT Department ]  [ HR Department ]    [ Finance Department ]  [ Sales Dept ]
  (VLAN 10 - Wired)  (VLAN 20 - Hybrid)   (VLAN 30 - Wired)     (VLAN 40 - Wireless)
       |                                                           |
 [ Network Printer ]                                    [ Wireless Access Points ]
```

> *Note: For the full Draw.io vector diagram, refer to `diagrams/network-topology.png` and `diagrams/network-topology.pdf` in this repository.*

---

## System Administration Roles & Collaboration

### 1. Helpdesk Technician
* **Responsibilities:** First-line end-user support, ticket queue management, PC setup/imaging, peripheral troubleshooting, basic password resets.
* **Skills:** Troubleshooting, customer service, OS deployment, basic network diagnostics, hardware replacement.
* **Common Tools:** AnyDesk, Jira Service Management, Windows AD Users & Computers, Sysprep, Wireshark, Cable Testers.
* **Certifications:** CompTIA A+, Microsoft Certified: Modern Desktop Administrator Associate, ITIL 4 Foundation.

### 2. Network Administrator
* **Responsibilities:** Network architecture maintenance, switch/router/firewall configuration, VPN establishment, bandwidth monitoring, subnets, VLAN management.
* **Skills:** TCP/IP routing, switching, IP addressing & CIDR, firewall policy management, Wi-Fi deployment, network troubleshooting.
* **Common Tools:** Cisco IOS CLI, Wireshark, PRTG Network Monitor, PuTTY, GNS3/Packet Tracer, SolarWinds.
* **Certifications:** Cisco Certified Network Associate (CCNA), CompTIA Network+, Juniper JNCIA-Junos.

### 3. Linux System Administrator
* **Responsibilities:** Managing Linux servers, kernel updates, system service optimization (Nginx/Apache), SSH security, bash scripting, backup automation.
* **Skills:** Linux CLI fluency, shell scripting (Bash/Python), systemd services, storage management (LVM, RAID), security hardening.
* **Common Tools:** SSH, Ansible, Docker, Htop/Top, Cron, Systemd, UFW/iptables, Vim/Nano.
* **Certifications:** Red Hat Certified System Administrator (RHCSA), Linux Foundation Certified System Administrator (LFCS), CompTIA Linux+.

### 4. Cloud Administrator
* **Responsibilities:** Provisioning and managing cloud infrastructure (AWS/Azure/GCP), IAM role management, cost optimization, automated deployments, cloud security monitoring.
* **Skills:** Cloud service configuration (EC2, S3, VPC), Infrastructure as Code (Terraform), IAM policies, monitoring & alerts.
* **Common Tools:** AWS Management Console, AWS CLI, Terraform, CloudWatch, Azure Portal, Docker.
* **Certifications:** AWS Certified Solutions Architect – Associate, AWS Certified SysOps Administrator – Associate, Microsoft Certified: Azure Administrator Associate (AZ-104).

### How These Roles Collaborate
Inside an organization like ABC Startup Solutions, these four professionals form an interconnected technical team. The **Helpdesk Technician** serves as the front line, identifying workstation or user-level network issues and escalating complex network outages to the **Network Administrator**. The Network Administrator maintains stable LAN/WAN connectivity and firewall policies, enabling the **Linux System Administrator** to host and manage secure on-premises applications, local database servers, and active directory services. Meanwhile, as workloads scale or require offsite disaster recovery, the Linux System Administrator collaborates with the **Cloud Administrator** to bridge local resources with cloud infrastructure (hybrid cloud deployment). Together, they establish a cohesive, secure, and resilient IT ecosystem that supports uninterrupted business operations.

---

## Infrastructure Recommendations

### 1. Internet Service Provider (ISP)
* **Recommendation:** Primary 500 Mbps Enterprise Fiber Line (e.g., PLDT Enterprise or Globe Business) paired with a secondary 200 Mbps Fiber connection from an alternate vendor.
* **Justification:** Enterprise fiber guarantees a Service Level Agreement (SLA) with 99.9% uptime, symmetric download/upload speeds, and dedicated support. A dual-WAN setup on the router provides automatic failover during unexpected carrier outages.

### 2. Server Specifications & Virtualization
* **Recommendation:** Dell PowerEdge R450 paired with Type-1 Hypervisor virtualization (Proxmox VE or VMware ESXi).
* **Justification:** Running Proxmox or ESXi on hardware with 64GB ECC RAM allows running multiple virtual machines (Domain Controller, File Server, Docker Host, Local Git Server) on a single physical host, maximizing hardware utilization, fault tolerance, and backup snapshot efficiency.

### 3. Backup Strategy (3-2-1 Rule)
* **Recommendation:** Implement the standard 3-2-1 Backup Strategy:
  * **3** Copies of critical data (1 Primary operational data + 2 Backups).
  * **2** Different storage media types (Local Synology NAS RAID 5 + Encrypted Cloud Object Storage like AWS S3 / Backblaze B2).
  * **1** Offsite / Air-gapped location (Weekly physical G-DRIVE backup stored offsite).
* **Justification:** Protects the company against ransomware infection, hardware failures, physical disasters (fire/flooding), and accidental data deletion.

### 4. Security & Antivirus
* **Recommendation:** Deploy **Microsoft Defender for Business** paired with **FortiGate Next-Generation Firewall (NGWF)**.
* **Justification:** Provides centralized endpoint threat management, automated remediation, malicious web filtering, intrusion prevention system (IPS), and active monitoring across all Windows/Mac endpoints.

### 5. Password & Access Control Policy
* **Recommendation:** Enforce Active Directory domain-wide password rules: minimum 12 characters, complexity requirements, mandatory Multi-Factor Authentication (MFA) via Microsoft Authenticator for Microsoft 365 and VPN, and Role-Based Access Control (RBAC).
* **Justification:** Password complexity coupled with MFA eliminates over 90% of account compromise risks and credential-harvesting attacks.

### 6. Expansion & Scalability Plan
* **Recommendation:** Allocate spare port capacity on the 48-port switch (current usage ~25 ports) and implement subnetting with room for growth (`/24` subnets per department allow up to 254 hosts each).
* **Justification:** As employee headcount increases from 20 to 50+, additional IP addresses and physical switch ports are readily available without requiring immediate capital expenditure or network restructuring.

---

## Technologies Used
* **Documentation & Formatting:** Markdown, GitHub Flavored Markdown
* **Network Topology Design:** Draw.io / Diagrams.net
* **Operating Systems & Software:** Windows 11 Pro, Ubuntu Server 24.04 LTS, Cisco IOS, Microsoft Defender, Synology DSM
* **Hardware Vendors:** Dell, Cisco, Synology, Ubiquiti UniFi, Lenovo, APC

---

## Challenges Encountered
1. **Budget-to-Requirement Balancing:** Determining realistic enterprise-grade equipment (such as Cisco managed switches vs. consumer routers) while respecting startup capital limitations required thorough research into price-to-performance ratios.
2. **Subnetting & VLAN Design:** Ensuring proper network isolation across departments while permitting controlled inter-VLAN routing for shared resources (like the network printer and server) required careful firewall rule mapping.
3. **Role Boundaries & Technical Synergy:** Distinguishing the exact boundaries between Network, Linux, Cloud, and Helpdesk roles required researching industry standards to present a clear collaborative workflow.

---

## Personal Reflection

### What I Learned
Through this project, I gained a deep practical understanding of how system administration extends far beyond daily software installation or desktop troubleshooting. Infrastructure planning demands a holistic view of an organization's business model, security stance, and operational requirements. I learned how to create technical hardware and software inventories, design segmented network topologies with VLANs and firewalls, and establish layered backup and security strategies suited for an enterprise environment.

### Most Challenging Task
The most challenging aspect was formulating the network topology and translating departmental workflow requirements into concrete networking components. Configuring IP subnets, VLAN isolation, and ensuring redundant WAN connectivity required synthesising theoretical networking concepts into a practical, real-world design.

### Importance of Planning Before Deployment
Planning before deployment is crucial in system administration because reactive IT architecture leads to high operational costs, security vulnerabilities, downtime, and network bottlenecks. Unplanned purchases often lead to incompatible hardware, unmanageable cable layouts, and improper network segmentation. Creating a comprehensive plan allows an organization to minimize capital expenditure, enforce strict security controls from day one, and scale effortlessly as business demands expand.

### Value for Future Career as a System Administrator
This project significantly enhances my readiness as an entry-level System Administrator by giving me hands-on experience in producing enterprise-grade technical documentation. Demonstrating the ability to bridge business requirements with technical execution—communicating through detailed inventories, network diagrams, and rationale-backed recommendations—builds the exact core competencies expected by IT managers and prospective employers.

---

## References
1. Cisco Systems. (2023). *Small Business Network Design Guide*. Cisco Systems Technical Documentation.
2. Tanenbaum, A. S., & Wetherall, D. J. (2014). *Computer Networks* (5th ed.). Pearson.
3. Microsoft Corporation. (2024). *Security baselines for Windows 11 and Enterprise Endpoints*. Microsoft Learn.
4. Synology Inc. (2023). *Data Backup Solutions with the 3-2-1 Strategy*. Synology Knowledge Center.
5. National Institute of Standards and Technology (NIST). (2020). *Framework for Improving Critical Infrastructure Cybersecurity*. U.S. Department of Commerce.
