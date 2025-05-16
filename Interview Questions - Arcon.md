#interview 
## Networking: 
* Difference between http and https?
	* HTTP and HTTPs are both web protocols used to transfer data between a browser and a server.
	* HTTP
		* Hyper Text Transfer Protocol
		* Transmits data in plain text making it vulnerable to eavesdropping and tampering.
	* HTTPS
		* Hyper Text Transfer Protocol Secure
		* Encrypts data using SSL/TLS ensuring that even if intercepted, the data remains unreadable.
		* This encryption provides a layer of security making it more difficult for unauthorized parties to access sensitive information.

* Why https is more secured than http ? Default ports for http and https.
	* HTTPS uses encryption to protect data during transmission.
	* HTTPS uses TLS/SSL (Transport Layer Security / Secure Socket Layer) protocols to encrypt data, making it unreadable to eavesdroppers.

* What is firewall? 
	* Is a security system
		* either hardware, software or both
	* Monitors and controls incoming and outgoing network traffic
		* based on predefined security rules.
	* Purpose
		* Protects your network from unauthorized access.
		* Blocks malicious traffic like viruses, hackers or unwanted connections.
		* Allows only safe, approved communication.
	* Types
		* Network Firewall
			* Installed on routers or gateways to protect an entire network.
		* Host-based Firewall
			* Installed on individual computers to protect that device.
		* Hardware Firewall
			* A physical device that filters traffic.
		* Software firewall
			* A program running on a system.
	* How it works
		* A firewall checks data packets coming in or going out and decides to
			* Allow if traffic is safe
			*  Block if it's suspicious or not allowed by the rules.
	* Example
		* If hacker tries to access your system through an open port, the firewall can block that connection, keeping your device safe.

* What is VPN?
	* Creates a secure, encrypted connection over the internet between your device and a remote server. 
	* It hides your IP address and encrypts your internet traffic, protecting your data from hackers and surveillance. 
	* VPNs are commonly used for privacy, accessing geo-restricted content, and connecting to corporate networks remotely. 
	* By masking your real location, a VPN can make it appear as if you're browsing from another country.
	* It is a crucial tool for both personal security and secure business communication over public networks.

* What is Load Balancer?
	* A load balancer is a system or a device that distributes incoming network traffic across multiple servers to ensure no single server is overwhelmed.
	* Why use a load balancer
		* Improves performance
			* Distributes traffic efficiently
		* Ensures high availability
			* If one server fails, traffic shifts to healthy ones.
		* Scalability
			* Easily add more server as traffic grows
		* Better use experience
			* Faster and more reliable services
	* Types of load balancing
		* Round Robin
			* Traffic sent to each server in a fixed rotation
		* Least Connections
			* New traffic goes to the server with the fewest current connections
		* IP Hash
			* Based on the user's IP address to ensure they hit the same server
	* Types of load balancers
		* Hardware Load Balancers
			* Physical devices (eg. F5, Cisco)
		* Software Load Balancers
			* Programs like NGINX, HAProxy
		* Cloud Load Balancers
			* Managed by cloud providers
			* eg. AWS ELB, Azure Load Balancer, Google Cloud Load Balancing

* Command to identify ip address of your own system. 
	* For Linux
		* `ip a`
	* For windows
		* `ipconfig`
	* 

* Command to identify hostname of your own system.
	* `hostname`
	* `uname -n`

* Operating systems: Difference between Desktop OS and Server OS. 

| Feature                | Desktop OS                                | Server OS                                                         |
| ---------------------- | ----------------------------------------- | ----------------------------------------------------------------- |
| Purpose                | Designed for eveyday personal use         | Designed to provide services to other computers                   |
| Examples               | Windows 10/11, Ubuntu Desktop, macOS      | Windows Server, Ubuntu Server, Red Hat Enterprise Linux           |
| User Interface         | Has a full GUI                            | Often minimal or no GUI to save resources                         |
| Resource Usage         | Optimized for graphics and multitasking   | Optimized for performance, netwroking and stability               |
| Applications           | Runs apps like browsers, MS Office, games | Runs services like                                                |
| User Access            | One or few users at a time                | Handles many users/requests simultaneously                        |
| Security & Permissions | Less strict                               | Stricter access controls and user management                      |
| Hardware Requirements  | Lower hardware needed                     | Needs higher RAM, CPU, storage depending on load                  |
| Updates                | Frequent, sometimes automatic             | Controlled with a focus on stability and uptime                   |
| Networking features    | Basic networking tools                    | Advance networking features (load balancing, remote access, etc.) |
## Linux: 
* **basic commands**
	* `chmod` 
		* Used to change file permission for (read, write, execute) for users, group and others.
		* Basic syntax
			* `chmod [permission] [filename]`
		* Numeric (Octal) Mode
			* Read (r): `4`
			* Write (w): `2`
			* Execute (x): `1`
			* Example
				* `chmod 777 file`
		* Symbolic Mode
			* `chmod u+x file`: Add execute to user
			* `chmod go-w file`: Remove write from group and others
			* `chmod u=r file`: Set user permission to read only
		* For directories
			* To make a directory accessible
				* `chmod 755 my_folder`
	* `ls -la`
		* `ls`: List files and directories
		* `-l`: Long listing format
		* `-a`: Show all files, including hidden ones
	* `man`
		* `man` stands for manual.
		* Displays manual (documentation) for Linux commands, programs or configuration files.
		* Example
			* `man ls`
	* `sudo`
		* superuser do
		* Allows regular user to run commands using root privileges - temporarily and securely.
		* Basic syntax
			* `sudo [command]`
		* Example
			* `sudo apt update`
				* This runs `apt update` command as root.
	* `rm`
		* Used to remove files and directories.
		* Once deleted with `rm`, files are permanently deleted.
		* Basic syntax
			* `rm [options] file`
		* Example
			* `rm file`
			* `rm -r file`
	* `mv`
		* Used to 
			* Move files or directories from one location to another.
			* Rename files or directories.
			* Basic Syntax
				* `mv [options] source target`
			* Example
				* Rename a file
					* `mv oldname newname`
				* Move a file to another directory
					* `mv file.txt /home/user/Documents/`
				* Rename and move at the same time
					* `mv oldname /home/user/Documents/newname`
				* Move an entire folder
					* `mv folder1 /home/user/Documents/`
	* `pwd`
		* stands for Present Working Directory
		* Displays full path for current working directory you are in.
		* Usage
			* `pwd`
	* `cd`
		* Change working directory
		* Used to move between directories in the filesystem.
		* Basic Syntax
			* `cd [directory_path]`
	* `touch`
		* Used to create new empty files
		* Update access and modification time of existing files
		* Basic Syntax
			* `touch filename`
	* `mkdir`
		* stands for "make directory"
		* used to create new directories in filesystem
		* Basic syntax
			* `mkdir [options] directoryname`
	* `chown`
		* stands for change ownership
		* used to change owner or group of file or directory
		* Basic Syntax
			* `chown [options] [owner]:[group] filename`
* what is telnet 
	* TELecommunication NETwork
	* is a network protocol and command line tool used to
		* Remotely access another computer or network device
		* Send command to a remote system using TCP/IP.
	* What it does
		* Creates a virtual terminal connection over a network.
		* It's used to login to a remote machine and run commands as if you were sitting at that computer.
	* Basic Usage
		* `telnet [hostname or IP] [port]`
	* Example
		* `telnet 192.168.1.10 23`
* default port for ssh and telnet
	* ssh: `22`
	* telnet: `23`

* command to change the password of the user 
	* To change your own password
		* `passwd`
	* To change password of another user
		* `sudo passwd username`

## Windows: 
* What is Active Directory?
	* Active Directory (AD) is a directory service developed by Microsoft for Windows Domain Networks.
	* It is used to centrally manage users, computers, and other resources in an organization.
	* Key Functions of AD
		* User and Group Management
			* Manage user accounts, passwords and group permissions
		* Authentication
			* Handles login, password verification, and access control
		* Authorization
			* Grants or denies access to resources (files, printers, apps, etc.)
		* Centralized Policy
			* Apply system settings and restrictions using Group Policy
		* Resource Organization
			* Organize users, computers, printers in a structured way
	* Commonly used in
		* Businesses
		* Schools
		* Government Organizations
	* Key Components
		* Domain
			* Logical Group of objects (users, computers, etc.)
		* Domain Controller (DC)
			* Server that runs AD and manages authentication
		* OU (Organizational Unit)
			* Container to organize users/computers by department or function
		* Group Policy
			* Tool to control user and computer settings centrally
		* LDAP
			* Protocol used for querying AD directory data
	* Use Case
		* When an employee logs in to a work computer, AD
			* verifies their username and password
			* applies group policies
			* gives access to shared folders, printers and email

* What is a cluster?
	* 

* What is the registry? 
	* Windows registry is a centralized database that stores
		* Configuration Settings
		* System Information
		* User Preferences
		* Software and Hardware Details
	* It is essential for windows operating system to run properly.
	* Registry stores data for
		* Operating System: Boot settings, system behavior
		* Installed Software: License keys, paths, settings
		* User Profiles: Desktop background, screen saver, themes
		* Hardware: Device drivers, plug and play settings
	* Registry Structure
		* Organized in a tree-like structure, similar to folders and files.
		* Top-level sections (called "hives"):
			* `HKEY_LOCAL_MACHINE (HKLM)`
				* System wide settings and hardware config
			* `HKEY_CURRENT_USER (HKCU)`
				* Settings for currently logged in user
			* `HKEY_CLASSES_ROOT (HKCR)`
				* File associations and COM object info 
			* `HKEY_USERS`
				* Settings for all users in the system
			* `HKEY_CURRENT_CONFIG (HKCC)`
				* Current hardware profile settings
		* Accessing the registry
			* Press `Win+r`
			* `regedit`

* What is RDP? 
	* Remote Desktop Protocol
	* It is a Microsoft protocol 
	* Allows to remotely access and control another Windows computer over a network.
	* What does RDP let you do?
		* View and control remote desktop screen
		* Access files, programs, and system settings
		* Use remote PC as if you were sitting in front of it
	* Common Use Cases
		* Remote Support
		* Work From Home
		* Server Administration

* Default port for RDP
	* 
Database: 
-Difference between DDL and DML. 
-Difference between alter and update. 
-Difference between drop, truncate and delete. 
-Default port for MSSQL and MySQL. 
-Steps to take DB backup under SSMS. 
-SSMS query to take DB backup.