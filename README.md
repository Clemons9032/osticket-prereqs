# osticket-prereqs
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial is a setup and install guide for osTicket ticketing systems


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (21H2)

<h2>List of Prerequisites</h2>

- virtual machines
- osTicket install folders/dependencies
- azure account

<h2>Installation Steps</h2>

<img width="927" height="532" alt="screenshots-for-portfolio-osticket-prereqs" src="https://github.com/user-attachments/assets/7ee2f78a-9000-43d9-9dd1-0ac341a85d70" />

So the first step is to set up an azure virtual machine
</p>
<br />
<img width="1893" height="1051" alt="Screenshot 2026-01-25" src="https://github.com/user-attachments/assets/3c2bd0e5-300a-4d56-a8e4-c1390699834a" />


To get to the virtual machines, just go to the search bar at the top of the page and type in virtual machines. Click on virtual machines and you'll get taken to the create virtual machines page
</p>
<br />

<p>
<img <img width="582" height="517" alt="Screenshot-vmhomepage" src="https://github.com/user-attachments/assets/bdc9d6b0-a8d0-4a5a-8669-545dc0fac97d" />


</p>
<p>
Once you're on the virtual machines homepage, click and create and you'll come to the configuration screen for your vm.
</p>
<br />
<img width="792" height="532" alt="screenshots-vmconfig" src="https://github.com/user-attachments/assets/224a8a58-0d06-4b3f-8b85-a6a63e6c5dda" />

You'll notice subscription in the setup screen. Brand new users get a free trial. I no longer qualify so it'll say pay as you go for me



Next is making a new resource group. Our resource group is going to be named osTicket for the sake of this project




<img width="801" height="512" alt="Screenshot-rgcreation" src="https://github.com/user-attachments/assets/0c3a31fd-d6ff-44f3-836e-e017bef1c69d" />


Next we will name the vm osticket-vm and we're going to change the region to East US 2. You might be somewhere else in the world. This is just where i'm located



<img width="795" height="535" alt="screenshot-vmnameandregion" src="https://github.com/user-attachments/assets/019088f2-2600-4f56-94eb-534548b56265" />


After setting up our vm name and region, we're going to choose the image file that our vm will run. In this case, we're going to choose windows 11 

<img width="790" height="523" alt="screenshot-imageselection" src="https://github.com/user-attachments/assets/f755d6bf-ff95-44da-9f96-59980412d3d2" />



After choosing Windows 10, we're now going to set up our login credentials for the vm. For this lab, I'm going to use labuser as my username. This is a unhealthy practice so only do this for testing purposes.

<img width="800" height="540" alt="screenshot-createvm" src="https://github.com/user-attachments/assets/bb0e66bb-482f-413d-b655-54149a4f2c74" />



After setting up username and password we're going to scroll to the bottom and make sure we have the license button checked. If not, we'll have to come back and click it



<img width="800" height="540" alt="screenshot-createvm" src="https://github.com/user-attachments/assets/bb0e66bb-482f-413d-b655-54149a4f2c74" />


Next click Review & Create and you'll go through a final validation and can start deploying your vm

<img width="750" height="553" alt="Screenshot 2026-01-25 072359" src="https://github.com/user-attachments/assets/4262fdeb-4879-4891-aa64-15ef9999f4d2" />


Once vm is deployed, remote desktop into the vm by getting the public ip address of the vm and using that to remote into the vm


After logging in to the vm, we're now ready to start the process of installing osTicket. 





<img width="756" height="537" alt="image" src="https://github.com/user-attachments/assets/e229c09e-02be-4b3a-bdff-98bf6d2852de" />


To get to remote desktop, press the windows key if you're using windows and type in mstsc. Next type the address of your public ip address to connect to your vm


<img width="1033" height="911" alt="screenshot-mstsc" src="https://github.com/user-attachments/assets/3771caf6-6827-4501-a9de-5f46b6042156" />





