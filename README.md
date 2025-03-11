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
Choose a remote desktop application of your choice, if you're on Windows RDC (Remote Desktop Connection) comes already installed. After you get your Remote Desktop go back to your VM in Azure and get the IP. Once you put in the IP it will ask you for your username and password that you chose while making the VM (make sure to have these written down to avoid the hassle of searching Azure for it if you so happen to forget. 
</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/2cb783b49fb409500e570958f45771805845a3a4/Screenshot%202025-03-10%20222736.jpg) 


  <h2>3. Download osTicket installation Files </h2>

  
(https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0) 

copy and paste the link above to install the installation files onto the VM. 
Once they've installed go to files/downloads and then right click the file and extract all. 
</p>
<br />

<p> 



  <h2>4. Enable IIS and CGI</h2>
Go to programs and features by searching Control Panel in computers searchbox. Once you are there you'll want to press uninstall a program. Then press turn windows features on or off with the shield. Find the Internet Information Services file and enable the file. Next you'll want to enable to CGI file by clicking the World Wide Web Services File then drop down the Application development features and enable CGI. 
</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-50-44.png) 
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-50-52.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-51-26.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-51-55.png)



  <h2>5. Install PHP Manager and Rewrite Module from the installation files</h2>
Go back to the osTicket Installation files folder and install "PHPManagerForllS_V1.5.0". After, then install "rewrite_amd64_en-US.msi". 

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-53-41.png)



  <h2>6. Create a Directory File in Windows C </h2>
Go to C drive by going to files and going all the way down to Windows(C:) and Create a File with the exact words of PHP

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-53-41.png)

