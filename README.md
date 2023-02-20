# osticket-prereqs
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

<h2>List of Prerequisites</h2>

- Create a Microsoft Azure account
- Create a Resource group
- Creat a virtual Machine account
- Put both under the same name
- Make sure it is under the same region and choose windows 10
- The following picture is how it should look like 
 <img src="https://i.imgur.com/8dgsOhR.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/mJpVN6D.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. If you are on winows open your remote desktop app, if you are on an apple device you will need to download the remote desktop app from the apple store
 2. copy and paste your ip address from your Azure virtual machine and create an account
 3. Go to windows, run, control panel, programs, internet information services, click on CGI
 Here is the link for all of the files you will need https://drive.google.com/drive/u/1/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
 Above is a picture of how your screen should look like after completing this step
</p>
<br />

<p>
<img src="https://i.imgur.com/04RCVTx.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
1. From the link earlier click on the PHP management file and download it https://drive.google.com/file/d/1RHsNd4eWIOwaNpj3JW4vzzmzNUH86wY_/view
 2. next download the rewrite file
 https://drive.google.com/file/d/1tIK9GZBKj1JyUP87eewxgdNqn9pZmVmY/view
 3. Go to This PC, windows(c), right click, new, folder, name it PHP
 4. Next download the PHP 7.3.8 filehttps://drive.google.com/file/d/1snNMtLdCOpMtkCyD4mvl9yOOmvVIp9fP/view
 5. Go into thiss file and click "extract all"
 6. Next click and download the VC_redist file
 https://drive.google.com/file/d/1s1OsGF3-ioO0_9LYizPRiVuIkb3lFJgH/view
 7. Do the same with the MySQL file
 https://drive.google.com/file/d/1_OWh9p7VQLcrB0q_V7qT8yHl0xo5gv7z/view
 8. Create a username and password 
</p>
<br />

<p>
<img src="[[https://i.imgur.com/DJmEXEB.png](https://i.imgur.com/iPr8UQS.jpg)](https://i.imgur.com/8dgsOhR.jpg](https://i.imgur.com/MTjrEuT.jpg)" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Open IIS as an Admin

Register PHP from within IIS

Reload IIS (Open IIS, Stop and Start the server)

Install osTicket v1.15.8
Download osTicket from the Installation Files Folder
Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

</p>
<br />


<p>

</p>
<br />



</p>
<p>
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browse, observe the changes

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
<p>
<img src="https://i.imgur.com/MTjrEuT.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
</p>
<br />

