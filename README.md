# Azure Virtual Machine VPN Setup

## Overview
In this lab, a Windows 10 Virtual Machine was deployed in a geographically distant Azure region to simulate a remote environment for VPN testing and global connectivity verification.

## Environments and Technologies Used
- Microsoft Azure (Virtual Machines, Resource Groups)
- Remote Desktop (RDP)
- WhatIsMyIPAddress.com

## Operating Systems Used
- Windows 10 (21H2)

## High-Level Steps
1. Created a new Resource Group in Azure.
2. Deployed a Windows 10 VM in a different country or region.
3. Logged into the VM via Remote Desktop.
4. Verified public IP address using WhatIsMyIPAddress.com.

## Actions and Observations
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Creating Azure VM"/>
</p>
<p>
Deployed the Windows 10 VM in a foreign region to simulate remote access and network routing differences.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Checking Public IP"/>
</p>
<p>
Confirmed that the VM’s IP address reflected its geographic location by using WhatIsMyIPAddress.com.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Connecting via RDP"/>
</p>
<p>
Accessed the VM remotely using RDP and confirmed smooth connection and location-based routing.
</p>
<br />
