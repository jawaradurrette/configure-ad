<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This page outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (22H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Set Up Azure Virtual Machines: Create a Domain Controller VM, Create a Client VM
- Establish Connectivity: Verify network communication between Client-1 and DC-1
- Install and Configure Active Directory: Install Active Directory Domain Services on DC-1
- Join Client VM to Domain: Configure Client-1 to use the Domain Controller's IP for DNS
- Enable Remote Access and Create User Accounts: Set permissions for domain users to use Remote Desktop on Client-1

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/G4s3JT9.png" height="80%" width="80%" alt="Azure Virtual Machines"/>
</p>
<p>
Here I have set up virtual machines in Azure provisioning and configuring the necessary resources. Each VM requires a network interface for communication within Azure and potentially a public IP address for external access. Security is managed through network security groups (NSGs) that define ingress and egress rules. Additionally, each VM is backed by a disk resource, where the operating system and data are stored.
</p>
<br />

<p>
<img src="https://i.imgur.com/lgtOKok.png" height="80%" width="80%" alt="Ensuring Connectivity"/>
</p>
<p>
This perpetual ping is showing the successful connection between the DC-1 virtual machine and the Client-1 virtual machine. 
</p>
<br />

<p>
<img src="https://i.imgur.com/RHPDpla.png" height="80%" width="80%" alt="Active Directory Install"/>
</p>
<p>
  This is the Active Directory Users and Computers (ADUC) management console, which indicates that the Active Directory Domain Services (AD DS) role has been installed on this server. This tool is mainly used by administrators to manage users, groups, computers, and other objects within an Active Directory domain. This is also part of an Active Directory domain and is configured as a domain controller.
</p>
<br />

<p>
<img src="https://i.imgur.com/dw5LGen.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Client-1 has successfully joined what I have named the jawara.com domain for fun, as confirmed by the message "Welcome to the jawara.com domain." This process is typically done to integrate the computer into a corporate network for example, allowing for centralized management and access to domain resources.
</p>
<br />

<p>
<img src="https://i.imgur.com/vuuvoKT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Finally, I configure remote desktop to be used by members of the domain.
</p>
<br />
