#interview 
* `ping`
	* Used to test connectivity between your computer and another device over a network.
	* `ping [hostname or IP address]`
	* Example:
		* `ping google.com`
	* Common Options:
		* `-t`
			* Ping the target until stopped.
		* `-n [count]`
			* Send a specific number of pings.
		* `-l [size]`
			* Set the size of the packet in bytes
		* `-4`
			* Force using IPv4.
		* `-6`
			* Force using IPv6.

* `netstat`
	* Used to display active network connections, open ports, routing tables, and network interface statistics.
	* Basic syntax:
		* `netstat`
	* Common Options:
		* `-a`
			* Show all connections and listening ports.
		* `-n`
			* Show addresses and ports numerically.
		* `-o`
			* Show PID (Process ID) of the owning process for each connection.
		* `-b`
			* Show the executable that created each connection.
		* `-e`
			* Show Ethernet statistics (like bytes sent/received).
		* `-r`
			* Display the routing table.
		* `-s`
			* Show statistics for each protocol (TCP, UDP, ICMP, etc.)

* `arp`
	* Used to view and manage the Address Resolution Protocol (ARP) cache, which maps IP address to MAC address on your local network.
	* Basic Syntax:
		* `arp [options]`
	* Common Options:
		* `-a`
			* Display current ARP table for all interfaces.
		* `-a [ip address]`
			* Display ARP entry for  specific IP Address
		* `-g`
			* Same as `-a`.
		* `-d [ip address]`
			* Delete an ARP entry for a specific IP.
		* `-s [ip address] [mac address]`
			* Manually add a static ARP entry

* `pathping`
	* Combination of `ping` and `tracert`.
	* Shows the path packets take to a destination.
	* Useful for diagnosing 
		* network latency 
		* packet loss issues
	* Example
		* `pathping google.com`
			* traces route to `google.com`
			* pings each hop
			* provides loss and latency statistics.
```swift
Computing statistics for 200 seconds...
Source to Here   This Node/Link
Hop RTT   Lost/Sent = Pct  Lost/Sent = Pct  Address
1    1ms  0/100 =  0%       0/100 =  0%      192.168.1.1
2   10ms  0/100 =  0%       0/100 =  0%      10.0.0.1
3   30ms  5/100 =  5%       5/100 =  5%      isp.example.net
```
	* Hop: Each router the packet passes through
	* RTT: Round trip time to that hop
	* Lost/Sent: Packet loss details
	* Helps pinpoint where packet loss or delay is happening.

* `tracert`
	* Used to trace path that packets take from your computer to target host.
	* Shows each hop along the way.
	* Basic Syntax:
		* `tracert [hostname or ip address]`
	* Example
		* `tracert google.com`
```swift
Tracing route to google.com [142.251.42.14]
over a maximum of 30 hops:

  1     2 ms     1 ms     2 ms  192.168.0.1
  2     3 ms     3 ms     3 ms  172.25.0.162
  3     *        4 ms     *     172.25.0.161
  4     *        *        *     Request timed out.
  5     3 ms     4 ms     4 ms  22.188.100.175.mipl.com [175.100.188.22]
  6     4 ms     4 ms     4 ms  172.253.69.227
  7     4 ms     4 ms     3 ms  209.85.248.61
  8     3 ms     3 ms     3 ms  bom12s19-in-f14.1e100.net [142.251.42.14]

Trace complete.
```
	* Each line is a router along the route to the destination.
	* Shows 3 ping times per hop.
	* Asterisk means no response.

* `tracert` vs `pathping`
	* `tracert` shows the route only
	* `pathping` shows route + packet loss/latency

* `nslookup`
	* Used to query DNS servers and find out IP addresses for domain names.
	* Basic Syntax:
		* `nslookup [hostname or ip address]`
	* Find ip address of a domain
		* `nslookup google.com`
	* Find reverse lookup (find domain from IP)
		* `nslookup 8.8.8.8`
	* Advanced Usage
		* Type `nslookup` to enter into interactive mode
			* `set type=MX`
				* `google.com`
					* This shows the Mail Exchange (MX) records for Gmail.

* `ipconfig`
	* Used to view and manage IP configuration details of your network interfaces.
	* Especially helpful for troubleshooting network issues.
	* Basic Syntax:
		* `ipconfig [options]`
	* Display basic IP information
		* `ipconfig`
			* Shows IP address, subnet mask and default gateway for each adapter.
		* `ipconfig /all`
			* Display detailed information.
			* Includes MAC address, DHCP status, DNS servers, lease times, etc.
	* Network reset and troubleshooting options
		* `ipconfig /release`
			* Releases current IP address (used with DHCP)
		* `ipconfig /renew`
			* Requests new IP address from DHCP server
		* `ipconfig /flushdns`
			* Clears DNS cache
		* `ipconfig /displaydns`
			* Show contents of the DNS cache
		* `ipconfig /registerdns`
			* Renews DHCP lease and re-registers DNS records (needs admin)

* `route`
	* Used to view and manage the IP routing table, which determines how computer sends packets to different networks.
	* Common Commands
		* `route print`
			* Displays the current routing table
		* `route add 192.168.2.0 mask 255.255.255.0 192.168.1.1`
			* Adds a static route
		* `route -p add 10.10.10.0 mask 255.255.255.0 192.168.1.1`
			* Add a persistent route
		* `route delete 192.168.2.0`
			* Delete a route

* `hostname`
	* Used to display name of computer (host) on the network.
	* Syntax
		* `hostname`
	* Change hostname
		* `Rename-Computer -NewName "NewPCName" -Restart`

* `getmac`
	* Used to display MAC address of your computer's network adapters.
	* Basic Syntax
		* `getmac [options]`
	* Common Options
		* `getmac /v /fo list`
			* `/v`: Verbose
			* `/fo`: Formats output as a list for easier reading

* `nbtstat`
	* Used to troubleshoot NetBIOS over TCP/IP.
	* Displays NetBIOS name, tables and network connections for local and remote computers.
	* Basic Syntax
		* `nbtstat [options]`
	* Common Options
		* `nbtstat -n`
			* Shows NetBIOS names registered locally on the computer
		* `nbtstat -a [hostname]`
			* Displays NetBIOS table for a remote system using its name
		* `nbtstat -A [ip address]`
			* Same as `-a`, but uses IP address instead of name
		* `nbtstat -c`
			* Shows NetBIOS name cache 

* `tasklist`
	* Displays list of all running processes on your system, including
		* process IDs (PID)
		* memory usage
		* user that owns them
	* Basic Syntax
		* `tasklist [options]`

* `taskkill`
	* Used to terminate running processes by their PID or image name.
	* Basic Syntax
		* `taskkill /pid [PID}`
		* `taskkill /im [image name]`
	* Kill a process
		* `taskkill /pid 1234`
	* Force kill
		* `taskkill /pid 1234 /f`

* `systeminfo`
	* Displays detailed information about computer's hardware, operating system, network and update history.
	* Syntax
		* `systeminfo`

* `netsh`
	* Allows to display and modify the network configuration of a computer.
	* It is powerful for managing network settings like
		* IP addresses
		* firewall
		* rules
		* port forwarding
		* wireless networks
	* Common Uses
		* View network configuration
			* `netsh interface ip show config`
		* Set static ip address
			* `netsh interface ip set address name="Ethernet" static 192.168.1.100 255.255.255.0 192.168.1.1`
* `net view`
	* Used to display a set of network resources, such as shared computers and devices on your local network (LAN).
	* Common Usage
		* `net view`
			* View all devices on the network
		* `net view \\ComputerName`
			* View shared resources on a specific computer
		* `net view /domain:YourDomainName`
			* View devices in a specific domain

* msinfo32
