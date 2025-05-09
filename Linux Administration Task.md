#LinuxTasks
## 2a. Open Multiple gnome-terminals - try multiple users with su - cmd
* Open multiple Gnome terminal - `ctrl + shift + N`
* Switch into another user accounts - `su - hardik`
## 2b. Run commands 
1. `date` : Displays current date and time.
2. `touch abc` : Create an empty text file.
3. `rm abc`: Remove file.
4. `history`: Check command history.
5. `mkdir cat`: Create a new directory.
6. `rm -rf /cat*`: Delete all sub directories from parent directory.
7. `df -i`: Shows inode usage instead of disk space usage.
8. `df -k`: Shows disk space usage in kilobytes (KB).
9. `whatis`: Searches the whatis database for complete words.
10. `--help`: --help flag is commonly used to display usage instructions, options and examples.
11. `man`: Shows the manual documentation for all commands.
12. `rm -i`: Used to delete a file with confirmation.
13. `mkdir -p`: Used to create directories along with any necessary parent directories without throwing errors if they already exist.
14. `ls -ld`: Used to display information about the directory itself, not the contents.
## 2c. Create 2 files abc and xyz under /boot nd create ff.txt and tt.txt under /var and /usr/local
```bash
touch /boot/xyz
touch /boot/abc
ll -ltrh /boot

touch /var/ff
touch /var/ff
ll -ltrh /var

touch /usr/local/ff
touch /usr/local/tt
ll -ltrh /usr/local
```
## 2d. Use cp command to copy a multiple file and directory
```bash
cp /opt/hardik/* /home
```
## 2e. Take snapshot run rm -rf /* and revert
* Snapshot: It is a point-in-time copy of a file system, capturing its state at a specific moment. 
* `rm -rf`: It is a powerful (and dangerous ⚠️) command used to forcefully and recursively delete files and directories.
## 3b. del a word, copy 2 lines, del 4 lines, copy word, undo, redo, set num, unset num
* Copy : `yw`
* Copy 2 lines: `2yy`
* Undo: `u`
* Delete word: `dw`
* Delete line: `dd`
* Delete 4 lines: `4dd`
## 3c. search and replace all words from a file
* Search and replace: `:%s/old_word/new_word/g`
* Particular line: `:$s/old_word/new_word/g`
## 3d. del a trailing line from cursor, try go to particular line no, try :set ic
* Delete from cursor to the end of the line: `D`
* Go to a particular line number: `:linenumber`
* View line numbers: `set nu` No numbers: `set nonu`
## 4a. split horizontally and vertically nd try writing with split window over link files in vi editor
* Horizontal split: `split filename`
## 4b. try setting password with vi and also try removing the same
* Set Password: `:X`. Write file and exit. 

## 4c. Try nano options - copy a word, copy a line, del a line, del 2 words
* Copy a word:
	* Move cursor to the start of the word. Press `Ctrl + ^`. This sets the mark.
	* Use arrow keys to highlight the word. 
	* Press `Alt + 6`. This copies the word. Press `Ctrl + U` to copy.
* Copy a line:
	* Move the cursor anywhere on the line. 
	* Press `Ctrl + K` -> cuts the line. Then press `Alt + 6` -> copies instead of cutting.
	* Paste with `Ctrl + U`.
* Delete a line:
	* `Ctrl + K` -> Deletes entire line.
* Delete two words:
	* Move to the start of the first word.
	* Press `Ctrl + K` to mark. Select the two words and press `Ctrl + K` to delete the selection.
## 5a. Create a file called my_file under /home and create 2 hard links
* Create a file 
	* `touch my_file`
* Create 2 hard links 
	* `ln /home/my_file /home/hardlink1`
	* `ln /home/my_file /home/hardlink2`
## 5b. verify the hardlinks with linkcount and inode number
* To verify the hard links. Check the inode number:
	* `ls -li /home/hardlink1 /home/hardlink2`. 
* What to check here:
	* Inode number(First column): Should be identical for all two.
	* Link count(3rd column after permission): should show 3 meaning there are three hard links to the same inode (including the original file). 
## 5c. Create a shortcut of my_file.txt under /root/Desktop
* Create a file `touch /abc`
* Create the symbolic link: `ln -s /abc /hardik/abc`
```bash
ln -s ---> Creates soft link.
/abc ----> the original file.
/hardik/abc ----> the shortcut on hardik
```
## 6a. Del parent file abc and check orphan files
* Delete parent file: `rm /abc`
* Check the links:
	* Check hard link: `cat /hardik/hardlink1`
		* This will work because because `hardlink1` points to the same inode (same file content still exists).
	* Check soft link: `cat /hardik/softlink1`
		* This will fail because `softlink1` points to a path `/abc` which no longer exists. 
		* This is now an orphaned symlink.
## 6b. Use unlink command to remove link
* Create a file: `touch /abc`
* Create softlink and hardlink of `/abc`:
	* `ln /abc /hardik/hardlink1` `ln -s /abc /softlink1`
* Unlink link:
	* `unlink /abc`
## 6c. Try opening approx 100 terminals and try tab completion with cmds
* `ctrl + shift + N` --> 100 times
## 6d. change date and time nd history clear temp nd perm
* Change date
	* `date --set='Wed Apr 23 18:37:30'`
* Clear command history
	* `history -c`
## 6e. create user sachin nd set passwd, switch user (useradd sachin) (su - sachin) and del user userdel –r cmd
* Create a new user
	* `useradd sachin`
* Set password for the user
	* `passwd sachin`
* Switch to user `sachin`
	* `su - sachin`
* Delete user
	* `userdel -r sachin`
## 6f. create a group cartoon and add tom and jerry users in that group
* Create the group
	* `groupadd cartoon`
* Create users
	* `useradd tom` `useradd jerry`
* Add users to group
	* `usermod -aG cartoon tom`
	* `usermod -aG cartoon jerry`
## 7a. create a file `myfile` under `/opt`.`susan` and `shamu` able to read and execute.
* Create file in /opt 
	* `touch /opt/myfile`
* Create two users 
	* `useradd susan` `useradd shamu`
* Create a new group for access control 
	* `groupadd projectgroup`
* Add created users to the group 
	* `usermod -aG projectgroup susan`
	* `usermod -aG projectgroup shamu`
* Change the group ownership of the file
	* `chown :projectgroup /opt/myfile`
* Set appropriate permissions
	* `chmod 750 /opt/myfile`
		* This sets: `owner: read, write` `group: read, execute` `Others: no access`
## 10a. Try switch to runlevels `0 1 2 3 4 5 6`
* Check current runlevel:
	* `runlevel`
```bash
init 0   # Shutdown
init 1   # Single-user mode
init 2   # Multi-user (rarely used)
init 3   # CLI-multiuser
init 4   # Custom (acts like 3 until modified)
init 5   # Gui mode
init 6   # Reboot
```
## 10b. Go to single user mode from splash screen reset root password
* Reboot system (Interrupt)
	* At GRUB menu, select default boot entry, then press `e` to edit it.
* Edit boot 
	* Find line that starts with
		* `kernel vmlinuz-...`
	* Move to end of line
	* Add number
		* `1`
* Boot into single user mode
* Reset root password
	* `passwd root`
* Reboot system
	* `reboot`
## 10d. Change default runlevel 5 to 3
* Default runlevel is set in `/etc/inittab` file.
* `vi /etc/inittab`
	* Look for line
		* `id:5:inittab`
		* This means that current runlevel is `5`.
	* Change it to runlevel `3`:
		* Make changes in line:
			* `id:3:inittab`
	* Save and exit. 
	* Reboot to apply.
## 11a. try changing runlevel 6 under `/etc/inittab` and resolve with a reboot
* Same as 10d.
## 11b. try `startx` command from runlevel 3 and execute `runlevel`/`who –r` cmd
* Switch to Runlevel 3
	* `init 3`
* Run the `startx` command in run level 3
	* `startx`
		* This will start the X server and launch a basic graphical session.
* Verify the runlevel
	* `runlevel`
* Check current runlevel
	* `who -r`
## 11c. Try less and more cmd 5 examples 
* `less` command
	* View a file with scroll support.
		* `less /etc/fstab`
	* Search for a string inside the file
		* `less /etc/fstab`
			* `/proc`
				* Searches the proc.
	* Open the file and start at line 100
		* `less +100 /etc/fstab`
	* View a file with line numbers
		* `less -N /etc/fstab`
	* Combine with `grep` using pipe
		* `grep "Jimi" /abc | less`
* `more` command
	* View a file page by page
		* `more filename`
	* View long command output
		* `ls -l filename | more`
	* Start viewing from a specific line
		* `more +25 filename`
	* Use with piped command
		* cat filename | more
	* Search for a word inside more
			* `/keyword`
## 12a. Create 10 files. Set full permissions & find the same files with `find` command and delete all files.
* Create a file inside `/tmp`:
	* `mkdir -p /tmp/testfiles`
	* `touch /file{1..10}`
		* This creates file `file1,...file10`.
* Set full file permissions:
	* `chmod 777 /tmp/testfiles/file*`
		* Now all files have full permissions (Read, Write, Execute)
* Verify Permissions:
	* `ls -l /tmp/testfiles`
* Find files with permission 777:
	* `find /tmp/testfiles -type f -perm 0777`
		* lists files with exact `777` permissions.
* Delete those files using `find`:
	* `find /tmp/testfiles -type f -perm 0777 -exec rm -f {} \;`
		* `exec` execute a command on the found file.
		* `rm -f {}` force delete the file 
		* `\;` ends the `exec` command
	* All the `777` permission files will be deleted.
## 12b. Find 10 days older modified file | find particular users file | find 700 perm files.
* **Find files modified 10 days ago:**
	* `find /home -type f -mtime +10`
		* `/home` directory where you want to search.
		* `-mtime +10` modified more than 10 days ago.
* **Find files belonging to a particular user:**
	* `find /home -type f -user susan`
* **Find files with 700 permissions:**
	* `find /home -type f -perm -0700`
		* Finds file with exact `700` permissions.
## 12c. Find more than 100KB file with `find` and redirect to `/opt/hardik`
* Find files more than `100KB` and redirect to `/opt/hardik`:
	* `find /home -type f -size +100k > /opt/hardik `
		* `-type f` only files.
		* `-size =100k` files more than 100 kilobytes.
		* `>` redirect the output into `/opt/hardik`
## 39a. Create 2 user, del 1 user without data and 1 with data
* Create two users
	* `useradd Wilson`
	* `useradd Nichiket`
* Delete `Nichiket` and remove their home directory
	* `userdel -r Nichiket`
* Delete `Wilson` and keep their home directory
	* `userdel Wilson`
* Check if home directories still exist
	* `ls /home`
## 39b. Try `useradd` and `usermod` with flags `-u` `-s` `-d` `-c`
* `useradd` command (Create `Nichiket` with Custom Attributes)
	* `useradd -u 1501 -s /bin/bash -d /home/Nichiket -c "Custom Nichi" Nichiket`
		* `-u 1501` 
			* Sets UID to 1501
		* `-s /bin/bash` 
			* Sets login shell
		* `-d /home/Nichiket`
			* Sets home directory
		* `-c "Custom Nichi"`
			* Sets the comment field (user description)
* `usermod` command (Modify Existing User)
	* Modify `Nichiket`
		* `usermod -u 1601 -s /bin/bash -d /home/Nichiket -c "Modify Nichiket" Nichiket`
	* Change the home directory and also move files
		* `mv /home/Nichiket /home/NewNichiket`
		* `chown Nichiket:Nichiket /home/NewNichiket`
## 39c. Add users in group, change primary and secondary group of a user
* Add a user to a secondary group
	* `usermod -aG groupname username`
		* `aG` means append to group.
	* Example
		* `usermod -aG friends gandhar`
* Change a user's primary group
	* `usermod -g groupname username`
		* This replaces the primary group
	* Example
		* `usermod -g developers hardik`
* Set both primary and secondary groups
	* `usermod -g primarygroup -G group1,group2 username`
	* Example
		* `usermod -g staff -G cloud,devops hardik`
## 39d. Create user joe without using `useradd`, `adduser` 
* Create a group for joe
	* `groudadd joe`
* Create a home directory
	* `mkdir /home/joe`
* Manually add `joe` to `/etc/passwd`
	* `vi /etc/passwd`
	* Add this line at the end
		* `joe:x:1602:1502::/home/joe:/bin/bash`
			* `1602` UID
			* `1502` GID
			* `/home/joe` Home Directory
			* `/bin/bash` Default shell
* Set Ownership and Permission
	* Ownership
		* `chown joe:joe /home/joe`
	* Permission
		* `chmod 755 /home/joe`
* Create basic file from `/etc/skel`
	* `cp -r /etc/skel/. /home/joe`
	* `chown -R joe:joe /home/joe`
* Switch to user
	* `su - joe`
## 40a. Create 10 users and passwd in a single command with for loop script
* Create a file `create_users.sh`
```bash
#!/bin/bash
for i in {1..10}
do
 username="user$i"
 password="pass@123$i"
 useradd $username
 echo "$username:$password" | chpasswd
 echo "Created $username with password $password"
done
```
* Make it executable
	* `chmod +x create_users.sh`
* Run it
	* `./create_users.sh`
## a. try getent | id | grep for all 10users and del 5 users with same loop
* Verify all 10 users using `getent`, `id` and `grep`
* Delete 5 users using a loop
```bash
#!/bin/bash

echo "Checking all 10 users:"
for i in {1..10}
do
    username="user$i"
    
    # Check if user exists using getent
    if getent passwd "$username" > /dev/null; then
        # Print user info using id
        id "$username"
    else
        echo "$username does not exist."
    fi
done

echo -e "\nDeleting users user6 to user10:"
for i in {6..10}
do
    username="user$i"
    
    # Delete user along with home directory
    if id "$username" &>/dev/null; then
        userdel -r "$username"
        echo "Deleted $username"
    else
        echo "$username not found"
    fi
done
```
* `getent passwd username`
	* Checks if the user exists in `/etc/passwd`
* `id username`
	* shows GID, UID, and group info.
* `userdel -r`
	* Deletes the user and their home directory.
* Make the file executable
	* `chmod +x your_script.sh`
* Run the file
	* `./your_script.sh`
## 40b. try chage -d 0 and change all 6 fields of shadow file with same cmd, read man shadow
* `chage` command
	* Used to change user password aging policies and effectively modifies the sixth field of the `/etc/shadow` file, among others.
* Understanding `/etc/shadow` fields 
	* `username:password:lastchg:min:max:warn:inactive:expire`
		* `lastchg`: Last password change (days since Jan 1,1970)
		* `min`: Minimum days between password changes.
		* `max`: Maximum days password is valid.
		* `warn`: Warning period (days before expiry).
		* `inactive`: Inactive period after expiry.
		* `expire`: Expiration date (absolute days since Jan 1,1970)
* Use `chage` to set all 6 modifiable fields
	* `chage -d 0 -m 5 -M 90 W- 7 -I 30 -E 2025-12-31 username`
		* `-d 0`: Sets last password change to today (forces change on next login)
		* `-m 5`: Minimum 5 days between password changes.
		* `-M 90`: Maximum 90 days before password must be changed.
		* `-W 7`: Start warning the user 7 days before expiration.
		* `-I 30`: Account becomes inactive 30 days after password expires.
		* `-E 2025-12-31`: Account expires on Dec 31,2025.
* Verify settings with
	* `chage -l username`
## 40c. Disable users with /sbin/nologin | passwd –l | all user with /etc/nologin, test all
* Disable users with `/sbin/nologin`
	* Change single user's shell
		* `usermod -s /sbin/nologin username`
* `passwd -l`
	* Used to lock a user account, making it impossible to log in with a password but it does not disable the shell.
		* `passwd -l gandhar`
		* It adds a `!` in front of user's hash in `/etc/shadow`.
	* To unlock a locked account
		* `passwd -u gandhar`
* `/etc/nologin`
	* What is `/etc/nologin`?
		* If the file `/etc/nologin` exists, all non root users are prevented from logging in.
		* When they try, they'll see the contents of the file as a message.
		* Root can still log in.
	* Create `/etc/nologin` with a message
		* `echo "System maintenance is in progress. Logins are disabled." > /etc/nologin`
## 40d. find last 10 users with awk and head command | compgen | primary | try chfn | chsh | finger commands
* Get last 10 logged in users 
	* `last | awk '{print $1}' | head -n 10`
		* `last` - Shows login history
		* `awk '{print $1}'` - Extracts the username field.
		* `head -n 10` - Shows the last 10 user entries.
* List all users
	* `compgen -u`
* Get primary group of a user
	* `id -gn gandhar`
* View or change user info
	* `chfn`
		* Change full name and info
			* `chfn gandhar`
				* Changes user's full name, room number, work phone, etc.
	* `chsh`
		* Change login shell
			* `chsh gandhar`
				* Changes the default shell for the user.
* Get user info using `finger` - Ask doubt to Sadhiq (finger command not found; how to install the package)
	* `finger gandhar`

