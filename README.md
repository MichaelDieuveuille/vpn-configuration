
   <img src="https://github.com/user-attachments/assets/9c326204-d498-43be-83f6-64432181a312" alt="proton-vpn" width="600">

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
<img width="2502" height="1301" alt="Screenshot 2025-11-11 195920" src="https://github.com/user-attachments/assets/a73d59d4-9146-4c95-942e-d9524dbd538e" />

</p>
<p>
The VPN configuration process began by establishing the foundational infrastructure within Microsoft Azure. A new Resource Group was created to logically contain all associated resources, ensuring the environment remained organized and easily manageable. Once the group was established, a Windows 10 Virtual Machine was deployed within it. To simulate global connectivity, the VM was intentionally placed in a data center region that differed geographically from the user's own location — for example, deploying in <strong>West Europe</strong> while working from the United States. This regional distinction would later make the change in network routing through the VPN more visible.
</p>
<br />

<p>
<img width="2504" height="1302" alt="Screenshot 2025-11-11 200043" src="https://github.com/user-attachments/assets/b743f9c4-4469-45e9-b32a-8d2ad73f4cad" />


</p>
<p>
After deployment, the VM was accessed using the Remote Desktop Protocol (RDP). Logging in through RDP provided a full Windows 10 environment  hosted in Azure’s cloud infrastructure. Before introducing the VPN, the VM’s baseline network configuration was tested. Using a web browser, the site <code>whatismyipaddress.com</code> was accessed to identify the VM’s current public IP address and its associated geographic location. This served as the “before” snapshot — the IP typically corresponded to the Azure data center region (e.g., Amsterdam or Dublin) where the VM resided.
<br />

<p>
<img width="2510" height="1299" alt="Screenshot 2025-11-11 200425" src="https://github.com/user-attachments/assets/dd14f54b-78a5-458e-a672-7137b3fae3a9" />


</p>
<p>
The next phase focused on implementing the VPN. A VPN client such as ProtonVPN was downloaded and installed directly onto the virtual machine.  Once installed, the VPN client was configured and connected to a server located in a completely different region, such as Japan or Canada. This connection rerouted all outgoing traffic through an encrypted VPN tunnel, effectively masking the VM’s original Azure-assigned IP address. During this stage, the VPN client’s interface confirmed a successful connection and displayed the newly assigned VPN server’s location.
</p>
<br />

 <p>
 <img width="2559" height="1247" alt="Screenshot 2025-11-11 205215" src="https://github.com/user-attachments/assets/e4c219d8-63e7-4e1f-aa8c-e502e2c41d29" />

  </p>
<p>
  To verify that the VPN was functioning correctly, the same IP verification process was repeated. Opening <code>whatismyipaddress.com</code> again revealed a completely different public IP address, now corresponding to the VPN’s geographic region instead of Azure’s data center. This clearly demonstrated that the virtual machine’s traffic was being securely tunneled through the VPN. Screenshots taken before and after this test provided visual evidence of the IP and location change, validating that the VPN successfully altered the network routing path.
    </p>
<img width="2559" height="1261" alt="Screenshot 2025-11-11 205310" src="https://github.com/user-attachments/assets/440d4556-e95b-475f-9ddc-fad047ac4dc1" />

 <p>
The experiment concluded with documentation and analysis. Observations confirmed that Azure VMs can effectively emulate real-world network configurations and VPN use cases. The combination of Azure infrastructure and VPN technology illustrated a fundamental networking concept — encrypting and rerouting traffic to ensure privacy and security across geographically distributed systems. This setup not only provided a demonstration of VPN behavior in a controlled cloud environment but also offered a practical understanding of how organizations can use similar setups to protect data, anonymize connections, and simulate remote user behavior.
