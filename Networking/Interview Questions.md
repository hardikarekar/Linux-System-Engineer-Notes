#networking 
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