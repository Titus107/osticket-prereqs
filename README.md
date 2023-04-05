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

Open Internet Information Services (IIS) and double-click on PHP Manager. Select "Register new PHP version" and browse to your PHP directory then select "php.cgi".
<p>
</p>
<p>
