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
Create the Domain Controller virtual machine by opening Oracle VirtualBox and selecting the Windows Server 2019 ISO file   
<br />
<img src="https://i.imgur.com/P7VmjVT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<br />
Continue following the steps: 
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
We will begin by installing Windows Server 2019
<img src="https://i.imgur.com/sVsSE6t.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue following the setup 
<img src="https://i.imgur.com/Y6wEqFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/acgwPwo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3uhfcmk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select Custom: Install Windows Only
<img src="https://i.imgur.com/EUGjO21.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/dUGElMK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/k4ahk2S.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Create a password for the built-in administrator account 
<img src="https://i.imgur.com/LCUWONy.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
There is a menu to select "Ctrl+Alt+Delete" by selecting Input < Keyboard < Insert Ctrl+Alt+Delete
<img src="https://i.imgur.com/czN1GAZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/VjzlZA2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Server Manager will automatically open on startup 
<img src="https://i.imgur.com/xVodMax.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
We will first Insert Guest Additions CD Image for a better viewing experience by selecting Devices < Insert Guest Additions CD Image
<img src="https://i.imgur.com/FmKgIz8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Open File Explorer < This PC < Open CD Drive (D:) VirtualBox Guest Addition
<img src="https://i.imgur.com/3fkNgfd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Select VBoxWindowsAdditions-amd64
<img src="https://i.imgur.com/oy4SI8w.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Continue with the Oracle VM VirtualBox Guest Additions Setup
<img src="https://i.imgur.com/MYmwSpv.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/mhSYttj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XSMtdDM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/QQ686K8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
Once the installation is complete, reboot your computer
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
<img src="https://i.imgur.com/xvvoNFF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3EqnJU3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/W2YtOPt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/DVTbPKM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HzKVrEq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/JTvr3uX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/3S05MtE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/cB4HO4g.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/7c7yVoW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/87FKpGb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/bB7kLOC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/PVAzlO7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/rKPLZzi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/S781mM0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/GPNLVPM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/nFDcp23.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/6538daB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/haWEqMj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/UCiQnTu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/isbut7L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/s7qHnj8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/n8QTJGX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XEmDEXr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/juJRCws.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/faAJcLk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/UKNmos7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/pBoZvcr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/n9djvcN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Aw3ijj8.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Op7bjlw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/sKHnRfE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/2zNUzxD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/mhINaaM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/wGCFKNE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ZGn7kDP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/0AkNnOj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/idr9kJm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HcFPJ3h.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/hXBBDFd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/kGbJqYl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/KQOujDa.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/WgWHOBq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/IBu5S53.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/6qYO2zp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/GjiKVc4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/0HhKh7Y.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/qg6CWtH.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ixI8NUK.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ouPGz5e.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HzMXVsx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/XinKH28.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/AaQbT13.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/QAPKVGZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/IiNaP0K.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/NIb1chl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/AYD1jrl.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/GUeltZT.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/B4VqfqP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/vnvkabm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/lRJznf5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/L76nwrn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/RJfyYVL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/byQmEiX.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/sgFfYrQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/aqv4tNS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/nilPXpV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/wZDppgY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/NtDLSnQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/gMYdpXo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/1hRB9Vd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/udTytis.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/Vme8g8s.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ZoCJLZ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/oXRkBaF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/2yzvmJF.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/pb4SZPI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/zE463Hh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/HllJ9Ck.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/kD1LHgw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/07AmUhQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/GxGGxNi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ZJ29h4L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/S2bmSTc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/I6upEHd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/pd3OqO4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/ownhaN5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/KtfLZBm.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ptPbgFi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/IpmDc74.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/39sARj4.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/NLauz7N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/a4G57IN.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/oWsu5GC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/SYGEm7R.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/8K57XY5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/5R8Mm6L.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/PHHOi07.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/cLjeNGL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/De4DsJD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/djCxn7C.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/7IgmZuB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/4hF8ch9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/vHFtbrV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/La4VAsp.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/I3lDnEL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/qfnB3A1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/WHR8m3x.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/nU17g2l.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/b1EkiPc.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/Kd10DBn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/ypP0rCU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/WACaYBM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/AXtSlii.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/bCatpF3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/mQJHHHJ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/AQftja0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<img src="https://i.imgur.com/kCmhpUd.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/sLRy3Lh.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<img src="https://i.imgur.com/l6vT0cW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
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
