# VM-osticket-installation
<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/f/fa/Microsoft_Azure.svg" alt="Microsoft Azure logo" width="120"/>
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="400"/>


</p>

<h1> Microsoft Azure VM & osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket. Along with the Virtual Machine utilized from Microsoft Azure.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Azure Subscription – so I can create a Windows 10 Virtual Machine.
- Windows 10 VM (4 vCPUs) – created in Azure and accessible with RDP.
- Valid RDP client(Windows App downloaded on MAC) – to log into the VM remotely.
- osTicket-Installation-Files.zip – available for download (containing osTicket, PHP, MySQL, IIS tools, etc.).
- Stable Internet Connection

<h2>Installation Steps</h2>

<p>
  <img src="images/step1-osticket-vm.png" height="80%" width="80%" alt="Step 1 - Azure VM Creation"/>
</p>
<p>
  Step 1: Create VM & Connect → Make an Azure Windows 10 VM → log in via Remote Desktop.
</p>

<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 2: Prepare Files → Install IIS & Dependencies → Enable IIS with CGI → Install PHP Manager, Rewrite Module, VC_redist, and MySQL.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 3: Set Up PHP → Create C:\PHP → unzipped PHP 7.3.8 into it → register php-cgi.exe in IIS → restart IIS.
</p>

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 4: Deploy osTicket → Unzip osTicket v1.15.8 → move “upload” folder into C:\inetpub\wwwroot\ → rename it osTicket → restart IIS.
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 5: Configure osTicket → Enable PHP extensions (imap, intl, opcache) → rename ost-sampleconfig.php to ost-config.php → set permissions
</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Step 6: Database & Final Setup → Install HeidiSQL → create DB osTicket → finish browser setup
</p>
<br />
