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
Create the Domain Controller virtual machine by opening Oracle VirtualBox and selecting the Windows Server 2019 ISO file   <br/>
<img src="https://i.imgur.com/P7VmjVT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Continue following the steps: <br/>
<img src="https://i.imgur.com/GalWY8v.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br/>
<img src="https://i.imgur.com/Bkcwq6Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br/>
<img src="https://i.imgur.com/dd7tZkj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Once the Domain Controller is created, go into the settings of the virtual machine:  <br/>
<img src="https://i.imgur.com/LzujwtV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Configure the network adapters:  <br/>
<img src="https://i.imgur.com/V42Up3J.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<h2>Domain Controller Windows Setup:</h2>
<img src="https://i.imgur.com/aKQRgx3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/sVsSE6t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Y6wEqFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/acgwPwo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3uhfcmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/EUGjO21.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/dUGElMK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/k4ahk2S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/LCUWONy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/czN1GAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/VjzlZA2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/xVodMax.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/FmKgIz8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3fkNgfd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/oy4SI8w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/MYmwSpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/mhSYttj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XSMtdDM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/QQ686K8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Y1wlYTk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ojQf3fa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/O0fIi7Q.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eyaRrMy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ISXPCwF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/SKE7fZ3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/F4xeqrO.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/JuySACq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/I4eBApW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/tBKfpfJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/eibOPCQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/BmkCoId.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/gwIoB8T.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/qwATla5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/G6v9oFt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/WzOrDfB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3MeKyXj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/WRaHogF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Xo52TKs.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
