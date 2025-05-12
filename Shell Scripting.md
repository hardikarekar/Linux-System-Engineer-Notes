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
## Logical Operators
* `&&` AND Operator
	* Runs the second command only if the first command succeeds
		* `command1 && comand2`
	* Example
		* `mkdir test && cd test`
			* `cd test` will run only if `mkdir test` was successful.
* `||` OR Operator
	* Runs the second command only if the first command fails.
		* `command1 || command2`
	* Example
		* `mkdir test || echo "Failed to create folder"`
			* `echo` only runs if `mkdir test` fails.
* Combine both
	* `command1 && command2 || command3`
		* This means
			* If `command1` succeeds, then run `command2`.
			* If either `command1` fails or `command2` fails, then run `command3`.
## Different Operators
* `()` Parentheses
* `{ }` Expansion
* `[ ]` test
* `*` Select All
* `.` Current directory
* `&` run process in background
* `&&` AND logic
* `|` one command output to another
* `||` OR logic
* `;` Terminate
* `$` End
* `^` Karet
* `#` Comment
* `>` Redirect
* `>>` Append
## STD IN + STD OUT + STD ERROR
* stdin - Standard Input
	* File descriptor
		* `0`
	* Used to provide input to commands.
	* Example
		* `cat`
	* Redirect from a file
		* `cat < file.txt`
* stdout - Standard output
	* File descriptor
		* `1`
	* Used for normal output from a program or command.
	* Example
		* `echo "Hello" > hello.txt`
			* Redirect stdout to a file.
* stderr - Standard Error
	* File descriptor
		* `2`
	* Used for error messages.
	* Example
		* `ls /not/found 2> error.txt`
			* Redirects stderr to a file.
## Test Command
* Test command evaluates conditional expressions and is often used in shell scripts to check file properties, string comparisons, or numeric values.
* It returns a status code
	* `0` for true
	* `1` for false
* It is used within `[ ]` in scripts, like `[ condition ]`.
* Syntax
	* `test expression`
	* `[ expression ]`
## Variable
* Variable contains value which varies.
* How to define variables
	* `a=b`
		* `a`: variable
		* `b`: value
	* `country=india`
		* `country`: variable
		* `india`: value
* Variable are stored in memory.

* How to set environment variable
	* Edit `/etc/profile`
		* At end of file, add
			* `export a=b`
	* Reload file
		* `. /etc/profile`
* Shell variable 
* Environment variable
* How to see all variables
	* `env | less`

* `set`
	* 
