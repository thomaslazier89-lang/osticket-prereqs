# 🟦 osTicket — Prerequisites and Installation

<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="40%">
</p>

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system **osTicket**.

---

## 📘 Learning Outcomes

- Configure a virtual server  
- Connect server with client machines  
- Install and configure ticketing software for admins, agents, and users  
- Understand the essential elements of ticket submission and resolution  

---

## 🖥️ Environments and Technologies Used

- **Microsoft Azure (Virtual Machines / Compute)**  
- **Remote Desktop**  
- **Internet Information Services (IIS)**  

---

## 🧩 Operating Systems Used

- **Windows 10 (21H2)**  

---

## 📋 List of Prerequisites

- Enable Internet Information Services (IIS)  
- Install Web Platform Installer  
- Install MySQL  
- Install C++ Redistributable  
- Configure permissions and install osTicket  

---

# 🛠️ Installation Steps

## 1️⃣ Create or Sign In to an Azure Account

<p align="center">
  <figure>
    <img src="https://i.imgur.com/rC9ZI2h.png" alt="Azure signup page" width="70%">
    <figcaption><em>Azure account signup portal</em></figcaption>
  </figure>
</p>

If you do not have an Azure account, go to  
<a href="https://microsoft.azure.com">https://microsoft.azure.com</a> and create a **free** or **pay-as-you-go** account.

---

## 2️⃣ Create an Azure Virtual Machine (VM)

<div align="center">
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/cN5HPsV.png" alt="Azure VM basics screen" width="45%">
    <figcaption><em>VM creation wizard - Basics</em></figcaption>
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/0bX6ZiH.png" alt="Azure VM review screen" width="45%">
    <figcaption><em>VM creation wizard - Review and create</em></figcaption>
  </figure>
</div>

Navigate to the <a href="https://portal.azure.com/auth/login">Azure Portal</a>, log in, and create a **Virtual Machine**.

---

## 3️⃣ Configure VM Basics

<p align="center">
  <figure>
    <img src="https://i.imgur.com/Olnnzeo.png" alt="Azure VM basics configuration" width="70%">
    <figcaption><em>Configure VM name, image, and region</em></figcaption>
  </figure>
</p>

Choose region **East US 2** for better cost efficiency.

---

## 4️⃣ Optimize Your VM Settings

<p align="center">
  <figure>
    <img src="https://i.imgur.com/UsGysGz.png" alt="Azure VM size and settings" width="70%">
    <figcaption><em>Select a cost-effective VM size and confirm credentials</em></figcaption>
  </figure>
</p>

Use the following credentials for this lab:

```text
Username: Adminuser
Password: osTicketPassword1
```

> ⚠️ **Security Reminder:**  
> Passwords in plain text are unsafe in real-world environments.  
> Always use a secure password manager (KeePass, LastPass, NordPass, etc.).  
> Credentials shown here are for lab/demo purposes only.

---

## 5️⃣ Log Into the VM

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

---

## 6️⃣ Download the osTicket Installation Files

<p align="center">
  <figure>
    <img src="https://i.imgur.com/SgAgGz1.png" alt="Browser showing osTicket download link" width="70%">
    <figcaption><em>Download osTicket installation files inside the VM</em></figcaption>
  </figure>
</p>

Within the VM, open this link to download the installer:

- <a href="https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&amp;export=download&amp;authuser=0">osTicket Installation File (Google Drive)</a>

---

## 7️⃣ Extract the Files

<p align="center">
  <figure>
    <img src="https://i.imgur.com/GeRjOPp.png" alt="Extracting osTicket zip file" width="70%">
    <figcaption><em>Extract the osTicket zip file to the Desktop</em></figcaption>
  </figure>
</p>

Locate the downloaded zip file in your **Downloads** folder, right-click it, and select **Extract All**.  
Set the destination to your **Desktop**.

---

## 8️⃣ Enable CGI in IIS

<p align="center">
  <figure>
    <img src="https://i.imgur.com/JGA0G2I.png" alt="Windows features - IIS and CGI" width="70%">
    <figcaption><em>Enable IIS and CGI from Windows Features</em></figcaption>
  </figure>
</p>

To install IIS with CGI support:

1. Open **Control Panel**  
2. Go to **Programs and Features** → **Turn Windows features on or off**  
3. Enable:  
   - **Internet Information Services**  
   - Under **Application Development Features**, check **CGI**

---

## 9️⃣ Install PHP Manager & URL Rewrite

<p align="center">
  <figure>
    <img src="https://i.imgur.com/RrT7jLd.png" alt="Installing PHP Manager and URL Rewrite" width="70%">
    <figcaption><em>Run installers for PHP Manager and URL Rewrite</em></figcaption>
  </figure>
</p>

Download and install:

- **PHP Manager for IIS**  
- **URL Rewrite Module**  

---

## 🔟 Create the PHP Directory

<p align="center">
  <figure>
    <img src="https://i.imgur.com/RrT7jLd.png" alt="PHP folder and files" width="70%">
    <figcaption><em>Create C:\PHP and extract PHP binaries</em></figcaption>
  </figure>
</p>

Create a new folder:

```text
C:\PHP
```

Extract the **php-7.3.8** zip contents into this folder.

---

## 1️⃣1️⃣ Install VC Redist + MySQL

<p align="center">
  <figure>
    <img src="https://i.imgur.com/RrT7jLd.png" alt="MySQL and VC Redist installation" width="70%">
    <figcaption><em>Install VC Redistributable and MySQL</em></figcaption>
  </figure>
</p>

Install:

- `VC_redist.x86.exe`  
- `MySQL 5.5.62`  

For MySQL, choose:

- **Typical Setup**  
- **Launch Configuration Wizard** (after install)  
- **Standard Configuration**  

---

# 🎉 Installation Complete!

You now have a Windows 10 VM configured with IIS, PHP, MySQL, and the osTicket installer files ready for configuration.

From here, you can proceed to:

- Configure osTicket in IIS  
- Set up the database and permissions  
- Complete the web-based installer  
- Begin using osTicket for ticket management

Happy labbing! 🧪
