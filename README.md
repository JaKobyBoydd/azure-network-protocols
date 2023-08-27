# Setting Up A Domain Controller<p align="center">

In this tutorial, we will set up a Domain Controller through azure. <br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Server Manager
- Domain Users and Computers

<h2>Operating Systems Used </h2>

- Windows Server 2019 Datacenter-x64 Gen2 


<h2>High-Level Steps</h2>

- Create a Virtual Machine through azure
- Install Active Directory Domain Services
- Add a new Forest

<h2>Actions and Observations</h2>

<p>
The first step is to create a virtual machine through azure. In order for us to set up a domain controller, the operating system needed is a windows datacenter. Under operations choose, "Windows Datacenter 2019 x62 Gen2". For the size of the vm, choose at least 2 vcpus.
</p>
<p>
<img src="https://i.imgur.com/ods5SDo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Once the VM is created head to the computer's nic to change the domain controller's ip. Head to the settings on the left hand side and select networking. In the network settings go to the network interface, ip configurations, and select ip coonfig1. Lastly change the private ip address allocation from dynamic to static.
</p>
<p>
<img src="https://i.imgur.com/d1o4Db3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
<img src="https://i.imgur.com/hZ9Nxe9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<img src="https://i.imgur.com/W77wTge.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />

<p>
Now head to the VM and in the server manager go to add roles and features in order to install Active Directory Domain Services. After that is installed, go to the exclamation point in the top right corner and promote the server to a domain controller. Add a new forest and create a root domain name. Create a password and continue the installation process. Once active directory domain services is installed you can go to tools in the top left corner and select, Domain Users and Computers.
</p>

