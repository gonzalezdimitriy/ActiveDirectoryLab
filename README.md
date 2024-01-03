<h1>Active Directory Lab</h1>


<h2>Description</h2>
In the lab I'm going to walk through how to create an Active Directory home lab using Oracle Virtual Box. Configuring and runnning thhe lab definiteley helped to develop my understanding on how active directory and windows networking works, so I'm sure it can do the same for you!
<br />


<h2>Languages and Utilites Used</h2>

- <b>PowerShell</b> 
- <b>Oracle Virtual Box</b>



<h2>Environments Used<h2>

- <b>Windows 10 (22H2)</b> 
- <b>Server 2019</b> 
<h2>Lab walk-through:</h2>
Below is a diagram of how this lab is going to be set up. In the diagram, you can see that there is going to be two seperate Network adapters connected to the Domain Controller. One will be used to connect to the internet while the other is used to connect to the private network (housing +1k users !!)  <br/>
<img src="https://i.imgur.com/00dV8qb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Step One:Download Oracle VirtualBox & Extension package.  <br/>
<img src="https://i.imgur.com/0sVk2cf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Two : Follow onscreen-instructions until Oracle VirtualBox launches (see below) <br/>
<img src="https://i.imgur.com/ptr7AWe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Three: Download Windows 10 (64-bit) & Create ISO file <br/>
<img src="https://i.imgur.com/rFvmnYK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Four: Download Windows Server 2019 ISO file <br/>
<img src="https://i.imgur.com/WK3oJgq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Step Five: Open Oracle VM VirtualBox and create a virtual machine, this will be our computer that houses Windows server.  <br/>
<img src="https://i.imgur.com/dLB8Nn7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Six: Before opening "DC", adjust settings and enable a second network adapter to connect to the internal network   <br/>
<img src="https://i.imgur.com/oZ5xY0s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Seven: Wire Cables Through to Front , Cable Manage, and Plug in SATA Cable into SSD  <br/>
<img src="https://i.imgur.com/lPXZFMm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Eight: Plug in Case Headers & SATA Cables <br/>
<img src="https://i.imgur.com/GvOdObw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Nine: Install the 24-pin Connector to Give the Motherboad Power <br/>
<img src="https://i.imgur.com/fqpn3Kj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Ten: Install the 8-pin Connector to give the CPU Power <br/>
<img src="https://i.imgur.com/nV3r2JG.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Eleven: Install the 3-pin Connectos to power on the Case Fans, CPU Cooler, and the CPU Coolers RGB <br/>
<img src="https://i.imgur.com/IDkWFk7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Twelve: Install the GPU and plug in the 8-Pin(6+2-Pin) <br/>
<img src="https://i.imgur.com/h1pJAQT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Thirteen: Power on the PC to test <br/>
<img src="https://i.imgur.com/Fj0AloL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Fourteen: Plug in Windows 11 USB and change Boot Priority to USB First, then restart PC
<img src="https://i.imgur.com/B5iVwl8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Fifteen: Follow On-Screen Steps to Download Windows 11
<img src="https://i.imgur.com/XUnO87F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Sixteen: Windows is successfully installed !!
<img src="https://i.imgur.com/bY606v8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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



