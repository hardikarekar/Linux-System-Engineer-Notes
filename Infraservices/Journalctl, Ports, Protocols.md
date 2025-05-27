* Journalctl
	* Used to check logs
	* Fetches logs from `/var/log`
	* General Usage
		* View all logs
			* `journalctl`
		* View logs with most recent entries first
			* `jornalctl -r`
		* Follow logs in real time (like `tailf`)
			* `journalctl -f`
	* Boot and kernel logs
		* Logs from the current boot
			* `journalctl -b`
		* Logs from the previous boot
			* `journalctl -b -1`
		* View kernel messages only
			* `journalctl -k`
	* Time based filtering
		* Logs since yesterday
			* `journalctl --since=yesterday`
		* Logs from a specific time range
			* `journalctl --since "2025-05-24 10:00" --until "2025-05-27 16:00"`
		* Logs from past hour
			* `journalctl --since "1 hour ago"`
	* Service specific logs
		* Logs for a specific service 
			* `journalctl -u ssh`
	* Filtering by priority
		* Only show error messages
			* `journalctl -p err`
		* Show critical, alert and emergency messages
			* 
* 