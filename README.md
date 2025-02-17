
<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://youtu.be/LOzmM5ZjKi0?si=STw6QM9ySkw-jWcs)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Create Virtual Machines (Microsoft Azure)
- Install osTicket files
- Enable IIS with CGI
- Install C++ drive redistributable
- Install MySQL
  

<h2>Installation Steps</h2>

![image](https://github.com/user-attachments/assets/85c14ac0-30cf-411d-be98-e780269d8f9f)


>>
</p>
<p>
Create a resource group inside Microsoft Azure. Then Create a Windows 10 virtual machine.
</p>
<br />

![image](https://github.com/user-attachments/assets/e869aefe-c354-4808-a04c-2ca9984754c3)

Once your deployment of your virtual machine is completed, then you will go to osTicket virtual machine that you created and look up the Public IP address. This address is needed to connect to your remote desktop.

![image](https://github.com/user-attachments/assets/922a0b74-2270-4840-bf7a-24f4b18e69a1)

After remote desktop is installed, take the IP address from your virtual machine and select "add PC" on your remote desktop device and input the IP address.

![image](https://github.com/user-attachments/assets/9688de5b-75b5-44ad-bc8d-8a5d2007b655)



Inside of the remote dektop, open the internet to https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and download the zip file. Once the zip file is downloaded a zip folder will be placed on your desktop. Select extract all from this folder.

![image](https://github.com/user-attachments/assets/301b48b1-45de-4f70-8da9-1c93a3ce639b)

Next we will enable IIS (internet information services) in windows (remote desktop) with CGI by going to Control Panel and then go to programs and select "turn windows features on/off".

![image](https://github.com/user-attachments/assets/ef7d8a6a-d401-400f-b6d8-27d274b82f52)

Now that we have IIS installed, we are going to install CGI. in the same folder, expand the IIS folder and you will see World Wide Web Services. This is a dependency that osticket needs to work.

![image](https://github.com/user-attachments/assets/d36f960e-4a68-4ca0-9596-f83a1547a0fc)

After expanding the World Wide Web Services folder, you want to then scroll to Application Development Features and expand that folder and select CGI.

![image](https://github.com/user-attachments/assets/560061f8-9459-40a7-9e2d-7ab7ab2929a5)


From the osticket installation files folder, install PHP manager for IIS (PHPManagerForIIS_V1.5.0.msi) as well as installing the Rewrite Module (rewrite_amd64_en-US.msi).

![image](https://github.com/user-attachments/assets/35a3e803-bea6-4150-bda6-0380c691e14c)


create the directory C:\PHP and from the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

![image](https://github.com/user-attachments/assets/649173f9-1613-4c5f-9ec5-a0b65eef1ef8)


From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe (also known at C++ redistributable) and then install MySQL (mysql-5.5.62-win32.msi)

![image](https://github.com/user-attachments/assets/5561a1d6-c006-41ad-aa1d-4f61c2ffbe78)

once MySQL is installed, open IIS as admin and register PHP from within the IIS.

![image](https://github.com/user-attachments/assets/070b7e2e-706a-42e7-ab22-168f93396636)

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to "osticket". Then go to "sites" ->default -> osTicket and right click Browse *80.


![image](https://github.com/user-attachments/assets/fd032aa6-8e98-4370-b803-4af74800c2f0)




Next, rename ost-config.php from: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php and change it to: C:\inetpub\wwwroot\osTicket\include\ost-config.php



![image](https://github.com/user-attachments/assets/755df1db-1044-4af3-80b0-816b4ab00a79)

Once the files have been renamed, next you want to open file explorer to give the software permissions in ost-config.php. Select disable inheritance -> Remove All and add 
new permissions -> Everyone -> All. It is important to note that in a real life system, it is not a good idea to select "everyone" but for this tutorial we will be allowing everyone to have access and then we can customize permissions inside of osTicket.

![image](https://github.com/user-attachments/assets/86dc1a36-9489-47c0-861f-563b1bb82fb2)

Once you have given the software permissions, your screen should look like the following. Inside of the osTicket basic installation page, you will be able to create an admin.

![image](https://github.com/user-attachments/assets/e7752b5e-5345-446f-8284-2234253d9b32)








