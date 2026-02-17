# Azure Active Directory

# introduction
This lab demonstrates how to build a basic Active Directory environment in Azure using two virtual machines:
DC01 – Domain Controller, DNS, and DHCP server
Client01 – Windows client joined the domain
The purpose of this lab is to practice domain management, user creation, and remote desktop access in a safe, isolated environment.

# section 1: create resource group and virtual machine in Azure
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%201.png)

-Create a resource group, and while creating this, you have to choose a region that best works for you

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%202.png)

- Now create the virtual machine in Azure

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%203.png)

-When creating the virtual machine, go to select image and choose Windows Server 2019 Datacenter - x64 Gen 2

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%204.png)

- While creating the Virtual machine, create a name for the virtual machine. You then need to select the resource group you created before, and you need to make sure  the region matches up with the resource group
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%205.png)

- Here, you need to select a size that best works for you and create a username and password for the virtual machine
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3ff2d9cbe5b870ab0d6f1762539273d50011145c/Screenshot%206.png)

-You then need to make sure that RDP is allowed for your virtual machine. Click next until the network makes sure there is a public IP, and then click review + create, and then create

# section 2: configure virtual machine to have a static IP and set DNS to the static IP
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%207.png)

-Now that the virtual machine is created, go to the virtual machine in Azure and click the virtual machine you created 
-then go to the networking section, click on networking, click the network interface, and then click IP configuration

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%208.png)

- When you have clicked on IP configuration in the allocation section, it will be set to dynamic. Set it to static, and copy the private IP address provided

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%209.png)

- Now, on the left-hand side of the screen, under settings, you will see an option named DNS servers. Click that 
- When you are in this section, click Customize, and in the area below DNS server, input the private IP address from the static IP you configured earlier
- and then save and make sure to restart your virtual machine
  
# section 3: allow LDAP and DNS
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%2010.png)

-Go back to the network section for the virtual machine created and add port rules for DNS and LDAP

# section 4: deploy the Virtual machine in Windows app
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%2011.png)

-Make sure ot have the "Windows app" application installed, and in this app, click the plus sign in the top right corner and input the public IP address created for the virtual machine you have created so that you can deploy the virtual machine

# section 5: install Active Directory and create a domain
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2012.png)

-Now that you are in the Windows virtual machine you have created, click Add Roles and Features

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2013.png)

- Make sure that the right server is selected, which should be the virtual machine that you have created, displaying the static IP address you configured in Azure 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2014.png)

- for server roles select Active Directory Domain Services
- Now that that is selected, click next until you can install

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2015.png)

- After the installation is done, click the flag with the yellow warning sign
- now click promote this server to a domain controller
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2016.png)

- Now that we are here, select Add a new forest, and select a name for your domain and input it into the root domain name section
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2017.png)

- After picking a name, create a password for the domain controller account
- and click next until you see install, and then click install
  
# section 6: create a domain controller account for the Active Directory 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2018.png)

- After doing the domain controller in Server Manager, click on Tools and then click on Active Directory Users and Computers
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2019.png)

- Now, right-click the domain you made, go to New, and select organization unit
- Create the organization unit and name it whatever you want
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2020.png)

- now right click on the Organizational unit you created, click New, and go to user
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2021.png)

- Now that we have created a user, create one that you can remember( you can use your own name to make it easy)
- and then click next
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2022.png)

- for the password pick password never expires( is not normally recommended in a work space but works with the lab)
- Create a password for your user
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2023.png)

- Now that the user is created, right-click the user and go to properties
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2024.png)

- While in properties, click add for groups, the user can be in and input domain admins( to make this user account a domain admin)
- press ok and then apply
- After all this is done, sign out of the admin account

# section 7: log into the domain controller account and install DHCP
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/326d7c6b7d87c7554927698ab15f95fce1965b52/Screenshot%2025.png)

- When you log out of the admin account while in the Windows apps, go back to the virtual machine you created and now input the domain controller account user that you have created instead of the admin account

# section 8: set up DHCP scope
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2027.png)

- Now that you are in the domain controller account, go to Server Manager, go to Add Roles and Features, select DHCP, click on Add Features, and next until you see install

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2026.png)

- Now that DHCP is installed, go to Tools in the Server Manager and click DHCP

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2028.png)

- Under the domain you created, you should see IPv4, which you need to right-click and select new scope

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2029.png)

- after clicking add scope in the scope name section, input your private IP address, and at the end, put 100-200(so my private IP is 172.16.0.4, so I input 172.16.0.100-200)
- then press next
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2030.png)

- When you see the IP address range in the static IP section, input 172.16.0.100
- in the end IP address input 172.16.0.200
- and for the length input 24 while leaving the subnet mask as is after you pick the length
# section 9: add PowerShell script to automate user account to the domain
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2036.png)

-Now go to Internet Explorer 

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2037.png)

- input https://github.com/joshmadakor1/AD_PS/archive/master.zip
- to make sure you can get to this website. Go to Internet Settings, go to Security, and make sure this website is trusted
- save the download you go from the website inputted 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2038.png)

- go to your downloads and find names
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2039.png)

- click on the names document
- edit the document and input your name into the document, and save it to downloads

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2040.png)

-now click on the Windows sign, go to Windows PowerShell ISE, and right click
- Go to more and click on Run as Administrator
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2041.png)

- Once in the Windows PowerShell ISE, in the command line input "cd C:\users\a-Ennett\downloads"( I selected a-Ennett since that is the user account I am in, and I selected downloads since that is where the script I need is at)
- after that, click on add script
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2042.png)

- Now that we can add a script, select the script we were able to download from the website earlier(Which is "1_CREATE-USERS") and click on open
- 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2043.png)

- When the script is displayed, run the script, which is the green arrow in the top taskbar bar
- and this script is to automate multiple users into the Active Directory

# section 10: create the second virtual machine  and set the DNS to the first virtual machine's private IP
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2031.png)

- create the second virtual machine c
- Choose the same resource group you used in the first virtual machine
- Name the virtual machine and choose the same region used in the first virtual machine
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2032.png)

- In the image section, select the Windows 10 Enterprise version 22H2 - x64 Gen2
- and create a username and password
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2033.png)

- When you are in the networking section, make sure that the virtual network and subnet are the same as the first virtual machine, or the lab will not work
- In this case, we don't need a public IP either.
- and create the virtual machine
- 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2034.png)

- After the creation of the virtual machine, just like earlier in the first virtual machine, go to dns server
- Once we are here, input the private static IP address used in the first virtual machine so that everything can connect and work

![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2035.png)

- Also in the networking section, make sure that DNS, LDAP, and RDP are allowed for the second virtual machine
  
# section 11: make sure remote desktop logon is allowed for the second virtual machine
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f0afaa4cf0067b221bffb61e5a7466daf8480905/Screenshot%2044.png)

- Go back to the domain controller account and go to group policy management
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f0afaa4cf0067b221bffb61e5a7466daf8480905/Screenshot%2046.png)

- Once we are here, go to edit for the domain controller
 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f0afaa4cf0067b221bffb61e5a7466daf8480905/Screenshot%2047.png)

- While in edit, go to Allow log on through Remote Desktop Service properties
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e2f9e49db7cddf5d55dbec37813818154d157a24/Screenshot48.png)

- Click Add and input administrator and remote desktop users 
- then click apply so that these rules are in place
- This is so that we can RDP to our second virtual machine that we created in Azure, since it doesn't have a public IP address
  
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e2f9e49db7cddf5d55dbec37813818154d157a24/Screenshot49.png)

- Once the rule is applied, go to the command prompt, run it as an administrator, and run the command gpupadte /force
  
# section 12: make sure everything shows up when pinging 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e2f9e49db7cddf5d55dbec37813818154d157a24/Screenshot50.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/70d416a75363c1bdcb52e1a1b470b6949a5a24e5/Screenshot%2051.png)

# section 13: have the second virtual machine join the domain in the Active Directory
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/70d416a75363c1bdcb52e1a1b470b6949a5a24e5/Screenshot%2052.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/70d416a75363c1bdcb52e1a1b470b6949a5a24e5/Screenshot%2053.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/70d416a75363c1bdcb52e1a1b470b6949a5a24e5/Screenshot%2054.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/04ce0c289e4857e36df2ede1138bc8f329590f74/screenshot%2055.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/04ce0c289e4857e36df2ede1138bc8f329590f74/Screenshot%2056.png)


# section 14: make sure everything works with remote logons 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/04ce0c289e4857e36df2ede1138bc8f329590f74/Screenshot50.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/04ce0c289e4857e36df2ede1138bc8f329590f74/Screenshot%2057.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/82f3bd38b2f755c0853882fe7f881daa405ada73/Screenshot%2058.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e4dc21116a286bb42bc276aa54d6311920333786/Screenshot%2059.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e4dc21116a286bb42bc276aa54d6311920333786/Screenshot%2060.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e4dc21116a286bb42bc276aa54d6311920333786/Screenshot%2061.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e4dc21116a286bb42bc276aa54d6311920333786/Screenshot%2062.png)

