<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10, verison 22H2 x64</b> 

<h2>List of Prerequisites</h2>

- Operating System | Azure VM Windows 10 or later and/or Linux VM.
- Hardware Requirements
- Minimum 8 GB memory, 2 vCPUs
-  Web Browser
| Microsoft Edge, Google Chrome, Brave, Safari and more. 
- Install/Enabling IIS With CGI
- Install and Configure osTicket


---------------

<h2>1. Create a Azure VM</h2>
Press create Virtual Machine in Azure and create its own resource group at the top, Change Avaliablity to (Zone 2) and change your image to Windows 10 Pro, verison 22H2 - 64 Gen2.
Lastly, Change size to 4 vCPU, if u can't 2 vCPU is perfectly fine its just 4 is preferred for a smoothier operation. 
</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/ded8743bf86ba0d296bce40d9adf5bd690264f24/Screenshot%202025-03-10%2022-06-11.jpg) 



<h2>2. Sign into Virtual Machine</h2>
Choose a remote desktop application of your choice, if you're on Windows RDC (Remote Desktop Connection) comes already installed. After you get your RD go back to your VM in azure and get the IP. Once you put in the IP it will ask you to put in your username and password that you chose while making the VM (make sure to have these written down to avoid the hassle of searching Azure for it if you so happen to forget. 
</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/ded8743bf86ba0d296bce40d9adf5bd690264f24/Screenshot%202025-03-10%2022-06-11.jpg) 
