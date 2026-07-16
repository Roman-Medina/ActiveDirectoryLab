<h1>Active Directory Home Lab</h1>


##  Project Overview

Welcome to my portfolio! This space is dedicated to my hands-on work in systems administration, cloud infrastructure, and identity security. 

My path into this field began while studying for the **Microsoft Azure Fundamentals (AZ-900)** certification. As I explored cloud architectures, what stood out to me was that *modern cloud security begins and ends with identity.* Fascinated by how user access and permissions actually function under the hood, I realized that to truly master cloud identity, I first needed to understand its foundational, on-premises roots. 

This project is a complete walkthrough of how I built an isolated **Active Directory Domain Services (AD DS)** environment from the ground up. To ensure high-quality documentation, this repository maps out my deployment process step-by-step. Through this hands-on setup, I configured DNS and DHCP services, scripted bulk user provisioning via PowerShell, and deployed strict Group Policy security settings.

This hands-on foundation directly fuels my current preparation for the **Azure Administrator (AZ-104)** certification. Understanding how traditional Active Directory operates on-premises is crucial for mastering hybrid identity, Microsoft Entra ID Connect, and cloud tenant management. This repository serves as a live portfolio of my technical curiosity, system administration capabilities, and readiness for modern IT Support and Cloud IAM roles.


##  Technologies, Tools, and Environments Used

*   **Virtualization Platform:** Oracle VirtualBox Manager
*   **Operating Systems:** 
    *   Windows Server 2019
    *   Windows 10 Pro (64-bit)
*   **Automation & Scripting:** PowerShell
*   **Protocols & Services:** Active Directory Domain Services (AD DS), DNS, DHCP

---

- <b>Windows 10</b> (64-bit)
- <b>Windows Server 2019</b>


##  Project Walkthrough

> **Note:** Below is the step-by-step documentation of the installation, configuration, and verification phases of this lab.

### Step 1: Virtual Network & VM Setup
*   **Action:** Created an isolated NAT Network in Oracle VirtualBox to allow VM-to-VM communication while preventing external DHCP interference.
*   **Execution:** Installed Windows Server 2019 (designated as Domain Controller `DC-01`) and Windows 10 Pro (designated as Client `CL-01`) with static/assigned IP schemas.
*   *(Insert screenshot of your VirtualBox Manager showing both VMs running, or your VirtualBox network settings here)*

### Step 2: Active Directory & Network Services Configuration
*   **Action:** Promoted `DC-01` to a Domain Controller, established the local forest/domain (e.g., `mydomain.local`), and configured DNS and DHCP scopes.
*   **Verification:** Verified that IP addresses were dynamically leasing to clients and domain names were resolving correctly.
*   *(Insert screenshot of the Active Directory Users and Computers console or DHCP Server Scope options here)*

### Step 3: Bulk User Creation via PowerShell
*   **Action:** Executed a custom PowerShell script to read a mock HR database `.csv` file and dynamically generate OUs, security groups, and 100+ simulated users.
*   **Execution:** 
    ```powershell
    # (You can paste a short snippet of your PowerShell loop code here!)
    ```
*   *(Optional: Insert screenshot of your populated OU structure in Active Directory after running the script)*

### Step 4: Workstation Domain Join & GPO Enforcement
*   **Action:** Joined the Windows 10 client machine to the domain and applied targeted Group Policy Objects (GPOs) to restrict access and map network drives.
*   **Verification:** Logged in as a standard domain user to confirm GPOs successfully applied (e.g., restricted access to Control Panel).
*   *(Optional: Insert screenshot of the successful domain login or GPResult output from the client command prompt)*
