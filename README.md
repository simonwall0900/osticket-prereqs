<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This project documents the prerequisites, installation, and configuration of the open-source help desk ticketing system osTicket. It provides a step-by-step overview of the deployment process while demonstrating the foundational knowledge required to successfully implement and manage a functional IT help desk environment


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 11</b> (21H2)

<h2>List of Prerequisites</h2>


- Setup a Virtual Machine in Azure
- Install the osTicket Requirements
- Install osTicket itself
- Do the after-installation configuration of osTicket
- Explore osTicket as a Help Desk Professional (Create, Interact, and close Tickets

<h2>Installation Steps</h2>

<p>
<img width="1284" height="579" alt="IMG_4958" src="https://github.com/user-attachments/assets/3e08c601-3af7-4582-a9c9-0fa702eedd5b" />

</p>
<p>
The first step in this project was creating a virtual machine (VM) in Microsoft Azure to host the osTicket help desk system.

VM Setup Process Created a Resource Group in Microsoft Azure. Selected the appropriate region and configuration settings for the Resource Group. Navigated to the Virtual Machines section in the Azure portal. Selected Create → Azure Virtual Machine. Selected the Resource Group created during the first step. Configured the VM settings while keeping the selected region consistent with the Resource Group. Completed the VM deployment. Connected to the Windows VM using Remote Desktop (RDP). Accessed the VM and prepared the environment for the osTicket installation.


</p>
<br />

<p>
<img width="1284" height="866" alt="IMG_4959" src="https://github.com/user-attachments/assets/acfeca76-0658-4ee5-b27c-962e7b6bc46c" />

</p>
<p>

Install IIS

IIS (Internet Information Services) is used to host the osTicket web application.

To prepare the Windows virtual machine for osTicket, Internet Information Services (IIS) was installed as the web server. IIS allows the VM to host and serve the osTicket web application.

Installation Process Opened Server Manager on the Windows virtual machine. Selected Add Roles and Features. Selected Web Server (IIS) from the available server roles. Continued through the installation wizard and installed the required IIS components. Restarted the server when necessary to complete the installation. Verifying IIS

After installation, IIS was tested by opening a web browser on the virtual machine and navigating to:

http://localhost

The IIS welcome page appeared, confirming that IIS was successfully installed and running.

Result

IIS was successfully configured on the Windows virtual machine, providing the web server environment required to continue with the osTicket installation.


</p>
<br />

<p>
<img width="1284" height="626" alt="IMG_4960" src="https://github.com/user-attachments/assets/5d2d7137-2ab2-4e9e-bf04-776e3fa618e1" />

</p>
<p>
To support osTicket, PHP was installed and configured on the Windows virtual machine. PHP is required to process the application's web files and allow osTicket to run through IIS.

Installation Process Downloaded a PHP version compatible with the osTicket release. Extracted the PHP files to the Windows virtual machine. Created a PHP directory: C:\PHP Configured PHP to work with IIS. Enabled the required PHP extensions needed by osTicket. Added the PHP directory to the Windows system PATH when required. Restarted IIS to apply the configuration changes. Verifying PHP

To verify that PHP was installed and configured correctly, a test PHP file was created in the IIS website directory:

The PHP test file was then opened through a web browser.

If the PHP information page loads successfully, it confirms that PHP is installed and communicating correctly with IIS.

Result

PHP was successfully installed and configured on the Windows virtual machine. This provided the PHP environment required for osTicket to process its web application files and continue with the installation.


</p>

<img width="1284" height="589" alt="IMG_4961" src="https://github.com/user-attachments/assets/6082ed74-117d-41bc-8260-a5517dae1643" />

</p>

To provide osTicket with a database for storing tickets, users, settings, and other application data, MySQL was installed and configured on the Windows virtual machine.

Installation Process Installed MySQL on the Windows virtual machine. Created a secure administrator password during the installation. Started the MySQL database service. Verified that the MySQL service was running correctly. Created a dedicated database for osTicket. Created a separate database user for the osTicket application. Assigned the appropriate permissions to the osTicket database user. Database Configuration

The following database was created for the osTicket installation:

Database: osticket User: osticket_user

Using a dedicated database and user helps keep the osTicket application organized and allows database access to be managed separately from the MySQL administrator account.

Result

MySQL was successfully installed and configured. A dedicated osTicket database and user were created with the required permissions, providing the database environment needed to continue the osTicket installation.

<p>
<img width="1284" height="575" alt="IMG_4962" src="https://github.com/user-attachments/assets/031a3aef-b5d7-425f-9173-4dc1bbfeb2e2" />


  After configuring IIS, PHP, and MySQL, the next step was to download and prepare the osTicket installation files on the Windows virtual machine.

Installation Process Downloaded the osTicket installation package. Extracted the downloaded files on the Windows virtual machine. Copied the extracted osTicket files into the IIS website directory.

The files were placed in:

C:\inetpub\wwwroot\osticket Verified that the osTicket files were copied correctly and were accessible within the IIS website directory. Result

The osTicket application files were successfully placed in the IIS web directory. This prepared the application to be accessed through a web browser and allowed the osTicket installation process to continue.
</p>


<img width="1284" height="1018" alt="IMG_4963" src="https://github.com/user-attachments/assets/4852bd18-80b2-4f73-b25a-ef6706f63ddd" />



After installing and configuring IIS, PHP, MySQL, and the osTicket application files, the final step was to verify that osTicket was running correctly.

Verification Process Opened a web browser on the Windows virtual machine. Navigated to:http://localhost/osticket Verified that the osTicket interface loaded successfully. Confirmed that the application was accessible through the IIS web server. Result

The successful loading of the osTicket interface confirmed that the required components were installed and configured correctly. The system was now ready to be used as an IT help desk ticketing platform.

The completed environment allows users to submit support requests as customers, while help desk employees can access, manage, update, and resolve those tickets as agents. This demonstrates the complete foundation of a functional help desk environment.


<br />
