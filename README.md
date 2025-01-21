<h1>Packet Tracer - Configuring IP Addresses on a Router's Interfaces and Enabing Them</h1>

<p align="center">
I'll be configuring the IP addresses of the interfaces of this router in this network diagram: <br/>
<img src="https://i.imgur.com/3gzePNr.png" height="80%" width="80%"/>
<br />
<br />
I accessed the router's CLI and entered Configuration mode from Privileged Exec mode. Then I enter interface configuration mode for gigabit ethernet 0/0 by entering the command "interface gigabitEthernet 0/0". Then I assign the IP adress with the subnet mask to this interface with the command "ip address 15.255.255.254 255.0.0.0". Then I add a description to this interface, "description ## to switch 1##, to indicate that this interface is routed to switch 1. Finally, I enable the interface by entering "no shutdown": <br/>
<img src="https://i.imgur.com/yke5szL.png" height="80%" width="80%"/>
<br />
<br />
Now I'll configure the IP address for the gigabit ethernet 0/1 interface, add a description, and enable it: <br/>
<img src="https://i.imgur.com/yBvqON8.png" height="80%" width="80%"/>
<br />
<br />  
I'll go through the same exact steps to configure the gigabit ethernet 0/2 interface: <br/>
<img src="https://i.imgur.com/ilFEZWM.png" height="80%" width="80%"/>
<br />
<br />  
Now I'll exit out of Configuration mode and I'll verify if the IP addresses to the interfaces were configured correctly. To do this I'll use the command "ip interface brief". It appears the interfaces have been configured successfully: <br/>
<img src="https://i.imgur.com/AhHk19L.png" height="80%" width="80%"/>
<br />
<br />  
I can also verify if the interface IP addresses were set correctly by viewing the running configuration with the command "sh run": <br/>
<img src="https://i.imgur.com/VyUOPss.png" height="80%" width="80%"/> 
<br />
<br />  
Lastly, I'll save the new running configurations to the startup configurations with the "write" command: <br/>
<img src="https://i.imgur.com/YhWSrxN.png" height="80%" width="80%"/> 
<br />
<br />  
</p>

