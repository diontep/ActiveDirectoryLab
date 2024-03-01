<h1>Active Directory Home Lab</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
In this lab we're going to walk through how to create an Active Directory home lab enviroment using Oracle Virtual Box. Configuring and running this lab will definitely help your understanding of how active directory and windows networking works, so I'd highly recommend running through it a couple times, ask questions where stuff is unclear and eventually try to build it on your own without watching. Please let me know if you have any questions!
<br />


<h2>Languages and Utilities Used</h2>

- <b>Active Directory</b> 
- <b>PowerShell</b> 
- <b>Command Prompt</b>

<h2>Environments Used </h2>

- <b>Oracle VirtualBox</b>

- <b>Windows Server 2019</b>
  
- <b>Windows 10</b> (21H2)

<h2>Program walk-through:</h2>

<p align="center">
Topology <br/>
<img src="https://i.imgur.com/ozAFMKu.jpg" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />


<h2>Download Oracle VirtualBox:<h2>

[Oracle VirtualBox](https://www.virtualbox.org/)

<h2>Download Windows Server 2019:<h2>
 
[Server 2019](https://www.microsoft.com/en-us/evalcenter/evaluate-windows-server-2019) 
 
<h2>Download Windows 10 Disc Image ISO:<h2> 

[Windows 10](https://www.microsoft.com/en-us/software-download/windows10ISO)
<br />
<br />
<img src="https://i.imgur.com/P7VmjVT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/GalWY8v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/Bkcwq6Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/dd7tZkj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/LzujwtV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/V42Up3J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Domain Controller Windows Setup:</h2>
<img src="https://i.imgur.com/aKQRgx3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will begin by installing Windows Server 2019:
<img src="https://i.imgur.com/sVsSE6t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue following the setup:
<img src="https://i.imgur.com/Y6wEqFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/acgwPwo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3uhfcmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select "Custom: Install Windows Only"
<img src="https://i.imgur.com/EUGjO21.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/dUGElMK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/k4ahk2S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Create a password for the built-in administrator account:
<img src="https://i.imgur.com/LCUWONy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
There is a menu to select "Ctrl+Alt+Delete" by selecting Input < Keyboard < Insert Ctrl+Alt+Delete:
<img src="https://i.imgur.com/czN1GAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/VjzlZA2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Server Manager will automatically open on startup: 
<img src="https://i.imgur.com/xVodMax.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will first Insert Guest Additions CD Image for a better viewing experience by selecting Devices < Insert Guest Additions CD Image:
<img src="https://i.imgur.com/FmKgIz8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Open File Explorer < This PC < Open CD Drive (D:) VirtualBox Guest Addition:
<img src="https://i.imgur.com/3fkNgfd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select VBoxWindowsAdditions-amd64:
<img src="https://i.imgur.com/oy4SI8w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue with the Oracle VM VirtualBox Guest Additions Setup:
<img src="https://i.imgur.com/MYmwSpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/mhSYttj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XSMtdDM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/QQ686K8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Once the installation is complete, reboot your computer:
<img src="https://i.imgur.com/Y1wlYTk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Set Up IP Addressing:</h2>
<img src="https://i.imgur.com/ojQf3fa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Click the 🖥️ icon located on the bottom right of your screen Select Network to access your Network Settings 
 Select change adapter options 
<img src="https://i.imgur.com/O0fIi7Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eyaRrMy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Rename Ethernet to _INTERNET_ and Ethernet 2 to X_Internal_X
<img src="https://i.imgur.com/ISXPCwF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Right click each network < Select Status then select Details to view the home IP address of _INTERNET_ and X_Internal_X
<img src="https://i.imgur.com/SKE7fZ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/F4xeqrO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Rename PC:</h2>
Go to the Start Menu < System
<img src="https://i.imgur.com/JuySACq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Rename this PC
<img src="https://i.imgur.com/I4eBApW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will rename this PC to "DC" which stands for Domain Controller
<img src="https://i.imgur.com/tBKfpfJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eibOPCQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Now we will restart 
<img src="https://i.imgur.com/BmkCoId.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/gwIoB8T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Assign IP Address:</h2>
We will Ctrl+Alt+Delete to unlock 
<img src="https://i.imgur.com/qwATla5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Click on Network < Change adapter options
<img src="https://i.imgur.com/G6v9oFt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Right click X_Internal_X < select Properties
<img src="https://i.imgur.com/WzOrDfB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Internet Protocol Version 4
<img src="https://i.imgur.com/3MeKyXj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will assign the IP address to match the internal NIC listed in the topology   
<img src="https://i.imgur.com/WRaHogF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Copy the following
<img src="https://i.imgur.com/Xo52TKs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Install Active Directory Domain Services:</h2>
We are going to now create a domain:
<img src="https://i.imgur.com/xvvoNFF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3EqnJU3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select "Role based or feature-based installation"
<img src="https://i.imgur.com/W2YtOPt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the server that you are going  to install
<img src="https://i.imgur.com/DVTbPKM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Active Directory Domain Services
<img src="https://i.imgur.com/HzKVrEq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Add Features
<img src="https://i.imgur.com/JTvr3uX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select next
<img src="https://i.imgur.com/3S05MtE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/cB4HO4g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue 
<img src="https://i.imgur.com/7c7yVoW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/87FKpGb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Proceed with the installation 
<img src="https://i.imgur.com/bB7kLOC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Once Active Directory Domain Services is installed select Promote this server to a domain controller 
<img src="https://i.imgur.com/PVAzlO7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In the Active Directory Domain Services Configuration Wizard, select add a new forest and enter "mydomain.com"
<img src="https://i.imgur.com/rKPLZzi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Domain Name System (DNS) server and Global Catalog (GC)
<img src="https://i.imgur.com/S781mM0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Enter the Directory Services Restore Mode (DSRM) password 
<img src="https://i.imgur.com/GPNLVPM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Set the NetBIOS domain name as "MYDOMAIN"
<img src="https://i.imgur.com/nFDcp23.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select next
<img src="https://i.imgur.com/6538daB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Proceed with the installation
<img src="https://i.imgur.com/haWEqMj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/UCiQnTu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
Your computer will now be restarted
<img src="https://i.imgur.com/isbut7L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/s7qHnj8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
<img src="https://i.imgur.com/n8QTJGX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Sign in as Administrator 
<img src="https://i.imgur.com/XEmDEXr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the start menu and select Active Directory Users and Computers
<img src="https://i.imgur.com/juJRCws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select and right click mydomain.com 
<img src="https://i.imgur.com/faAJcLk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select New < Organizational Unit
<img src="https://i.imgur.com/UKNmos7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Name Organizational Unit "_ADMINS"
<img src="https://i.imgur.com/pBoZvcr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The _ADMINS folder has now been created. Select and right click the folder. Select User. 
<img src="https://i.imgur.com/n9djvcN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Create a new user by entering in their information 
<img src="https://i.imgur.com/Aw3ijj8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Set a password 
<img src="https://i.imgur.com/Op7bjlw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Your new user has now been created 
<img src="https://i.imgur.com/sKHnRfE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/2zNUzxD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select and right click the user then select properites
<img src="https://i.imgur.com/mhINaaM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/wGCFKNE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the Member Of tab then select Add
<img src="https://i.imgur.com/ZGn7kDP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Add the user to Domain Admins
<img src="https://i.imgur.com/0AkNnOj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The user is now a member of Domain Admins
<img src="https://i.imgur.com/idr9kJm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Sign out
<img src="https://i.imgur.com/HcFPJ3h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select other user and enter the credentials of the user you just created 
<img src="https://i.imgur.com/hXBBDFd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/kGbJqYl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
You are now signed in
<img src="https://i.imgur.com/KQOujDa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
On Server Manager select Add roles and features 
<img src="https://i.imgur.com/WgWHOBq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select next
<img src="https://i.imgur.com/IBu5S53.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Role based or feature-based installation 
<img src="https://i.imgur.com/6qYO2zp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the DC server
<img src="https://i.imgur.com/GjiKVc4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Remote Access 
<img src="https://i.imgur.com/0HhKh7Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Group Policy Management
<img src="https://i.imgur.com/qg6CWtH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select DirectAccess and VPN and select Routing
<img src="https://i.imgur.com/ixI8NUK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the following:
<img src="https://i.imgur.com/ouPGz5e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Proceed with the installation 
<img src="https://i.imgur.com/HzMXVsx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select close
<img src="https://i.imgur.com/XinKH28.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Tools then select Routing and Remote Access
<img src="https://i.imgur.com/AaQbT13.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Rigt click DC (local) then select Configure and Enable Routing and Remote Access
<img src="https://i.imgur.com/QAPKVGZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/NIb1chl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Proceed with the Server Setup Wizard
<img src="https://i.imgur.com/AYD1jrl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Network address translation (NAT)
<img src="https://i.imgur.com/GUeltZT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Use this public interface to connect to the Internet (Select _INTERNET_)
<img src="https://i.imgur.com/B4VqfqP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Complete the Server Setup Wizard 
<img src="https://i.imgur.com/lRJznf5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/L76nwrn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Remote Access Server and Network Address Translation are now configured 
<img src="https://i.imgur.com/RJfyYVL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>DHCP Server on Domain Controller:</h2>
We are going to allow our Windows 10 clients to get an IP address that will allow them to browse the internet
by selecting "Add roles and features"
<img src="https://i.imgur.com/byQmEiX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select role based or feature based installation 
<img src="https://i.imgur.com/sgFfYrQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the server now named "DC.mydomain.com"
<img src="https://i.imgur.com/aqv4tNS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select DHCP Server
<img src="https://i.imgur.com/wZDppgY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue Installation 
<img src="https://i.imgur.com/nilPXpV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
Select next
<img src="https://i.imgur.com/NtDLSnQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Install
<img src="https://i.imgur.com/gMYdpXo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Wait for installation 
<img src="https://i.imgur.com/1hRB9Vd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Once installation is complete select tools < DHCP
<img src="https://i.imgur.com/udTytis.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We can now set up our scope
<img src="https://i.imgur.com/Vme8g8s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
DHCP's allow computers on the network to automatically receive their IP addresses
<img src="https://i.imgur.com/ZoCJLZ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We are going to create a scope that will give IP addresses in range 172.16.0.100 by right clicking IPv4 and selecting new scope
<img src="https://i.imgur.com/oXRkBaF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will name the scope the IP range "172.16.0.100-200" and select next
<img src="https://i.imgur.com/2yzvmJF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The start IP address will be "172.16.0.100" end IP address will be "172.16.0.200"
length is 24 and the subnet mask by default is "255.255.255.0"
<img src="https://i.imgur.com/pb4SZPI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We skip exclusions
<img src="https://i.imgur.com/zE463Hh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Lease duration is how long you can have an IP address before it needs to be refreshed so we will select 8 days
<img src="https://i.imgur.com/HllJ9Ck.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will select yes for configuring DHCP options meaning we will want to tell clients which server to use for DNS and the gateway
<img src="https://i.imgur.com/kD1LHgw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Referring to the network diagram we are going to use the IP address of the domain controller that has NAT configured on it"172.16.0.100"
<img src="https://i.imgur.com/07AmUhQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select add
<img src="https://i.imgur.com/GxGGxNi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will use the domain controller as our DNS server to join the domain
<img src="https://i.imgur.com/ZJ29h4L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/S2bmSTc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Skip WINS server
<img src="https://i.imgur.com/I6upEHd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select "yes" to activate the scope
<img src="https://i.imgur.com/pd3OqO4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Finish installation
<img src="https://i.imgur.com/ownhaN5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Right click "dc.mydomain.com" and select authorize and then right click once more and select refresh 
<img src="https://i.imgur.com/KtfLZBm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We can see our IPV4 turned green as well as our scope 
<img src="https://i.imgur.com/ptPbgFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We are going to make a configuration that allows us to browse the internet from the domain controller 
<img src="https://i.imgur.com/IpmDc74.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We are going to configure this local server
<img src="https://i.imgur.com/39sARj4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Since we have to make a configuration that lets us browse the Internet from the domain controller.
we do this by disabling IE Enchanted Security Configuration 
<img src="https://i.imgur.com/NLauz7N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We are going to copy and paste the link to the source code powershell script that allows us to create users by opening internet explorer
<img src="https://i.imgur.com/a4G57IN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Paste the link and click enter
<img src="https://i.imgur.com/oWsu5GC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
The link will now download. After the download is complete we click "Save as" to the desktop 
<img src="https://i.imgur.com/SYGEm7R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will extract this script from the desktop 
<img src="https://i.imgur.com/8K57XY5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
When we open this folder we will see a PowerShell script file and a plaintext file called names
<img src="https://i.imgur.com/5R8Mm6L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In this file contains a thousand randomized names
<img src="https://i.imgur.com/PHHOi07.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
At the very top of the list add your name. We are going to use this file to programmatically create all of these users
<img src="https://i.imgur.com/cLjeNGL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will save and close the file then run Windows Powershell Ise as administrator (Start < Windows PowerShell Ise < More < Run as administrator)
<img src="https://i.imgur.com/De4DsJD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br /> 
Select Yes
<img src="https://i.imgur.com/djCxn7C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Source Code for the Powershell Script:</h2>
<img src="https://i.imgur.com/7IgmZuB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select File < Open 
<img src="https://i.imgur.com/4hF8ch9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select This PC
<img src="https://i.imgur.com/vHFtbrV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Open the AD_PS-master folder
<img src="https://i.imgur.com/La4VAsp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the 1_CREATE_USERS Powershell Script to open
<img src="https://i.imgur.com/I3lDnEL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We have now opened the Powershell script
<img src="https://i.imgur.com/qfnB3A1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Before we do anything we are going to enabke the execution of all scripts on this server. Type "Set-ExecutionPolicy Unrestricted" then select enter
<img src="https://i.imgur.com/WHR8m3x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Yes to All
<img src="https://i.imgur.com/nU17g2l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
To pull and create the thousands of users we are going to enter code by typing in "cd C:\Users\userofyourchoice\Desktop\AD_PS-master" then select enter
<img src="https://i.imgur.com/Kd10DBn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Type in ls. We will see that the "names.txt" is listed. "names.txt" is the code that creates the thousands on users mentioned earlier
<img src="https://i.imgur.com/ypP0rCU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Towards the top of your screen click green arrow icon to "Play" then select "Run once"
<img src="https://i.imgur.com/WACaYBM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
This will import the active directory module and start creating the users
<img src="https://i.imgur.com/AXtSlii.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/bCatpF3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In the meantime open active directory users and computers < right click mydomain.com < select refresh < you will see the _USERS folders that the script created
<img src="https://i.imgur.com/mQJHHHJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
If we right click mydomain.com and select "find" you will see a window that you can use to search specific users
<img src="https://i.imgur.com/AQftja0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
You are able to search yourself once the script has finished running.
<img src="https://i.imgur.com/kCmhpUd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Now that all of our users are created and our environment is now set up we can refer to our network diagram.
<img src="https://imgur.com/maxxUwb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
The only thing we need to set up is our Windows 10 virtual machine in VirtualBox
<img src="https://imgur.com/SwWrfmf.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<h2>Creating Windows 10 Virtual Machine:</h2>
<br />
We are going to name this machine "CLIENT1" and use Windows 10 64-bit version
<img src="https://i.imgur.com/IFF4ybI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Set the RAM to atleast 2GB and CPU to atleast 4
<img src="https://i.imgur.com/XwLYjYA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Create a hard disk now and select next
<img src="https://i.imgur.com/ChuvW7V.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Before we turn on the client virtual machine right click and go to settings then go to advanced and turn on the clipboard to allow copy and paste 
<img src="https://i.imgur.com/sZ2p9fg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
On the network tab and select internal network as the virtual machine configuration in order to get a DHCP address from the domain controller 
<img src="https://i.imgur.com/sSmBWFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
When powering on the virtual machine locate where the Windows 10 ISO was downloaded in File Explorer and select it then click "Mount"
<img src="https://i.imgur.com/agvAk37.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<h2>Windows 10 Installation:</h2>
Proceed with installation 
<img src="https://i.imgur.com/qNvBcSF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/5jmZMYT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/wCPTWX9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select "I don't have product key"
<img src="https://i.imgur.com/kukTlF7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Choose Windows 10 Pro
<img src="https://i.imgur.com/EJbYWHM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Accept the license terms and select next
<img src="https://i.imgur.com/GSQidS6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select the drive and continue 
<img src="https://i.imgur.com/itkVFKI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3XIYn2D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select your region
<img src="https://i.imgur.com/Zx3h3rh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Connect to your network
<img src="https://i.imgur.com/BazFQ4Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue with limited setup
<img src="https://i.imgur.com/ysET2SS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
When asked "Who's going to use this PC?" enter in "user" for the name
<img src="https://i.imgur.com/oZH4ZwC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/90uVUxN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select next and skip entering in a password 
<img src="https://i.imgur.com/rV29636.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select accept
<img src="https://i.imgur.com/Nk1AbYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue
<img src="https://i.imgur.com/1mOVdxN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/RJ46O3N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/RS2xd1m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/BmTEmPa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/hwKrKkD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We are going to make sure the internet is working by clicking start < command prompt
<img src="https://i.imgur.com/y3c0BTw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
In the command line we are going to type "ipconfig /all" 
<img src="https://i.imgur.com/jj7fRD4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Since the default gateway isn't showing we are going to type "ipconfig" the default gateway is 172.16.0.1
<img src="https://i.imgur.com/1NEORSk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will now renew the ip configuration by entering in ipconfig /renew
<img src="https://i.imgur.com/17Ubxif.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/0sCAJ9Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/MQFGdvr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Incase you do not see the default gateway we are going to open the domain controller (DC) virtual machine 
<img src="
<br />
<img src="https://i.imgur.com/UNyxxL5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/6KZes77.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/jx3psHr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/TT5DuI7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/meyPBas.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/27yOXrI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/0UqXLRt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/FjakocH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/9lbIwXB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/uTHHomV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/eMCsQjL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/Ef9pg0k.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/aI1wDEv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/nvWQLp6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/fAI2gvm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/2yZhhBk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/kIB5RzQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/tcmh1oq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/8xSJP0s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/3oXYB5F.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/BazFQ4Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ysET2SS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/oZH4ZwC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/t7VxUjj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/90uVUxN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/rV29636.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Nk1AbYx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/sLRy3Lh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1mOVdxN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/RJ46O3N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/RS2xd1m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/BmTEmPa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hwKrKkD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/y3c0BTw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/jj7fRD4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/1NEORSk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/17Ubxif.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/0sCAJ9Z.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/MQFGdvr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/KnLIccI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/AUqfAaO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/eKok5cL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/9ZYPgTx.png  height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/CTUrZ2d.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/5ZuTjyB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/fxqUrSa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/QrAyJ7C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/lneneJp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/FQ7VX09.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/7YchlAy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/P1LSew5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/6VMWOvn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ozqT5pt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/SRLKu49.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/n82HMBT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
 

<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />











<br /><p align="center"><!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
