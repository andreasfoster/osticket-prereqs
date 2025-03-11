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



  <h2>6. Create a Directory File in C drive and extract PHP files into it </h2>
Go to C drive by going to files and going all the way down to Windows(C:) and Create a File with the exact words of PHP. Then go back to the Installation Files and right click on the PHP 7.4.8 folder, Press Extract Files and click on the browse buttom with 3 dots and go to Windows(C:) and extract the files to that exact PHP folder that you created.


</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/2532c01ef7d61ec1dad42174e085438d7462b708/Screenshot%202025-03-09%2022-55-10.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/2532c01ef7d61ec1dad42174e085438d7462b708/Screenshot%202025-03-09%2022-56-00.png)

  
  <h2>7. Install VC redist </h2>
Go back to the osTicket Installation files folder and install "VC redist x86". 

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/af8b46c4d417671a01fe30263a3f18c6ca99a56c/Screenshot%202025-03-09%2022-53-41.png)



  <h2>8. Install MySQL </h2>
Go back to the osTicket Installation files folder and install "MySQL 5.5.62". After choose Typical Setup Type at the top, click launch when finished and install. when the Config pop up comes up choose Standard Configuration. After that it will ask you to enter a password, ENTER "root" for new root password and then press execute.

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/87d631de6de5b62ba41f8932979b8d96a9461bee/Screenshot%202025-03-09%2022-57-50.png) 



  <h2>9. Register PHP from within IIS and Installing osTicket </h2>
Search up Internet Information Services with the Windows searchbox, right click program and press run as administrator. After it is open press the PHP Manager Icon and click the purple text at the top that says register new PHP verison. When the path screen pops up press the 3 dots and go to the windows C drive and go to the PHP file that you created earlier, once you click on the file youll see a purple icon that says php.cgi that youll press and open for IIS.

After reload the Manager by clicking on osticket-vm thats under connects and pressing refresh. Go back to the Installation files folder and extract the osTicket folder, once you're done open another file manager tab and go back to the Windows C: drive, go to inetpub and the very top of the page and go to wwwroot then drag the upload folder from the extracted osTicket folder there. Lastly Rename the upload folder that you just draged into wwwroot to exactly "osTicket".

Go back to IIS Manager and refresh like we did earlier and then press start if you havent already. Next expain the file under connections until you can see sites, click sites, press osTicket and click browse 80.

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-00-23.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-02-07.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-02-36.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-03-38.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-08-01.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-08-57.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fc4a85e53eb14bff353ff9815cfe594a89778cff/Screenshot%202025-03-09%2023-11-18.png)


  

  <h2>10. Enable dlls, Rename ost-config.php and assign permissions to ost.config.php  </h2>
Go back to the IIS manager and go to the osTicket file beneath the sites file we were just at and click PHP Manager. and the bottom youll see purple text that says enable or disable an extension click on that and right click enable each of the following "php_imap" "php_intl" "php_opcache". 

After go back to the Windows C drive and click inetpub/wwwroot/osTicket/include then scroll all the way down to find "ost-sampleconfig.php". delete the sample out of the name and make sure it came out as "ost-config.php". After that right click and go to properties to we can give osTicket access to this file. Go to security press advanced and disable inheritance and press remove all inherited permissions from this object. next press add click principal and put everyone and then apply. 

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/a07601fafe4b00322eb3b183e7e83ce645b5ab1f/Screenshot%202025-03-09%2023-14-13.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/a07601fafe4b00322eb3b183e7e83ce645b5ab1f/Screenshot%202025-03-09%2023-14-48.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/a07601fafe4b00322eb3b183e7e83ce645b5ab1f/Screenshot%202025-03-09%2023-18-27.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/a07601fafe4b00322eb3b183e7e83ce645b5ab1f/Screenshot%202025-03-09%2023-19-18.png)





  <h2>11. Setup + Install HeidiSQL  </h2>
Go back to the osTicket site, refresh and continue. fill out the top half information once you reach the database settings part go to the Installation Files folder and download HeidiSQL and before u press finished make sure that the launch HeidiSQL box is checked. at the bottom left press new and type in the username and password "root" and press open. After right click the drop down folder named unnamed and press create new and then press database, after that type in exactly "osTicket" and press ok. Now you can go back to the osTicket site enter in osTicket for (MySQL Database) and type root for username and password, go down and press Install Now!

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/98c9d8c3d98ac2cef49718c7672ec3e65b126355/Screenshot%202025-03-09%2023-25-40.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/98c9d8c3d98ac2cef49718c7672ec3e65b126355/Screenshot%202025-03-09%2023-26-37.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/98c9d8c3d98ac2cef49718c7672ec3e65b126355/Screenshot%202025-03-09%2023-27-18.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/98c9d8c3d98ac2cef49718c7672ec3e65b126355/Screenshot%202025-03-09%2023-28-26.png)
  
  <h2>11. Congrats! you have now installed osTicket  </h2>
Now that you're done you can signin your database with the admin info that u created and now explore the ticketing system! 

</p>
<br />

<p> 
  
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fce884832c733b243f8c32b282cadfc1dd2aee04/Screenshot%202025-03-09%2023-28-52.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fce884832c733b243f8c32b282cadfc1dd2aee04/Screenshot%202025-03-09%2023-31-23.png)
  ![image alt](https://github.com/andreasfoster/osticket-prereqs/blob/fce884832c733b243f8c32b282cadfc1dd2aee04/Screenshot%202025-03-09%2023-31-35.png)
