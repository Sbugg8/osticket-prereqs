
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

- Create Virtual Machines (Microsoft Azure)
- Install osTicket files
- Install MySQL/ setup user name and password
- Item 4
- Item 5

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

After remote desktop is installed, take the IP address from your virtual machine and select "add PC" on your remote desktop device and input the IP address

![image](https://github.com/user-attachments/assets/9688de5b-75b5-44ad-bc8d-8a5d2007b655)



Inside of the remote dektop, open the internet to https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD and download the zip file. Once the zip file is downloaded a zip folder will be placed on your desktop. Select extract all from this folder.

![image](https://github.com/user-attachments/assets/301b48b1-45de-4f70-8da9-1c93a3ce639b)

Next we will enable IIS (internet information services) in windows (remote desktop) with CGI.

![image](https://github.com/user-attachments/assets/ef7d8a6a-d401-400f-b6d8-27d274b82f52)



