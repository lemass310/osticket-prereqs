<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Steps</h2>

- Install/Enable IIS with CGI
- Download and install installation files
- Open IIS and Register PHP
- Dowanload osTicket
- Enable extensions through IIS
- Rename & assign permission to ost-cofig.php file
- Download and install HeidiSQL & create a new session + database
- Set up osTicket in browser and install

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install/Enable IIS in Windows with CGI: World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Create the directory C:\PHP then Download and install the following files:</h2>

- PHPManagerForIIS_V1.5.0.msi
- rewrite_amd64_en-US.msi
- (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP
- VC_redist.x86.exe
- mysql-5.5.62-win32.msi
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin and register PHP from within IIS, then reload IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download osTicket v1.15.8: Download osTicket-v.1.15.8.zip. Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Reload IIS then go to sites -> Default -> osTicket
On the right, click “Browse *:80”
Double-click PHP Manager. Click “Enable or disable an extension”
Enable: php_imap.dll, php_intl.dll, php_opcache.dll
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Rename & assign permission to ost-cofig.php file
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Download and install HeidiSQL & create a new session + database:
Open Heidi SQL
Create a new session, root/Password1
Connect to the session
Create a database called “osTicket”
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open osTicket in browser: Open IIS -> Go to sites -> Default -> osTicket -> On the right, click “Browse *:80”
  
Set up osTicket in browser by first naming Helpdesk and creating a default email. And then filling out these sections:
MySQL Database: osTicket
MySQL Username: root
MySQL Password: Password1
Click “Install Now!”
</p>
<br />
