<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This is a brief overview of the prerequisites and install of osTicket <br />



<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable & Install IIS w/ CGI
- Open IIS as Admin
- Register PHP from IIS
- Install osTicket & Enable PHP Extensions
- Setup osTicket In Browser

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/hKtXaok.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/YVNS2pt.png" height="45%" width="45%" alt="Disk Sanitization Steps"/>
</p>
<p>
Starting off by creating an Azure Virtual Machine that's Windows 10 with 4 vCUPs. Using Remote Desktop Protocol (RDP) is used to log into the VM. 

The osTicket-Installation-Files.zip is downloaded and unzipped onto the desktop of the VM. This folder contains all necessary files for installing osTicket, PHP, MySQL, and other dependencies.

Setting Up IIS with CGI:
Going in Windows Features then check;
Internet Information Services>World Wide Web Services>Application Development Features>CGI (checked)

</p>
<br />

<p>
<img src="https://i.imgur.com/p0bNeDQ.png" height="55%" width="48%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/KecLNUA.png" height="55%" width="48%" alt="Disk Sanitization Steps"/>
</p>
<p>
Installing PHP, MySQL, and Other Dependencies:

PHP Manager for IIS
PHP is installed by extracting it to C:\PHP.
PHP is registered in IIS using the PHP Manager for IIS, pointing to the php-cgi.exe file in the C:\PHP folder

Installing osTicket:
The osTicket v1.15.8 installation files are extracted, and the upload folder is copied to the IIS root directory (C:\inetpub\wwwroot\), renamed to osTicket.
IIS is restarted to reflect the new changes and serve the osTicket site.
The php_imap.dll, php_intl.dll, and php_opcache.dll extensions are enabled via the PHP Manager in IIS
</p>
<br />

<p>
<img src="https://i.imgur.com/KrTwOCY.png" height="50%" width="45%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/DnvQszr.png" height="50%" width="45%" alt="Disk Sanitization Steps"/>
  <img src="https://i.imgur.com/0nQ14YR.png" height="50%" width="45%" alt="Disk Sanitization Steps"/>
</p>
<p>
After installing the PHP extensions, configuring the osTicket settings to finalize the installation. User access should be allowed in the interface
</p>
<br />
