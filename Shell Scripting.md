#linux
* Shell
	* Application/Environment to run scripts. 
	* It is a special user program which provides an interface for the user to run programs/scripts.
* Scripting 
	* Programming
* Terminal will take input
	* Shell will send input to CPU
		* Processing
			* Output
				* Shell will take output and send to terminal
					* Output
* Can you run script without a terminal?
	* Yes
* Can you run a terminal without shell?
	* No
* Types of shell
	* SH shell
	* Bash shell
	* CSH
	* TCSH
	* KSH
* Bash is a enhanced version of sh.
* Find Linux supported shells
	* `cat /etc/shells`
* How to find current shell
	* `ps` 
		* Process status
* How to write a script
	* `touch /opt/my_script`
* How to execute a script?
	* Give execute `x` permission to file
		* `chmod +x /opt/my_script`
	* 3 ways
		* `./myscript`
			* Enter into directory and execute.
		* `/opt/myscript`
			* Enter absolute path.
		* `bash /opt/myscript`
			* Here script executes without `x` permission.
* How to write a backup script
```bash
#!/bin/bash

cp -rv /opt/* /usr/local/src
```
* How to run script in debugging mode
	* `bash -x /mnt/backup`
* Cron Scheduler
	* How to add script in Cron
		* `crontab -e`