# Basic Home Lab Running Active Directory

This repository provides a step-by-step guide on setting up a basic home lab running Active Directory using Oracle VirtualBox and Windows Server 2019. Following a tutorial by [Josh Madakor](https://www.youtube.com/@JoshMadakor), this setup allows users to gain hands-on experience with Active Directory, DHCP, domain management, and user authentication in a virtualized environment.

## Overview

The guide covers the entire process, from downloading and configuring VirtualBox to installing Windows Server 2019 and Windows 10, setting up a domain controller, and connecting a client machine to the domain.

## Key Steps Included
  1. Setting Up VirtualBox
     - Download and install [Oracle VirtualBox](https://www.virtualbox.org/).
     - Download [Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO) and [Windows Server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019)
 ISO files.
  2. Creating the Domain Controller
     - Set up a new Virtual Machine (VM) for the domain controller.
     - Assign two network adapters (one for internet access, one for a private network).
     - Install Windows Server 2019 and configure IP settings.
     - Name the server and install Active Directory Domain Services (AD DS).
  3. Configuring Network and Routing
     - Enable internet access for private network clients.
     - Configure DHCP on the domain controller.
  4. Populating Active Directory
     - Use a [PowerShell script](https://github.com/MSMercado/Basic-Home-Lab-Active-Directory/tree/main/AD_PS-master) to create 1,000 Active Directory users automatically.
  5. Setting Up a Client Machine
     - Create a new VM for a Windows 10 client.
     - Connect the client to the private network.
     - Join the client to the Active Directory domain.
  6. Testing Domain Login
     - Log into the client machine using a domain account.


## Diagram and Screenshots

This repository includes a network diagram and step-by-step screenshots to help visualize the setup process.

This lab provides a great starting point for learning Active Directory administration, network configuration, and domain management in a safe, controlled environment. 🚀

Network Diagram:
![Diagram](active_directory_diagram.jpg)

## Creating a new virtual machine

To create a new virtual machine in VirtualBox, start by clicking on "New" and entering "Domain Controller" as the name. Next, choose "Windows Server 2019" as the operating system and select its ISO file as the boot media. This will prepare the virtual machine for installation, allowing you to proceed with setting up the domain controller.

![](attachments/Pasted%20image%2020230402145533.png)

![](attachments/Pasted%20image%2020230402145610.png)

##  Configuring Network Adapters for the Virtual Machine

To configure the virtual machine, assign it two network adapters—one for internet access and the other for the private network. This setup ensures that the domain controller can communicate externally while also managing internal network traffic.

![](attachments/Pasted%20image%2020230402145806.png)

![](attachments/Pasted%20image%2020230402145820.png)

##  Installing Windows Server 2019 and Configuring IP Addressing

Install Windows Server 2019 on the virtual machine and set up the IP addressing for the internal network. This ensures proper communication between the domain controller and other devices within the private network.

![](attachments/Pasted%20image%2020230402150458.png)

![](attachments/Pasted%20image%2020230402150538.png)

##  Naming the Server and Installing Active Directory

Assign a name to the server and install Active Directory to set up the domain. This step establishes the domain controller, allowing user authentication and network management within the environment.

![](attachments/Pasted%20image%2020230402150727.png)

![](attachments/Pasted%20image%2020230402153253.png)

##  Configuring Routing for Internet Access

Set up routing on the domain controller to allow clients on the private network to access the internet. This ensures seamless connectivity while maintaining network control and security.

![](attachments/Pasted%20image%2020230402153829.png)

![](attachments/Pasted%20image%2020230402153904.png)

![](attachments/Pasted%20image%2020230402154123.png)

##  Setting Up DHCP on the Domain Controller

Configure the DHCP service on the domain controller to automatically assign IP addresses to devices on the private network. This simplifies network management and ensures efficient IP allocation.

![](attachments/Pasted%20image%2020230402154312.png)

![](attachments/Pasted%20image%2020230402154041.png)

![](attachments/Pasted%20image%2020230402154439.png)


##  Running the PowerShell Script to Create Users

Execute the PowerShell script to automatically create 1,000 users in Active Directory. This streamlines the process of user management and simulates a real-world environment with multiple accounts.

[Power Shell script for creating users](https://github.com/MSMercado/Basic-Home-Lab-Active-Directory/tree/main/AD_PS-master)

##  Creating a Client Virtual Machine and Installing Windows 10

Create a new virtual machine named "Client1" and install Windows 10 on it. This allows you to set up a client machine that can be connected to the domain for testing and management.

![](attachments/Pasted%20image%2020230402155056.png)


##  Connecting the Client Machine to the Private Network and Joining the Domain

Connecting the Client Machine to the Private Network and Joining the Domain

![](attachments/Pasted%20image%2020230402155713.png)

![](attachments/Pasted%20image%2020230402155807.png)

##  Logging into the Client Machine with a Domain Account

Log into the client machine using a domain account. This verifies the successful domain integration and allows access to network resources based on user permissions.

![](attachments/Pasted%20image%2020230402160005.png)

![](attachments/Pasted%20image%2020230402160120.png)
