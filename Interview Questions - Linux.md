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
				* 
5}  What is Telnet and its Port No
6}  How Patching Works
7}  What is Bootprocesse
8}  How Cron Works 
9}  What is Shell ,CLI and Source 
10}  What is Rysnc and Cp ? How its Work
