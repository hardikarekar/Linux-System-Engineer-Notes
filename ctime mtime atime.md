#homework 
* Timestamps that track different types of changes to a file.
* `mtime` - Modification Time
	* What it is
		* Time when the file content was last modified.
	* Changes when
		* You add/remove/overwrite contents in a file.
	* `touch abc`
	* View with
		* `ls -l file` 
		* `stat abc`
* `ctime` - Change Time
	* Time when file metadata (permission, ownership, etc.) is changed.
	* Also changes if `mtime` is updated.
	* Does not mean creation time.
	* `chmod 744 file.txt`
		* `ctime` is updated.
	* View with
		* `stat file.txt`
* `atime` - Access Time
	* Time when the file was last read (accessed), not necessarily modified.
	* `cat file.txt` 
		* `atime` is updated.