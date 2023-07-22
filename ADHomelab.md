<h1>Active Directory Home Lab</h1>

 ### [Medium Blog Post](https://medium.com/@jsta388/unveiling-the-power-of-windows-server-2019-a-journey-into-virtual-labs-5774c607d31c)
 ### [Josh Madakor Video Walkthrough](https://youtu.be/MHsI8hJmggI)

<h2>Description</h2>
In this hands-on virtual adventure, you'll learn how to set up a powerful and immersive environment using VirtualBox, exploring the wonders of Active Directory, Group Policy Objects, and the mighty PowerShell scripting language. Embark on this journey to expand your IT knowledge and discover the boundless potential of Windows Server 2019 in real-world scenarios.
<br />


<h2>Utilities Used </h2>

- <b>Windows 10</b> 
- <b>Windows Server 2019</b>
- <b>Powershell</b>

<h2>Brief Walkthrough:</h2>

Hardware Requirements: <br/>
- Ensure your computer meets the hardware requirements for running virtual machines smoothly.
- Having at least 16GB of RAM is recommended to allocate sufficient resources to the virtual machines.
- Consider using an SSD for improved performance, as it will help with faster VM boot times and overall responsiveness.<br />
<br />

Installing VirtualBox:  <br/>
- Visit the official VirtualBox website (https://www.virtualbox.org/) and download the installer suitable for your operating system.
- Run the installer and follow the setup wizard to install VirtualBox on your computer.
- Once installed, launch VirtualBox to begin creating virtual machines.<br />
<br />

Installing Windows Server 2019: <br/>
- In VirtualBox, click on "New" to create a new virtual machine.
- Give the virtual machine a name and choose "Microsoft Windows" as the type and "Windows Server 2019 (64-bit)" as the version.
- Allocate enough RAM (e.g., 4GB or more) and create a virtual hard disk with a size of at least 40GB.
- Select "Create a virtual hard disk now" and choose the virtual disk file type (VDI is recommended).
- Choose "Dynamically allocated" as the storage option to save disk space as the VM's storage grows only as needed.
- Click "Create" to finish creating the virtual machine.
- Select the newly created virtual machine and click on "Settings."
- Under "Storage," click on the optical drive and select the Windows Server 2019 ISO file as the bootable media.
- Start the virtual machine to begin the Windows Server installation process.
- Follow the on-screen instructions to install Windows Server 2019.<br />
<br />

Creating a Domain Controller:  <br/>
- Once Windows Server 2019 is installed, log in with your administrator credentials.
- Open "Server Manager" from the taskbar and click on "Add roles and features."
- Follow the wizard and select "Active Directory Domain Services" to install the role.
- After the installation is complete, a yellow warning flag appears on the Server Manager. Click on it and choose "Promote this server to a domain controller."
- In the "Deployment Configuration" section, choose "Add a new forest" and enter your desired domain name (e.g., "mylab.local").
- Set the Directory Services Restore Mode (DSRM) password, which is important for restoring Active Directory in case of emergencies.
- Review the settings, and if everything looks good, click "Install" to promote the server to a domain controller.<br />
<br />

- Adding Client Machines to the Domain:  <br/>
- Create additional virtual machines for Windows 10 clients, following similar steps as creating the domain controller virtual machine.
- Ensure that all virtual machines are in the same VirtualBox network (NAT, Bridged, or Host-Only) to allow communication between them.
- Start a Windows 10 client VM and go through the Windows setup process.
- Once the setup is complete, log in using the local administrator account.
- Go to "Control Panel" > "System" > "Advanced system settings."
- In the "Computer Name" tab, click "Change," choose "Domain," and enter the domain name you created earlier (e.g., "mylab.local").
- Click "OK" and provide domain administrator credentials when prompted.
- Restart the client machine, and you should now be able to log in using domain credentials.<br />
<br />

Active Directory User Management:  <br/>
- On the domain controller, open "Active Directory Users and Computers" from the "Tools" menu in "Server Manager."
- Create new organizational units (OUs) to organize users and computers logically.
- Right-click on the OU where you want to create a new user and select "New" > "User."
- Follow the wizard to enter user details such as full name, username, and password.
- Customize user properties, such as group memberships, login scripts, profile settings, and account expiration date.
- Similarly, create and manage computer accounts in the appropriate OUs.<br />
<br />

Group Policy Objects (GPO):  <br/>
- Open "Group Policy Management Console" from the "Tools" menu in "Server Manager."
- Explore the existing "Default Domain Policy" and "Default Domain Controllers Policy" GPOs created by default.
- Create new GPOs by right-clicking on the "Group Policy Objects" container and selecting "New."
- Link the GPOs to specific OUs or the domain root by right-clicking on the appropriate OU and selecting "Link an existing GPO."
- Configure various settings like password policies, desktop backgrounds, security settings, software installation, etc., within each GPO.
<br />

PowerShell Scripting for Automation:  <br/>
- To begin PowerShell scripting, open PowerShell ISE (Integrated Scripting Environment) on the domain controller.
- Start learning the basics of PowerShell and its syntax by following tutorials and examples available online.
- Write PowerShell scripts to automate repetitive tasks, such as creating multiple users with specific properties or modifying GPO settings.
- Test your scripts in a controlled environment before applying them in your production domain.
- Script used will be attached to repo AD_PS-master.zip
<br />

Experiment and Explore:  <br/>
- Now that your homelab is up and running, take the time to experiment and explore various features and services offered by Windows Server 2019 and Active Directory.
- Set up additional roles like DNS, DHCP, and File Server to expand your lab's capabilities and simulate real-world scenarios.
- Try integrating Windows Server with other technologies, such as Microsoft Exchange or Microsoft SQL Server, to enhance your learning.
<br />

Remember, setting up a homelab is a continuous learning process, and it's normal to encounter challenges along the way. Don't hesitate to explore online forums, communities, and resources for assistance and to share your experiences with others. Continuously expand your knowledge by staying up-to-date with the latest developments in Windows Server and the IT industry. Your homelab journey will provide invaluable hands-on experience and make you more confident in tackling real-world IT tasks. Happy homelabbing, and enjoy your exciting IT adventure!

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
