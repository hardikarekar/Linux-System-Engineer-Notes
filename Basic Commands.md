#linux 
* Check where you are: 
	* `pwd`
	* Prints the current working directory.
* List contents of directory:
	* `ls`
	* Basic listing add flags to customize:
		* `ls -l` --> long format (details like size, date, permissions).
		* `ls -a` --> shows all files including hidden files (`.` dot files).
		* `ls -lh` --> human readable size (KB, MB, GB)
	* `ls -l` 
		* Used to see full properties.
		* Shows 9 fields:
			* type of file
			* permissions
			* selinux (Security Enhanced Linux)
			* link count
			* owner 
			* group 
			* timestamp
			* file or directory name
			* file size
* Change directory:
	* `cd <directory>`
	* `cd /home/user` --> go to that directory.
	* `cd ..` --> go up one level.
	* `cd ~` --> go to the home directory.
	* `cd /` --> go to the rooting directory.
	* `cd -`  --> go back to previous directory.
* See the path of command:
	* `which <command>`
		* `which ls` --> Might return `/bin/ls`.
* Display current date and time:
	* `date`
* Create new directory:
	* `mkdir new_directory` --> will create directory `new_directory` in the current location.
	* `mkdir directory1 directory2` --> create multiple directories in current location.
* Create empty file:
	* `touch my_file` --> a file will be created as an empty file.
	* `touch my_file1 my_file2`
* See available drives and mounts:
	* `df -h` --> shows how storage is distributed.
* Delete (remove) files or directories:
	* `rm` --> permanently delete files.
	* `rm file` --> deletes a file.
	* `rm file1 file2` --> delete multiple files.
	* `rm -i file` --> asks for confirmation before deleting.
	* `rm -f file` --> force delete (no warning).
	* `rm -r folder` --> recursively delete a directory and its contents.
	* `rm -rf folder` --> force + recursive delete (very dangerous).
* One line description of a command:
	* `whatis <command>`
		* Gives a brief summary of what a command does.
		* Useful when you want a quick idea without reading the manual.
* Detailed manual pages:
	* `man <command>`
		* Shows the full documentation for a command.
		* Tells you options, flags, usage, etc.
* Quick help for commands:
	* `<command> --help` --> gives a quick overview of how to use a command.
		* Shows all flags and options.
		* Helpful if you don't want to open the manual page.