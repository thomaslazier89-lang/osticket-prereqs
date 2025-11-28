# 🟦 osTicket — Prerequisites and Installation

![osTicket logo](https://i.imgur.com/Clzj7Xs.png)

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system **osTicket**.

## 📘 Learning Outcomes

- Configure a virtual server  
- Connect server with client machines  
- Install and configure ticketing software for admins, agents, and users  
- Understand the essential elements of ticket submission and resolution  

## 🖥️ Environments and Technologies Used

- **Microsoft Azure (Virtual Machines / Compute)**  
- **Remote Desktop**  
- **Internet Information Services (IIS)**  

## 🧩 Operating Systems Used

- **Windows 10 (21H2)**  

## 📋 List of Prerequisites

- Enable Internet Information Services (IIS)  
- Install Web Platform Installer  
- Install MySQL  
- Install C++ Redistributable  
- Configure permissions and install osTicket  

# 🛠️ Installation Steps

## 1. Create or Sign In to an Azure Account

![Azure Account](https://i.imgur.com/rC9ZI2h.png)

If you do not have an Azure account, go to:  
https://microsoft.azure.com

## 2. Create an Azure Virtual Machine (VM)

![Azure VM Screen 1](https://i.imgur.com/cN5HPsV.png)  
![Azure VM Screen 2](https://i.imgur.com/0bX6ZiH.png)

Navigate to the  
[Azure Portal](https://portal.azure.com/auth/login),  
log in, and create a virtual machine.

## 3. Configure VM Basics

![VM Create](https://i.imgur.com/Olnnzeo.png)

Choose region **East US 2** for cost savings.

## 4. Optimize Your VM Settings

![VM Settings](https://i.imgur.com/UsGysGz.png)

Use credentials:

```
Adminuser
osTicketPassword1
```

## 5. Log Into the VM

<div align="center">
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/sq5rTOF.png" alt="VM overview with public IP" width="30%">
    <figcaption><em>Remote Desktop</em></figcaption>
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/W6eBwIL.png" alt="Remote Desktop connection prompt" width="30%">
    <figcaption><em>Remote Desktop connection dialog</em></figcaption>
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/fd5O8mm.png" alt="Windows login screen" width="30%">
    <figcaption><em>Windows login screen inside the VM</em></figcaption>
  </figure>
</div>

Use your VM’s **public IP** and the credentials you configured to connect via Remote Desktop.

## 6. Download the osTicket Installation Files

![Download](https://i.imgur.com/SgAgGz1.png)

Download here:  
https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0

## 7. Extract the Files

![Extract Files](https://i.imgur.com/GeRjOPp.png)

Right-click → **Extract All** → choose Desktop.

## 8. Enable Internet Information Services with CGI

![IIS Setup](https://i.imgur.com/JGA0G2I.png)

Navigate to:

**Control Panel → Add/Remove Features → Turn Windows Features On or Off → Click IIS and Expand Drop-Down Menu→ Application Development Features → CGI**

## 9. Install PHP Manager & URL Rewrite

![PHP Manager](https://i.imgur.com/RrT7jLd.png)

Install:

- **PHP Manager**  
- **URL Rewrite** 

## 10. Create the PHP Directory

![PHP Directory](https://i.imgur.com/RrT7jLd.png)

Create:

```
C:\PHP
```

Extract **php-7.3.8** into this folder.

## 11. Install VC Redist + MySQL

![MySQL Install](https://i.imgur.com/JJ6RA25.png)

Install:

- `VC_redist.x86.exe`
- `MySQL 5.5.62`

Choose:

- **Typical Setup**  
- **Launch Configuration Wizard**  
- **Standard Configuration**
- **Username/Password:**

```
root
root
```
## 12. Open IIS as an Administrator

![IIS Setup](https://i.imgur.com/fwrf7Wa.png)

Open **IIS** as an admin using the search bar.


## 13. Register PHP and Reload IIS 

<div align="center">
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/syshlq6.png" alt="Click PHP Manager" width="30%">
    <figcaption><em>Remote Desktop</em></figcaption>
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/G1HavBE.png" alt="Click Register PHP" width="30%">
    <figcaption><em>Click Register new PHP version</em></figcaption>
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/r6saYWi.png" alt="Remote Desktop connection prompt" width="30%">
    <figcaption><em>Provide the path to the file</em></figcaption>
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/Ijiz0gO.png" alt="Windows login screen" width="30%">
    <figcaption><em>Return to the IIS Home Screen and Restart</em></figcaption>
  </figure>
</div>

## 14. Open IIS as an Administrator

## 15. Install osTicket v1.15.8 and Reload IIS

## 16.

## 17.

## 18.
# 🎉 Installation Complete!
