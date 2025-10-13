# VM-osticket-installation
<p align="center">
<img src="https://upload.wikimedia.org/wikipedia/commons/f/fa/Microsoft_Azure.svg" alt="Microsoft Azure logo" width="120"/>
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo" width="400"/>


</p>

<h1> Microsoft Azure VM & osTicket - Prerequisites and Installation</h1>
This project demonstrates the deployment of the open-source help desk ticketing system, osTicket, on a Microsoft Azure Virtual Machine. It highlights key IT concepts including cloud infrastructure provisioning, system configuration, and application installation in a virtualized environment.<br />


<h2>My Personal Video Demonstration</h2>

<p align="center">
  
[![Watch the video](https://img.youtube.com/vi/Z08HAyrbrcY/0.jpg)](https://www.youtube.com/watch?v=Z08HAyrbrcY)

</p>



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
  Step 1: Created VM & Connect → Made an Azure Windows 10 VM → Logged in via Remote Desktop.
</p>

<br />

<p>
  <img src="images/step2-prepare-files.png" height="80%" width="80%" alt="Step 2 - Prepare Files"/>
</p>
<p>
  Step 2: Prepared Files → Installed IIS & Dependencies → Enabled IIS with CGI → Installed PHP Manager, Rewrite Module, VC_redist, and MySQL.
</p>

<br />

<p>
<img src="images/step3-setup-php.png" height="80%" width="80%" alt="Step 3 - Setup PHP"/>
</p>
<p>
Step 3: Set Up PHP → Created <code>C:\PHP</code> → Unzipped PHP 7.3.8 into it → Registered <code>php-cgi.exe</code> in IIS → Restarted IIS.
</p>


<p>
<img src="images/step4-deploy-osticket.png" height="80%" width="80%" alt="Step 4: Deploy osTicket"/>
</p>
<p>
Step 4: Deployed osTicket → Unzipped osTicket v1.15.8 → Moved “upload” folder into C:\inetpub\wwwroot\ → Renamed it osTicket → Restarted IIS.
</p>

<br />

<p>
<img src="images/step5-config-osticket.png" height="80%" width="80%" alt="Step 5: Configure osTicket"/>
</p>
<p>
Step 5: Configured osTicket → Enabled PHP extensions (imap, intl, opcache) → Renamed ost-sampleconfig.php to ost-config.php → Set permissions
</p>
<br />

<br />

<p>
<img src="images/step6-database-final-setup.png" height="80%" width="80%" alt="Step 6: Database & Final Setup"/>
</p>
<p>
Step 6: Database & Final Setup → Installed HeidiSQL → Created DB osTicket → Finished browser setup
</p>
<br />

<br />
