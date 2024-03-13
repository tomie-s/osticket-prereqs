<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

<ul>
  <li>Install osTicket dependencies
    <ul>
      <li>IIS in Windows</li>
      <li>PHP Manager for IIS</li>
      <li>Rewrite Module</li>
      <li>PHP</li>
      <li>VC redist</li>
      <li>MySQL</li>
    </ul>
  </li>
  <li>Register PHP from within IIS Manager</li>
  <li>Download osTicket</li>
  <li>Enable osTicket extensions on PHP manager within IIS Manager</li>
  <li>Setup osTicket account</li>
  <li>Install HeidiSQL and create osTicket database</li>
  <li>Connect osTicket account to database on MySQL & Complete osTicket install</li>
</ul>

<h2>Installation Steps</h2>

<b>Install osTicket dependencies</b>
<p>
Before installing and setting up OsTicket, I find and install the osTicket dependencies listed above such as IIS Windows Server which will allow the osTicket website to run on the Windows virtual machine.
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/c99195c3-32e9-49ff-8504-dfc1313f8f89" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/4880f6fb-57ea-4495-962d-37cddbba2ad7" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Register PHP from within IIS Manager</b>
<p>
Open up IIS as an administrator, click on 'PHP manager', and click 'Register new PHP version'. In the window that opens, select the 'php-cgi.exe' file to complete the registration. Restart IIS manager to ensure PHP registration is active. 
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/d5a01aed-2203-4324-b052-0ec0d266b4b1" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/4225749e-29df-41d9-99ef-a757ba0cbab7" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Download osTicket</b>
<p>
Download osTicket and once the download is complete, extract and copy the 'upload' folder to your local C: drive to install osTicket. Finally, rename the upload folder to osTicket and restart IIS manager.
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/574f553b-347e-41bb-83fb-5ae4c0783e85" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/d751ff0f-0328-4b02-bf9e-3aef173a0fa4" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Enable osTicket extensions on PHP manager within IIS Manager</b>
<p>
Within the IIS manager, go to 'sites -> Default -> osTicket' and click “Browse *:80” to launch the OsTicket Installer. The installer will show some missing extensions which will need to be enabled. Go back to the IIS manager, still viewing 'sites -> Default -> osTicket', click PHP manager -> PHP extension and enable these extension: php_imap.dll, php_intl.dll, and php_opcache.dll. Finally restart IIS manager. 
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/a8e32358-bebc-4f55-9a58-44a2167596b1" height="45%" width="45%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/0f5ee14d-1179-42cc-a2ef-06d7f3938658" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Setup osTicket account</b>
<p>
Fill in the new name of the osTicket account and add in an email that will be used by the system as default to collect all requests from customers. Also set up the admin user account.
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/23dfd7b1-b6fe-41f3-8caa-fcad70a2a7eb" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Install HeidiSQL and setup osTicket database</b>
<p>
Download in install HeidiSQL to connect to a SQL server. Launch HeidiSQL and create a new session to create a database called 'osTicket'.
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/9de80032-0e55-46ef-b9ce-2672399e70ab" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
<br />

<b>Connect osTicket account to database on MySQL & Complete osTicket install</b>
<p>
Continue the account setup on osTicket installer to add in the new database information. Once all the information is filled out, click 'Install Now'. Next screen should show that osTicket was successfully installed.
</p>
<p>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/adf0ed32-1705-4317-a5da-7cb15c015b62" height="65%" width="65%" alt="Disk Sanitization Steps"/>
<img src="https://github.com/tomie-s/osticket-prereqs/assets/59409588/87332a04-5a56-4598-832e-6be2c699d343" height="65%" width="65%" alt="Disk Sanitization Steps"/>
</p>
<br />
