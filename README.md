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
<h3>!ATTENTION!</h3>

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
- Create the directory C:\PHP

<p>
<img src="https://i.imgur.com/8iMweJQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
<img src="https://i.imgur.com/4aS1cYb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 5. Install VC_redlist</h3>

To get started, download and install [VC_redlist.x86.exe](https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view?usp=share_link)

<p>
<img src="https://i.imgur.com/SLOnkDi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
- Typical Setup
- Launch Configuration Wizard (after install)
- Standard Configuration
- Password1

<p>
<img src="https://i.imgur.com/4bDWGEL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/2EIOHc2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/st5nHhw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Xjg6eqq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/30gwFCK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/qfhlXf3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 7. Register PHP</h3>

Register PHP from within IIS
- Open IIS as an Admin
- PHP Manager -> Register new PHP version
- Browse and select C:\PHP\php-cgi.exe
- Reload IIS (Open IIS, Restart server)

<p>
<img src="https://i.imgur.com/VThLRK1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/eyX4qAm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/XPme1pX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/GA5aw2b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/SnAirhU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h3>Step 8. Install osTicket</h3>

To get started, download [osTicket v1.15.8](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) (osTicket-v1.15.8.zip)

After downloading
- Copy “upload” folder to c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload“ to “osTicket”

<p>
<img src="https://i.imgur.com/FNxFszY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/KNsf1nc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/SG6uU2T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Dg1ZzKA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Reload IIS (Open IIS, Restart server)

On the left hand side click on the drop down then:
- Go to sites -> Default -> osTicket
- On the right, click “Browse *:80(http)”

After clicking, a web browser should open to the osTicket page.

<p>
<img src="https://i.imgur.com/Jq51FWc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/JzfIJwR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/UzLimtr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**There are some extensions that are not enabled:**
- Go back to IIS, sites -> Default -> osTicket
- Double-click PHP Manager
- Click “Enable or disable an extension”
  - Enable: php_imap.dll
  - Enable: php_intl.dll
  - Enable: php_opcache.dll
- Refresh the osTicket site in your browser and observe any changes.

<p>
<img src="https://i.imgur.com/n01Uv0g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/OsSC3jD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DNU36xI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/BVUALxV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/TvHrJSF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Rename ost-sampleconfig.php to ost-config.php**

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

<p>
<img src="https://i.imgur.com/LGM44MP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Assign Permissions to “os-config.php”**
- Right click on "os0config.php" -> Properties
- Security tab -> Advanced
- Disable inheritance -> Remove all inherited permissions from this object
- Click Add -> Select a principal
- Type “Everyone” in the box -> Check Names -> OK
- Check “Full Control” box -> OK

<p>
<img src="https://i.imgur.com/P9e9fv9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/6xWvITH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/XfEVzYh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/olcTfu1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/DlCGgb0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/qWnZocK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/ipnLK5p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Pxk9COC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Q6ofncI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

- Continue setting up osTicket in the browser (click Continue).
- Fill out everything until you get to the Database Settings.

<p>
<img src="https://i.imgur.com/8V2ZrGC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/LFPUe1T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

<h3>Step 9. Install HeidiSQL</h3>

To get started, download and install [HeidiSQL 9](https://docs.google.com/document/d/1WovrX2DaS9xkfaSr4LXyB4YnnWpXIgPCMMbbfgHmGVw/edit) (HeidiSQL_12.3.0.6589_Setup)

<p>
<img src="https://i.imgur.com/U6ma0yU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/p4AmLho.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

After installation, open HeidiSQL.
- On the bottom left click “New” to create a new session
- Connect to the session
- On the left side of the page right click “Unnamed”
- Create new -> Database
- Name the database “osTicket”

<p>
<img src="https://i.imgur.com/wefQgCo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/5qJ7V2y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/B9ysz6p.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/Jdfc917.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Continue Setting up osTicket in the browser.

**MySQL Database: osTicket**
- MySQL Username: root
- MySQL Password: Password1
- Click “Install Now!”

<p>
<img src="https://i.imgur.com/Oc3CH0T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/HZJiL97.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Congratulations, and hopefully osTicket was successfully installed!**
- Browse to your help desk [login page](http://localhost/osTicket/scp/login.php)

<h3>!ATTENTION!</h3>

There are some files that need to be deleted.
- Delete: C:\inetpub\wwwroot\osTicket\setup

<p>
<img src="https://i.imgur.com/eqwrcWv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

**Set Permissions to “Read” only on “ost-config.php” file**

(C:\inetpub\wwwroot\osTicket\include\ost-config.php)
- Right click “ost-config.php” file and select “Properties”
- Security -> Advanced
- Everyone -> Edit
- Allow only:
  - Read & Execute
  - Read

<p>
<img src="https://i.imgur.com/y5coTkF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/0d34sao.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/tbb1HD0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/bhTI9Ws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/40xpuMY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Congratulations! osTicket was successfully installed! 

The following two tutorials will demonstrate how to set up osTicket by adding users, administrators, and resolving and managing tickets.
