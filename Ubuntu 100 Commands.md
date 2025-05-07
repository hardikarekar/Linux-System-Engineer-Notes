#homework 
## File and Directory Commands
1. `ls` -- List Files.
2. `ls -l` -- List with details.
3. `ls -a` --Show hidden files.
4. `cd /path/` -- Change directory.
5. `pwd` -- Present working directory.
6. `mkdir newfolder` -- Create folder.
7. `rmdir foldername` -- Remove empty folder.
8. `rm -r foldername` -- Remove folder with files.
9. `touch filename` -- Create empty file.
10. `cp file1 file2` -- Copy file.
11. `cp -r dir1 dir2` -- Copy folder.
12. `mv oldname newname` -- Rename or move.
13. `rm filename` -- Delete file.
14. `cat filename` -- Display file content.
15. `more filename` -- View large files page by page.
16. `head filename` -- First 10 lines.
17. `tail filename` -- Last 10 lines.
18. `tail -f logfile` -- Live log file view.
19. `stat filename` -- Detailed file info.
## File Permissions
1. `chmod 777 filename` -- Full Permission.
2. `chmod 644 filename` -- Normal Permission.
3. `chown user:group filename` -- Change owner.
4. `chgrp group filename` -- Change group.
5. `find . -type f -perm 0777` -- Find files with 777.
## Searching Files
1. `find /path -name "file.txt"` -- Find by name.
2. `find /path -type d` -- Find directories.
3. `find /path -mtime +10` -- Modified > 10 days ago.
4. `locate filename` -- Fast file search.
5. `grep "text" filename` -- Search inside file.
6. `grep -r "text" /folder` -- Recursive search.
## System info
1. `uname` -- System name.
2. `uname -a` -- Detailed system info.
3. `hostname` -- Machine hostname.
4. `uptime` -- How long system is running.
5. `whoami` -- Current user.
6. `date` -- Current date/time.
7. `id` -- User and group IDs.
8. `cal` -- Calendar.
9. `df -h` -- Disk usage.
10. `du -sh /path` -- Folder size.
11. `free -h` -- RAM usage.
12. `top` -- Live system monitor.
13. `lscpu` -- CPU info.
14. `lsblk` -- Block devices (disks).
15. `lsusb` -- USB devices.
16. `lspci` -- PCI devices.