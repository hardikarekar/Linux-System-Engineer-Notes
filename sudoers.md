* Sudoers file is a critical configuration file that controls which users can execute commands with elevated privileges using the `sudo` command.
* Location
	* `/etc/sudoers`
* Should be edited with `visudo`.
* Controls 
	* Who can use `sudo`.
	* What commands they can run.
* Uses a specific syntax for access control rules.
* Sudoers file structure
	* Contains these elements
		* Default settings
			* System wide sudo behavior
		* User privilege specifications
			* Who can run what commands.
		* Aliases
			* For grouping users, hosts and commands.
		* Include directives
			* For including other configuration files.
* Basic syntax
	* `user host = (run_as_user:group) command`
* For example
	* `john ALL=(ALL:ALL) ALL`
		* This allows `john` to run any command on any host as any user.
* Common Example
	* Give a user full sudo access.
		* `Gandhar ALL = (ALL:ALL) ALL`
	* Allow password less sudo
		* `Gandhar ALL = (ALL:ALL) NOPASSWD:ALL`
	* Restrict to specific commands
		* `username ALL = (ALL:ALL) /bin/ls, /usr/bin/apt`