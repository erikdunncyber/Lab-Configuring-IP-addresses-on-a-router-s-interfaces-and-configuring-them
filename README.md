# Lab-Configuring-IP-addresses-on-a-router-s-interfaces-and-configuring-them
<h1>Packet Tracer - Configuring a Cisco Router's Hostname, Password, and Password Encryption through the CLI</h1>

<p align="center">
I created a simple LAN with 3 PCs connected to a switch, connected to a router: <br/>
<img src="https://i.imgur.com/qiDAbcX.png" height="80%" width="80%"/>
<br />
<br />
I accessed the CLI of the router and entered Privleged Exec mode by entering "enable". Through Privleged Exec mode I enter Global Configuration mode by entering "configure terminal". To change the router's hostname I enter the command "hostname MyRouter". Now the router's hostname is MyRouter: <br/>
<img src="https://i.imgur.com/WneCOsk.png" height="80%" width="80%"/>
<br />
<br />
To add a password I'll enter "enable password CCNA". Now the password to access Privleged Exec mode on this router is CCNA: <br/>
<img src="https://i.imgur.com/t3qsniP.png" height="80%" width="80%"/>
<br />
<br />
To verify if the password was set correctly, I'll access the running configuration of this router. To do this I'll exit Global Configuration mode by entering "exit" and enter "show running-config" to view the current running configuration. The running configuration shows that the password was set to CCNA:  <br/>
<img src="https://i.imgur.com/NFBTD8U.png" height="80%" width="80%"/>
<br />
<br />
To ensure that current and future passwords are encrypted I'll enter Global Configuration mode again and enter "service password-encryption" to set passwords to be encrypted:  <br/>
<img src="https://i.imgur.com/TM7KQul.png" height="80%" width="80%">
<br /> 
<br />
To verify that password encryption was enabled, I'll exit global cofiguration mode to go back to Privileged Exec mode and check the running configuration. It appears that password encryption has been set successfully:  <br/>
<img src="https://i.imgur.com/icsZtiX.png" height="80%" width="80%"/>
<br />
<br />
The current encryption used for passwords isn't very secure, so I'll create a new password that is encrypted using the MD-5 hashing algorithm. To do this I'll enter "enable secret Networks" through global configuration mode. The new, more secure password, "Networks", should now be configured and the old, unsecure password "CCNA" should now be disabled:  <br/>
<img src="https://i.imgur.com/zs3jQv0.png" height="80%" width="80%"/>
<br />
<br />
I'll verify if the new password was set by accessing the running configuration. It appears to be configured correctly:  <br/>
<img src="https://i.imgur.com/vxhZ7YJ.png" height="80%" width="80%"/>
<br />
<br />
Now I'll save the running configuration to the startup configuration. There are three different commands I can enter to do this, "write", "write memory", and "copy running-config startup-config".:  <br/>
<img src="https://i.imgur.com/CpvhN3D.png" height="80%" width="80%"/>
<br />
<br />
Again, I'll verify if the running configuration has saved to the startup configuration. I'll enter "show startup-config" and it appears that the running configuration has been transfered over correctly judging by how the new MD-5 hashed password shows:  <br/>
<img src="https://i.imgur.com/KFRg4yb.png" height="80%" width="80%"/>
  
</p>

