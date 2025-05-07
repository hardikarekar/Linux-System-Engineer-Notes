# Connect Centos7 to the Internet
* Check network adapter settings in VMware:
	* Power off the CentOS 7 VM.
	* Go to VM > Settings.
	* Select the Network Adapter.
	* Make sure 
		* It is connected.
		* Network connection set to NAT.
	* Click ok.
* Start the VM and Check Network Interfaces:
	* `ip a`
* Enable and restart the Network Interface:
	* `nmcli device status`
	* If it shows disconnected, run
		* `nmcli connection show`
	* 
