# Azure Virtual Machine VPN Setup

## Overview
In this lab, a Windows 10 Virtual Machine was deployed in a geographically distant Azure region to simulate a remote environment for VPN testing and global connectivity verification.

## Environments and Technologies Used
Microsoft Azure (Portal)
Windows 10 Virtual Machine
Remote Desktop Connection (RDP)
ProtonVPN (or other VPN client)
Web browser (for IP verification)

## Operating Systems Used
- Windows 10 (Client)

## High-Level Steps
1. Created a new Resource Group in Azure.
2. Deployed a Windows 10 VM in a different country or region.
3. Connect to the Virtual Machine using Remote Desktop.
4. Verify the Virtual Machine’s public IP and geographic location.
5. Install and configure a VPN client on the Virtual Machine.
6. Re-verify the IP and location after VPN connection.
7. Analyze and document results.

## Actions and Observations
<p>
<img width="2559" height="1234" alt="Screenshot 2025-11-07 184928" src="https://github.com/user-attachments/assets/d4d3797a-0d70-45be-b6df-8f2b56a8e09a" />

</p>
<p>
Checked VM's IP address and its geographic location using WhatIsMyIPAddress.com. 
</p>
<br />

<p>
<img width="2559" height="1103" alt="Screenshot 2025-11-07 185005" src="https://github.com/user-attachments/assets/f2d374e2-96e3-4dd4-a9b1-9002e8a65c0a" />

</p>
<p>
Changing the IP address of the VM using ProtonVPN and setting up a VPN in order to change the geographic location.
</p>
<br />

<p>
<img width="2559" height="1259" alt="Screenshot 2025-11-07 185022" src="https://github.com/user-attachments/assets/eecd4123-d2cf-492b-a267-c6da2d5c24da" />

</p>
<p>
Confirmed that the VM’s IP address reflected its geographic location by using WhatIsMyIPAddress.com.
</p>
<br />
