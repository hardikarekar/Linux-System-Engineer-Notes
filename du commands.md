#homework
* `du` is disk usage.
* Used to check disk usage of files and directories.
* Here are 20 commands
	* Total size of current directory.
		* `du`
	* Human readable size(KB, MB GB)
		* `du -h`
	* Total size of current directory (human readable)
		* `du -sh`
	* Show size of all sub directories
		* `du -h --max-depth=1`
	* Size of a specific folder
		* `du -sh /path/to/folder`
	* Size of each file in a directory
		* `du -ah /path/to/dir`
	* Exclude specific files or directories
		* du -h --exclude="*.log"
	* Display size in MB
		* `du -sm *`
* Advanced and filtered output
	* Sort directories by size
		* `du -sh * | sort -h`
	* Top 5 largest directories
		* `du -sh * | sort -hr | head -n 5`

