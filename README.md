<h1>VPN Configuration on Windows Server</h1>

<h2>Overview</h2>
<p>Installed and configured VPN services in Windows Server to enable secure remote access to Azure-hosted networks.</p>

<h2>Environments and Technologies Used</h2>
<ul>
  <li>Microsoft Azure (Virtual Network / Gateway)</li>
  <li>Windows Server (Remote Access Role)</li>
  <li>PowerShell, RDP</li>
</ul>

<h2>Operating Systems Used</h2>
<ul>
  <li>Windows Server 2019/2022</li>
  <li>Windows 10</li>
</ul>

<h2>High-Level Steps</h2>
<ol>
  <li>Installed Remote Access and Routing roles.</li>
  <li>Configured VPN protocol (PPTP/L2TP).</li>
  <li>Allowed VPN ports through NSG/firewall.</li>
  <li>Connected client via built-in Windows VPN client.</li>
</ol>

<h2>Actions and Observations</h2>

<p><img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="VPN Role Installation"/></p>
<p>VPN role installed and configured for inbound connections.</p>

<p><img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="VPN User Access"/></p>
<p>Configured user access permissions for VPN authentication.</p>

<p><img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Client Connection Test"/></p>
<p>Client successfully connected to VPN and accessed internal resources.</p>
