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
