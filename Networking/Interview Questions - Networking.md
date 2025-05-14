#interview
 * What is network?
	 * System of interconnected devices (such as computers, servers, switches, routers and more) that communicate with each other to share resources, data and services.
	 * Types of networks
		 * LAN (Local Area Network)
			 * Covers a small area like a home, office or building.
		* WAN (Wide Area Network)
			* Spans large geographical areas like the internet.
		* MAN (Metropolitan Area Network)
			* Covers a city or large campus.
		* PAN (Personal Area Network)
			* Used for personal devices within a small range e.g., Bluetooth.
	* Key Components
		* Nodes 
			* Devices like computers or printers.
		* Links
			* Wired or wireless connections.
		* Protocols
			* Rules for communication e.g., TCP/IP.

* What is DHCP server?
	* DHCP server (Dynamic Host Configuration Protocol server) automatically assigns IP addresses and other network configuration settings (like [[DNS server]], [[gateway]], [[subnet mask]]) to devices (clients) on a network.
	* Why is it useful
		* Without DHCP every device would need to be manually configured with an IP address.
		* Makes network setup automatic and efficient.
	* How it works
		* DHCP Discover
			* Client sends a broadcast request to find a DHCP server.
		* DHCP offer
			* Server replies with an available IP address and configuration.
		* DHCP Request
			* Client requests to use offered IP.
		* DHCP Acknowledgement
			* Server confirms and assigns IP to client.
	* Real life example
		* When you connect your phone or laptop to a Wi-Fi, it usually gets an IP address automatically/
			* This is done by the DHCP server in the Wi-Fi router.

* What is VPN
	* VPN (Virtual Private Network) is a service or technology.
	* Creates a secure, encrypted connection over a less secure network - typically internet.
	* Purpose 
		* Privacy
			* Hides your IP address and online activity.
		* Security
			* Encrypts data so hackers can't steal information especially on public Wi-Fi.
		* Access Control
			* Allows remote users to securely connect to company's internal network.
		* Bypass Geo-restrictions
			* Lets users access websites or service blocked in certain countries.
	* How it works
		* You connect to a VPN server.
		* Your internet traffic is encrypted and sent through a secure tunnel.
		* The website or service sees the VPN server's IP, not your real one.
	* Real Life Example
		* If you are using public Wi-Fi at a café and log into your bank account using a VPN, your data is much safer from hackers.
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
* Basic topology
	* Bus topology
		* Structure
			* All devices are connected to a single central cable (bus).
		* Pros
			* Easy to setup, cost effective.
		* Cons
			* If the main cable fails the entire system goes down.
	* Star topology
		* Structure
			* All devices connect to a central device (like a switch or hub).
		* Pros
			* Easy to manage and expand; one device failure doesn't affect others.
		* Cons
			* If the central hub fails the whole network stops.
	* Ring topology
		* Structure
			* Each device is connected to two other devices, forming a ring.
		* Pros
			* Data travels in one direction, reducing collisions.
		* Cons
			* A single failure can disrupt the entire network unless a dual ring is used.
	* Mesh topology
		* Structure
			* Every device connects to every other device.
		* Pros
			* High reliability and fault tolerance.
		* Cons
			* Expensive an complex setup.
	* Tree topology
		* Structure
			* A combination of star and bus topologies.
			* Devices are connected in a hierarchy.
		* Pros
			* Scalable and easy to manage in large networks.
		* Cons
			* If the root node fails, the whole network is affected.
	* Hybrid topology
		* Structure
			* Mix of two or more different topologies.
		* Pros
			* Flexible and scalable.
		* Cons
			* Can be complex and expensive.
* Basic IP configuration commands
	* Windows
		* `ipconfig`
			* Shows ip address, subnet mask, gateway and more.
		* `ipconfig /all`
			* Displays full network details, including MAC address and DNS.
		* `ipconfig /release`
			* Releases the current IP address.
		* `ipconfig /renew`
			* Requests a new IP address from DHCP server.
		* `ping <IP or hostname>`
			* Tests connectivity to another device or website.
		* `tracert <hostname>`
			* Traces the path data takes to a host.
		* `netstat`
			* Shows active connection and ports.
		* `nslookup <domain>`
			* Checks DNS resolution for a domain.
	* For Linux
		* `ifconfig`
			* Shows or configures network interfaces (older systems).
		* `ip a` or `ip addr`
			* Shows IP address info (preferred over `ifconfig`).
		* `ip route`
			* Displays routing table.
		* `ping <IP or hostname>`
			* Tests network connectivity.
		* `traceroute <hostname>`
			* Traces the path to a host (like `tracert` in Windows).
		* `nslookup <domain>`
			* DNS lookup.
		* `dig <domain>`
			* Advanced DNS query tool.
		* `nmcli`
				* Network Manager CLI for managing connections (modern Linux distros).
* OSI Model

Final 
* IP Address
	* IP (Internet Protocol) address is a unique identifier assigned to every device connected to a network. 
	* It helps devices locate and communicate with each other.
	* Types
		* IPv4
			* 32-bit
			* `192.168.1.10`
		* IPv6
			* 128-bit
			* `2001:0db8:85a3::8a2e:0370:733`|
* Host
	* A host is any device connected to a network that has an IP address and can send or receive data.

* Subnetting
	* Process of dividing a large network into smaller, more manageable subnetworks.
	*  Subnet masks define how an IP address is split between the network and the hosts.
	* Each subnet has its own 
		* network address
		* broadcast address
		* range of usable host addresses.
	* Subnetting allows better control of traffic and **reduces congestion** by keeping local traffic within subnets.

* OSI Model
	* **Application Layer** (Layer 7): It provides services directly to the user, such as email, web browsing, and file transfers.
	* **Presentation Layer** (Layer 6): It translates, encrypts, and compresses data for the application layer.
	* **Session Layer** (Layer 5): It manages sessions or connections between applications, keeping communication organized.
	* **Transport Layer** (Layer 4): It ensures reliable data transfer using protocols like TCP and UDP, managing error checking and flow control.
	* **Network Layer** (Layer 3): It handles routing and addressing, determining how data travels between devices across different networks.
	* **Data Link Layer** (Layer 2): It organizes data into frames and handles error detection and MAC addressing for local delivery.
	* **Physical Layer** (Layer 1): It transmits raw bits over physical media like cables, radio waves, or fiber optics.

* Networking Devices
	* Router
		* **Function:** Routes data between different networks (e.g., local network to the internet).
		* **Role:** Connects multiple networks, typically between local area networks (LANs) and wide area networks (WANs).
		* **Example:** Home router, enterprise routers.
	* Switch
		* **Function:** Connects devices within the same network (LAN) and forwards data using MAC addresses.
		* **Role:** Operates at the Data Link layer (Layer 2) to manage traffic within a single network.
		* **Example:** Connecting computers, printers, and servers in an office.
	* Hub
		* **Function:** Broadcasts data to all devices in a network.
		* **Role:** A simple, older networking device that does not differentiate between devices (unlike switches).
		* **Example:** Used for basic networking in small, unmanaged environments.
	* Modem
		* **Function:** Broadcasts data to all devices in a network.
		* **Role:** A simple, older networking device that does not differentiate between devices (unlike switches).
		* **Example:** Used for basic networking in small, unmanaged environments.
	* Access Point (AP)
		* **Function:** Provides wireless access to a wired network.
		* **Role:** Enables Wi-Fi connectivity for devices to connect to a wired LAN.
		* **Example:** Wi-Fi routers or wireless access points in an office or home.
	* Firewall
		* **Function:** Protects networks by filtering incoming and outgoing traffic based on predefined security rules.
		* **Role:** Acts as a security device, monitoring and controlling network traffic.
		* **Example:** Hardware or software firewalls deployed at the network perimeter or between network segments. 
	* Bridge
		* Function: Connects two or more network segments and operates at the Data Link layer (Layer 2).
		* **Role:** Reduces network traffic by dividing the network into segments and filtering data.
		* **Example:** Connecting two LANs that use the same protocol.
	* Gateway
		* **Function:** Acts as an entry and exit point for data between different networks, often with different protocols.
		* **Role:** Operates at Layer 3 and above, translating data between different network architectures.
		* **Example:** Translating between an internal network and the internet.
	* Repeater
		* **Function:** Regenerates and amplifies signals to extend the range of a network.
		* **Role:** Used to boost network signals over long distances, ensuring data integrity.
		* **Example:** Extending Wi-Fi or wired network coverage in large areas.
* DHCP
	* DHCP server (Dynamic Host Configuration Protocol server) 
	* Automatically assigns 
	* IP addresses
	* other network configuration settings like 
		* DNS server
		* Gateway, 
		* Subnet Mask to devices (clients) on a network.
	* Why is it useful
		* Without DHCP every device would need to be manually configured with an IP address.
		* Makes network setup automatic and efficient.
	* How it works
		* DHCP Discover
			* Client sends a broadcast request to find a DHCP server.
		* DHCP offer
			* Server replies with an available IP address and configuration.
		* DHCP Request
			* Client requests to use offered IP.
		* DHCP Acknowledgement
			* Server confirms and assigns IP to client.
	* Real life example
		* When you connect your phone or laptop to a Wi-Fi, it usually gets an IP address automatically.
			* This is done by the DHCP server in the Wi-Fi router.
* Static IP
	* A **static IP** is an IP address that is manually assigned to a device and does not change over time. 
	* Static IPs ensure a consistent address for the device. 
	* They are commonly used for 
		* **servers**
		* **network printers**,
		* **routers** 
			* where consistent access is required. 
		* Setting a static IP involves configuring the network settings on the device or within the network's DHCP server. 
		* Static IPs are ideal for **port forwarding**, **remote access**, and **network management** since their address remains fixed.
* DNS Server
	* **DNS server** (Domain Name System server) translates human-readable domain names like www.example.com into IP addresses that computers can understand. 
	* It acts as a directory that maps domain names to their corresponding **IP addresses**, enabling devices to communicate over the internet. 
	* When you enter a website's name in your browser, a DNS query is made to resolve the domain to an IP address. 
	* There are different types of DNS servers, including 
		* **recursive** (which queries other servers for answers)  
		* **authoritative** (which holds the actual records for domains). 
* VPN 
	* Creates a secure, encrypted connection over the internet between your device and a remote server. 
	* It hides your **IP address** and encrypts your internet traffic, protecting your data from hackers and surveillance. 
	* VPNs are commonly used for **privacy**, accessing **geo-restricted content**, and connecting to **corporate networks remotely**. 
	* By masking your real location, a VPN can make it appear as if you're browsing from another country.
	* It is a crucial tool for both personal security and secure business communication over public networks.

* Firewall
	* A **firewall** is a security system that monitors and controls incoming and outgoing network traffic based on predefined rules. 
	* It acts as a barrier between a trusted internal network and untrusted external networks, such as the internet. 
	* Firewalls can be hardware devices, software applications, or a combination of both. 
	* They help prevent **unauthorized access**, **malware**, and **cyberattacks** by filtering traffic and blocking suspicious connections. 
	* Firewalls are essential in both personal devices and enterprise networks to maintain data security and network integrity.
* SSL
	* **SSL (Secure Sockets Layer)** is a security protocol that encrypts data transmitted between a user's browser and a web server. 
	* It ensures that sensitive information like passwords, credit card numbers, and personal details remain private and protected from eavesdropping. Websites using SSL have URLs that start with **https://** instead of **http://**, and often show a padlock icon in the browser. 
	* SSL uses a system of **public and private keys** to securely exchange data over the internet. 
* TCP/IP
	* **TCP/IP (Transmission Control Protocol/Internet Protocol)** is the foundational communication protocol suite for the internet and most networks. **IP** handles addressing and routing, ensuring data packets reach the correct destination, while **TCP** ensures reliable delivery by managing data flow, error checking, and retransmission. TCP/IP breaks data into packets, sends them across networks, and reassembles them at the receiving end. It supports various protocols like HTTP, FTP, SMTP, and DNS, enabling different types of communication. TCP/IP's layered architecture (Application, Transport, Internet, and Network Access) makes it scalable, robust, and adaptable to different technologies.
* UDP
	* **UDP (User Datagram Protocol)** is a communication protocol used for sending data over a network without establishing a connection. It is **faster** than TCP because it does **not guarantee delivery**, ordering, or error correction of packets. UDP is ideal for real-time applications like **video streaming**, **online gaming**, and **VoIP**, where speed is more important than reliability. Each UDP packet, called a **datagram**, is sent independently and may arrive out of order or not at all. Because of its lightweight nature, UDP is commonly used where low latency is critical.
* ncpa.cpl
* sysdm.cpl
* |   |   |
|---|---|
`free -h`: Shows memory usage in human-readable format


|          |                                            |
| -------- | ------------------------------------------ |
| `vmstat` | Displays memory, CPU, and system processes |


Change ip 
`sudo ip addr add 192.168.1.100/24 dev eth0` 
`sudo ip route add default via 192.168.1.1`
Cron fields
```scss
* * * * * command_to_run
│ │ │ │ │
│ │ │ │ └───── Day of the week (0 - 7) (Sunday=0 or 7)
│ │ │ └──────── Month (1 - 12)
│ │ └──────────── Day of the month (1 - 31)
│ └──────────────── Hour (0 - 23)
└──────────────────── Minute (0 - 59)
```

