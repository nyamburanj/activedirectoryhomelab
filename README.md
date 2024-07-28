This project is based on creating an active directory home lab. An Active Directory is used by majority of organizations to manage resources , users , computers and groups. This project is based on setting it up and using it for having one that can be used for future cybersecurity projects.
<h1>Active Directory Home Lab Project</h1>


<h2>Description</h2>
Active Directory (AD) is a directory service developed by Microsoft that provides a centralized platform for managing network resources such as users, computers, and applications within a Windows domain. It organizes these resources into a hierarchical structure, allowing administrators to control access, apply security policies, and manage permissions efficiently. In cybersecurity, Active Directory is vital because it helps enforce security measures through robust authentication and authorization processes. By centralizing identity management, AD allows for consistent implementation of security policies, monitors access to sensitive resources, and simplifies the process of responding to security incidents. This centralized approach is crucial for maintaining a secure and organized network environment, minimizing the risk of unauthorized access and data breaches. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>Oracle Virtual Box</b> 
- <b>Windows 10 ISO</b>
- <b>Server 2019 ISO</b>
- <b>Kali Linux</b> 
- <b>Windows</b> 

<h2>Program walk-through:</h2>
Given the project was using two avenues of primarily using Kali Linux terminal and Nessus , there was first the need to install Nessus to begin vulnerability scanning there. After that , was using the nmap command on the kali linux terminal to also begin scanning there. By the end of both scanning , two results from the sources were generated.

<p align="center">

  <b>Initial Diagram/Mapout: </b>
  ![image](https://github.com/user-attachments/assets/4e91bff8-ab6f-4a71-8f52-5ecde520cd9a)

This diagram is an illustration of how the Active Directory will be setup. To begin with , the project will use Oracle VirtualBox which is already installed to download two virtual machines: Windows 10 and Server 2019. These will be used separately. Then the server19 will be used as a domain controller and house the Active Directory.

It will have two networkadapters : once used to connect to outside network and other used to connect to the Virtual Box Private Network which clients can connect to. This is where we will install Sever 2019 on it. We will assign Ip address on it for the internal network while for the external network that connects to the internet will automatically get it from out HOme router.

Once installed we will install Active Directory and create our domain and configure a Remote Access Server (RAS) and Network Address Translation (NAT)  and routing so that clients on private network can access internet using domain controlle. Then we will set up a DHCP so that our windows 10 machine can automatically have an IP address. 

Next , we will run a Powershell script that will automatically create 1000 users. We then create another VM for Windows and name the VM Client 1, that will connect to the Virtual Box Private Network. Client 1 will be joined to the Domain and log into it with one of the domain accounts we created.
  
  
  
 



