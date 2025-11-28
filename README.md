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

![Login 1](https://i.imgur.com/sq5rTOF.png)  
![Login 2](https://i.imgur.com/W6eBwIL.png)  
![Login 3](https://i.imgur.com/fd5O8mm.png)

Use your VM’s **public IP** to connect.

## 6. Download the osTicket Installation Files

![Download](https://i.imgur.com/SgAgGz1.png)

Download here:  
https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0

## 7. Extract the Files

![Extract Files](https://i.imgur.com/GeRjOPp.png)

Right-click → **Extract All** → choose Desktop.

## 8. Enable CGI in IIS

![IIS Setup](https://i.imgur.com/JGA0G2I.png)

Navigate to:

**Control Panel → Add/Remove Features → Turn Windows Features On or Off → IIS → Application Development Features → CGI**

## 9. Install PHP Manager & URL Rewrite

![PHP Manager](https://i.imgur.com/RrT7jLd.png)

Install:

- PHP Manager  
- URL Rewrite  

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

## 13. Register PHP and Reload IIS

## 14. Open IIS as an Administrator

## 15. Install osTicket v1.15.8 and Reload IIS

## 16.

## 17.

## 18.
# 🎉 Installation Complete!
