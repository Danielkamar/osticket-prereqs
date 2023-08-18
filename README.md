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

- Install / Enable IIS in Windows With CGI and Common HTTP Features
- Install PHP Manager for IIS 
- Install Rewrite Module
- Create the directory C:\PHP
- Install PHP
- Install Visual C++ Redistributable
- Install MySQL
- Register PHP from within IIS
- Install Osticket
- Open Osticket installer on web
- Enable Extensions
- Assign permission to ost-config php
- Install Heidi SQL and create a database
- Finish setup on osticket web installer
- Cleanup

  
<h2>Installation Steps</h2>
<br />
Open Control panel, go to windows features 
Then check the CGI Box under Internet Information Service, the IIS Mangement Console under Web Management Tools and check all the Boxes Under the Common HTTP features
<br />
<br />
<img src="https://i.imgur.com/BBWZGOz.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Download and Install PHP Manager
<br />
<br />
<img src="https://i.imgur.com/3hTB0ze.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Download and Install Rewrite Module
<br />
<br />
<img src="https://i.imgur.com/1SVp67b.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Create a folder and name it PHP in C:
<br />
<br />
<img src="https://i.imgur.com/hCi7QLn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Download PHP 7.3.8 and unzip it into C:\PHP
<br />
<br />
<img src="https://i.imgur.com/SOCVAhR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Download and Install VC_redist.x86.exe
<br />
<br />
<img src="https://i.imgur.com/fSdRIqW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Download and Install MySQL 5.5.62. Also create a memorable password during installation.
<br />
<br />
<img src="https://i.imgur.com/Nn0vFoA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Open IIS as admin, double click on PHP Manager. Click on Register New PHP Version, navigate to PHP folder and choose the cgi file.  
 Lastly, click the restart button to make sure the changes registers. 
<br />
<br />
<img src="https://i.imgur.com/K3PwCnc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
After downloading Osticket, copy the upload folder and paste it in C:\ineptpub\wwwroot. Then rename the upload folder in C:\ineptpub\wwwroot to Osticket 
<br />
<br />
<img src="https://i.imgur.com/bZ5CgMZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Open IIS as admin again, Go to sites -> Default -> osTicket then click on browse 80 at the right.
<br />
<br />
<img src="https://i.imgur.com/s8ZzYVJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Open IIS again, go to IIS, sites -> Default -> osTicket, double click on PHP Manager. Enable the following extensions:  php_imap.dll, php_intl.dll, and php_opcache.dll. Then click on the restart button.
<br />
<br />
<img src="https://i.imgur.com/V6la17T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Go to : C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php, rename ost-sampleconfig.php as ost-config.php. Then give all permission on ost-config.php to everyone.
<br />
<br />
<img src="https://i.imgur.com/IBnpEax.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Download and Install Heidi SQL, Create a new session; username is root and password is the same as the password you set for SQL. After creating a session, create a database and name it osticket
<br />
<br />
<img src="https://i.imgur.com/z11yUE1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Go back to Osticket web installer and fill in all the missing boxes. Congratulations osticket has been successfully installed. 
<br />
<br />
<img src="https://i.imgur.com/AKXXfK6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Delete C:\inetpub\wwwroot\osTicket\setup and change the permission on C:\inetpub\wwwroot\osTicket\include\ost-config.php to read only
<br />
<br />


