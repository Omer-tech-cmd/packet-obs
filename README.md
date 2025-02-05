![image](https://github.com/user-attachments/assets/8dc47cc4-73d8-45ab-98c6-a6e501fac2f9)

<b>
<h1>Azure Windows-Linux Packet Transfer Observation</h1>

This lab shows how to observe packet traffic between virtual machines in Microsoft Azure. <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Protocol (RDP 3389)
- ICMP
  
<h2>Operating Systems Used</h2>

- Windows 10
- Linux (Ubuntu 22.04)

<h2>Installation of Wireshark into our Windows 10 Virtual Machine</h2>

<p>
  After<a href= "https://github.com/Omer-tech-cmd/azure-vm-creation"> connecting to our Windows 10 virtual machine,</a> we download Wireshark from <a href= "https://www.wireshark.org/download.html"> here</a> .
  
  
  After downloading the software, we should see the setup wizard that we downloaded in the downloads folder of our Windows 10 virtual machine

  
  ![image](https://github.com/user-attachments/assets/e1c4b496-324d-4300-8800-de1bebe7f725)

  Now, we simply run the setup wizard and follow the installation process. We don’t need to change anything; we can just proceed with the default settings.

  After completing the installation, we should see the Wireshark application when we search it. 


  ![image](https://github.com/user-attachments/assets/be3ab4ba-382c-4b97-b6f0-007ce4a926e0)

<h2>Observing the Actual Traffic</h2>
   After opening the Wireshark application, we should see a screen that says "Ethernet", "Adapter for loopback traffic capture", "ETW reader" and so. 
   
   We are going to highlight "Ethernet" section and press the little blue fin on top left corner of our application.    

![image](https://github.com/user-attachments/assets/629f68c6-c915-4eaf-8c14-6b63ce497919)


  Now, we should see a lot of traffic being captured as it passes through our Windows 10 virtual machine.

  
![image](https://github.com/user-attachments/assets/8be13b7d-4301-48f3-8fae-39b91cea59f3)

  <h2>Filtering the Traffic</h2>
 To filter the traffic, we can apply a display filter in this section.

![image](https://github.com/user-attachments/assets/190fd895-0c07-45b9-84df-74bd514d8579)

 
 We will filter out all traffic except for ICMP traffic.


![image](https://github.com/user-attachments/assets/7801946d-696b-4d2b-b95f-57b5bf5d0abd)

Next, we'll find our Linux virtual machine's private IP address by checking our virtual machines in Microsoft Azure.

![image](https://github.com/user-attachments/assets/1a9a81f8-8eb3-44bd-9f0f-66ea08c4931d)


Next, we’ll open PowerShell on our Windows 10 virtual machine and try to ping our Linux virtual machine by typing "ping <Linux virtual machine's private IP address>" in PowerShell.

If everything is set up correctly, we should see both the ICMP requests and replies recorded in Wireshark.

![image](https://github.com/user-attachments/assets/e11d22af-825b-4860-95ad-6c7cc69ac31c)

So basically that's how we observe packet traffic between our virtual machines, hope this helps.

</b>




 








</p>
