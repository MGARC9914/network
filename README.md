<p align="center">
<img src="https://i.imgur.com/Ua7udoS.png" alt="Traffic Examination"/>
</p>

<h1>Network Security Groups (NSGs) and Inspecting Traffic Between Azure Virtual Machines</h1>
In this tutorial, we observe various network traffic to and from Azure Virtual Machines with Wireshark as well as experiment with Network Security Groups. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Various Command-Line Tools
- Various Network Protocols (SSH, DNS, DHCP, ICMP)
- Wireshark (Protocol Analyzer)

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu Server 20.04

<h2>High-Level Steps</h2>

- Create two VMs
- Install Wireshark
- Understand the different network protocols 
- Work with Network Security Groups(Azure version of firewall)

<h2>Actions and Observations</h2>

<p>
<li>The first thing we do is install both Windows and Linux virtual machines from azure.</li>
</p>
<p>
<img src="https://i.imgur.com/0dIfWds.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Next go to the Windows vm and click on a browser to install wireshark.</li>
</p>
<p>
<img src="https://i.imgur.com/06oLb8y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/a9zXHyX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Once Wireshark is installed, double click on "Ethernet" to observe what is happening in the virtual network.</li>
</p>
<p>
<img src="https://i.imgur.com/mP5APqx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/iUi2nxc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

