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
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%207.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%208.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%209.png)

# section 3: allow LDAP and DNS
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%2010.png)

# section 4: deploy the Virtual machine in Windows app
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/4dd3cccc2939cbbdbda54f57f1081920873da6fc/Screenshot%2011.png)

# section 5: install Active Directory and create a domain
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2012.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2013.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2014.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2015.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2016.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2017.png)

# section 6: create a domain controller account for the Active Directory 
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2018.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2019.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/98f3e489ebfe4e4fea479fd059828a2f39b98736/Screenshot%2020.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2021.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2022.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2023.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/3a02de0f71466d83ab42e367dd81cb38493541fa/Screenshot%2024.png)
# section 7: log into the domain controller account and install DHCP
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/326d7c6b7d87c7554927698ab15f95fce1965b52/Screenshot%2025.png)

# section 8: set up DHCP scope
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2027.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2026.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2028.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2029.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/eb4c83919bb5378f33a5a421bf43dc99e6339ea9/Screenshot%2030.png)

# section 9: add PowerShell script to automate user account to the domain
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2036.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2037.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2038.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2039.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2040.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2041.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2042.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f77bb2cb2ad00e629e158883cb56a579812f518b/Screenshot%2043.png)

# section 10: create second virtual machine  and set DNS to the first virtual machine's private IP
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2031.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2032.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2033.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2034.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/54b7124897ee19ecb9e74986b8240a512286a7ee/Screenshot%2035.png)

# section 11: make sure remote desktop logon is allowed for the second virtual machine
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f0afaa4cf0067b221bffb61e5a7466daf8480905/Screenshot%2044.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f0afaa4cf0067b221bffb61e5a7466daf8480905/Screenshot%2046.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/f0afaa4cf0067b221bffb61e5a7466daf8480905/Screenshot%2047.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e2f9e49db7cddf5d55dbec37813818154d157a24/Screenshot48.png)
![image alt](https://github.com/jaidenework/active-directory-lab-/blob/e2f9e49db7cddf5d55dbec37813818154d157a24/Screenshot49.png)


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

