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
<img src="images/osTicket-Step1b.png" >



































































