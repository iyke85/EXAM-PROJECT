<p align="center">
<img src="https://i.imgur.com/6xuIYna.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
This tutorial outlines the implementation of on-premises Active Directory within Azure Virtual Machines.<br />


<h2>Video Demonstration</h2>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- PowerShell

<h2>Operating Systems Used </h2>

- Windows 10 (21H2)
- Ubuntu 20.4

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1
- I set up two Azure virtual machines, one running Windows 10 and the other running Linux. Both are organized under the same resource group named AD-LAB and share a virtual network called VM1-vent.
- <img src="https://i.imgur.com/cyNFPtC.png" alt="Microsoft Active Directory Logo"/>
- Step 2
- I used Remote Desktop Protocol (RDP) to access my Windows VM, where I downloaded Wireshark, a network protocol analyzer.
- <img src="https://i.imgur.com/o95g8Z0.png" alt="Microsoft Active Directory Logo"/>
- Step 3
- To check the connectivity of my Linux VM, I used the ping command to send ICMP packets to its private IP address, 10.0.0.5. I then filtered for ICMP in Wireshark to analyze the packet exchange.
- <img src="https://i.imgur.com/rYekHg0.png" alt="Microsoft Active Directory Logo"/>
- Step 4
- I returned to the network security group (firewall) settings of my Linux VM. I created an inbound rule to block ICMP traffic and observe the effects on connectivity, resulting in connectivity timeout and packet loss.
- <img src="https://i.imgur.com/PErEHsW.png" alt="Microsoft Active Directory Logo"/>
- <img src="https://i.imgur.com/XlKBSK8.png" alt="Microsoft Active Directory Logo"/>
- Step 5
-After observing the effects of blocking ICMP traffic, I modified the inbound rule in the network security group settings for my Linux VM to allow ICMP traffic again. Then, I conducted a continuous ping to further monitor the echo requests and responses.
- <img src="https://i.imgur.com/49MktQd.png" alt="Microsoft Active Directory Logo"/>
- <img src="https://i.imgur.com/M4XRDcs.png" alt="Microsoft Active Directory Logo"/>

-  Step 6
-  Furthermore, I used SSH (Secure Shell Protocol) to remotely access my Linux VM, allowing me to analyze the network connection in more detail.
-  <img src="https://i.imgur.com/auEcVXp.png" alt="Microsoft Active Directory Logo"/>
-  Step 7
-  I ran the nslookup command to query the DNS records for amazon.com and facebook.com, observing the responses to understand the DNS protocol behavior.
-  <img src="https://i.imgur.com/ksyPXUZ.png" alt="Microsoft Active Directory Logo"/>
-  
- 
- 

<h2>Deployment and Configuration Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
