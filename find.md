#homework 
* Basic Syntax
	* `find [path] [options] [expression]`
		* Example
			* `find /home -name "*.txt"`
				* This finds all `.txt` files under /home.
* Find by name
	* `find /path -name "filename"`
	* Case sensitive
		* `find /path -iname "filename"`
* Find by file type
	* f = file
		* `find /path -type f`
	* d = directory
		* `find /path -type d`
* Find by size
	* Files larger than 100MB
		* `find / -size +100M`
	* Files smaller than 1kb
		* `find / -size -1k`
* Find by modification time
	* Modified in the last 1 day
		* `find / -mtime -1`
	* Modified more than 7 days ago
		* `find / -mtime +7`
* Execute commands on results
* Find all `.log` files  
	* `find /var/log -type f -name "*.log"`
