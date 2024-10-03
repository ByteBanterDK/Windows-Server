<h1>Active Directory Configuration</h1>

<h2>Description</h2>
<p>
    This project involves setting up and configuring Active Directory (AD) on a Windows Server 2019 environment. The goal is to create a functional AD domain, manage users and organisational units, and configure group policies to ensure a secure and well-organised network infrastructure. This setup includes installing Windows Server 2019 on a virtual machine, configuring the server roles, and establishing network connections between the server and client machines.
</p>

<h2>Ownership Statement:</h2>
This project and all associated files are the original work of ByteBanterDK. If you use any part of this project, please ensure you comply with the applicable laws and regulations in your jurisdiction, including but not limited to copyright laws in the United Kingdom. For any enquiries or collaboration opportunities, please contact me at DenisKTechnology@protonmail.com.

<h2>Key Objectives</h2>
<ul>
    <li><strong>Download and Install Windows Server 2019:</strong> Obtain the Windows Server 2019 ISO and set it up on a virtual machine.</li>
    <li><strong>Configure Active Directory:</strong> Set up AD DS (Active Directory Domain Services) and create a new forest and domain.</li>
    <li><strong>Manage Users and Groups:</strong> Create organisational units, add users, and manage groups within the AD structure.</li>
    <li><strong>Configure Group Policies:</strong> Implement group policies to manage user and computer settings across the domain.</li>
    <li><strong>Establish Network Connectivity:</strong> Configure network settings to allow communication between the server and client machines.</li>
    <li><strong>Integrate Client Machines:</strong> Add Windows 10 client machines to the domain and manage them through AD.</li>
</ul>

<h2>Utilities Used</h2>
<ul>
    <li><strong>Virtualisation Software:</strong> VirtualBox</li>
    <li><strong>Operating Systems:</strong> Windows Server 2019, Windows 10</li>
</ul>

<h2>Environments Used</h2>
<ul>
    <li><strong>Operating Systems:</strong> Windows Server 2019, Windows 10</li>
    <li><strong>Hardware:</strong> Virtual Machines</li>
    <li><strong>Tools:</strong> Windows Server Manager, Active Directory Users and Computers, Group Policy Management</li>
</ul>

<h2>Program Walk-through</h2>

<h3>Step 1: Download Windows Server 2019 ISO</h3>
<img src="https://i.imgur.com/N4INUDj.png" alt="Windows Server 2019 Download">
<p>
    <strong>Search for Windows Server 2019:</strong><br>
    Action: Open your preferred search engine (e.g., Google) and type "Windows Server 2019 download".<br>
    Explanation: This search will help you find the official Microsoft link for downloading Windows Server 2019.
</p>
<img src="https://i.imgur.com/X8TSF7F.png" alt="Microsoft Evaluation Centre">
<p>
    <strong>Find the Microsoft Evaluation Centre:</strong><br>
    Action: Scroll through the search results to find the Microsoft link titled "Windows Server 2019 | Microsoft Evaluation Centre".<br>
    Explanation: The Microsoft Evaluation Centre provides a free trial version of Windows Server 2019.
</p>
<p>
    <strong>Download the ISO:</strong><br>
    Action: Click on "ISO DOWNLOADS" on the Microsoft Evaluation Centre page. Choose the appropriate language (for this demonstration, select English).<br>
    Explanation: The ISO file is a disc image that contains all the files needed to install Windows Server 2019. The download can take between 10 to 30 minutes, depending on your internet speed.
</p>

<h3>Step 2: Set Up Windows Server 2019 on VirtualBox</h3>
<img src="https://i.imgur.com/zfH405i.png" alt="VirtualBox New VM Setup">
<p>
    <strong>Create a New Virtual Machine:</strong><br>
    Action: Open VirtualBox and click on "New".<br>
    Explanation: This starts the process of creating a new virtual machine (VM), which will host your Windows Server 2019 installation.
</p>
<img src="https://i.imgur.com/C5dBZBJ.png" alt="Name Your Virtual Machine">
<p>
    <strong>Name Your Virtual Machine:</strong><br>
    Action: Enter a name for your VM (e.g., "Windows Server 2019"). Click on the drop-down menu for the ISO image and select the Windows Server 2019 ISO you downloaded.<br>
    Explanation: Naming your VM helps you identify it easily among other VMs you might have.
</p>
<img src="https://i.imgur.com/k3HMVc6.png" alt="Configure Memory and CPU">
<p>
    <strong>Configure Memory and CPU:</strong><br>
    Action: Allocate 6GB of RAM and 3 CPUs for the VM. Click "Next".<br>
    Explanation: Adequate memory and CPU allocation ensures the VM runs smoothly without lag or performance issues.
</p>
<p>
    Remember to create a memorable username and password; this will be for logging in before gaining access to the Windows Server 2019:
</p>
<img src="https://i.imgur.com/0HAHZbc.png" alt="Create Username and Password">

<h3>Step 3: Configure Virtual Hard Disk</h3>
<img src="https://i.imgur.com/3YZjRrp.png" alt="Virtual Hard Disk Setup">
<p>
    <strong>Create a Virtual Hard Disk:</strong><br>
    Action: Choose a virtual hard disk size between 50GB and 100GB. Click "Next" and then "Finish".<br>
    Explanation: The virtual hard disk will store the operating system and other files. A size of 50GB or more is recommended to ensure there's enough space for the installation and future updates.
</p>

<h3>Step 4: Finalise VM Configuration</h3>
<img src="https://i.imgur.com/NqoJTWO.png" alt="VM Final Configuration">
<p>
    <strong>Review and Finalise:</strong><br>
    Action: Review your VM settings and click "Finish".<br>
    Explanation: Ensure all settings are correct before finalising the setup. This includes checking the name, ISO image, memory, CPU, and hard disk settings.
</p>
<p>
    <strong>Boot Up Windows Server 2019:</strong><br>
    Action: Start your Windows Server 2019 virtual machine and allow it to boot up. This process may take up to 5 minutes.<br>
    Explanation: During this phase, the virtual machine loads the necessary files and prepares for the installation process.
</p>
<p>
    <strong>Language and Region Selection:</strong><br>
    Action: A pop-up box will appear to select the language, time format, currency format, and keyboard or input method. Choose "United Kingdom" for all options, then click "Install now".<br>
    Explanation: Selecting the correct language and region ensures that Windows Server 2019 is installed with the appropriate settings for your location.
</p>
<img src="https://i.imgur.com/PNWd9lF.png" alt="Windows Server 2019 Edition Selection">
<p>
    <strong>Windows Server 2019 Edition Selection:</strong><br>
    Action: Choose "Windows Server 2019 Standard Evaluation (Desktop Experience)" from the available options.<br>
    Explanation: This edition provides a full desktop experience along with evaluation features. Click "Next" to proceed.
</p>
<img src="https://i.imgur.com/CVRdtkl.png" alt="Accept Licence Terms">
<p>
    <strong>Accept Licence Terms:</strong><br>
    Action: Read and accept the licence terms by checking the box, then click "Next".<br>
    Explanation: Accepting the licence terms is necessary to proceed with the installation of Windows Server 2019.
</p>
<img src="https://i.imgur.com/V3cfwMi.png" alt="Custom Installation">
<p>
    <strong>Custom Installation:</strong><br>
    Action: Select "Custom: Install Windows only (advanced)" as the installation type.<br>
    Explanation: This option allows you to customise the installation settings, including choosing the disk where Windows will be installed.
</p>
<img src="https://i.imgur.com/halAGfU.png" alt="Disk Selection">
<p>
    <strong>Disk Selection:</strong><br>
    Action: Choose the virtual hard disk that you set up earlier for Windows Server 2019 installation. Click "Next" to continue.<br>
    Explanation: Selecting the correct disk ensures that Windows is installed in the intended location.
</p>
<img src="https://i.imgur.com/21ml6D1.png" alt="Installation Process">
<p>
    <strong>Installation Process:</strong><br>
    Action: Windows will begin the installation process, which involves copying files, preparing for installation, and configuring settings. This process may take between 20 minutes to 1 hour, depending on your system's performance.<br>
    Explanation: During this phase, Windows Server 2019 installs the necessary files and prepares the system for first-time use.
</p>
<img src="https://i.imgur.com/b0Daup6.png" alt="Windows Server 2019 Startup Screen">
<p>
    Now that you've reached the Windows Server 2019 startup screen, proceed by pressing Ctrl + Alt + Delete on your keyboard to unlock the system. Remember the administrator password you created earlier. Start the Server Manager by clicking on "Manage" and then "Add Roles and Features".
</p>
<img src="https://i.imgur.com/H2zIgQt.png" alt="Adding Roles and Features">
<h3>Adding Roles and Features</h3>
<p>
    <strong>Open Add Roles and Features Wizard:</strong><br>
    Action: After launching Server Manager, click on "Manage" and then "Add Roles and Features". The "Add Roles and Features Wizard" pop-up box will appear.
</p>
<img src="https://i.imgur.com/1lg4nx9.png" alt="Before You Begin">
<p>
    <strong>Before You Begin:</strong><br>
    Click "Next >" to proceed.
</p>
<img src="https://i.imgur.com/PuaZLSO.png" alt="Installation Type">
<p>
    <strong>Installation Type:</strong><br>
    Select "Role-based or feature-based installation" and proceed to the next configuration.
</p>
<img src="https://i.imgur.com/0plHaCR.png" alt="Server Selection">
<p>
    <strong>Server Selection:</strong><br>
    Choose "Select a server from the server pool" and then select your Windows Server computer name. Click "Next" to continue.
</p>
<img src="https://i.imgur.com/trZin20.png" alt="Server Roles">
<p>
    <strong>Server Roles:</strong><br>
    Tick the box for "Active Directory Domain Services" and proceed by clicking "Next".
</p>
<img src="https://i.imgur.com/KMVqFHE.png" alt="Features">
<p>
    <strong>Features:</strong><br>
    Leave the features at their default settings. Click "Next" to proceed with the Active Directory Domain Services (AD DS) installation.
</p>
<img src="https://i.imgur.com/MsF6P6z.png" alt="Confirmation">
<p>
    <strong>Confirmation:</strong><br>
    Review the selected options and proceed by clicking "Install". A message will inform you that the installation could take up to 45 minutes.
</p>

<h3>Post-Deployment Configuration</h3>
<img src="https://i.imgur.com/IyMKs9W.png" alt="Active Directory Domain Services Configuration Wizard">
<p>
    <strong>Active Directory Domain Services Configuration Wizard:</strong><br>
    Click on "Add a new forest" and type a root domain name. Proceed by clicking "Next".
</p>
<img src="https://i.imgur.com/otCdDlQ.png" alt="Domain Controller Options">
<p>
    <strong>Domain Controller Options:</strong><br>
    Create a password and keep all other settings at their default values. Click "Next", but skip DNS options such as "Create DNS delegation".
</p>
<img src="https://i.imgur.com/6gaE1Z7.png" alt="Additional Options">
<p>
    <strong>Additional Options:</strong><br>
    Verify the NetBIOS name assigned to the domain. Click "Next" to proceed.
</p>
<img src="https://i.imgur.com/PJ40IOc.png" alt="Paths and Review Options">
<p>
    <strong>Paths and Review Options:</strong><br>
    Skip these options and proceed.
</p>
<img src="https://i.imgur.com/PJ40IOc.png" alt="Prerequisites Check">
<p>
    <strong>Prerequisites Check:</strong><br>
    Click on "Install". This process could also take up to 45 minutes depending on your network speed. Once completed, your Windows Server computer will reset.
</p>
<img src="https://i.imgur.com/duTKRmA.png" alt="Logging Back In">
<h3>Logging Back In</h3>
<p>
    Log back into your server using your domain name/administrator credentials.
</p>
<img src="https://i.imgur.com/ObSfm4T.png" alt="Configuring Active Directory Users and Computers">
<h3>Configuring Active Directory Users and Computers</h3>
<p>
    Launch Server Manager, click on "Tools", and select "Active Directory Users and Computers".
</p>
<img src="https://i.imgur.com/NdupDE9.png" alt="View > Advanced Features">
<p>
    <strong>View > Advanced Features:</strong><br>
    Enable "Advanced Features" to access additional options.
</p>
<img src="https://i.imgur.com/SEDHRy2.png" alt="Creating Organizational Units (OUs)">
<p>
    <strong>Creating Organisational Units (OUs):</strong><br>
    Right-click on your domain and choose "New > Organisational Unit". Name it "Cyber Security" and select "Protect container from accidental deletion".
</p>
<img src="https://i.imgur.com/TabeDax.png" alt="Adding Users">
<p>
    <strong>Adding Users:</strong><br>
    Add users with appropriate first and last names. Consider using a user logon name that uniquely identifies them. Create passwords for these users, considering various security options.
</p>
<img src="https://i.imgur.com/Zpx0fGV.png" alt="Creating Groups">
<p>
    <strong>Creating Groups:</strong><br>
    Right-click and select "New > Group". Name it "Cyber Security Soc Analyst".
</p>
<img src="https://i.imgur.com/fUNwdr2.png" alt="Assigning Users to Groups">
<p>
    <strong>Assigning Users to Groups:</strong><br>
    Highlight the users you created, right-click, and select "Add to a group". Type the group name and click "OK".
</p>
<img src="https://i.imgur.com/zeRzX7A.png" alt="Exploring User Properties">
<p>
    <strong>Exploring User Properties:</strong><br>
    Right-click on a user and select "Properties". Explore the various tabs such as "General", "Address", "Account", "Profile", "Telephones", "Organisation", "Sessions", and "Environment" to configure user settings.
</p>

<h4>General:</h4>
<ul>
    <li><strong>First Name:</strong> Refers to the user's first name.</li>
    <li><strong>Last Name:</strong> Refers to the user's last name.</li>
    <li><strong>Initials:</strong> Typically used for abbreviations of the user's name.</li>
    <li><strong>Display Name:</strong> The name displayed in the directory and other services.</li>
    <li><strong>Description:</strong> A brief description of the user, often used for identification.</li>
    <li><strong>Office:</strong> The physical location or office of the user.</li>
    <li><strong>Telephone Number:</strong> The user's contact number.</li>
    <li><strong>Email:</strong> The user's email address.</li>
    <li><strong>Web Page:</strong> If applicable, this is the user's personal or professional website.</li>
</ul>

<h4>Address:</h4>
<ul>
    <li><strong>Street:</strong> The user's street address.</li>
    <li><strong>P.O. Box:</strong> If applicable, the user's postal box number.</li>
    <li><strong>City:</strong> The city where the user resides.</li>
    <li><strong>State/Province:</strong> The state or province where the user resides.</li>
    <li><strong>Zip/Postal Code:</strong> The postal code of the user's area.</li>
    <li><strong>Country/Region:</strong> The country or region where the user resides.</li>
</ul>

<h4>Account:</h4>
<ul>
    <li><strong>Logon Hours:</strong> Specifies the times during which the user is allowed to log in. This restricts login access outside of specified hours.</li>
    <li><strong>Log on To:</strong> Allows the user to log in to specific computers within the domain. This can restrict access to only specified machines.</li>
    <li><strong>Account Expires:</strong> Sets an expiration date for the user account. After this date, the account will be disabled.</li>
    <li><strong>Account Options:</strong>
        <ul>
            <li>User Must Change Password at Next Logon: Forces the user to change their password the next time they log in.</li>
            <li>User Cannot Change Password: Prevents the user from changing their password.</li>
            <li>Password Never Expires: Ensures the user's password never expires.</li>
            <li>Account is Disabled: Disables the user's account, preventing login.</li>
        </ul>
    </li>
</ul>

<h4>Profile:</h4>
<ul>
    <li><strong>Profile Path:</strong> Specifies the path to the user's profile.</li>
    <li><strong>Logon Script:</strong> Specifies a script to run when the user logs in.</li>
    <li><strong>Home Folder:</strong> Specifies the path to the user's home folder.</li>
</ul>

<h4>Telephone:</h4>
<ul>
    <li><strong>Office:</strong> The user's office telephone number.</li>
    <li><strong>Home:</strong> The user's home telephone number.</li>
    <li><strong>Mobile:</strong> The user's mobile phone number.</li>
    <li><strong>Fax:</strong> The user's fax number.</li>
</ul>

<h4>Organisation:</h4>
<ul>
    <li><strong>Job Title:</strong> The user's job title or position within the organisation.</li>
    <li><strong>Department:</strong> The department the user belongs to.</li>
    <li><strong>Company:</strong> The company the user works for.</li>
    <li><strong>Manager:</strong> The user's manager or supervisor.</li>
    <li><strong>Direct Reports:</strong> Employees who report directly to the user.</li>
</ul>

<h4>Sessions:</h4>
<ul>
    <li><strong>End a Disconnected Session:</strong> Specifies what action to take when a session is disconnected.</li>
    <li><strong>Active Session Limit:</strong> Limits the duration of an active session.</li>
    <li><strong>Idle Session Limit:</strong> Limits the duration of an idle session.</li>
    <li><strong>Allow Reconnection:</strong> Determines if users can reconnect to disconnected sessions.</li>
</ul>

<h4>Environment:</h4>
<ul>
    <li><strong>Start the following program at logon:</strong> Specifies a program to start automatically when the user logs in.</li>
    <li><strong>End a disconnected session:</strong> Specifies what action to take when a session is disconnected.</li>
</ul>

<h3>Remote Control:</h3>
<p> 
 <ul>
            <li>Allows administrators to remotely control the user's session.</li>
            <li>Requires user's permission for remote control.</li>
            <li>Specifies the level of control the remote administrator has over the user's session.</li>
        </ul>

   <section>
        <h2>Download Windows 10 ISO Image</h2>
        <ol>
            <li>Search for a Windows 10 ISO image on your preferred search engine.</li>
            <li>Click on the appropriate link to download the installation media.</li>
            <li>Accept the licence terms and choose to create installation media (USB flash drive, DVD, or ISO file).</li>
            <li>Select the default settings unless you need to change the language.</li>
            <li>Choose the ISO file option and proceed with the download.</li>
        </ol>
        <p>This process could take up to 30 minutes depending on your internet speed.</p>
        <img src="https://i.imgur.com/xyUAD1g.png" alt="Download Windows 10 ISO">

  <section>
        <h2>Create a New Virtual Machine (VM) for Windows 10</h2>
        <ol>
            <li>In your VM software, such as VirtualBox, click on "New" to create a new VM.</li>
            <li>Set up a name for the VM and proceed with the default settings.</li>
            <li>Allocate recommended resources, such as 2GB of RAM and 1 CPU, to ensure smooth performance.</li>
            <li>Set up a virtual hard disk for the VM, preferably around 50GB in size.</li>
            <li>Finish setting up and configuring the VM.</li>
        </ol>
        <img src="https://i.imgur.com/00OMIx6.png" alt="Create New VM">
    </section>

   <section>
        <h2>Configure Windows 10 VM Settings</h2>
        <ol>
            <li>Go into the settings of the Windows 10 VM.</li>
            <li>Scroll down to storage settings and click on the empty storage device.</li>
            <li>Choose the disk file option and select the Windows 10 ISO file you downloaded.</li>
            <li>Start the Windows 10 VM and let it load until the Windows setup screen appears.</li>
        </ol>
        <img src="https://i.imgur.com/Jb8NRMD.png" alt="VM Settings">
    </section>

   <section>
        <h2>Install Windows 10</h2>
        <ol>
            <li>Proceed with the Windows setup process, clicking "Next" until prompted.</li>
            <li>If prompted for a product key, select the option "I don't have a product key".</li>
            <li>Choose Windows 10 Home edition and accept the licence terms.</li>
            <li>Select the custom installation option and choose the virtual hard disk you set up earlier.</li>
            <li>Follow the installation process, which may take up to 1 hour.</li>
        </ol>
        <img src="https://i.imgur.com/uBFZaTA.png" alt="Windows Setup">
    </section>

   <section>
        <h2>Network Setup</h2>
        <ol>
            <li>After the Windows 10 installation is complete, go back to your VM settings.</li>
            <li>Scroll down to network settings and attach the VM to a bridge adapter to enable internet connection.</li>
            <li>Repeat the same process for the Windows Server 2019 VM to ensure both computers have connectivity.</li>
        </ol>
        <img src="https://i.imgur.com/slK08hm.png" alt="Network Setup">
    </section>

   <section>
        <h2>Region and Keyboard Layout</h2>
        <ol>
            <li>Select your region and the appropriate keyboard layout.</li>
            <li>Skip the option for a second keyboard layout.</li>
        </ol>
        <img src="https://i.imgur.com/qrP12Ph.png" alt="Region and Keyboard Layout">
    </section>

   <section>
        <h2>Initial Setup</h2>
        <ol>
            <li>Wait for the system to load, which may take a few minutes.</li>
            <li>Choose "Set up for personal use" and click "Next".</li>
        </ol>
        <img src="https://i.imgur.com/4skGDiF.png" alt="Initial Setup">
    </section>

   <section>
        <h2>Account Setup</h2>
        <ol>
            <li>Opt for an offline account and choose "Limited experience".</li>
            <li>Set up a name for the PC and create a strong password.</li>
            <li>Answer security questions and click "Next".</li>
        </ol>
        <img src="https://i.imgur.com/I8fowjM.png" alt="Account Setup">
    </section>

   <section>
        <h2>Optional Settings</h2>
        <ol>
            <li>Click "Not Now" for the option to continue where you left off by importing from another browser.</li>
            <li>Turn off "Find my device" as it's not needed for this demonstration.</li>
            <li>Choose the second option for sending diagnostic data to Microsoft.</li>
            <li>Turn off options for improving inking and typing.</li>
        </ol>
        <img src="https://i.imgur.com/Mla6ajo.png" alt="Optional Settings">
    </section>

   <section>
        <h2>Customisation</h2>
        <p>Skip the customisation page by clicking "Skip".</p>
        <img src="https://i.imgur.com/iLBUV7Q.png" alt="Customisation">
    </section>

   <section>
        <h2>Finalisation</h2>
        <p>Allow the system to set up everything you configured, which may take several minutes.</p>
        <img src="https://i.imgur.com/jNcQsfu.png" alt="Finalisation">
    </section>

   <section>
        <h2>Obtaining IP Addresses</h2>
        <p>On both the Windows Server 2019 and Windows 10 machines, open Command Prompt (CMD) and type "ipconfig /all" to retrieve the IP addresses. Note down the IPv4 address of each machine.</p>
        <img src="https://github.com/user-attachments/assets/b2748b15-4293-471e-8973-e62462ce81e0" alt="IP Configuration">
    </section>

   <section>
        <h2>Configuring Windows Defender Firewall</h2>
        <p>On Windows 10, open Windows Defender Firewall with Advanced Security.</p>
        <ol>
            <li>Navigate to "Inbound Rules" and create a new rule.</li>
            <li>Choose "Custom rule type" and under scope, select the IP address of the Windows 10 machine.</li>
            <li>Name the rule and click "Finish" to allow data connection to the Windows Server 2019 machine.</li>
            <li>Repeat the same process for outbound rules, ensuring that the Windows 10 machine can send data.</li>
        </ol>
        <img src="https://github.com/user-attachments/assets/67f05822-912e-45f0-9791-29253b16af55" alt="Firewall Configuration">
    </section>

   <section>
        <h2>Refreshing IP Address</h2>
        <p>If the Windows Server 2019 machine didn't allow data through the assigned IP address, use the command "IPCONFIG /RENEW" to obtain a new IP address. Ensure that the IPv4 print is enabled in the inbound settings of the firewall.</p>
        <img src="https://github.com/user-attachments/assets/9ce6f703-fc6f-4a61-9c80-f1e95ca4f13f" alt="Refreshing IP Address">
    </section>

   <section>
        <h2>Configuring DNS Server</h2>
        <p>On the Windows 10 machine, right-click on the internet connection and select properties.</p>
        <ol>
            <li>Choose "Internet Protocol Version 4 (TCP/IPv4)" and configure the DNS server to the IP address of the Windows Server 2019 computer.</li>
            <li>Optionally, set an alternative DNS server like 1.1.1.1 or 8.8.8.8.</li>
        </ol>
        <img src="https://i.imgur.com/Jmx7ZVY.png" alt="Configuring DNS Server">
        <p><strong>Explanation:</strong></p>
        <p>By configuring the DNS server on the Windows 10 machine to the IP address of the Windows Server 2019 computer, you ensure that all DNS queries from the client machine are directed to the server, allowing for efficient name resolution within your network. This is particularly useful in environments where the Windows Server is managing DNS records for local resources.</p>
        <p>Setting an alternative DNS server, such as 1.1.1.1 or 8.8.8.8, provides a fallback option in case the primary DNS server (the Windows Server) becomes unavailable. This ensures that the Windows 10 machine can still resolve external domain names and maintain internet connectivity, thereby enhancing reliability and reducing potential downtime.</p>
    </section>

   <section>
        <h2>Joining the Domain</h2>
        <ol>
            <li>After completing basic configurations, search for "About your PC" and navigate to "Advanced system settings".</li>
            <li>Under "Computer Name", click on "Change" and input the domain name created during the first forest domain setup.</li>
            <li>Enter the desktop computer name and the username and password created while setting up the user on the Windows Server 2019.</li>
            <li>Restart the computer, and upon login, select the domain name under "Sign in to".</li>
        </ol>
        <img src="https://i.imgur.com/jUScLOI.png" alt="Joining Domain">
    </section>
   
   <section>
        <h2>Viewing Computers in Active Directory</h2>
        <p>Open the "Computers" folder in Windows Server 2019 to see the computer automatically added to the domain.</p>
        <img src="https://i.imgur.com/AaEw868.png" alt="Active Directory">
    </section>

   <section>
        <h2>Accessing Local Security Policy</h2>
        <p>Navigate to "Local Security Policy" through the "Tools" menu in Server Manager. Explore Group Policy Management, understanding its importance in Active Directory for centralised management of system and user configurations.</p>
        <img src="https://i.imgur.com/NNCUQjb.png" alt="Local Security Policy">
    </section>

   <section>
        <h2>Creating a Group Policy Object (GPO)</h2>
        <ol>
            <li>Right-click on the domain and select "Create a GPO in this domain and link it here."</li>
            <li>Name the GPO (e.g., Department GP), and then edit it.</li>
        </ol>
        <img src="https://i.imgur.com/FpwUtQb.png" alt="Creating GPO">
    </section>

   <section>
        <h2>Group Policy Management Editor</h2>
        <p>Understand the two main sections: "Computer Configuration" and "User Configuration."</p>
        <img src="https://i.imgur.com/YgN9mlw.png" alt="Group Policy Management Editor">
    </section>

   <section>
        <h2>Computer Configuration</h2>
        <p><strong>Definition:</strong> Computer Configuration settings in Group Policy apply to computer objects within the scope of the policy.</p>
        <p><strong>Purpose:</strong> It allows administrators to manage settings related to the computer's operating system, hardware, and security.</p>
        <p><strong>Examples of Policies:</strong></p>
        <ul>
            <li>System settings: Controls system behaviour, such as power management, device installation, and Windows Firewall configurations.</li>
            <li>Administrative Templates: Provides a wide range of settings for controlling various aspects of the computer's behaviour, including security settings, desktop configurations, and system services.</li>
            <li>Security Settings: Enforces security policies related to account policies, local policies, and security options.</li>
        </ul>
        <p><strong>Usage:</strong> Computer Configuration settings are applied when the computer starts up or when Group Policy is refreshed.</p>
    </section>

   <section>
        <h2>User Configuration</h2>
        <p><strong>Definition:</strong> User Configuration settings apply to user objects within the scope of the policy.</p>
        <p><strong>Purpose:</strong> It allows administrators to manage settings specific to individual user accounts, such as desktop appearance, application settings, and access permissions.</p>
        <p><strong>Examples of Policies:</strong></p>
        <ul>
            <li>Folder Redirection: Redirects folders like Documents, Desktop, and Favourites to network locations for easier management and backup.</li>
            <li>Software Installation: Allows administrators to deploy and manage software installations for specific user accounts.</li>
            <li>Group Policy Preferences: Provides additional configuration options, such as mapping network drives, configuring printers, and setting environment variables.</li>
        </ul>
        <p><strong>Usage:</strong> User Configuration settings are applied when a user logs on to a computer or when Group Policy is refreshed.</p>
    </section>

   <section>
        <h2>Configuring Group Policies</h2>
        <p>Under "Administrative Templates," configure policies such as enabling logoff at the Start menu and hiding desktop icons.</p>
        <img src="https://i.imgur.com/irx3ift.png" alt="Configuring Group Policies">
    </section>

   <section>
        <h2>Viewing Changes on Windows 10</h2>
        <p>Log in to the Windows 10 virtual machine and observe the applied policies, such as the removal of desktop details.</p>
        <img src="https://i.imgur.com/zYWEPuG.png" alt="Viewing Changes">
    </section>

   <section>
        <h2>Exploring Account Policies</h2>
        <p>Edit the default domain policy and navigate to "Computer Configuration" > "Windows Settings" > "Security Settings."</p>
        <img src="https://i.imgur.com/9ZbWLPn.png" alt="Account Policies">
    </section>

   <section>
        <h2>Password Policy</h2>
        <ul>
            <li>Enforce Password History: Determines how many previous passwords Windows remembers to prevent users from reusing them.</li>
            <li>Maximum Password Age: Sets the maximum number of days a password can be used before the user must change it.</li>
            <li>Minimum Password Age: Specifies the minimum number of days a password must be used before the user can change it.</li>
            <li>Minimum Password Length: Defines the minimum number of characters required for a password.</li>
            <li>Password Complexity Requirements: Ensures passwords meet specific complexity criteria, such as containing a mix of uppercase letters, lowercase letters, numbers, and special characters.</li>
            <li>Store Passwords Using Reversible Encryption: Determines whether passwords are stored in reversible encrypted format, which is generally not recommended for security reasons.</li>
        </ul>
    </section>

   <section>
        <h2>Account Lockout Policy</h2>
        <ul>
            <li>Account Lockout Threshold: Specifies the number of failed login attempts allowed before an account is locked out.</li>
            <li>Reset Account Lockout Counter After: Sets the duration after which failed login attempts are reset.</li>
            <li>Account Lockout Duration: Determines how long an account remains locked out before automatically unlocking or requiring administrator intervention.</li>
        </ul>
    </section>

   <section>
        <h2>Kerberos Policy</h2>
        <ul>
            <li>Enforce User Logon Restrictions: Ensures users must log on only from authorised computers.</li>
            <li>Maximum Lifetime For Service Ticket: Specifies the maximum time a service ticket is valid before it expires.</li>
            <li>Maximum Lifetime For User Ticket: Sets the maximum time a user's ticket-granting ticket (TGT) is valid.</li>
            <li>Maximum Lifetime For User Ticket Renewal: Determines the maximum time a user can renew a ticket.</li>
            <li>Maximum Tolerance For Computer Clock Synchronisation: Defines the maximum time difference allowed between a client and server's clocks for Kerberos authentication.</li>
        </ul>
    </section>

   <section>
        <h2>Blocking Inheritance</h2>
        <p>In Active Directory, blocking inheritance allows administrators to prevent child objects (such as Organisational Units or OUs) from inheriting Group Policy Objects (GPOs) from parent containers.</p>
        <img src="https://i.imgur.com/0nxfFMV.png" alt="Blocking Inheritance">
    </section> 
Advantages:

Granular Control: It enables administrators to apply specific policies to individual OUs without affecting the entire domain.
Customization: Allows for tailored configurations based on the unique requirements of different organizational units.
Minimizing Policy Conflicts: Helps in avoiding conflicts that may arise when conflicting policies are inherited from parent containers.
Disadvantages:

Increased Complexity: Managing multiple inheritance-blocked OUs can become complex and may require careful planning and documentation.
Potential for Overlapping Policies: Without careful planning, blocking inheritance may lead to overlapping policies, causing unintended consequences or conflicts.
Administration Overhead: Requires ongoing monitoring and maintenance to ensure consistency and avoid unintended policy interactions.
<img src="https://i.imgur.com/fBF1wmZ.png">
Enforced Settings:

Enforced settings, also known as "No Override," ensure that GPOs applied to parent containers are enforced on child objects, even if those child objects have Block Inheritance applied.

Explanation:

Forced Application: Enforced settings override any Block Inheritance settings on child objects, ensuring that policies from higher-level containers are applied.
Hierarchy Preservation: Allows administrators to maintain a consistent hierarchy of policies across the domain, ensuring critical policies are applied uniformly.
Prevention of Policy Evasion: Enforcing settings prevents administrators at lower levels from overriding important policies set at higher levels, maintaining security and compliance standards.
<img src="https://i.imgur.com/BoTkEke.png">
<h2>Exploring Default Domain Policy Settings</h2>

<p>The Default Domain Policy is a critical component of Active Directory, governing various settings that ensure the security and functionality of user accounts and computers within the domain. Below are key aspects of the Default Domain Policy:</p>

<h3>General Settings</h3>
<ul>
    <li><strong>Password Policies:</strong> These settings dictate the complexity and expiration of user passwords, helping to protect accounts from unauthorized access.</li>
    <li><strong>Account Lockout Policies:</strong> Define thresholds for failed login attempts, which can prevent brute-force attacks by locking accounts after a specified number of failed attempts.</li>
    <li><strong>Kerberos Authentication Settings:</strong> Crucial for secure authentication within the domain, these settings manage ticket lifetimes and renewal processes.</li>
</ul>

<h3>Details</h3>
<p>This section includes additional settings related to user rights assignments, such as:</p>
<ul>
    <li>Who can log on locally</li>
    <li>Who can access the computer from the network</li>
    <li>Who can shut down the system</li>
</ul>
<p>It may also encompass settings related to auditing and user profile configurations, which are essential for tracking user activity and managing user environments.</p>

<h3>Links</h3>
<p>The Links section specifies which Organizational Units (OUs) the policy is linked to. This determines which users and computers are affected by the policy. By default, the Default Domain Policy is linked to the root of the domain, applying its settings to all objects unless overridden by a more specific policy linked to a child OU.</p>

<h3>Security Filtering</h3>
<p>Security filtering allows you to specify which users or groups the policy applies to. By default, the Default Domain Policy applies to all authenticated users in the domain, but you can use security filtering to target specific groups or users as needed, enhancing security and management efficiency.</p>

<h3>Delegation</h3>
<p>Delegation settings determine which users or groups have permission to edit the policy. By default, only members of the Domain Admins group can edit the Default Domain Policy, but this permission can be delegated to other users or groups if necessary, allowing for more flexible management.</p>

<h3>Policies</h3>
<p>This section contains the actual policy settings that define the behaviour of computers and users in the domain. Examples include:</p>
<ul>
    <li>Windows Firewall settings</li>
    <li>Internet Explorer configurations</li>
    <li>Other system configurations that impact user experience and security</li>
</ul>

<p>Understanding these settings is crucial for maintaining a secure and well-organised Active Directory environment, ensuring that user accounts are protected and that policies are effectively enforced.</p>

<h2>Outro: Lessons Learned and Project Summary</h2>

<p>In this project, we embarked on a comprehensive journey to set up and configure Active Directory within a Windows Server 2019 environment, while also integrating Windows 10 client machines. Through a series of methodical steps, we gained valuable insights into the intricacies of network management, user administration, and security policy enforcement.</p>

<h3>Key Steps and Lessons Learned:</h3>

<ol>
    <li>
        <strong>Configuring Windows 10 VM Settings:</strong>
        <p>We began by accessing the settings of the Windows 10 virtual machine and selecting the appropriate ISO file for installation. This foundational step ensured that our environment was ready for the subsequent configurations.</p>
    </li>
    <li>
        <strong>Installing Windows 10:</strong>
        <p>The installation process taught us the importance of selecting the right edition and understanding the implications of product keys. By opting for a custom installation, we gained hands-on experience in managing virtual hard disks.</p>
    </li>
    <li>
        <strong>Network Setup:</strong>
        <p>Attaching the VM to a bridge adapter highlighted the significance of network connectivity in a virtualised environment. Ensuring both the Windows Server and Windows 10 machines could communicate was crucial for the success of our Active Directory setup.</p>
    </li>
    <li>
        <strong>Initial Setup and Configuration:</strong>
        <p>During the initial setup, we learned how to create user accounts and configure optional settings, emphasising the need for strong passwords and privacy considerations.</p>
    </li>
    <li>
        <strong>Obtaining IP Addresses:</strong>
        <p>Using the <code>ipconfig /all</code> command reinforced our understanding of network configurations and the importance of IP addresses in facilitating communication between devices.</p>
    </li>
    <li>
        <strong>Configuring Windows Defender Firewall:</strong>
        <p>We explored the intricacies of Windows Defender Firewall, learning how to create inbound and outbound rules to allow data connections between the Windows 10 and Windows Server 2019 machines.</p>
    </li>
    <li>
        <strong>Configuring DNS Server:</strong>
        <p>Setting the DNS server on the Windows 10 machine to the IP address of the Windows Server 2019 computer demonstrated the importance of efficient name resolution within our network.</p>
    </li>
    <li>
        <strong>Joining the Domain:</strong>
        <p>We successfully joined the Windows 10 machine to the domain, reinforcing our understanding of domain management and user authentication.</p>
    </li>
    <li>
        <strong>Viewing Computers in Active Directory:</strong>
        <p>Opening the "Computers" folder in Windows Server 2019 allowed us to verify that the newly added computer was correctly integrated into the domain.</p>
    </li>
    <li>
        <strong>Accessing Local Security Policy:</strong>
        <p>Exploring Group Policy Management through the "Tools" menu in Server Manager provided insights into centralised management of system and user configurations.</p>
    </li>
    <li>
        <strong>Creating a Group Policy Object (GPO):</strong>
        <p>We created and edited a GPO to manage settings for the domain, learning how to enforce policies effectively across user accounts and computers.</p>
    </li>
    <li>
        <strong>Configuring Group Policies:</strong>
        <p>Under "Administrative Templates," we configured various policies to manage user and computer settings, enhancing our understanding of policy application.</p>
    </li>
    <li>
        <strong>Viewing Changes on Windows 10:</strong>
        <p>Logging in to the Windows 10 VM allowed us to observe the applied policies, demonstrating the immediate impact of our configurations.</p>
    </li>
    <li>
        <strong>Exploring Account Policies:</strong>
        <p>Editing the default domain policy to configure password and account lockout policies highlighted the importance of security in user management.</p>
    </li>
    <li>
        <strong>Blocking Inheritance:</strong>
        <p>We learned about the implications of blocking inheritance in Active Directory, which allows for more granular control over policy application.</p>
    </li>
    <li>
        <strong>Enforced Settings:</strong>
        <p>Understanding enforced settings and their role in maintaining policy hierarchy was crucial for ensuring that critical policies are applied uniformly.</p>
    </li>
    <li>
        <strong>Exploring Default Domain Policy Settings:</strong>
        <p>Reviewing the default domain policy settings and their impact on user accounts and security reinforced the importance of proper policy management.</p>
    </li>
</ol>

<p>Overall, this project has equipped us with essential skills in Active Directory management, network configuration, and security policy enforcement. These competencies are invaluable in today’s IT landscape, where effective user management and security are paramount. As we continue to develop our expertise, the knowledge gained from this project will serve as a strong foundation for future endeavours in IT administration and cybersecurity.</p>

<h2>Get in Touch</h2>
<p>
    If you have any questions about this project or would like to collaborate on future endeavours, feel free to reach out to me at!
    
<img align="left" alt="ByteBanterDK | Gmail" width="22px" src="https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Fcdn-1.webcatalog.io%2Fcatalog%2Fprotonmail%2Fprotonmail-icon.png&f=1&nofb=1&ipt=6df4d08d62fc42ad07c8ae70905a4a6c79ce00471af3644e6281517111e85d03&ipo=images"/>DenisKTechnology@protonmail.com


