 <p align="center">
 <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
 </p>
 
 <h1>osTicket - Prerequisites and Installation</h1>
 This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system, osTicket.<br />
 
 <h2>Environments and Technologies Used</h2>
 
  - Microsoft Azure (Virtual Machines)
  - Remote Desktop
  - Internet Information Services (IIS)
  - osTicket
 
 <h2>Operating Systems Used </h2>
 
 - Windows 10</b> (21H2)
 
 <h2>List of Prerequisites</h2>
 
 ### [Collection of Prerequisite Downloads](https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD)
 
 - Internet Information Services (IIS)
 - PHP Manager
 - URL Rewrite Module
 - Visual Studio Redistributable
 - MySQL
 - osTicket
 - HeidiSQL
 
 <h2>Installation Steps</h2>

 <h3>Step 1: Enable IIS</h3>
  
 - To enable IIS, open the start menu and go to the Control Panel.
 - In the Control Panel, under Programs, click “Uninstall a program”. This will open the Programs and Features menu.
   > <img src="https://github.com/user-attachments/assets/4ad0f34e-d942-42d0-b5b4-a72368d9033f" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - Once inside Programs and Features, select “Turn Windows feature on or off” on the left side of the window.
 - In the Windows Features directory, locate Internet Information Services and enable it by checking the box next to it.
   > <img src="https://github.com/user-attachments/assets/78277d87-3101-4d93-926b-65fd6894725d" height="30%" width="30%" alt="Disk Sanitization Steps"/>
 - After checking that box, navigate to CGI by taking the following path: 
   > Internet information Services > World Wide Web Services > Application Development Features > CGI 
 - Check the box next to CGI, then click OK to save the changes.
 - When the installation finishes click Close.

 <br />

 <h3>Step 2: Install PHP Manager</h3>
  
 - Find and Run the PHP Manager installation file.
 - In the installation wizard, click Next.
 - Read the License Agreement and select “I Agree” then click Next.
 - If the UAC shows up, click Yes.
 - Click Close when the installation finishes.
   > <img src="https://github.com/user-attachments/assets/47ad74b4-7629-444f-a40c-8154759ed4a2" height="40%" width="40%" alt="Disk Sanitization Steps"/>

 <br />

 <h3>Step 3: Install URL Rewrite Module</h3>
  
 - Find and Run the URL Rewrite Module installation file.
 - In the installation wizard, read the License Agreement and select “I accept the terms in the License Agreement” then click Install.
   > <img src="https://github.com/user-attachments/assets/361d14cc-db74-42b6-9b0f-b7aca312aadf" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - If the UAC shows up, click Yes.
 - Click Finish when the installation is done.

 <br />

 <h3>Step 4: Create PHP Directory</h3>
  
 - Find the PHP directory .zip file.
 - Open File Explorer and navigate to the C:\ drive.
 - Create a folder in the C:\ drive named “PHP”.
   > <img src="https://github.com/user-attachments/assets/599db2f8-6409-4892-97f1-b32f462370cc" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - From the PHP directory .zip file, extract the contents into the PHP folder that was just made in the C:\ drive.

 <br />

 <h3>Step 5: Install Visual Studios Redistributable</h3>
  
 - Find and Run the Visual Studios Redistributable installation file.
 - In the installation wizard, read the License Agreement and select “I agree to the license terms and conditions” then click Install.
   > <img src="https://github.com/user-attachments/assets/bd105adb-02d5-4ddc-b118-28ff4b171158" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - If the UAC shows up, click Yes.
 - Click Close when the installation finishes.

 <br />

 <h3>Step 6: Install MySQL</h3>
  
 - Find and Run the MySQL installation file.
 - In the installation wizard, click Next.
   > <img src="https://github.com/user-attachments/assets/5ba89953-1789-412f-be92-5572afcb4c00" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - Read the License Agreement and select “I accept the terms in the License Agreement” then click Next
 - Click Typical when choosing a setup type.
 - Click Install
 - If the UAC shows up, click Yes.
 - Before clicking Finish, make sure the “Launch the MySQL Instance Configuration Wizard” box is marked.
 - If the UAC shows up, click Yes.
 - In the MySQL Server Instance Configuration Wizard, click Next.
   > <img src="https://github.com/user-attachments/assets/91bc96a9-95e1-4723-911f-a9a0642ab206" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - When choosing a configuration type, select Standard Configuration then click Next.
 - Leave the Windows Options alone and click Next.
 - In Security Options, make sure Modify Security Settings is selected and input the password you want for your root server account. Make sure you write this down so you don’t forget it. The username will be “root”.
   > <img src="https://github.com/user-attachments/assets/a55b1740-c638-4e39-8997-b4d450698d79" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - Once you’ve chosen your password, click Next.
 - Click Execute on the Ready to execute screen.
 - Click Finish when the installation is done.

 <br />

 <h3>Step 7: Register PHP in IIS</h3>
  
 - Open the Start menu and search “IIS”, then Run IIS as an Administrator.
 - If the UAC shows up, click Yes.
 - In the IIS Manager, locate and open PHP Manager in the middle panel.
   > <img src="https://github.com/user-attachments/assets/78a9ffe6-f069-4635-a53d-a8233f5c32bd" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - Under PHP Setup, click “Register new PHP version”.
 - In the Register new PHP version pop-up, navigate to and open the PHP directory on the C:\ drive.
 - Select the php-cgi executable, then click OK.
 - Navigate back to the home page of the IIS Manager.
 - Click on Restart in the Manage Server panel on the right side of the window.

 <br />

 <h3>Step 8: Install osTicket</h3>
  
 - Find the osTicket .zip file
 - Extract the osTicket .zip file to a location that you can find easily
 - Open File Explorer and navigate to C:\inetpub\wwwroot
 - Copy the upload folder from the osTicket .zip file to the wwwroot folder.
 - In the wwwroot folder, rename upload to “osTicket”.
   > <img src="https://github.com/user-attachments/assets/90c59848-ad33-4bcd-a7f0-0056efb27fed" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - Navigate back to the IIS Manager as an Administrator and restart the server again.

 <br />

 <h3>Step 9: Setup osTicket</h3>
  
 - In IIS Manager, Navigate to osTicket Server page by following this path in the Connections panel on the left: 
   > <system_name> > Sites > Default Web Site > osTicket
 - Click on osTicket in the tree.
 - From the osTicket Home in IIS Manager, locate and open PHP Manager.
 - Under PHP Extensions, click on “Enable or disable an extension”.
   > <img src="https://github.com/user-attachments/assets/6aa506d4-2a65-41f6-bc0d-16a24f36b8af" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - From the list of extensions, right click on and enable “php_imap.dll”, “php_intl.dll”, and “php_opcache.dll”.
 - In File Explorer, navigate to C:\inetpub\wwwroot\osTicket\include.
 - Find the file “ost-sampleconfig.php” and rename it to “ost-config.php”.
   > <img src="https://github.com/user-attachments/assets/8d3956f8-6a4a-4284-af49-45430bbebe24" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - Right click on ost-config.php and select properties.
 - In the Properties window, go to the security tab and click Advanced.
 - In Advanced Security Settings, click the “Disable inheritance” button and select “Remove all inherited permission from this object”.
 - Next, click Add. In the pop-up window click “Select a principal” and add the Users that will manage the Server and click OK.
 - Check “Full control” and click OK.
 - Back on the Advanced Security Settings window, click Apply then OK.
 - Then click OK on the Properties window.
 - From the osTicket Home in IIS Manager, select “Browse” in the Actions panel on the right.
   > <img src="https://github.com/user-attachments/assets/4dc4455d-aa8c-45c4-a581-55ec39a87fb6" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - On the osTicket web page, click Continue at the bottom.
 - Fill in the requested credentials until you reach the Database Settings. Make sure the System Default Email and Admin Email are different.

 <br />

 <h3>Step 10: Install HeidiSQL</h3>
  
 - Find and Run the HeidiSQL installation file
 - If the UAC shows up, click Yes.
 - In the installation wizard, read the License Agreement and select “I accept the agreement” then click Next.
   > <img src="https://github.com/user-attachments/assets/2ab9bd9d-7127-41a2-9d26-4d32e2e112f2" height="40%" width="40%" alt="Disk Sanitization Steps"/>
 - Click Next on Select Destination Location.
 - Click Next on Select Start Menu Folder.
 - Make sure all the boxes are checked for Select Additional Tasks and click Next.
 - Click Install.
 - When the installation finishes make sure the “Launch HeidiSQL” check box is marked and click Finish.
 - Click Skip when the HeidiSQL update notice pops up.
 - In the bottom left corner of the HeidiSQL Session Manager window click New
   > <img src="https://github.com/user-attachments/assets/ba0348e3-0323-4dfb-8100-d0bfdf7acd68" height="50%" width="50%" alt="Disk Sanitization Steps"/>
 - On the setup screen in the password section, put in the password for the MySQL database that was already created, then click Open.
 - In the Unnamed Server window, in the left panel, right click Unnamed  > Create New > Database
 - Name the new Database “osTicket” and click OK.

 <br />

 <h3>Step 11: Finish osTicket Setup</h3>
  
 - Return to the osTicket web page and fill in the Database Settings
   > MySQL Database - osTicket 
   > <br /> MySQL Username - root
   > <br /> MySQL Password - whatever password you wrote down
 - Click Install Now

 <br />

 <h3>Congrats! You’re done setting up osTicket!<h3/>

 <p>
 <img src="https://github.com/user-attachments/assets/1bd9a732-5417-4d39-a3fb-6fb85a228ed4" height="60%" width="60%" alt="Disk Sanitization Steps"/>
 </p>
