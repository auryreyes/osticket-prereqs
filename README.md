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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install / Enable IIS (Internet Information Services)
- Install PHP Manager for IIS
- Install Rewrite Module
- Install PHP 7.3.8
- Install VC_redlist
- Install MySQL
- Register PHP
- Install osTicket
- Install HeidiSQL

<h2>Installation Steps</h2>
! ATTENTION !

Before we begin, if you haven't already created an Azure Account or dont know how to launch a Virtual Machine in Azure, please refer to my [tutorial](https://github.com/auryreyes/create-azure-virtual-machine).

Create an Azure Virtual Machine Windows 10, 4 vCPUs
- Name: vm-osticket
- Username: labuser
- Password: (choose whatever password)

Use Remote Desktop Connection to connect to your Virtual Machine.

<h3>Step 1. Install / Enable IIS (Internet Information Services)</h3>

In essence, IIS is a web server for Windows.The virtual machine must have a web server running in order for osTicket to function from the browser.

Install / Enable IIS (Internet Information Services)
- Click on the start menu and type in “Control Panel” and open it
- Uninstall or change a program -> Turn Windows features on or off
- World Wide Web Services -> Application Development Features -> [X] CGI
- Click “OK” to proceed

<p>
<img src="https://i.imgur.com/TMcivpb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/lWj9Wd4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/JKfrWoY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/zQtGVWJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/bvfThCt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/ktNQjX2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/dmJW5v2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 2. Install PHP Manager for IIS</h3>

To get started, download and install [PHP Manager for IIS](https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view?usp=share_link) (PHPManagerForIIS_V1.5.0.msi)

Open after downloading to install
- File Explorer -> Downloads -> PHPManagerForIIS_V1.5.0

<p>
<img src="https://i.imgur.com/UpKeqsi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DU2vNzU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/iDuyxre.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/GwSYRQ5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 3. Install Install Rewrite Module</h3>

To get started, download and install [Rewrite Module](https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view?usp=share_link) (rewrite_amd64_en-US.msi)

Open after downloading to install
- File Explorer -> Downloads -> rewrite_amd64_en-US
- Create the directory C:\PHP

<p>
<img src="https://i.imgur.com/8iMweJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/qeDGv4R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Ikq4Ug0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/UyZknhw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/g4E9Lfz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/ad7RWmP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 4. Install PHP 7.3.8</h3>

To get started, download [PHP 7.3.8](https://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view?usp=share_link) (php-7.3.8-nts-Win32-VC15-x86.zip) 
- Extract file into C:\PHP

<p>
<img src="https://i.imgur.com/pb8pgaX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/8yuqunq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/nMs2Drq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 5. Install VC_redlist</h3>

To get started, download and install [VC_redlist.x86.exe](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)

Open after downloading to install
- File Explorer -> Downloads -> VC_redlist.x86

<p>
<img src="https://i.imgur.com/SLOnkDi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/L1ngDDA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Rzy6g27.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/r8yPEtb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 6. Install MySQL</h3>

MySQL Server is a database for osTicket. To get started, download and install [MySQL 5.5.62](https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view?usp=share_link) (mysql-5.5.62-win32.msi)

Open after downloading to install
- File Explorer -> Downloads -> mysql-5.5.62-win32
- Typical Setup
- Launch Configuration Wizard (after install)
- Standard Configuration
- Password1

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 7. Register PHP</h3>

Register PHP from within IIS
- Open IIS as an Admin
- PHP Manager -> Register new PHP version
- Browse and select C:\PHP\php-cgi.exe
- Reload IIS (Open IIS, Restart server)

<h3>Step 8. Install osTicket</h3>

To get started, download [osTicket v1.15.8](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) (osTicket-v1.15.8.zip)

After downloading
- Extract and copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload“ to “osTicket”

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Reload IIS (Open IIS, Restart server)

On the left hand side click on the drop down then:
- Go to sites -> Default -> osTicket
- On the right, click “Browse *:80(http)”

<h3>Step 9. Install HeidiSQL</h3>

To get started, download and install [HeidiSQL 9](https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit) (HeidiSQL_12.3.0.6589_Setup)

Open after downloading to install
- File Explorer -> Downloads -> File Explorer -> Downloads -> HeidiSQL_12.3.0.6589_Setup.exe

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
