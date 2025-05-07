#homework 
1. Change default runlevel to 6
	* Runlevel 6 means `reboot`.
	* Setting runlevel 6 will make the system reboot every time it starts resulting in a boot loop. NOT RECOMMENDED.
	* Default runlevel is set in
		* `/etc/inittab`
	* Open the file
		* `vi /etc/inittab`
	* Look for this line
		* `id:5:initdefault`
	* Change it to
		* `id:6:initdefault`
	* Save and exit
		* `:wq`
	* On next boot, system will immediately go into runlevel 6, which is reboot, and will keep rebooting endlessly.
2. Alias Command
	* Lets you create shortcuts for longer or more complex commands.
	* It's very useful to save time and reduce typing errors.
	*  `alias name=command`
	* Example
		* `alias ll='ls -l'`
			* Shortens `ls -l` to `ll`.
	* To remove an alias temporarily
		* `unalias ll`
	* To view current aliases
		* `alias`
	* 

