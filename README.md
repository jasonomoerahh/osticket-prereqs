<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system, osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/keotEGsMRrM)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS) w/ CGI, then install PHP Manager, Rewrite Module, and extract PHP 7.3.8 to C:\PHP
- Install dependencies including the C++ Redistributable and MySQL 5.5.62, and Setup Login Credentials
- Set up osTicket in IIS by placing the "upload" folder in C:\inetpub\wwwroot, renaming it to "osTicket", enabling required PHP extensions, and configuring permissions
- Use a browser to complete the osTicket setup, create the database with HeidiSQL, and finalize installation with the provided MySQL credentials


<h2>Installation Steps</h2>

<p>
<img src="https://github.com/user-attachments/assets/5e8ca262-d8b2-485f-a8ce-99631988ac34" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To setup osTicket, you first need to enable Internet Information Services (IIS) with the CGI feature, which allows PHP to work with IIS, using the "Turn Windows features on or off" utility. After enabling IIS, install PHP Manager for IIS and the URL Rewrite Module to manage PHP settings and URL routing. Finally, extract PHP 7.3.8 into the C:\PHP directory so that IIS can use it to process PHP scripts for osTicket.
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/698e04bc-e1e7-4b76-9ff5-4362b1c5e1b8" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To support PHP and MySQL functionality, install the  Microsoft Visual C++ distributable x86 as it’s required by PHP and MySQL to run properly. Download the MySQL Installer. During installation, you’ll be prompted to create login credentials. These credentials are essential for creating and connecting the osTicket database during the web-based setup.
  
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/5dbe6cc6-cf5a-4c11-8db3-240b6e671e8e" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
To set up osTicket in IIS, unzip your osTicket-v1.15.8.zip file and move the "upload" folder into C:\inetpub\wwwroot, then rename the folder to "osTicket". Open IIS, browse to the osTicket site, and use PHP Manager to enable required extensions like php_imap.dll, php_intl.dll, and php_opcache.dll. Finally, rename the configuration file to ost-config.php, adjust its permissions by disabling inheritance and granting Everyone full access so osTicket can complete the setup.
  
</p>
<br />

<p>
<img src="https://github.com/user-attachments/assets/81567bf7-41db-4b41-b20b-c1f726f31c33" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open a web browser and go to http://localhost/osTicket to launch the osTicket setup page, where you’ll enter basic helpdesk details. Then, open HeidiSQL, connect using the MySQL login credentials, and create a new database called osTicket. Return to the browser to complete the installation by entering the database name and credentials, then click “Install Now” to finalize the setup.
</p>
<br />
