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


After setting up our vm name and region, we're going to choose the image file that our vm will run. In this case, we're going to choose windows 10

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





<img width="1033" height="911" alt="screenshot-mstsc" src="https://github.com/user-attachments/assets/3771caf6-6827-4501-a9de-5f46b6042156"/>


This is what you should see once azure has started the deployment process


<img width="756" height="533" alt="screenshot-deployment" src="https://github.com/user-attachments/assets/26f79258-7e2c-4b0b-933b-a3ceda230fd2" />


once your vm is made, now its time to remote in to your virtual machine


<img width="752" height="512" alt="image" src="https://github.com/user-attachments/assets/9e2d9049-f797-4b0e-998f-ba4b21c44a95" />






To get to remote desktop, press the windows key if you're using windows and type in mstsc. Next type the address of your public ip address to connect to your vm


<img width="997" height="567" alt="image" src="https://github.com/user-attachments/assets/ee6c36e1-578a-40f4-bbdb-ba7852eb0821" />




In order to start the installation of osTicket, I'm going to bring the install files from my desktop to the vm

To do this, I'm going to open a browser in microsoft edge and copy the files from my folder




<img width="1061" height="576" alt="screenshot-ostickethome" src="https://github.com/user-attachments/assets/4a124bdb-1244-44cb-81b8-bc730a76c6be" />





Once logged in to our vm, we're going to download the osTicket install files inside the VM and start configuring our vm to set up the server for osTicket


<<img width="450" height="553" alt="screenshot-osticketinstallfiles" src="https://github.com/user-attachments/assets/60b353ca-72c6-404d-a126-bba4aea39e02" />





After clicking on the link, I'm going to select download anyway



<img width="460" height="560" alt="screenshot-osticketzip" src="https://github.com/user-attachments/assets/49d34fe7-e211-4d89-9716-a87272cd0998" />



After the file is downloaded, we're going to click on the manilla folder. This brings up the file explorer and if we go to downloads under this pc, we'll see the osTicket install folder





<img width="1015" height="573" alt="image" src="https://github.com/user-attachments/assets/971046cd-e2cd-485b-b79d-c26bfa3333d5" />




<img width="1073" height="594" alt="Screenshot 2026-01-25 082659" src="https://github.com/user-attachments/assets/037147fb-61a5-4455-af10-ed5259246051" />





Next I'm going to drag the osTicket folder onto the desktop and extract the files onto the desktop. After dragging the files onto the desktop, I'm going to right-click the folder and choose extract all files.                                                            



When I do that you'll see an additional folder carrying the contents of the unzipped folder.





<img width="1088" height="612" alt="screenshot-osticket-unzipped" src="https://github.com/user-attachments/assets/5647d13f-29a5-4c4e-8539-d4922be8db9f" />




To make the process easier, we can delete the zipped folder for osTicket since we've already extracted all of the data out of the zip folder






<img width="1095" height="612" alt="screenshot-zipfolder-delete" src="https://github.com/user-attachments/assets/5bacb35a-b6a8-499b-8906-13bdf1cfffe6" />



The next step is to enable IIS in windows. IIS stands Internet Interactive Services and this is what is going to help us turn this vm into our server for osTicket.


So normally, if a service is running on a server then when you go to the page it should bring up the server of whatever service that you're running. 


For the purposes of this lab, we're going to enter the loopback address and when we do this it should show an error saying this page can't be found. The loopback address is designed to test servers and connectivity on any local server. This address basically refers to your local computer as itself. So once osTicket is set up on the server we can go back and watch how it's changed. 

For now though, go to microsoft edge in the browser and type in 127.0.0.1 and see what is shown.



<img width="1101" height="601" alt="screenshot-osticket-iis" src="https://github.com/user-attachments/assets/08343f61-9834-47f6-bb97-676202655e85" />



As you can see, it's showing that the page can't be reached but we're about to change that.



So to get to IIS, click on the start button and type control panel



<img width="1067" height="591" alt="screenshot-controlpanel" src="https://github.com/user-attachments/assets/93a15ca4-710d-410d-98f1-00ad55960cfd" />



Next, click on programs




<img width="1081" height="592" alt="screenshot-programs" src="https://github.com/user-attachments/assets/e2b77c4a-f398-47f9-8d73-8f3a8fd606c5" />



After clicking programs, next click on programs and features, and turn windows features on or off




<img width="1098" height="606" alt="IIS" src="https://github.com/user-attachments/assets/8a0e626e-7c60-4ddb-944f-041b8018dab3" />



From here, I'm going to click on the Internet Information Services box and check the box. After checking box, click on the + sign beside the checked box and it'll bring up some sub features. Click on world wide web services and click on application development features

with CGI




<img width="1063" height="597" alt="wwws" src="https://github.com/user-attachments/assets/728016ed-cb8d-4138-a75b-758e3b350321" />





<img width="1072" height="572" alt="cgi" src="https://github.com/user-attachments/assets/49f40f66-b7c5-4441-89d2-46b2372b3755" />



After enabling the features, it's going to start installing the web server.



<img width="1072" height="565" alt="iis-install" src="https://github.com/user-attachments/assets/ca9fbc37-adb8-4df9-b7dd-08873613f80c" />




If we go back to the webpage of our server, It's going to look different now. When I go and refresh the loopback address, I get the actual server homepage now.





<img width="1082" height="573" alt="iss-server" src="https://github.com/user-attachments/assets/8d3b9880-c3ca-4a71-ac1a-94d4b6e4b21e" />


Now I'm ready to start the installation process for osTicket. From the osticket install file I'm going to install PHP Manager for IIS






<img width="575" height="446" alt="Screenshot 2026-01-25 093257" src="https://github.com/user-attachments/assets/6af0fa6b-31d5-427b-ba4a-7c519d609b79" />



Once PHP Manager for IIS is installed, then the next thing that we're going to install is the Rewrite Module




<img width="1062" height="565" alt="screenshot-rewrite" src="https://github.com/user-attachments/assets/f27f4d85-5d65-4036-a6c1-efac6b4bfe9a" />


<img width="1062" height="558" alt="Screenshot 2026-01-25 093452" src="https://github.com/user-attachments/assets/6c08f485-b007-476b-9cb7-3adf06358e43" />



<img width="1063" height="576" alt="screenshot rewrite-finish" src="https://github.com/user-attachments/assets/144b9fe6-d969-4073-8ebe-09c34b108503" />



After the rewrite module is finished installing, then I'm going to create a new directory called C:\PHP



<img width="1057" height="560" alt="screenshot-php" src="https://github.com/user-attachments/assets/b024f797-5467-45cf-b549-88072644d0e5" />


After making the C:\PHP directory next we're going to unzip the PHP 7.3.8 folder and extract the files from this folder

To extract the files from the PHP folder, just right click the folder and click extract all. Instead of extracting everything right away into the default browser, we can click on browse and go to the C:\PHP folder that we just made and choose that as our extraction point



<img width="1073" height="605" alt="screenshot-phpextraction" src="https://github.com/user-attachments/assets/5ef816cc-5251-4f28-9f92-92e03bfcdaff" />

After that's done, I'm going to install the VC_redist.x86.exe file.



<img width="1084" height="593" alt="Screenshot 2026-01-25 151632" src="https://github.com/user-attachments/assets/399a3bec-eb89-49e7-87c0-3c726c3afa02" />



After that's finished installing, I'm going to install the MySQL 5.5.62 executable. Now this is the database that osTicket will use to store our user data for the entire osTicketing system.




<img width="1018" height="567" alt="screenshot-mysql" src="https://github.com/user-attachments/assets/285640f1-d915-4aff-b18c-73038ed70577" />










<img width="259" height="194" alt="Screenshot 2026-01-25 152510" src="https://github.com/user-attachments/assets/cf156337-1edb-41d3-833f-56d740039f37" />


Once we're at the setup stage,I'm going to choose typical for the setup type




<img width="263" height="197" alt="Screenshot 2026-01-25 152518" src="https://github.com/user-attachments/assets/b1e0c918-cd38-4f12-9168-d372a7ff494f" />





After installtion, the MySQL will open automatically. When prompted, choose standard configuration for the setup type and click next





<img width="268" height="195" alt="screenshot-mysqlconfig" src="https://github.com/user-attachments/assets/3eac1bb5-1c4a-415d-a7b6-a3d91569e5c5" />


This next part is extremely important. We have to choose a password for the mysql server and we'll need to remember this for later.



<img width="267" height="197" alt="screenshot-rootmysql" src="https://github.com/user-attachments/assets/e6be40cb-0c89-4b12-b976-b588c75848be" />


Just for the sake of this demonstration, I made this password pretty simple but never under any circumstances would you do this in a real-life scenario. It's not best practices to do this.



<img width="262" height="187" alt="mysql-execute" src="https://github.com/user-attachments/assets/dcb03662-804a-49c1-b407-67ea5871d078" />



Now hit execute and finish the configuration and install


After the install, I'm going to open IIS as an Admin and the best way to do this is by going to the start menu and typing IIS in the search bar.



<img width="420" height="324" alt="Screenshot 2026-01-25 154124" src="https://github.com/user-attachments/assets/eedbbd72-3a70-4936-b68e-dd31175d73e5" />


Click open as Admin and we're going to register PHP within IIS.



The reason for this is to let the server know that PHP is on the network



After opening IIS, click on PHP manager




<img width="467" height="547" alt="screenshot-phpmanager" src="https://github.com/user-attachments/assets/5ca586ca-c40e-4794-aecc-c12d9d6f961a" />






After clicking on PHP manager, we're going to click on register PHP



<img width="555" height="573" alt="screenshot-phpregister" src="https://github.com/user-attachments/assets/3fed50b2-dd8b-4715-be48-804ad22d7a33" />



Once we click on register PHP, we have to give IIS the path to the PHP file and we're going to do that by opening another file explorer window and navigating to the php.cgi folder 

To get there, click on the three dots beside the search bar and it'll bring up the file explorer






<img width="307" height="110" alt="screenshot-pathforphp" src="https://github.com/user-attachments/assets/33fd2357-dc2d-4e03-831a-66f4d93b5b7e" />





Once file explorer is open, then'll we'll navigate to the C drive and click on the PHP folder and after clicking on the PHP folder, double-click on the php.cgi executable and it'll provide the path for IIS to identify PHP on its server






<img width="481" height="535" alt="screenshot-php cgipath" src="https://github.com/user-attachments/assets/4e8e84e5-0391-4b31-a1c3-1e238fdca956" />



Now we're going to restart the server.

Go back to the IIS homepage and you'll see osticket server 







<img width="551" height="568" alt="screenshot-osticketrestart" src="https://github.com/user-attachments/assets/17f407d6-d790-411a-947c-ca1858d2fa87" />

After on the right side of the screen, I'm going to click stop and once the start button turns green again, I'm going to start the server back up



Now to install the osTicket file


From the osTicketinstallation folder, unzip the osTicket-v1.15.8 and move the upload folder into C:\inetpub\wwwroot







<img width="423" height="328" alt="osticket12" src="https://github.com/user-attachments/assets/d04feffc-7d46-4359-b97f-471bcaab3b09" />



Extract the folder by right clicking on it and clicking extract all. I'm going to extract the folder to the default destination





<img width="608" height="307" alt="screeenshot-extractfolderosticket" src="https://github.com/user-attachments/assets/b8ceafff-55b8-4dd1-9717-48147633954a" />

After extracting the folder, I'm going to click on the newly made unzipped folder and once it's open, we'll see two folders. I'm going to move the upload folder into the C:\inetpub\wwwroot folder




<img width="552" height="562" alt="Screenshot inetpub" src="https://github.com/user-attachments/assets/5915e6a8-17be-4299-a628-7acf5e7954b1" />




We'll see two folders after the extraction called scripts and upload. We're moving the upload folder into the inetpub\root folder. 







<img width="550" height="537" alt="Screenshot-osticket-move-to-root" src="https://github.com/user-attachments/assets/7d45ebde-0672-40c1-ae1c-f9a284eca6e3" />




After moving the uploade folder into the inetpub\wwwroot folder we're going to rename it to osTicket and the name has to be spelled exactly like it's written or it can mess up the configuration









<img width="530" height="530" alt="screenshot-uploadrename" src="https://github.com/user-attachments/assets/23f00e83-9fae-45ef-9113-98eb281ef307" />








To rename the folder, right-click on the upload folder and type in osTicket and continue. Just make sure it's spelled precisely how it's written











<img width="524" height="535" alt="Screenshot 2026-01-25 165943" src="https://github.com/user-attachments/assets/78fc3264-59a7-4aad-ab72-f30c8b4b5799" />




Reload the IIS server and stop and start the server again






<img width="497" height="554" alt="Screenshot 2026-01-25 170550" src="https://github.com/user-attachments/assets/ca613674-eec7-4486-99ec-133b36718531" />






























<img width="548" height="551" alt="Screenshot 2026-01-25 170805" src="https://github.com/user-attachments/assets/5c9c4e3f-5f06-4484-870e-5c88c5f8fc3e" />



After that go to sites-> Default-> osTicket then if you look on the right you can see the browse .80 tab. Click that and we can observe the changes in our osTicket











<img width="541" height="572" alt="Screenshot 2026-01-25 171012" src="https://github.com/user-attachments/assets/d099ccfc-296e-4732-8410-518c1632ddc0" />

 


















<img width="512" height="534" alt="Screenshot 2026-01-25 171139" src="https://github.com/user-attachments/assets/a62c3bff-546c-4b3e-ac89-e7e7f632c80d" />





After clicking the browse *80 button, it should refresh and the osTicket installer should be present on the actual server




<img width="463" height="538" alt="Screenshot 2026-01-25 171303" src="https://github.com/user-attachments/assets/e5def46d-fbc1-4c2f-8257-034b7418a6d9" />






If we look at the screenshot, you can see that some extensions aren't enabled so I'm going enable those extensions



To do that, open up the IIS menu again and go to sites,-> Default-> osTicket and double-click on PHP Manager








<img width="540" height="559" alt="Screenshot 2026-01-25 172046" src="https://github.com/user-attachments/assets/d0ca580b-c491-4e6c-9e64-b6f3ebe05b69" />
















<img width="555" height="573" alt="screenshot-phpregister" src="https://github.com/user-attachments/assets/aa563702-855c-4f4d-8fcb-86598e22c785" />






Click on enable or disable and extension and we're going to enable three extensions


Enable: php_imap.dll,
Enable: php_intl.dll,
Enable: php_opcache.dll




<img width="546" height="578" alt="Screenshot 2026-01-25 172753" src="https://github.com/user-attachments/assets/18d0aa21-dc2c-41a0-ac39-55333ef18341" />




After enabling these extensions, we're going to go back into the osTicket site in our browser and observe the changes.







 
 
 
<img width="549" height="566" alt="Screenshot 2026-01-25 173138" src="https://github.com/user-attachments/assets/c71d7150-0d08-4071-a3d4-b9c57ff518b8" />




As you can see, the extensions that had a x has now been enabled. The last two extensions aren't really important so no need to worry about those



So for the next step, I'm going to rename a folder in our hard drive to ost-config.php. This is necessary for osTicket to be configured properly



To get back here, just open up file explorer again and if you're confused on how to open it then you can press windows key and e and it'll bring up the file explorer




Click on inetpub and go to wwwroot folder









<img width="553" height="582" alt="Screenshot 2026-01-25 173755" src="https://github.com/user-attachments/assets/c46b48cf-eb1a-41d4-8b35-d8cf94487fac" />





















<img width="542" height="560" alt="Screenshot 2026-01-25 173934" src="https://github.com/user-attachments/assets/7f00be09-e375-413c-a6db-aa891f0b3e6d" />





Click on osTicket folder 















<img width="540" height="562" alt="Screenshot 2026-01-25 174125" src="https://github.com/user-attachments/assets/28c209bb-0fa0-4c31-bcbb-620481c8fb19" />




Next, click on the include folder










<img width="580" height="580" alt="Screenshot 2026-01-25 174323" src="https://github.com/user-attachments/assets/698932ac-b26e-4e92-b02c-c51822782192" />





After clicking on the include folder, we're going to find the ost-sample-config folder and once we find it, right click it and rename it to ost-sampleconfig.php. This has to be spelled correctly or else it'll mess up the config












<img width="554" height="570" alt="Screenshot 2026-01-25 174447" src="https://github.com/user-attachments/assets/c037f91a-9d91-4708-8693-11d621d2d1ab" />















<img width="539" height="569" alt="Screenshot 2026-01-25 174746" src="https://github.com/user-attachments/assets/3329c591-a8a7-4f54-afd6-ea1b0d593816" />







In order to be able make changes on the backend of the osTicket server, we have to enable permissions for this config folder so to do that, we right click the ost-config.php folder and click on properties













<img width="558" height="589" alt="Screenshot 2026-01-25 174953" src="https://github.com/user-attachments/assets/17e4f122-80f4-4518-b9e4-776db67e164d" />
















After getting to the properties menu, click on the security tab then click advanced








<img width="404" height="272" alt="Screenshot 2026-01-25 175222" src="https://github.com/user-attachments/assets/523e37ba-96c5-4c48-a390-7a2298e7d646" />



The advanced security settings for the config folder will open and from there, we're going to click on disable inheritance













<img width="498" height="311" alt="Screenshot 2026-01-25 182502" src="https://github.com/user-attachments/assets/d4e73ff9-d56f-4ba1-b313-edd551fc652c" />











Now there are no permissions so we're going to add our own permissions












 <img width="982" height="553" alt="Screenshot 2026-01-25 182727" src="https://github.com/user-attachments/assets/33b68da2-944d-4a08-9bef-871d802dfa32" />








Click on add to add new permissions

























<img width="622" height="644" alt="Screenshot 2026-01-25 183034" src="https://github.com/user-attachments/assets/9408d0b5-b76c-41ec-8b0a-132adbc294f5" />



On the next screen, click on select a principal and just for the ease of use and to make sure nothing goes wrong, i'm going to enter everyone in the object name group. You would not do this in a real-life environment though.















<img width="725" height="361" alt="Screenshot 2026-01-25 183814" src="https://github.com/user-attachments/assets/457f2eed-8c0f-4a7f-a005-05346f53a7ff" />



Now we're going to click full control for the basic permissions









<img width="756" height="356" alt="Screenshot 2026-01-25 184237" src="https://github.com/user-attachments/assets/ae36e664-c947-4c83-b6be-f9e1d895e070" />





So after enabling the permissions, this is how this advanced security settings configuration should be displaying









<img width="671" height="372" alt="Screenshot 2026-01-25 184450" src="https://github.com/user-attachments/assets/3066f799-68fe-4d5d-8500-c2a95adf1ead" />


 






 So now that the ost-config.php has full access to the configuration file we can continue the setup on osTicket













<img width="549" height="566" alt="Screenshot 2026-01-25 173138" src="https://github.com/user-attachments/assets/7816c119-9723-41c1-b906-b14b67f889a6" />





We should be able to name this whatever we want so for me, I'm going to name my helpdesk Malcolm's helpdesk


For the email, that doesn't matter. You can just put some random email




For the first and last name under the admin user section, you can put whatever you want in there. You can use your name if you want to.



For admin username and password we need to remember what you're going to use for it. The email address under the Admin User tab needs to be different from the setup email that you just used when naming your help desk








<img width="634" height="669" alt="Screenshot 2026-01-25 185924" src="https://github.com/user-attachments/assets/057497dd-2a35-4377-95b0-a5dd2fa8e885" />



Now we're going install Heidi SQL and that's located back in the osTicketInstallationfiles











<img width="500" height="367" alt="Screenshot 2026-01-25 190916" src="https://github.com/user-attachments/assets/702d5020-9c24-4f78-b0d7-b79f1b400ab7" />









Click on HeidiSQL file and start the installation











<img width="614" height="559" alt="Screenshot 2026-01-25 191145" src="https://github.com/user-attachments/assets/31f73fb4-fd5c-4ef1-99d0-9f6d35e6e85c" />



























<img width="420" height="292" alt="Screenshot 2026-01-25 191533" src="https://github.com/user-attachments/assets/d11a6f98-a2ca-4b36-923c-30f2a53f9258" />







































<img width="359" height="282" alt="Screenshot 2026-01-25 191559" src="https://github.com/user-attachments/assets/38417276-d8a1-4e83-b20c-0ce792c7df08" />







































<img width="347" height="276" alt="Screenshot 2026-01-25 191634" src="https://github.com/user-attachments/assets/7d5f82ee-7740-4444-8bc8-d9714b3ed5fe" />









 


























<img width="353" height="269" alt="Screenshot 2026-01-25 191721" src="https://github.com/user-attachments/assets/675ed51c-a8e9-46fd-a3b5-d4b81281f0d6" />





































<img width="362" height="272" alt="Screenshot 2026-01-25 191759" src="https://github.com/user-attachments/assets/5aeb1802-174a-4f7e-91cd-04588ec245de" />






































<img width="358" height="279" alt="Screenshot 2026-01-25 192005" src="https://github.com/user-attachments/assets/f518e66c-8b57-4932-a4a0-1427329e59fe" />





















So what I'm going to do is use HeidiSQL to communicate with the database that we set up. On the HeidiSQL home page click on new























<img width="426" height="294" alt="Screenshot 2026-01-25 192500" src="https://github.com/user-attachments/assets/006e3c53-f71e-4891-862b-42e9a5c745c4" />


















So after clicking next we're going to make a new session to log in to. If you remember earlier in the tutorial, we downloaded the MySQL install file and we had to set up the username and password. It's time to reenter it. So I chose something that would be simple. root for the username and password.

































After putting in our credentials, a connection will be opened to our database
























<img width="1217" height="678" alt="Screenshot 2026-01-25 193135" src="https://github.com/user-attachments/assets/d5c41e6f-cfa4-4c2c-b30c-0c628e01aefe" />






Right-Click on unnamed and click on create new and then click on database



















<img width="626" height="647" alt="Screenshot 2026-01-26 020343" src="https://github.com/user-attachments/assets/6d682124-f2f6-47f9-8887-b47c40ff7d5f" />




















So after connecting to the MySQL database, we have to make a database called osTicket and it has to be spelled exactly like this























<img width="635" height="664" alt="Screenshot 2026-01-26 020720" src="https://github.com/user-attachments/assets/61c07b52-fe9e-40d0-a6e1-b1d187db9cd2" />






After you finish creating the new database, you should see the osTicket database in your window.

















<img width="672" height="687" alt="Screenshot 2026-01-26 020856" src="https://github.com/user-attachments/assets/95193c87-8f39-485f-a9fa-a7caab005669" />














So osTicket is going to make use of this database that's set up now. It's empty at this point but once we actually start using, then this is how all of the data from the osTicket system will be stored and handled












So we can go back to the osTicket install screen in our browser and finish the setup by entering our MySQL Database, Username, and Password. The MySQL Database name will be osTicket, then put the username and password for the MySQL server that we set up and click install now after everything has been entered.



























<img width="632" height="376" alt="Screenshot 2026-01-26 021646" src="https://github.com/user-attachments/assets/acea7fa5-a842-4717-be6a-b4fd3503809e" />












































<img width="625" height="642" alt="Screenshot 2026-01-26 021935" src="https://github.com/user-attachments/assets/070a0c83-c05e-471e-8e18-7c1a330a7a60" />









And this is how I was able to install a open source ticketing system. It wasn't too hard but you have to do everything step by step to make sure no configurations are messed up during the process. One miscue and you may have to start all the way back over.










To log in to this account, we would go back into the web browser and type this url:




http://localhost/osTicket/scp/login.php. This is for the admin user login








http://localhost/osTicket/: This link will be for the end users log in and just to show you how this would work






















<img width="617" height="647" alt="Screenshot 2026-01-26 023154" src="https://github.com/user-attachments/assets/9f2ada5d-f89f-4747-885f-a43e0bd9607a" />













Log in page for the admin





























































