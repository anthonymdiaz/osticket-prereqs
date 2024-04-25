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

- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- MySQL 5.5.62
- HeidiSQL

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

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/e254f324-724d-4cde-a004-5f34708044a2)
   
2. Access Installation Files:
Access the provided Installation Files.

[https://drive.google.com/drive/folders/1V1NK4OMUUETnsSdhRddFZSk5hRfYo1qw?usp=sharing
](https://drive.google.com/drive/folders/1V1NK4OMUUETnsSdhRddFZSk5hRfYo1qw?usp=sharing)</p>
<br />

![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/18872d9e-6b15-423a-abb8-b6e51f5fd58b)

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

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/9218e93c-0629-4c51-825c-cbd2f479854b)

</p>
<p>
4. PHP Manager for IIS Installation:
Download and install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi) from the Installation Files.

[   https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
](https://drive.google.com/drive/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/400a8b23-1f5a-4ed5-a86d-5caae46a15ce)

</p>
<p>
5. Rewrite Module Installation:
Download and install the Rewrite Module (rewrite_amd64_en-US.msi) from the Installation Files.
</p>
<br />
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/5b790ad1-c6f3-46ce-9eab-3b86afd82a25)

</p>
<p>
6. PHP Setup:
Create directory C:\PHP.
Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) from the Installation Files, and unzip its contents into C:\PHP.
If prompted, choose to "Keep" the file.
</p>
<br />


   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/2c9842fe-3867-4300-8fd8-17028964ef95)

</p>
<p>
7. Additional Software Installation:
Download and install VC_redist.x86.exe and MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the Installation Files.
For MySQL installation, select Typical Setup, proceed with the Launch Configuration Wizard after installation, choose Standard Configuration, and set the password as "Password1".
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/21420ec5-f348-4e61-ada1-6a87976a042e)

</p>
<p>
8. Administrative Tasks:
Open IIS as an Administrator.
Register PHP from within IIS.
Reload IIS by stopping and starting the server.
</p>
<br />
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/db5ced48-e4aa-4259-8875-f0bba07ef90c)

</p>
<p>
9. osTicket Installation:
Download osTicket from the Installation Files.
Extract the "upload" folder and copy it to c:\inetpub\wwwroot.
Rename the copied "upload" folder to "osTicket".
Reload IIS.
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/84e3262f-d55f-4ccc-9982-ffda934fde1b)

</p>
<p>
10. PHP Configuration:
Enable specific PHP extensions (php_imap.dll, php_intl.dll, php_opcache.dll) from within PHP Manager in IIS.
Refresh the osTicket site in your browser to observe changes.
</p>
<br />
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/2b6269ff-19a5-4586-aa76-9603325e63a5)

</p>
<p>
11. Configuration File Adjustment:
Rename "ost-sampleconfig.php" to "ost-config.php" within C:\inetpub\wwwroot\osTicket\include.
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/b754cd90-9cc8-4c1a-a4e2-914ee62a11de)

</p>
<p>
12. Permissions Setup:
Assign permissions to ost-config.php: Disable inheritance, remove all existing permissions, and grant Everyone full access.
</p>
<br />
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/326e4b05-a390-4a46-a867-5f6c0da1615a)

</p>
<p>
13. Completing osTicket Setup:
Proceed with osTicket setup in the browser (click Continue), configuring details such as Helpdesk name and default email.
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/5747e462-61e0-4351-b975-eda27b13401c)

</p>
<p>
14. MySQL Database Setup:
Download and install HeidiSQL from the Installation Files.
Open Heidi SQL, create a new session with root/Password1 credentials, and connect to the session.
Create a database named "osTicket".
</p>
<br />
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/8ad75475-c0f3-4f13-bd37-90400feb934f)

</p>
<p>
15. Finalizing Installation:
Continue the osTicket setup in the browser, providing MySQL Database details (osTicket, root, Password1), and click "Install Now!"
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/a8efafff-f351-4b5f-8a51-be180506356b)

</p>
<p>
16. 
Clean up
Delete: C:\inetpub\wwwroot\osTicket\setup

   
   Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>

   ![image](https://github.com/anthonymdiaz/osticket-prereqs/assets/167942930/49f2d345-7d56-4748-9153-259bb784b1d4)

</p>
<p>
17. Verification:
Confirm successful installation without errors.
Access your help desk login page at 

   http://localhost/osTicket/scp/login.php.


   <br />
