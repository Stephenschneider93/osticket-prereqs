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

- Install IIS
- Install Web Platform Installer
- Install MySQL, set up username and password
- Configure permissions and install OS Ticket

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/oJrEQV9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
In Microsoft Azure, I created a Windows 10 Virtual Machine. Then I installed and Enabled IIS (Internet Information Services) which will allow my computer to run OSticket. Opening the control panel and then going to programs, turn windows features on or off. I scroll and find IIS and check the box, leading to opening World Wide Web Services, then to Application Development Features to check CGI. I then go to Common HTTP features and check all the boxes. After applying the changes, I then I use 127.0.0.1 to make sure my web server is working. Which is illustrated by my screenshot above.
</p>
<br />

<p>
<img src="https://i.imgur.com/4KYvuUP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
I then installed the Rewrite Module which is needed to run OSticket. Following that installation I downloaded the zipped folder of PHP, extracted all into a new folder I created on my (C:) drive named PHP. From there I installed MySQL Server 5.5 with the default settings and created a username and password. Downloading MySQL is creating a database for my computer to store all the tickets, users, and other application data to run OSticket. I then go into IIS as an administrator, go to PHP manager then register new PHP and click php-cgi and open. I downloaded OSticket and extracted the “upload” folder from OSticket into my webserver’s main folder, c:\inetpub\wwwroot. I then rename the upload folder to “OSticket”. I refresh IIS, go to sites, default web site, and select OSticket. From there I click Browse*80 which will bring up the screenshot above, meaning OSticket is working.
</p>
<br />

<p>
<img src="https://i.imgur.com/pa6Pghv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Although OSticket is working, there are a few extensions that aren’t enabled that need to be. So, I went back into IIS and into OSticket, clicked PHP manager, went to enabled or disable an extension and enabled various extensions. Such as, php_imap.dll, php_intl.dll, and php_opcache.dll. From there I go into OSticket folder, then include, and find ost-sampleconfig.php and rename the file to ost-config.php. I then set the permissions on this file, so I right click and go to properties, security, click on advanced. I remove all permissions and then type “everyone” to give everyone permissions to the file and then click apply. As shown on the screenshot above.
</p>
<br />
