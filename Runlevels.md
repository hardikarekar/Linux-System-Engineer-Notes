#linux 
## What is a runlevel?
*  A runlevel is a concept from traditional SysVinit systems that defines a state or mode of operation of the system.
* Each runlevel tells the system which services/processes should be running - like a startup profile.
* `runlevel` 
	* runlevel shows current and previous runlevels.
* Think of it like this -
	* runlevel = system mode
* Runlevel allows the system to boot into different modes based on your need - GUI, CLI, maintenance or shutdown.
* Role of runlevel in boot and shutdown:
	* In traditional SysVinit systems, runlevels control the system state - which services are started or stopped during
		* Bootup
		* Reboot
		* Shutdown
		* Recovery/Maintenance
	* During boot
		* System powers on.
		* Bootloader loads the kernel.
		* Kernel starts `init` (the first user space process).
		* `init` reads the the default runlevel from `/etc/initab`.
		* Based on the `init` it starts specific services and daemons.
* Common runlevels:
	* `0` --> Halt
		* shuts down the system
	* `1` --> Single user mode
		* Maintenance mode (no networking, for admins)
	* `2` --> Multi user 
		* Rarely used (network off)
	* `3` --> Multi user, CLI only
		* Boots to terminal (no GUI)
	* `4` --> Undefined/Custom
		* Can be configured by user
	* `5` --> Multi user with GUI
		* Boots into graphical desktop
	* `6` --> Reboot
		* Reboots the system.

## Change default runlevel
* `vim /etc/inittab`
* `id:3:initdefault:`
* `:wq!`
* `reboot`
