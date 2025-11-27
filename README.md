<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Learning Outcomes</h2>

-Configure a virtual server <br />
-Connect server with client machines <br />
-Install and configure ticketing software for admins, agents and users <br />
-Understand the essential elements of ticket submission and resolution <br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS)
- Install Web Platform Installer
- Install mySQL
- Install C++ Redistributable
- Configure Permissions and Install osTicket

<h2>Installation Steps</h2>

<figure>
  <img src="https://i.imgur.com/rC9ZI2h.png" width="80%">
  <figcaption> If you do not have an Azure account, navigate to [microsoft.azure.com](https://microsoft.azure.com) and set up a free or pay-as-you-go account..</figcaption>
</figure>

<br/>


<figure>
<img src="https://i.imgur.com/cN5HPsV.png" height="80%" width="80%" alt="VM Create"/>
<img src="https://i.imgur.com/0bX6ZiH.png" height="80%" width="80%" alt="VM Create"/>
  <figcaption>Next, navigate to the[Azure Portal](https://portal.azure.com/auth/login/ "Azure Portal Page"), login and create a virtual machine (VM). </figcaption>
</figure>
<br/>

<figure>
<img src="https://i.imgur.com/Olnnzeo.png" height="80%" width="80%" alt="VM Create"/>
<figcaption>Give your VM an appropriate name and set your region to East- US 2 for cost purposes.</figcaption>
</figure>
<br/>

<figure>

<img src="https://i.imgur.com/UsGysGz.png" height="80%" width="80%" alt="VM Create"/>
<figcaption>Set up your VM as above to optimize speed and cost. Use the username/password combination: Adminuser/osTicketPassword1. Fill the license check box at the end of the page, otherwise an error will be generated when you create the VM. Finally, click Review + Create and click Create at the bottom of the summary screen.  </figcaption>
</figure>
<br /><br/>


<figure>
<img src="https://i.imgur.com/sq5rTOF.png" height="80%" width="80%" alt="VM Create"/>fd5O8mm
<img src="https://i.imgur.com/W6eBwIL.png" height="80%" width="80%" alt="VM Create"/>
<img src="https://i.imgur.comfd5O8mm.png" height="80%" width="80%" alt="VM Create"/>
 <figcaption>Log into your newly created VM using its public IP address, and the credentials you created earlier.</figcaption>
</figure>
<br/>

<figure>
<img src="https://i.imgur.com/sq5rTOF.png" height="80%" width="80%" alt="VM Create"/>
<img src="https://i.imgur.com//fd5O8mm.png" height="80%" width="80%" alt="VM Create"/>
 <figcaption>Log into your newly created VM, using its public IP address.</figcaption>
</figure>
<br />

