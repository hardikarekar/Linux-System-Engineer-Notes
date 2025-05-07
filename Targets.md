#linux 
* A target is a named system state - like a "mode" that tells the `systemd` which services and units to start.
* Same as runlevels in older systems.
## Common Targets 
* `poweroff.target` - `0` 
	* Shuts down the system
* `rescue.target`  - `1` 
	* Single user mode (maintenance)
* `multi-user.target` -  `3` 
	* CLI mode, multi-user, networking
* `graphical.target` - `5` 
	* GUI mode with logic screen 
* `reboot.target`  - `6` 
	* Reboots the system.
* `default.target` 
	* What the system boots into by default
## Useful Commands
* Check current target:
	* `systemctl get-default`
* Set default target:
	* `systemctl set-default graphical.target`
* Set back to CLI only:
	* `systemctl set-default multi-user.target`
* Change target (temporarily) without rebooting:
	* `systemctl isolate rescue.target`
* List all available targets:
	* `systemctl list-units --type=target`
* Reboot into a specific target:
	* `systemctl isolate reboot.target`
