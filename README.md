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
Step Seven: Launch VM, when asked to select ISO file, select Windows 2019 Server ISO file  <br/>
<img src="https://i.imgur.com/868ojO9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Eight: Follow on-screen instructions, must pick Standard Evaulation (Desktop Experience) until Windows 2019 Server Begins to download. You can create your own password. <br/>
<img src="https://i.imgur.com/xWZb16X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/xtfrZBP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/NfUmCJH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/8qvIExg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Nine:Open DC and  open Adapter options. Rename networks "internet" and "xInternalx" respectively. Verify by checking which one is connected to the internet and which one has no connection. Adjust the IPV4 settings on "Internal" to match what's below  <br/>
<img src="https://i.imgur.com/mgSxBLM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/SsufRHf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Ten: Rename this pc "DC" <br/>
<img src="https://i.imgur.com/OPklHM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Eleven: Add Active Directory Domain Services to "DC" <br/>
<img src="https://i.imgur.com/PXXMvp8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/y0aQ50T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/D2N3Pm2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Twelve: Do Post-deployment configuration. This creates the domain  <br/>
<img src="https://i.imgur.com/mGFXdgz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/7t8UG9T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/2ao1ocn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
The log-on screen should look like this after
<img src="https://i.imgur.com/QHFU8XE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Thirteen: Create Dedicated Domain Admin Account<br/>
Open up Active Directory Users and Computers
<img src="https://i.imgur.com/OVXlHhk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Create new Organizational Unit and title it "_Admins"
<img src="https://i.imgur.com/VvCmD7u.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Create a new user under "Admins" and title as shown using your own name, then follow on screen instructions
<img src="https://i.imgur.com/zyOjC1i.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
To make new account admin account, open up properties on new account and click "Member of", then click "add". Now type "Domain Admins" and Check Name. Finally, apply
<img src="https://i.imgur.com/lbAkuGx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Fourteen: Log on with new admin account 
<img src="https://i.imgur.com/MGUz1GA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Fifteen: Now we're going to add RAS / NAT
<img src="https://i.imgur.com/SO7AQIL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Enable Remote Access
<img src="https://i.imgur.com/fwNZVKl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Enable Routing
<img src="https://i.imgur.com/K687eEE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Begin Installation
<img src="https://i.imgur.com/Pn8pCR8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Sixteen: Go to tools and select Routing and Remote Access
<img src="https://i.imgur.com/RFCGKnd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Follow on screen instructions and enable Network Address Translation (NAT)
<img src="https://i.imgur.com/xFdkMCF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Select interface titled "Internet", this allows internal clients to connect to the internet throught the "DC" server
<img src="https://i.imgur.com/97vyYWU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Seventeen: Now we're going to setup  a DHCP server, so we'll click on "Add roles and features" like we have been to add everything else. We'll enable "DHCP server" when given the option to do so, as shown below
<img src="https://i.imgur.com/FER5sHy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Begin installation
<img src="https://i.imgur.com/OTton8R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Step Eighteen: Go to tools and select DHCP to open up DHCP control panel
<img src="https://i.imgur.com/t03QGPW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
Right click IPv4 and select "New Scope"
<img src="https://i.imgur.com/lkqRPMw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
When asked for Scope name, title it "172.16.0.100-200", fill in IP Address Range as shown below
<img src="https://i.imgur.com/lo5htzU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
When asked for router IP address, we will put the "DC" servers IP address as shown below. Then click next until prompted to "finish"
<img src="https://i.imgur.com/bvvUxzy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


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



