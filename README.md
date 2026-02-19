<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>

</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project is a tuturiol meant to setup and install a guide for osTicket ticketing systemIt'll be built in microsoft azure for project ease and accessibility. It'll also be accompanied with a video highlighting install process. 


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

[![My Skills](https://skillicons.dev/icons?i=azure)](https://skillicons.dev)

- Microsoft Azure
- Remote Desktop Protocol
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

[![My Skills](https://skillicons.dev/icons?i=windows,)](https://skillicons.dev)


<h2>List of Prerequisites</h2>

 Virtual machines
- osTicket install folders/dependencies
- Azure Account

<h2>High-Level Deployment and Installation Steps</h2>


> [!Important]
> Each step will include written instructions as well as corresponding screenshots.
Expand the See screenshots section to view the images.


<h3>1. CREATE WINDOWS 10 VM <h3>
<p>The first step is to make our vm in the azure portal. Click on Virtual machines and select create new. I'm going to name the VM osTicket and I'm going to I'm going to place this VM in region East US 2. Next, we're going to choose windows 10 operating system. After that has been selected, we're going to make a username and account for to login to our vm. After you've chosen your credentials, continue to the bottom and make sure to check box asking if for windows 10/11 license. After that, just click on Review + Create.

<details><summary>See screenshots</summary>
<img src="/images/osTicket-Step1a.png" >
</details>

<details><summary>See screenshots</summary>
<img src="images/osTicket-Step1b.png" >
</details>
 
<p>With the VM created, we're going to Remote Desktop Protocol into the VM and start installation of osTicket. In order to RDP, we need the public IP address of the VM. Go to the portal and click on Virtual Machines. You'll see the osTicket virtual machine status. If you look on the right side of the screen you'll see the public IP address. Copy that and click on the windows icon. Type in Remote Desktop Protocol and open the application. Type in the public ip address and press enter.

<details><summary>See screenshots</summary>
<img src="images/osTicket-Step1c.png" >

<details><summary>See screenshots</summary>
<img src="images/osTicket-Step1d.png" >


<h3>2. INSTALLING osTICKET. </h3> 

Now that we've logged in, the first thing to do is to bring the osTicket install files over to the vm and unzip them unto the desktop. I've already gathered the necessary install files for osTicket beforehand. Right-click on the osTicket-Install folder and click extract all and make sure it's extracted to the desktop.

<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2a.png" >
</details>

<p> We're going to go to the control panel and click on programs and click on Turn windows features on or off.

 <details><summary>See screenshots</summary>
 <img src="images/osTicket-Step2b.png" >

 <details><summary>See screenshots</summary>
 <img src="images/osTicket-Step2c.png" >
 </details>

<p>Go to Internet Information Services and click the box beside it. Next under IIS look for World Wide Web Services and click on the dropbox and click on Application Development Features and click on enable CGI.

<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2d.png" >
</details>


**Notes**
So what is happening is after enabling the IIS feature, we're now able to go in and configure our server for osTicket. If you would type in 127.0.0.1 in a web browser then you could see the change in the server from the time IIS was disabled to the time after it's enabled and notice the change of the server. 

<details><summary>See screenshots</summary>
<img src="images/osTicket-IIS.png" >

<p>Next is to install PHP manager for IIS from the osTicket-Install Files that we're extracted to the desktop.
 <details><summary>See screenshots</summary>
<img src="images/osTicket-Step2f.png" >

Next we're going to install the Rewrite Module (rewrite_amd64_en-US.msi).
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2g.png" >

Once that's installed, we're going to create a directory named PHP on our C:\ drive. Next we're going to unzip the PHP folder into the newly created C:/PHP folder
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2h.png" >

Next we're going to unzip the PHP folder into the newly created C:/PHP folder
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2j.png" >

After the PHP folder has been extracted, the next step is to install the VC_redist.x86.exe from the osTicket install files folder.

<img width="482" height="299" alt="osTicket-Step2m" src="https://github.com/user-attachments/assets/b5f60e21-668f-4c01-82fb-c8c70886061d" />




Once the VC_redist.x86.exe file has been installed, the next step is to install the MySQL 5.5.62 file from the osTicket install folder
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2k.png" >

Now make sure to pick the typical option for the installation process
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2l.png" >

Next launch the configuration wizard after the install has finished and choose the standard configuration to continue the setup
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2r.png" >

On the next screen, just click continue and go to the following screen
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2s.png" >

So for this next step, we're setting the password that's going to be used to log into our MySQL server once it's configured. Now you wouldn't do this in a production environment but for the sake of time, I'm going to make the password root. This is very bad so make sure not do this in an actual production environment.
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2t.png" >

On the next screen, just click execute and wait for the configuration to complete.
<details><summary>See screenshots</summary>
<img src="images/osTicket-Step2u.png" >

The next step is to Open IIS as an Admin and Register PHP from within IIS.
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2v.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2w.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2x.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2y.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2AA.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2BB.png" >


<p>After registering the PHP in the PHP manager, It's time to install osTicket. From the osTicket install folder, extract the osTicket-v1.15.8.zip and we're going to copy the upload folder that's going to be in the new osTicket folder into the C:\inetpub\wwwroot. Within the directory, we're going to rename the upload folder to "osTicket"
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2CC.png" >

 
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2z.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2DD.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2EE.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2GG.png" >

Next we're going to reload the IIS menu and restart the server again
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2HH.png" >

If you go to browse *.80 we'll see that on the webpage we have some extensions that are not enabled for osTicket to function properly.
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2II.png" >

In order to enable these extensions, go back into IIS-> sites-> Default->osTicket
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2JJ.png" >

Click on the enable or disable extension and enable php_imap.dll->php_intl.dll->php_opache.dll and refresh the osTicket site and monitor the changes.
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2KK.png" >

Next we're going to rename the ost-sampleconfig.php to ost-config.php and in order to do that, we need to go back into the C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2LL.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2MM.png" >

<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2NN.png" >
<details>

<p>Next we need to change the permissions to allow osTicket permission to the configuration files. In order to do that, right-click on the ost-config.php file that we just renamed and choose properties.
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2OO.png" >

Next we're going to go to the security tab and disable inheritance. Normally we would never disable inheritance but for this example, I'm going to make it as easy as possible so the configuration is intact
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2PP.png" >

Next we're going to click on advanced under the security tab.
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2QQ.png" >

Next click on disable inheritance.
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2RR.png" >

A popup will appear asking to either convert inherited permissions into explicit permissions on this object or remove all inherited permissions from this object. For the sake of the lab, we're going to choose to remove all inherited permissions from this object. You would **never** click this option to remove all inheritance permissions in an actual production environment 
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2SS.png" >

Next we're going to select a principal 
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2TT.png" >

For the principal, we're going to name the principal everyone and allow full permissions control
<details><summary>See screenshot</summary>
<img src="images/osTicket-Step2UU.png" >







.
























 






























































