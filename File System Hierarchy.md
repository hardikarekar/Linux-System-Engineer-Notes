#linux 
# Navigating the file systems using Linux
###  I. Linux File System
* It is a way of organizing data and files on a storage device.
* Linux filesystem is **hierarchical** meaning it has a root directory `/` from which all other files and directories branch out forming a tree like structure. 
## II. File System Hierarchy Standard
* FHS defines the directory structure and directory contents in Linux Systems.
* The root directory `/` serves as the starting point of the file system.
* Key subdirectories include:
```txt
1) /bin: Essential command binaries like ls, cp and mv.
2) /boot: Bootloader files including the kernel.
3) /dev: Device files representing hardware components.
4) /etc: Configuration files for the system.
5) /home: User directories.
6) /lib: Essential shared libraries.
7) /mnt: Temporary mount point for filesystems.
8) /opt: Optional software packages.
9) /proc: Virtual file system providing process and kernel information.


10) /root: Home directory for the root user.
11) /sbin: System binaries, typically for administrative tasks.
12) /tmp: Temporary files.
13) /usr: Secondary hierarchy for user programs and data.
14) /var: Variable data files like logs, databases and email.