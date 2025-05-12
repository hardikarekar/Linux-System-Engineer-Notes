#interview
* What is difference between Linux and Unix
	* Origin
		* Unix
			* Developed in the 1970s at AT&T's Bell Labs.
		* Linux
			* Created by Linux Torvalds in 1991 as a free, open source clone if Unix, inspired by the Unix like system MINIX.
	* Licensing
		* Unix
			* Proprietary (commercial), owned by different vendors like IMB (AIX), Oracle (Solaris), HP (HP-UX).
		* Linux
			* Open source and free to use under the GNU General Public License (GPL).
		* Availability
			* Unix
				* Mainly used in servers, mainframes, and high-end enterprise systems.
			* Linux
				* Used in servers, desktops, smartphones (android), embedded systems and more.
			* System Variants
				* Unix
					* Multiple vendor-specific variants:
						* AIX (IBM)
						* Solaris (Oracle)
						* HP-UX (HP)
				* Linux
					* Many distributions (distros)
						* Ubuntu 
						* Red Hat
						* CentOS
						* Arch
						* Debian
			* User Base
				* Unix
					* Mostly used by large enterprises, data centers and academia.
				* Linux
					* Used by individuals, developers, enterprises and cloud platforms.
			* Development Community
				* Unix
					* Developed and maintained by commercial vendors.
				* Linux
					* Developed by worldwide community of developers and organizations.
			* Compatibility
				* Unix
					* Not as portable, usually tied to a specific hardware.
				* Linux
					* Highly portable, runs on almost every hardware platform.
* Who invented Linux
	* Linux was invented by Linus Torvalds, a Finnish computer science student, in 1991.
	* Key Facts
		* Linus was studying at the University of Helsinki. 
		* He was inspired by a Unix like teaching OS called Minix but found it limited.
		* So he decide to build his own free and open source operating system kernel.
		* He announced it on a newsgroup on August 25,1991 inviting others to contribute.
	* Quote from Linus's announcement
		* *I’m doing a (free) operating system (just a hobby, won’t be big and professional like GNU)”*
	* Linux is the kernel, not the entire OS. 
	* Most Linux systems today combine the Linux kernel with GNU tools, forming what's technically called GNU/Linux. 
* What is Grep and Top
	* `grep`
		* Global Regular Expression Print
		* Searches for pattern /text in files or output.
		* Example
			* `grep "error" logfile.txt`
				* Finds all lines containing the word "error" in `logfile.txt`
		* Common Options
			* `-i`: ignore case
			* `-r`: Recursively search in directories.
			* `-n`: Show line numbers
	* `top`
		* Task Manager for Linux
		* Syntax
			* `top`
				* You'll see a live updating dashboard similar to Task Manager in Windows
		* What it shows
			* System uptime
			* Load average
			* CPU usage
			* RAM and swap usage
			* List of processes with PID, user, CPU/mem usage, etc.
		* To quit
			* `q`
		* Popular alternatives
			* `htop`
				* More user friendly and colorized.
* Difference between Rpm and Yum
	* `rpm`
		* Red Hat Packet Manager
			* Low level tool for installing, querying and removing individual `.rpm` packages.
			* Does not handle dependencies automatically .
			* Basic usages
				* Install a package
					* `rpm -ivh package.rpm`
				* Remove a package
					* `rpm -e package_name`
				* List all installed packages
					* `rpm -qa`
				* List files in a package
					* `rpm -ql package_name`
			* `yum`
				* Yellowdog Update Modifier
				* High level package manager build on top of rpm.
				* Automatically resolves dependencies.
				* Connects to online or local repositories to install/update packages.
				* Basic Usage
					* Install a package
						* `yum install package_name`
					* Remove a package
						* `yum remove package_name`
					* Update all packages
						* `yum package_name`
					* List installed packages 
						* `yum list installed`
5}  What is Telnet and its Port No
* Telnet
	* Telnet is a network protocol used to connect to remote computers over TCP/IP and access the via as a command line interface (CLI).
	* Key points
		* Used for remote login and command execution.
		* Provides text based communication.
		* Unencrypted, so data (including passwords) is sent in plain text - not secure.
		* Mostly replaced by SSH in modern systems due to security concerns.
		* Default port number
			* `port 23 (TCP)`
		* Basic usage
			* `telnet [hostname or IP] [port]`
		* Example
			* `telnet 192.168.1.10 23`
		* Security Note
			* Telnet should not be used over public networks.
			* Use SSH (port 22) instead for secure remote access.
* How Patching Works
	* Patching is the process of updating software to fix bugs, close security vulnerabilities, or add new features.
	* Patching is done in three ways
		* Package Updates
			* Using a package manager to install updates (patches) from official repositories.
		* Manual source patching
			* Applying a `.patch` or `.diff` file to source code using the `patch` command.
		* Kernel patching
			* Updating or hot-patching the Linux kernel (eg using `livepatch` on Ubuntu)
	* Patching via Package Manager
		* `sudo apt update`: Refresh package lists
		* `sudo apt list--upgradable`: See what's available
		* `sudo apt upgrade`: Apply available patches
		* For security patches
			* `sudo unattended-upgrades`
	* Manual Patching via `patch` command
		* When modifying source code
			* Apply a patch
				* `patch < fix.patch`
			* Or for specific files
				* `patch somefile.c < fix.patch`
			* 
7}  What is Bootprocess
8}  How Cron Works 
9}  What is Shell ,CLI and Source 
10}  What is Rysnc and Cp ? How its Work
