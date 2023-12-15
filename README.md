<h1>SOC Lab</h1>

 
<h2>Description</h2>
 In this project i will be taking inspiration from ... This will be a deeper delve into firewall configurations, SIEM tool (Wazuh) in conjunction with threat intelligence tools.
 This is particularly intriguing lab as it takes the approach from ground up to the finish products purposely to better understand the technology behinnd some of these wonderful tools and help in optmizing it usage
<br />


<h2>OS and tools Used</h2>

- <b>Linux</b> 
- <b>Windows</b>
- <b>OPnsense</b>
- <b>Wazuh</b>
- <b>Cortex</b>
- <b>MISP</b>

<h2>Environment Used </h2>

- <b>Virtual Box</b>

<h2>Firewall installation and setup:</h2>

<p align="center">
Network Diagram: <br/>
<img src="https://imgur.com/MB62alk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 
 this is the network diagram i will be using for my SOC LAB. Firewall to use is OPnsense as stated earlier 
<br />
<br />
OPnsense installation:  <br/>
<img src="https://imgur.com/nP5j0IS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Assign IP address to the LAN interface and set up DHCP: <br/>
<img src="https://imgur.com/uNwXMDK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Homepage of firewall with ip firewall (10.200.200.254):  <br/><img src="https://imgur.com/sZv6r3b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
update opnsense firmware (may take some time):  <br/>
<img src="https://imgur.com/epkyRp7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wazuh (SIEM):  <br/>
<img src="https://imgur.com/w3q9uIm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

I installed wazuh (open source SIEM) using OVA file provided in the documentation
https://documentation.wazuh.com/current/deployment-options/virtual-machine/virtual-machine.html
<br />
<br />
I assigned an IP of 10.200.200.5 to the wazuh VM via sudo vi /etc/sysconfig/network-scripts/ifcg-eth0:  <br/>
<img src="https://imgur.com/Uwu3vHI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Wazuh Dasboard:  <br/>
<img src="https://imgur.com/7UugTea.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

Cortex, MISP & TheHive:  <br/>
<img src="https://imgur.com/Uwu3vHI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

With regards to threat intelligence i used Cortex, and MISP and deployed The hive as my insident response tool. This was achieved
by deploying an ubuntu server 22.04 and docker containers Assigning an ip address of 10.20.200.253. The YAML file used for the integration of these tools can be fond here
https://github.com/ls111-cybersec/thehive-cortex-misp-docker-compose-lab11update/blob/main/docker-compose.yml
</p>

TheHive dashboard:  <br/>
<img src="https://imgur.com/zEaOZVf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Cortex dashboard:  <br/>
<img src="https://imgur.com/OzlODN3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

MISP dashboard:  <br/>
<img src="https://imgur.com/yY9JJVg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
