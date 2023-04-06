# osticket-prereqs<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Heidi SQL
- MySQL
- osTicket
- PHP
- PHP Manager
- Rewrite AMD64

https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6 

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/0RdR9BT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
First we will create a virtual machine in Azure running Windows 10 and remotely connect to it. From there, copy and paste the link to the google drive with all of the prerequisites and download them to get started operating osTicket. 
</p>
<br />

<p>
<img src="https://i.imgur.com/d3sCjBU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
After having downloaded all of the prerequisites, open the control panel and navigate to programs. Under programs click on "turn Windows features on or off". This will bring up a menu; navigate to "Internet Information Services" and enable it, then click on its drop down menu. Click on "World Wide Web Services", then "Application Development Features" and enable "CGI". This will be necessary for us to enable in order for PHP Manager to run properly, which osTicket runs off of. 
</p>
<br />

<p>
</p>
<p>
Open your PHP Manager download and follow the instructions on the installer. Do the same for the Rewrite Module (rewrite_amd64_en-US.msi). Next, create a directory called "PHP" and unzip the contents of the PHP download into the folder. Following this, install vc_redist and MySQL (with standard configuration when prompted). 
</p>
<br />
<p>
<img src="https://i.imgur.com/YdyuHnm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

Open Internet Information Services (IIS) and double-click on PHP Manager. Select "Register new PHP version" and browse to your PHP directory then select "php.cgi". Restart the server. 
<p>
</p>
<p>
  </p>
<br />
<p>
<img src="https://i.imgur.com/tqMSo6K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Open the osTicket download and unzip the contents of the "upload" folder into C:/inetpub/wwwroot/. Reload IIS again. 
Now whilst still in ISS, go to ->sites ->default ->osTicket and browse the 80 folder. We should be taken to the osTicket localhost.
You'll notice that some of the recommended list are disabled; go back to the osTicket folder in ISS and click on ->PHP Manager ->Enable/Disable Extensions. Enable each extension that osTicket recommends on the list pictured above. 
<p>
  </p>
<br />
<p>
<img src="https://i.imgur.com/nGxazqD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Navigate in File Explorer to ->wwwroot ->osTicket ->include and find "ost-sampleconfig". Rename this to "ost-config". Open its properties, go to "security" then "advanced" and disable inheritance. Remove all inherited permissions from object. Add a permission and write in "everyone" then click "full control" for permissions. Apply and click ok for all prompts.
  </p>
<br />
<p>
<img src="https://i.imgur.com/3ZGrUlA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Return to osTicket in the browser and click "continue". Fill out all information fields for "system settings" and "admin user". Now open HeidiSQL which should be downloaded from earlier and install it. This is our database client. Once HeidiSQL is installed click "new" to add a new session and login with the credentials you created earlier from MySQL. If performed correctly, HeidiSQL will appear like image above. Right-click on "unnamed" and create a new database called "osTicket". 
Fill out the rest of the information in the osTicket browser and click "install". 
<p>
<img src="https://i.imgur.com/r9DPn4S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Congratulations, osTicket is now fully installed and ready to be used and configured. Our last task is to navigate in file explorer back to ->wwwroot ->osTicket and delete the "setup" folder.  
<p>
