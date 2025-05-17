* Public Ip and Private IP

| Private Ip                                | Public Ip                                        |
| ----------------------------------------- | ------------------------------------------------ |
| Used within private/local network (LAN)   | Globally unique IP address assigned by your ISP  |
| Cannot be routed on the internet directly | Used to communicate with devices on the internet |
* Private ip address range

| Class   | Ip range                      | CIDR           | Subnet Mask |
| ------- | ----------------------------- | -------------- | ----------- |
| Class A | 10.0.0 - 10.255.255.255       | 10.0.0.0/8     | 255.0.0     |
| Class B | 172.16.0 - 172.31.255.255     | 172.16.0/12    | 255.240.0   |
| Class C | 192.168.0.0 - 192.168.255.255 | 192.168.0.0/16 | 255.255.0.0 |
* RHEL 6 uses `network` service
	* Edit config file
		* `vi /etc/sysconfig/network-scripts/ifcfg-eth0`
	* Static ip config
```ini
DEVICE=eth0
BOOTPROTO=static
ONBOOT=yes
IPADDR=192.168.1.100
NETMASK=255.255.255.0
GATEWAY=192.168.1.1
DNS1=8.8.8.8
```
* 
	* Restart network
		* `service network restart`
* Assign static IP to `ens-33`
	* Edit the interface config file
		* `sudo vi /etc/sysconfig/network-scripts/ifcfg-ens33`
	* Use the following example configuration 
```ini
TYPE="Ethernet"
PROXY_METHOD="none"
BROWSER_ONLY="no"
BOOTPROTO="static"
DEFROUTE="yes"
IPV4_FAILURE_FATAL="no"
IPV6INIT="yes"
IPV6_AUTOCONF="yes"
IPV6_DEFROUTE="yes"
IPV6_FAILURE_FATAL="no"
IPV6_ADDR_GEN_MODE="stable-privacy"
NAME="ens33"
UUID="fe86671c-53b3-4a86-8997-3f8bb5c140cf"
DEVICE="ens33"
ONBOOT="yes"
ZONE=public
```
* 
	* Restart the network service
		* `sudo systemctl restart network`
	* Verify new ip
		* `ip addr show ens33`
