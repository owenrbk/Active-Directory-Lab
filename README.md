# ADDS & Entra/Zendesk Lab
Enterprise Infrastructure Simulation of Windows Server Active Directory Domain Services and Zendesk ticketing system, step by step with images.

## Project Overview
This lab simulates a professional corporate environment by bridging **On-Premises Windows Infrastructure** with **Cloud-based SaaS** tools. I built a private network from scratch, configured core networking services, and integrated a ticketing system to handle real-world Service Desk scenarios.

## Technical Implementation
* **Active Directory:** Setup of Forest/Domain (LAB.local) on Windows Server 2022.
* **Network Infrastructure:** * Implemented **DHCP** for automated IP assignment.
    * Configured **RRAS (NAT)** to provide internet access to a private internal subnet.
    * Configured **DNS Forwarders** for external name resolution.
* **Security & Governance:** * Managed **Group Policy Objects (GPOs)** to enable Remote Desktop (RDP) rights for domain users.
    * Controlled User Rights Assignment for specific Organizational Units (OUs).
* **Ticketing Systems:** Integrated **Zendesk** to manage user requests and incident lifecycles.

## Problem-Solving (Key Challenges)
* **DHCP Failure (APIPA):** Identified and resolved "169.254" IP issues by authorizing the DHCP server in AD and correcting interface bindings.
* **NAT Routing:** Successfully bridged a private VM to the internet by configuring a multi-homed DC as a NAT Gateway.
* **RDP Permissions:** Resolved "Sign-in right" errors by creating scoped GPOs for the 'Remote Desktop Users' group.
