<p align="center">
<img src="https://static.wixstatic.com/shapes/2ebf04_6ddec2f2c2eb4cd4ada9cef3f6ace924.svg" alt="osTicket Logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial provides an overview of the necessary prerequisites and installation procedures for deploying osTicket, an open-source platform for managing and resolving help desk support tickets.<br />


</p>

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop Connection
- Internet Information Services (IIS)

<h2>Operating System Used </h2>

- Windows 10</b> (22H2)

<h2>List of Prerequisites</h2>

- Enable Internet Information Services (IIS) and CGI.
- Install PHP Manager for IIS.
- Install URL Rewrite Module.
- Extract PHP into a new folder on Local Disk (C:) and register it in IIS.
- Install Microsoft Visual C++ Redistributable.
- Install MySQL and set up a password for root.
- Extract osTicket into the wwwroot folder.
- Enable php_imap.dll, php_opcache.dll, and php_intl.dll in IIS.
- Install HeidiSQL and create a new database.

<h2>Installation Steps</h2>

<p>
<p align="center"> 
<img width="1121" alt="Step 1  " src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/07d03ddf-db2b-4489-a5b4-68687f15b235">

</p>
<p>
Step 1: Create a resource group in Azure and name it "RG-LabOsTicket."
</p>
<br />

<p>
<p align="center"> 
<img width="1118" alt="Step 2" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/4ab6de21-6e90-46ff-8720-e69670c2255a">

</p>
<p>
Step 2: Create a virtual machine and select "RG-osTicket" as the resource group and "Windows 10 Pro, Version 22H2" as the image.
</p>
<br />

<p>
<p align="center"> 
<img width="1110" alt="Step 3" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/65e73d6b-4b63-4a5a-9206-033c4d95cc2c">

</p>
<p>
Step 3: Use the Remote Desktop Connection to connect to the virtual machine (VM) using its public IP address.
</p>
<br />

<p>
<p align="center"> 
<img width="530" alt="Step 4" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/a2b7bfcf-2cb7-416b-b835-595d5061c4c9">

</p>
<p>
Step 4: Navigate to "Turn Windows Features on or off" in the Control Panel menu.
</p>
<br />

<p>
<p align="center"> 
<img width="539" alt="Step 5 Pt 1" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/111938b0-55fc-4fd7-83c4-90f0502cb408">

</p>
<p align="center"> 
<img width="535" alt="Step 5 Pt 2" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/1750b74a-37bf-43da-8313-0a749ace69c7">

</p>
<p>
Step 5: Enable Internet Information Services (IIS) and CGI.
</p>
<br />

<p>
<p align="center"> 
<img width="548" alt="Step 6 Pt 1" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/9618c933-7e56-4d0d-95f2-306fd1e8753d">

</p>
<p align="center"> 
<img width="424" alt="Step 6 Pt  2" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/72eeb837-1491-4dc4-81c8-6165129ab752">

</p>
<p>
Step 6: Download and install <a href="https://iis.net/downloads/community/2018/05/php-manager-150-for-iis-10">PHP Manager For IIS</a>. 
</p>
<br />

<p>
<p align="center"> 
<img width="328" alt="Step 7" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/5fc4d7f3-05c2-468a-b5fd-06f58c74a529">
<p align="center"> 
<img width="411" alt="Step 7 Pt  2" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/8d009350-c35f-4ad6-b2e2-9c1a95250c49">
</p>
<p>
Step 7: Download and install <a href="https://iis.net/downloads/microsoft/url-rewrite">URL Rewrite Module</a>.
</p>
<br />
<p>
<p align="center"> 
<img width="452" alt="Step 8" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/bb96c89c-b271-4569-8066-9832a566e551">
</p>
<p>
Step 8: Navigate to Local Disk (C:) and create a new folder named "PHP."
</p>
<br />
<p>
<p align="center"> 
<img width="551" alt="Step 9 GitHub" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/b5fcadff-191b-441d-9f41-5a1cc141e575">
</p>
<p>
Step 9: Download <a href="https://windows.php.net/download">PHP:</a> Hypertext Preprocessor. 
</p>
<br />

<p>
<p align="center"> 
<img width="432" alt="Step 9" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/9a37ee57-4883-459d-99f2-8bcb37d938a2">
</p>
<p>
Step 10: Unzip the downloaded PHP file into the "PHP" folder on Local Disk (C:).
</p>
<br />
<p>
<p align="center"> 
<img width="361" alt="Step 10" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/2dc5e73c-02da-46e3-819a-4456e1039b73">
</p>
<p align="center"> 
</p>
<p>
Step 11: Download and install <a href="https://learn.microsoft.com/en-US/cpp/windows/latest-supported-vc-redist?view=msvc-170">Microsoft Visual C + + Redistributable</a>.
</p>
<br />
<p>
<p align="center"> 
<img width="383" alt="Step 11" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/74231a0b-aba8-4b9e-ae71-99415f58d515">
</p>
<p align="center"> 
<img width="371" alt="Step 11 Pt 2" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/6f83ec8e-fb19-42d5-90f8-d4c7587efb95">
</p>
<p>
Step 12: Download and install <a href="https://downloads.mysql.com/archives/community">MySQL</a>.
</p>
<br />

<p>
<p align="center"> 
<img width="371" alt="Step 12" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/e38b2127-21de-427d-bad8-911470d37b88">
</p>
<p>
Step 13: Launch the MySQL Instance Configuration Wizard, select "standard configuration", install as Windows Service, set a password under "Modify Security Settings", and click "Execute."
</p>
<br />

<p>
<p align="center"> 
<img width="550" alt="Launch IIS as Admin" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/e309287b-9558-4980-936c-7b5f1060932e">

</p>
<p>
Step 14: Launch Internet Information Services as an administrator and navigate to the PHP Manager.
</p>
<br />

<p>
<p align="center"> 
<img width="481" alt="Step 13" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/3f42a0a1-db2b-48af-97a6-e7a902ec2ac6">
</p>
<p align="center"> 
<img width="488" alt="Step 13 Pt 2" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/f2227ad8-2853-43da-b227-53320ad5163b">
</p>
<p align="center"> 
<p>
<img width="485" alt="Step 13 Pt  3" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/9f0f3cd7-dac6-4d81-af14-4ebfecca99d1">

Step 15: Click on "Register new PHP version" and locate the "php-cgi" file in the PHP folder that was created in the Local Disk (C:).
</p>
<br />

<p>
<p align="center"> 
<img width="552" alt="Step 14 Dwnld OsTicket" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/539e9e1f-edf7-4796-be1c-5d15ba1c5b19">
</p>
<p>
Step 16: Download and extract the latest version of <a href="https://osticket.com/download">osTicket</a>.
</p>
<br />

<p>
<p align="center"> 
</p>
<p>
<img width="555" alt="Step 15" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/1128503b-3aec-4c2a-9b2a-18faf5591aad">
Step 17: Open the "osTicket" folder and move the "upload folder" to the "wwwroot" folder in the "inetpub" folder of the Local Disk (C:).
</p>
<br />

<p>
<p align="center"> 
<img width="455" alt="Step 19" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/d649639c-bcb4-4699-b9c5-3e67fb7a4fb8">
</p>
<p>
Step 18: Rename the "upload" folder to "osTicket."
</p>
<br />

<p>
<p align="center"> 
<img width="545" alt="Step 17" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/57c221f3-2a62-4533-af4a-fc896e6b59e2">
</p>
<p>
Step 19: Return to the PHP Manager and select "Enable or disable an extension."
</p>
<br />

<p>
<p align="center"> 
<img width="647" alt="Step 18" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/883249dd-c417-44a6-ae23-ccbdd299d68e">
</p>
<p>
Step 20: Enable the following extensions in the PHP Manager:
- php_imap.dll
- php_opcache.dll
- php_intl.dll
</p>
<br />

<p>
<p align="center"> 
<img width="455" alt="Step 19" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/b7dd8516-1c34-4648-80c6-7d067b86a9f2">
</p>
<p>
Step 21: Navigate to the osTicket folder located in the wwwroot directory, open the "include" folder, and rename the file "ost-sampleconfig.php" to "ost-config.php."
</p>
<br />

<p>
<p align="center"> 
<img width="551" alt="Step 20" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/d253590a-f81d-46e6-a7f6-6712fe40422a">
</p>
<p>
Step 22: Open the Properties of ost-config.php by right-clicking on it. Then, go to the Security tab and click on Advanced. Finally, click on "Disable Inheritance."
</p>
<br />

<p>
<p align="center"> 
<img width="293" alt="Step 21" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/d5c15322-737e-4d6f-b327-3e80c671d58b">
</p>
<p>
Step 23: Click on "add", select "principle", type "everyone" and allow all basic permissions.
</p>
<br />

<p>
<p align="center"> 
<img width="748" alt="Step 22" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/9b9e2aff-5da8-4459-b770-78b03392bf52">
</p>
<p>
Step 24: Launch Microsoft Edge and navigate to https://localhost/osTicket/setup. Then, click on the "Continue" button located at the bottom of the page.
</p>
<br />

<p>
<p align="center"> 
<img width="939" alt="Step 23" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/354eda9f-a26b-4d4a-935f-b8979081f1ab">
</p>
<p>
Step 25: Complete all the required fields for the "System" and "Admin User" settings.
</p>
<br />

<p>
<p align="center"> 
<img width="451" alt="Step 24" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/381fbb4c-94c6-47b2-b748-d80d55836704">
</p>
<p>
Step 26: Download and install <a href="https://www.heidisql.com/installers/HeidiSQL_12.3.0.6589_Setup.exe">HeidiSQL</a>.
</p>
<br />

<p>
<p align="center"> 
<img width="506" alt="Step 25" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/d2a484fc-311a-462e-85de-62546d18be3c">
</p>
<p>
Step 27: Launch HeidiSQL, then click on "New" and enter the password for the root account that was set up earlier. Finally, click on "Open" to proceed.
</p>
<br />

<p>
<p align="center"> 
<img width="512" alt="Step 26" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/52c1c57e-96e3-4bf6-b4ee-1c44d58ea45e">
</p>
<p>
Step 28: Create a new database in HeidiSQL by right-clicking and selecting "Create new", then entering "OsTicket" as the name.
</p>
<br />

<p>
<p align="center"> 
<img width="495" alt="Step 27" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/1911c083-1d17-4de8-b4c4-22f795ad8e5e">
</p>
<p>
Step 29: Return to the osTicket setup page in Microsoft Edge and complete the remaining fields in the "Database Settings" section. After filling in all the required information, click on the "Install now" button.
</p>
<br />

<p>
<p align="center"> 
<img width="546" alt="Step 28" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/db242a83-3a02-45e5-a949-62e5734e5ce8">
</p>
<p>
Step 30: Navigate back to the "wwwroot" folder and locate the "osTicket" folder. Delete the "setup" folder.
</p>
<br />

<p>
<p align="center"> 
<img width="680" alt="Step 29" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/a311c683-7be6-4789-a0ca-e8241098d3f1">
</p>
<p>
Step 31: Access the include folder in osTicket, then navigate to ost-config.php. Right-click on ost-config.php, select Properties, then Security, Advanced, and modify the basic permissions by removing Full Control, Modify, and Write.
</p>
<br />

<p>
<p align="center"> 
<img width="791" alt="Step 30" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/aa2d2e81-895a-4fdb-b22f-d322f85aad2d">
</p>
<p>
Step 32: Log in to https://localhost/osTicket/scp/login.php.
</p>
<br />

<p>
<p align="center"> 
<img width="797" alt="Step 31" src="https://github.com/MalikS-Github/osticket-prereqs/assets/173410266/e054b708-7368-4d7b-b916-4588fe8df676">
</p>
<p>
Step 33: If everything was installed correctly, we should see this page.
</p>
<br />
