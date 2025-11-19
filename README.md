
   <img src="https://github.com/user-attachments/assets/9c326204-d498-43be-83f6-64432181a312" alt="proton-vpn" width="600">

# Azure Virtual Machine VPN Setup

## Overview
In this lab, a Windows 10 Virtual Machine was deployed in a geographically distant Azure region to simulate a remote environment for VPN testing and global connectivity verification.

## Environments and Technologies Used
- Microsoft Azure (Portal)
- Windows 10 Virtual Machine
- Remote Desktop Connection (RDP)
- ProtonVPN (or other VPN client)
- Web browser (for IP verification)

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
<b style="font-size: 40px;">Step 1: Created a new Resource Group in Azure.</b>
</p>
<img width="2502" height="1301" alt="Screenshot 2025-11-11 195920" src="https://github.com/user-attachments/assets/a73d59d4-9146-4c95-942e-d9524dbd538e" />

<p>
Create a Resource Group in Azure, then deploy a Windows 10 Virtual Machine within it. Once the VM is set up, use Remote Desktop Protocol (RDP) to log into the VM.
 
</p>
<br />

<p>
<b style="font-size: 40px;">Step 2: Deployed a Windows 10 VM in a different country or region.</b>
</p>
<img width="2504" height="1302" alt="Screenshot 2025-11-11 200043" src="https://github.com/user-attachments/assets/b743f9c4-4469-45e9-b32a-8d2ad73f4cad" />

<p>
Once the group was established, a Windows 10 Virtual Machine was deployed within it. As you can see, the operating system that I used is Windows 10 since it provides free services to Microsoft Azure. I created my username and password for this virtual machine to log in through those credentials. 
</p>

<p>
<b style="font-size: 40px;">Step 3: Connect to the Virtual Machine using Remote Desktop.</b>
</p>
<img width="2510" height="1299" alt="Screenshot 2025-11-11 200425" src="https://github.com/user-attachments/assets/dd14f54b-78a5-458e-a672-7137b3fae3a9" />

<p>
After deployment, the Virtual Machine was accessed remotely using Remote Desktop Protocol (RDP). By copying the VM’s public IP address from the Azure portal and entering it into the Remote Desktop Connection app, the user authenticated with the credentials set during creation. Through this connection, I can interact with the VM as if it were a local computer—installing software, managing files, and preparing the system for VPN configuration and testing.
</p>

<p>
<b style="font-size: 40px;">Step 4: Verify the Virtual Machine’s public IP and geographic location.</b>
</p>
<img width="2559" height="1247" alt="Screenshot 2025-11-11 205215" src="https://github.com/user-attachments/assets/e4c219d8-63e7-4e1f-aa8c-e502e2c41d29" />

<p>
Once inside the VM, open a web browser and navigate to https://whatismyipaddress.com/. View the IP information displayed and record it in Notepad or on a piece of paper for later reference.  This served as the “before” snapshot — the IP typically corresponded to the Azure data center region (e.g., US East 2, Virginia) where the VM resided. 
</p>
<br /> 

<p>
<b style="font-size: 40px;">Step 5: Install and configure a VPN client on the Virtual Machine.</b>
</p>
<img width="2559" height="1259" alt="Screenshot 2025-11-11 205332" src="https://github.com/user-attachments/assets/f9509b77-c318-4ebe-a08c-2f9b5df1f548" />

<p>
On your personal computer, sign up for the free version of Proton VPN at https://account.protonvpn.com/signup?plan=free&language=en. Inside the VM, download and install the Proton VPN client. Log in to the client using your Proton VPN credentials at https://account.protonvpn.com/login
</p>

<p>
<b style="font-size: 40px;">Step 6: Re-verify the IP and location after VPN connection.</b>
</p>
<img width="2559" height="1277" alt="Screenshot 2025-11-11 205402" src="https://github.com/user-attachments/assets/a2889b83-0977-4c2d-b572-09daf08d6d30" />

<p>
To verify that the VPN was functioning correctly, the same IP verification process was repeated. Opening <code>whatismyipaddress.com</code> again revealed a completely different public IP address, now corresponding to the VPN’s geographic region instead of Azure’s data center. This clearly demonstrated that the virtual machine’s traffic was being securely tunneled through the VPN. Screenshots taken before and after this test provided visual evidence of the IP and location change, validating that the VPN successfully altered the network routing path.
</p>

<p>
<b style="font-size: 40px;">Step 7: Analyze and document results.</b>
</p>
<img width="2559" height="1266" alt="Screenshot 2025-11-11 205415" src="https://github.com/user-attachments/assets/9016fbde-04f9-44ae-85cf-8f400c5fd092" />

<p>
Proving that the VPN configuration was a success, I searched Amazon and the delivery was set to the Netherlands. Observations confirmed that Azure VMs can effectively emulate real-world network configurations and VPN use cases. The combination of Azure infrastructure and VPN technology illustrated a fundamental networking concept — encrypting and rerouting traffic to ensure privacy and security across geographically distributed systems. This setup not only provided a demonstration of VPN behavior in a controlled cloud environment but also offered a practical understanding of how organizations can use similar setups to protect data, anonymize connections, and simulate remote user behavior.
</p>
