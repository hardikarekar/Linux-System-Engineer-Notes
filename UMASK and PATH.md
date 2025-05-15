#linux 
## UMASK
* What is umask?
	* User file creation mode mask
	* Controls default permission for settings for new files and directories created by a user.
	* It defines which permission bits to disable (or mask out) when new files or folders are created.
* Default file and directory permission
	* File: `666`
		* Read and write for all
	* Directory: `777`
		* Read, write and execute for all
* How it works
	* Suppose your umask value is `022`
		* File default `666` minus `022` = `644`
			* `rw-r--r--`
		* Directory default `777` minus `022` = `755`
			* `rwx-r-x-r-x`

* Create file with timestamp
	* `touch abc$(date +%Y-%m-%d_%H-%M-%S).txt`
`
``