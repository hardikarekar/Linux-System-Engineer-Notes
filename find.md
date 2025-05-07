#homework 
* Basic `find` usage
	* Find all files in current directory and subdirectories
		* `find filename`
	* Find a file by name
		* `find /path -name "filename"`
	* Find a file ignoring case
		* `find /path -iname "filename"`
	* Find all files with a specific extension
		* `find /path -name "*.log"`
	* Find all directories named backup
		* `find / -type d -name "directory_name"`
* By file type
	* Find only files
		* `find /path -type f`
	* Find only directories
		* `find /path -type d`
	* Find symbolic links
		* `find /path -type 1`
* By time (Modified/Accessed)
	* Find files modified in the last 7 days
		* `find /path -mtime -7`
	* Find files modified exactly 10 days ago
		* `find /path -mtime 10`
	* Find files accessed in the last 1 hour
		* `find /path -amin -60`
	* Find files changed in last 30 minutes
		* `find /path -cmin -30`
* By size
	* Find files larger than 100 MB
		* `find /path -type f -size +100M`
	* Find files smaller than 1KB
		* `find /path -type f -size -1k`
* By Permission or Ownership
	* Find files with `777` permissions
		* `find /path -type f -perm 777`
	* Find files not writable by others
		* `find /path -type f -perm 002`
	* Find files owned by a specific user
		* `find / -user username`
	* Find files owned by a specific group
		* `find / -group groupname`
* Combined conditions and actions
	* 

