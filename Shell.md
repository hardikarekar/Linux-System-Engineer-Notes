#Scripting 
# Chapter1 Introduction to Linux
* Linux is a free open source operating system based on Unix.
* Linus Torvalds originally created Linux with assistance of developers from around the world.
## What is Linux
* Linux is a kernel.
* A kernel provides access to computer hardware and control access to resources such as
	* Files and data
	* Running programs
	* Loading programs into memory
	* Networks
	* Security and firewall
	* Device driver management
	* Other resources etc.
* A Linux distribution includes
	* Linux kernel
	* GNU application utilities such as text editors, browsers, etc.
	* Collection of various GUI application and utilities.
	* Office application software
	* Software development tools and compilers
	* Thousands of ready to use application software packages
	* Linux installation programs/scripts
	* Linux post installation management tools daily work such as adding users, installing applications, etc.
## What is Linux Shell
* What is a shell
	* Shell is a user program or it is an environment provided for user interaction.
	* It is a command language interpreter.
	* Shell gets started when you
		* login
		* open a terminal
	* Shell is not a part of the system kernel, but uses system kernel to execute programs, create files, etc.
	* Different shells
		* BASH 
			* Bourne Again Shell
			* Most common shell
		* CSH
			* C Shell
		* KSH
		* TCSH
* Various ways to get shell access
	* Terminal
		* Linux desktop provides a GUI based login system.
	* Connect via secure shell (SSH)
		* You will get a shell prompt as soon as you login into remote server or workstation.
	* Use the console
		* Few Linux system also provide a text based login system.
* How do I find out my current shell name
	* `cat /etc/shells`
* 