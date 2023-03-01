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
<li>First, we will create two virtual machines one is going to Windows the other is Linux.</li>
</p>
<p>
<img src="https://i.imgur.com/0dIfWds.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Next, go to the Windows VM and click on a browser to install Wireshark.</li>
</p>
<p>
<img src="https://i.imgur.com/06oLb8y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/a9zXHyX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Once Wireshark is installed, double-click on "Ethernet" to observe what is happening in the virtual network.</li>
</p>
<p>
<img src="https://i.imgur.com/mP5APqx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/iUi2nxc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Now we're going to observe the different protocols.</li>
<li>The first one we're looking at is ICMP, type in ICMP on the search bar. You will see that it's empty because we haven't sent any traffic regarding ICMP.</li>
</p>
<p>
<img src="https://i.imgur.com/TByVpx2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li>Next, we're going to ping the Linux VM private IP address.</li>
<li>You can get the IP address by going to azure and clicking on the Linux virtual machine.</li>
  <img src="https://i.imgur.com/h8WYmDA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/9GxMgCS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/wL2ol3j.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li>Now you see traffic appearing in Wireshark.</li>
</p>
<br />

<p>
<li>Next, we're going to ping again but this time with a -t to keep pinging nonstop.</li>
</p>
<p>
<img src="https://i.imgur.com/zJFsn15.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Now we're going to use Network security groups on Azure to make a rule that prevents ICMP traffic.</li>
</p>
<p>
<img src="https://i.imgur.com/BqbRmiC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/0zTDorl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li>After clicking on Add and create the rule that will deny ICMP traffic.</li>
</p>
<p>
<img src="https://i.imgur.com/q2HSshi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li>After the rule was created you will see that the ICMP traffic was timed out.</li>
</p>
<p>
<img src="https://i.imgur.com/Ke8ggGu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/cKJ5H1A.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<br />

<p>
<li>Now we going to look at ssh protocol.</li>
<li>We are going to ssh to the Linux VM. We do that by going to cmd or PowerShell and typing in ssh {usernamme}@{private IP address of the Linux VM}.</li>
</p>
<p>
<img src="https://i.imgur.com/6woB2rk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/wVwCnwN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/6hMUn0T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>With the DHCP protocol, we're just going to renew the IP address. </li>
</p>
<p>
<img src="https://i.imgur.com/ojAr6yN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1KxLKox.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/G0IdRVW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<li>Lastly, with DNS, we can use the nslookup command to have data flow in Wireshark. </li>
</p>
<p>
<img src="https://i.imgur.com/zMtA41v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/TeTUkVr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />




