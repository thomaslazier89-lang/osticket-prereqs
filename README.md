🟦 osTicket - Prerequisites and Installation

This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.

📘 Learning Outcomes

Configure a virtual server

Connect server with client machines

Install and configure ticketing software for admins, agents, and users

Understand the essential elements of ticket submission and resolution

🖥️ Environments and Technologies Used

Microsoft Azure (Virtual Machines / Compute)

Remote Desktop

Internet Information Services (IIS)

🧩 Operating Systems Used

Windows 10 (21H2)

📋 List of Prerequisites

Enable Internet Information Services (IIS)

Install Web Platform Installer

Install MySQL

Install C++ Redistributable

Configure Permissions and Install osTicket

🛠️ Installation Steps
Step 1 — Azure Account Setup

If you do not have an Azure account, navigate to
microsoft.azure.com

and set up a free or pay-as-you-go account.

Step 2 — Create a Virtual Machine (VM)




Next, navigate to the
Azure Portal
,
log in, and create a virtual machine (VM).

Step 3 — Configure VM Basics

Give your VM an appropriate name and set your region to East US 2 for cost purposes.

Step 4 — Optimize VM Settings

Set up your VM as above to optimize speed and cost.
Use the username/password combination: Adminuser / osTicketPassword1.

⚠️ Security Reminder:
Including passwords in plain text is strongly discouraged in production environments.
Use a password manager such as KeePass, LastPass, or NordPass.

Step 5 — Log Into the VM






Log into your newly created VM using its public IP and the credentials you set earlier.

Step 6 — Download the osTicket Installation Files

Within the VM, open this webpage or copy and paste the following link to download the installer:

osTicket Installation File

Step 7 — Extract the Files

Find the downloaded zip file → Right-click → Extract All
Select your Desktop as the destination folder.

Step 8 — Enable CGI in IIS

To install IIS with the Common Gateway Interface:

Open Control Panel

Go to Add or Remove Features

Open Turn Windows Features On or Off

Navigate to:
Internet Information Services → Application Development Features → CGI

Step 9 — Install PHP Manager + URL Rewrite

Next, install PHP Manager and URL Rewrite.

Step 10 — Set Up PHP Directory

Create a new folder:

C:\PHP


Extract the php-7.3.8 zip file into this folder.

Step 11 — Install VC Redist + MySQL

Install:

VC_redist.x86.exe

MySQL 5.5.62

For MySQL, use:

Typical Setup →

Launch Configuration Wizard →

Standard Configuration
