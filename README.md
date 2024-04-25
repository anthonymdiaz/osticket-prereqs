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

- Item 1
- Item 2
- Item 3
- Item 4
- Item 5

<h2>Installation Steps</h2>

![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/8881d27e-555b-485a-aebf-14b142a02c0d)

</p>
<p>
1. Azure Virtual Machine Configuration:
   - Create a Windows 10 Azure Virtual Machine with 4 vCPUs.
   - Provide the following details:
     - Name: Vm-osticket
     - Username: labuser
     - Create a password you will remember
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
2. Access Installation Files:
Access the provided Installation Files.

[https://drive.google.com/drive/folders/1V1NK4OMUUETnsSdhRddFZSk5hRfYo1qw?usp=sharing
](https://drive.google.com/drive/folders/1V1NK4OMUUETnsSdhRddFZSk5hRfYo1qw?usp=sharing)</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
3. IIS Installation:
Enable IIS on Windows with CGI and Common HTTP Features:
World Wide Web Services -> Application Development Features ->
[X] CGI
[X] Common HTTP Features
Ensure the inclusion of IIS Management Console under Internet Information Services -> Web Management Tools -> IIS Management Console.
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
4. PHP Manager for IIS Installation:
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the Installation Files.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
5. Rewrite Module Installation:
Download and install the Rewrite Module (rewrite_amd64_en-US.msi) from the Installation Files.
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
6. PHP Setup:
Create directory C:\PHP.
Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the Installation Files, and unzip its contents into C:\PHP.
If prompted, choose to "Keep" the file.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
7. Troubleshooting PHP Download:
If encountering issues with downloading PHP 7.3.8, consider installing Google Chrome and retrying the download from there.
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
8. Additional Software Installation:
Download and install VC_redist.x86.exe and MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the Installation Files.
For MySQL installation, select Typical Setup, proceed with the Launch Configuration Wizard after installation, choose Standard Configuration, and set the password as "Password1".
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
9. Administrative Tasks:
Open IIS as an Administrator.
Register PHP from within IIS.
Reload IIS by stopping and starting the server.
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
10. osTicket Installation:
Download osTicket from the Installation Files.
Extract the "upload" folder and copy it to c:\inetpub\wwwroot.
Rename the copied "upload" folder to "osTicket".
Reload IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
11. PHP Configuration:
Enable specific PHP extensions (php_imap.dll, php_intl.dll, php_opcache.dll) from within PHP Manager in IIS.
Refresh the osTicket site in your browser to observe changes.
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
12. Configuration File Adjustment:
Rename "ost-sampleconfig.php" to "ost-config.php" within C:\inetpub\wwwroot\osTicket\include.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
13. Permissions Setup:
Assign permissions to ost-config.php: Disable inheritance, remove all existing permissions, and grant Everyone full access.
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
14. Completing osTicket Setup:
Proceed with osTicket setup in the browser (click Continue), configuring details such as Helpdesk name and default email.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
15. MySQL Database Setup:
Download and install HeidiSQL from the Installation Files.
Open Heidi SQL, create a new session with root/Password1 credentials, and connect to the session.
Create a database named "osTicket".
</p>
<br />
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
16. Finalizing Installation:
Continue the osTicket setup in the browser, providing MySQL Database details (osTicket, root, Password1), and click "Install Now!"
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
17. Verification:
Confirm successful installation without errors.
Access your help desk login page at http://localhost/osTicket/scp/login.php.
</p>
<br />
