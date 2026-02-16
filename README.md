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

The first step is to make our vm in the azure portal. Click on Virtual machines and select create new. We're going to make a Windows 10 vm. For the sake of this project, I'm going to name the vm osTicket and I'm going to I'm going to place this vm in East US 2. Next, we're going to choose windows 10 operating system. After that has been selected, we're going to make a username and account for to login to our vm. you can use whatever credentials you want to use for that. After you've chosen your credentials, continue to the bottom and make sure to check box asking if for windows 10/11 license.

<details><summary>See screenshots</summary>

<img width="1918" height="1078" alt="osTicket-Step1a" src="https://github.com/user-attachments/assets/9d8435f6-c48f-499f-af94-d3c9256dcc8c" />


After logging in to the vm, we're now ready to start the process of installing osTicket. 


This is what you should see once azure has started the deployment process


once your vm is made, now its time to remote in to your virtual machine

To get to remote desktop, press the windows key if you're using windows and type in mstsc. Next type the address of your public ip address to connect to your vm

In order to start the installation of osTicket, I'm going to bring the install files from my desktop to the vm

To do this, I'm going to open a browser in microsoft edge and copy the files from my folder

Once logged in to our vm, we're going to download the osTicket install files inside the VM and start configuring our vm to set up the server for osTicket

After clicking on the link, I'm going to select download anyway

After the file is downloaded, we're going to click on the manilla folder. This brings up the file explorer and if we go to downloads under this pc, we'll see the osTicket install folder

Next I'm going to drag the osTicket folder onto the desktop and extract the files onto the desktop. After dragging the files onto the desktop, I'm going to right-click the folder and choose extract all files.                                                            



When I do that you'll see an additional folder carrying the contents of the unzipped folder.

To make the process easier, we can delete the zipped folder for osTicket since we've already extracted all of the data out of the zip folder

The next step is to enable IIS in windows. IIS stands Internet Interactive Services and this is what is going to help us turn this vm into our server for osTicket.

So normally, if a service is running on a server then when you go to the page it should bring up the server of whatever service that you're running. 

For the purposes of this lab, we're going to enter the loopback address and when we do this it should show an error saying this page can't be found. The loopback address is designed to test servers and connectivity on any local server. This address basically refers to your local computer as itself. So once osTicket is set up on the server we can go back and watch how it's changed. 

For now though, go to microsoft edge in the browser and type in 127.0.0.1 and see what is shown.

As you can see, it's showing that the page can't be reached but we're about to change that.

So to get to IIS, click on the start button and type control panel



<img width="1067" height="591" alt="screenshot-controlpanel" src="https://github.com/user-attachments/assets/93a15ca4-710d-410d-98f1-00ad55960cfd" />



Next, click on programs




<img width="1081" height="592" alt="screenshot-programs" src="https://github.com/user-attachments/assets/e2b77c4a-f398-47f9-8d73-8f3a8fd606c5" />



After clicking programs, next click on programs and features, and turn windows features on or off




<img width="1098" height="606" alt="IIS" src="https://github.com/user-attachments/assets/8a0e626e-7c60-4ddb-944f-041b8018dab3" />



From here, I'm going to click on the Internet Information Services box and check the box. After checking box, click on the + sign beside the checked box and it'll bring up some sub features. Click on world wide web services and click on application development features

with  





























































