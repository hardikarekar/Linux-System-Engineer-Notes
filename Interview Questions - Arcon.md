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

* Command to identify hostname of your own system.
	* `hostname`
	* `uname -n`

* `netstat`: Display network status and protocol statistics

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
	* Group of connected computers (nodes) that work together as a single system to provide
		* High Availability
		* Load Balancing 
		* Redundancy

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
		* Hardware: Device drivers, plug and play setting
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
	* `3389`

* LDAP
	* Lightweight Directory Access Protocol
	* Used to access and manage directory services over a network.
	* Think of LDAP as
		* digital phonebook for your organization’s IT environment — storing usernames, passwords, email addresses, devices, groups, and more — all in a centralized database.
	* Common uses 
		* Authentication
			* Login validation for users across systems.
		* Centralized user management
			* Manage users, passwords and access in one place.
		* Organizational structure
			* Store company hierarchy (users, groups, departments)
		* App integration
			* Apps like Git, Jenkins, or JIRA use LDAP to authenticate users
	* LDAP is often used with
		* Active Directory
			* Microsoft's LDAP based directory service
		* OpenLDAP
			* Open source LDAP server for Linux

	* Default port
		* LDAP: `389`
		* LDAPS: `636`
		* Telnet: `23`
		* SSH: `22`
		* RDP: `3389`
		* MSQL: `1433`

* LDAPS
	* LDAP Secure
	* Encrypted Version of LDAP
	* Communication between the client and the LDAP server is secured using SSL/TLS
## Database:
* Difference between DDL and DML. 

| Feature         | DDL                                            | DML                                     |
| --------------- | ---------------------------------------------- | --------------------------------------- |
| Purpose         | Defines and manages structure of a database    | Manipulates data inside the objects     |
| Operations      | Create, modify, or delete tables, schemas,etc. | Insert, update, delete or fetch records |
| Common Commands | `CREATE` `ALTER` `DROP` `TRUNCATE`             | `INSERT` `UPDATE` `DELETE` `SELECT`     |
| Effect on data  | Affects schema, not the actual data            | Directly affects the data stored        |
| Auto Commit     | Yes changes are saved immediately              | No needs `COMMIT` to save changes       |
| Used By         | Database administrators / developers           | Application developers / users          |
* DDL Example
```sql
CREATE TABLE students (
  id INT,
  name VARCHAR(50)
);
```
* DML Example
```sql
INSERT INTO students (id, name) VALUES (1, 'John');
```

* Difference between alter and update

| Feature    | Alter                                         | Update                                |
| ---------- | --------------------------------------------- | ------------------------------------- |
| Purpose    | Changes the structure of a table              | Changes the data inside a table       |
| Type       | DDL (Data Definition Language)                | DML (Data Manipulation Language)      |
| Used for   | Add/remove columns, change data types, rename | Modify values in rows/records         |
| Affects    | The schema (design) of the table              | The content (data) of the table       |
| Common Use | Schema management by DBA                      | Data updates by users or applications |
Example of Alter
```sql
UPDATE employees
SET salary = 60000
WHERE id = 5;
```
* This adds a new column to the table.
Example of Update
```sql
UPDATE employees
SET salary = 60000
WHERE id = 5;
```
* This modifies the value if the `salary` column for one employee.

* Difference between drop, truncate and delete.

| Feature  | Drop                               | Truncate                                      | Delete                                  |
| -------- | ---------------------------------- | --------------------------------------------- | --------------------------------------- |
| Purpose  | Removes entire table               | Remove all rows from table                    | Remove specific rows from table         |
| Affects  | Table structure & data             | Data only (structure remains)                 | Data only (structure remains)           |
| Rollback | Not recoverable                    | May or may not be recoverable depends on DBMS | Recoverable if wrapped in a transaction |
| Speed    | Fastest (completely removes table) | Very fast (no row-by-row logging)             | Slow (logs each row deletion)           |
| Type     | DDL                                | DDL                                           | DML                                     |
* `DROP`
	* `DROP TABLE employees;`
		* Deletes the entire `employees` table (data + structure)
* `TRUNCATE`
	* `TRUNCATE TABLE employees;`
		* Deletes all records but keeps the table structure
* `DELETE`
	* `DELETE FROM employees WHERE department = 'HR';`
		* Deletes only the HR employees.

* Default port for MSSQL and MySQL.
	* Microsoft SQL Server 
		* Default Port: `1433`
		* Used for client connections to SQL server
	* MySQL
		* Default port: `3306`
		* Used for client connections to MySQL

* Steps to take DB backup under SSMS. 
-SSMS query to take DB backup.