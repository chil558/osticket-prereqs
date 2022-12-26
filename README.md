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

- Create a virtual machine within Azure (Optional)
- Install Microsoft Web Platform Installer
  -  Add MySQL 5.5
  - Add All simple versions of x86 PHP up until 7.3


<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/gZcxi4X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Install osTicket v1.15.8

- Download osTicket
- Extract and copy the “upload” folder INTO c:\inetpub\wwwroot
- Within c:\inetpub\wwwroot, Rename “upload” to “osTicket
</b>

Reload IIS

Go to sites -> Default -> osTicket

On the right, click “Browse *:80”

Go back to IIS, sites -> Default -> osTicket

Double-click PHP Manager

</p>
<br />

<p>
<img src="https://i.imgur.com/gZcxi4X.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

Double-click PHP Manager
  
Click “Enable or disable an extension

- Enable: php_intl.dll
- Enable: php_opcache.dll
</b>

Refresh the osTicket site in your browse, observe the changes

Rename C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php

- Disable inheritance -> Remove All
- New Permissions -> Everyone -> All
</b>

Continue Setting up osTicket in the browser (click Continue)

Name Helpdesk

Default email (receives email from customers)

Download and Install HeidiSQL

- Create a new session, root/Password1
- Connect to the session
- Create a database called “osTicket”
</b>

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  
Continue Setting up osticket in the browser

- MySQL Database: osTicket
- MySQL Username: root
- MySQL Password: Password1
</b>

Click “Install Now!”

Delete: C:\inetpub\wwwroot\osTicket\setup

Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php

</p>
<br />
