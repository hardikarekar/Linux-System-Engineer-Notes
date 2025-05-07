#linux 
* User
	* `useradd shamu`
		* Refers to `/etc/login.defs` + `/etc/default/useradd`
		* Updates 4 files `/etc/passwd`, `/etc/shadow`, `/etc/group`, `/etc/gshadow`
			* `/etc/passwd` - Contains 7 fields
				* username
				* x - passwd is in `/etc/shadow`
				* UID
				* GID
				* GECOS field
				* Home directory
				* Shell
			* `/etc/shadow`
				- Password stored here.
				- Password policies / Password aging.
				- Contains 9 fields.
					* Username.
					* Password is in Md5 encryption clear text mode.
			* `/etc/group`
				* Plain text file that defines the group on the system.
				* `group_name:password:GID:user_list`
					* `group_name` - Name of the group.
					* `password` - Usually empty or `x.`
					* `GID`- Group ID, a unique number identifying the group.
					* `user_list` - List of users who are members of the group.
			* `etc/gshadow`
				* Stores secure group account information, including encrypted group passwords.
				* It's more secure because it is readable only by root.
				* `group_name:password:admin_users:member_users`
					* `group_name` - Name of the group.
					* `password` - Encrypted group password
						* `!` or `*` - No login via this group password.
						* 
	* Creates home directory `/home/newuser` + `ownership` + `permission` + `cp /etc/skel/profiles`
	* `getent passwd`
		* Used to `cat /etc/passwd`
* Group
	* Collection of multiple users/members.
	* What is the purpose of group
		* Assign permission to multiple users.
	* Create a group
		* Assign permission
			* Permission inherited to all members of group.
	* Add group
		* `groupadd name`
	* Add users in group
		* `usermod -G group user`
	* `getent group`
		* Used to `cat /etc/group`
* Switch user 
	* `su - user`
	* Root login
		* `su -`
* Linux has 3 types of users
	* Super user `root` + Local user 
	* System User 
		* ftp, samba, nfs
	* Virtual User 
		* Not in `/etc/passwd`
* Who is administrator in Linux
	* `uid 0`
# Ownership and Permission
* `chown`
	* Used to change the owner/group of a file or directory.
		* `chown [ownername] [file]`
		* `chown [ownername]:[groupname] [file]`
* `chgrp`
	* Used to change the group ownership of a file or directory. 
		* `chgrp [groupname] [file]`
* `chmod`
	* Used to change file or directory permissions.
	* Two ways to change permission
		* Symbolic way
			* `ugo`
		* Octal way
			* `777` or `007`
	* Symbolic way
		* `chmod ugo + rwx [file]`
			* Give `r-w-x` permission to user, group and others for that file.
		* `chmod go - rw [file]`
			* Remove `r-w` permission for group and others for that file.
		* Directory permissions
			* Use `-R` to apply recursively
				* `chmod -R ugo + rwx [file]`
		* Single-line Command
			* `chmod u+rw,g+rx,o+rwx [file]`
	* Octal way
		* Read 
			* `4`
		* Write
			* `2`
		* Execute
			* `1`
		* Example
			* `chmod 633 [file]` 
* Permission `-rwxr-xr--`
	* 3 fields
		* User/owner
			* Permission for file owner
		* Group
			* Permission for group
		* Others
			* Permission for all other users
* Permission
	* Read + Write + Execute
	* Read
		* To view and copy file
	* Read + Write
		* To modify and delete
	* Execute
		* Programs, Scripts, Commands
		* To enter into a folder
* `usermod`
	* Used to modify an existing user account.
	* Syntax
		* `usermod [options] username`
	* Common options
		* Change username
			* `usermod -l newname oldname`
		* Add user to a group(append)
			* `usermod -aG group username`
		* Change login shell 
			* 
* `chage
# Advance Permissions
* `setfacl` - Set file access control list.
	* To set individual permission.
		* How to `setfacl`
			* `setfacl -m u:Pankaj:rwx /abc`
		* How to view `setfacl`
			* `getfacl /abc`
		* How to delete `setfacl`
			* `setfacl -x u:Pankaj /abc`
* Set UID `SUID`
	* Set User ID
	* If a file has SUID bit set, and the file is owned by root, then any user who runs it executes it with root privileges.
	* This is often used for essential system commands that need elevated privileges.
		* `chmod u+s /abc`
* Set GID `SGID`
	* Set Group ID
	* When SGID is set on a file, anyone running that file temporarily assumes the group permission of the file's group owner. 
		* `chmod g+s /abc`
* Sticky bit
	* Only owner of the file can delete in terms of full permission.
	* `chmod o+t /abc`
* Sudoers
	* sudoers file is a special configuration file that defines who can run what commands as which users using the `sudo` commands.
	* What is sudo?
		* `sudo` short for 'super user do' allows a  permitted user to run a command as the root user.
	* What is sudoers?
		* It's the access control file for sudo.
		* It tells the system which users or groups are allowed to use `sudo` and what commands they can run.
		* Located at `/etc/sudoers`.
		* Edit using 
			* `visudo`