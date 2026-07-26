# Incident Report

Ticket #: LAB001

A+ Objective: 2.6 (Core 2)

Date: 2026 - 07 - 26

Environment: VirtualBox — Windows 10 Client / Windows Server 2022

--------------------------------------------------------------------

#### Problem Description: 
The two machines (Client and Server) just had a clean install. The internal network has been set up, they can ping each other. However, this is not enough for the required workflow of the company. Active Directory needs to be set up, first on the server and then on the client.

#### Root Cause: 
A clean Installation.

#### Resolution Steps:
1 - Install Active Directory on the server via the Server Manager (Add roles and features button).
2 - Create and configure the Domain. I used the name lab.local
3 - After the automatic restart, create a user using the Server Manager (again). Tools > Active Directory Users and Computers. I created an user with the credentials LAB\tuser password:theP@55word
4 - Boot the client VM and make it a part of the domain. Right-click Start > System > Rename this PC (Advanced). After introducing the domain name (lab.local) and login in with the Administrator credentials, the computer will restart and be a part of the Windows Domain.
5 - A new option will appear in the login screen (Other user) and it will allow us to login to the Domain with the user we created earlier. See screenshot.

#### Outcome:
A Windows Domain has been created and the client machine is a part of it. It will allow us to use the Active Directory and change configurations on the client machine without having to directly tinker with it.
