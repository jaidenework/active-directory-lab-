# Azure Active Directory

# introduction
This lab demonstrates how to build a basic Active Directory environment in Azure using two virtual machines:
DC01 – Domain Controller, DNS, and DHCP server
Client01 – Windows client joined to the domain
The purpose of this lab is to practice domain management, user creation, and remote desktop access in a safe, isolated environment.

# section 1: create resource group and virtual machine in Azure
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%201.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%202.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%203.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%204.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%205.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%206.png)

# section 2: configure virtual machine to have a static IP and set DNS to the static IP

# section 3: allow LDAP and DNS

# section 4: deploy the Virtual machine in Windows app

# section 5: install Active Directory and create a domain

# section 6: create a domain controller account for the Active Directory 

# section 7: log into the domain controller account and install DHCP

# section 8: set up DHCP scope

# section 9: add PowerShell script to automate user account to the domain

# section10: create second virtual machine  and set DNS to the first virtual machine's private IP

# section 11: make sure remote desktop logon is allowed for the second virtual machine

# section 12: make sure everything shows up when pinging 

# section 13: have the second virtual machine join the domain in the Active Directory

# section 14: make sure everything works with remote logons 

