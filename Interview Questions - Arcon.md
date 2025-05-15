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
	* It hides your **IP address** and encrypts your internet traffic, protecting your data from hackers and surveillance. 
	* VPNs are commonly used for **privacy**, accessing **geo-restricted content**, and connecting to **corporate networks remotely**. 
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


Command to identify hostname of your own system. 

Operating systems: Difference between Desktop OS and Server OS. 
(1)Linux: 
-basic commands like chmod, ls -la, man, sudo, rm, mv, pwd, cd, touch, mkdir, chown 
-what is telnet 
-default port for ssh and telnet 
-command to change the password of the user 

(2)Windows: 
-What is Active Directory? 
-What is a cluster? 
-What is the registry? 
-What is RDP? 
Default port for RDP. 

Database: 
-Difference between DDL and DML. 
-Difference between alter and update. 
-Difference between drop, truncate and delete. 
-Default port for MSSQL and MySQL. 
-Steps to take DB backup under SSMS. 
-SSMS query to take DB backup.