# 🟦 osTicket — Prerequisites and Installation

![osTicket logo](https://i.imgur.com/Clzj7Xs.png)

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system **osTicket**.

## 🖥️ Environments and Technologies Used

- **Microsoft Azure (Virtual Machines / Compute)**  
- **Remote Desktop**  
- **Internet Information Services (IIS)**  

## 🧩 Operating Systems Used

- **Windows 10 (21H2)**   

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
   
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/W6eBwIL.png" alt="Remote Desktop connection prompt" width="30%">
   
  </figure>
  <figure style="display:inline-block; margin: 0 10px;">
    <img src="https://i.imgur.com/fd5O8mm.png" alt="Windows login screen" width="30%">
   
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

![IIS Setup](https://i.imgur.com/MKHEZ9l.png)

Click **PHP Manager**. 

![IIS Setup](https://i.imgur.com/G1HavBE.png)

Click **Register new PHP version**.

![IIS Setup](https://i.imgur.com/r6saYWi.png)

Provide the path to the file.   

![IIS Setup](https://i.imgur.com/Ijiz0gO.png) 

Return to the **IIS Home Screen** by pressing the home or back icon on the taskbar and **Restart**.


## 15. Install osTicket v1.15.8 and Reload IIS

![osTicket Setup](https://i.imgur.com/8DuWmV1.png)

Unzip the **osTicket-v1.15.8.zip** in its default location. Enter the folder and copy **Upload** into **C:\inetpub\wwwroot**, renaming it **osTicket**. Reload **IIS** again.


## 16. Open the Extensions Page

![osTicket Setup](https://i.imgur.com/ZmsDPG2.png)

Go to **Sites → Default Web Site → osTicket** and look in the right sidebar for **Browse *:80 (http)**. Observe that some extensions are disabled by default.


## 17. Enable Extensions

![osTicket Setup](https://i.imgur.com/N38AwwM.png)

Return to **Sites → Default Web Site → osTicket** and open **PHP Manager**. Scroll down the page until you find **Enable or disable an extension**. 

Enable:
- **php_imap.dll**
- **php_intl.dll**
- **php_opcache.dll**

Return to **Sites → Default Web Site → osTicket** and click **Browse *:80 (http)** again to note the changes to the host website.


## 18. Configure PHP file

![osTicket Setup](https://i.imgur.com/6kQFPlD.png)

Rename **C:\inetpub\wwwroot\osTicket\include\ost-config.php** to **ost-config.php**


## 19. Assign Permissions

![osTicket Setup](https://i.imgur.com/2cxtcJ1.png)

Right-click **ost-config.php** and select *Properties**. Open the **Security** tab, click **Advanced** and **Disable Inheritance**. 

![osTicket Setup](https://i.imgur.com/4wB1QRT.png)

Finally, click **Add** and enter the object name **Everyone** in the text field. Give the principal **Full control**. Click OK twice, then press **Apply**.


## 20. Set Up osTicket

![osTicket Setup](https://i.imgur.com/4wB1QRT.png)

If not already open, reopen the **Browse *80: (http)** page in **IIS**. Click **Continue** twice to open the **osTicket Basic Installation** page.

![osTicket Setup](https://i.imgur.com/8Ml4LXO.png)

Fill out the information as above, making sure to set your **mySQL** settings accurately. Use 

```
root
root
```

as the username/password combination.


## 21. Install HeidiSQL

![osTicket Setup](https://i.imgur.com//rFyHkBZ.png)

Return to the osTicket desktop file and install **HeidiSQL**. Open the program and create a new session with
```
root
root
```
as the User/Password. 


# 🎉 Installation Complete!
