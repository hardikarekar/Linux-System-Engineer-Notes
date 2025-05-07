#linux 
### I. Vim
* Vim is a powerful, free and open source text editor primarily used in a terminal environment, though it also has a graphical user interface (GUI).
* Opening Vim:
	* `vim filename` --> Opens the file (creates it if it doesn't exist).
* Vim has 3 modes:
	* Normal:
		* Navigate, delete, copy, etc.
		* How to enter: Press `esc`
	* Insert:
		* Type like a normal editor.
		* Press `i`, `a` or `o`.
	* Command:
		* Save, quit, etc.
		* Press `:` in normal.
* Insert mode (to type text):
	* `i` --> insert before cursor.
	* `a` --> insert after cursor.
	* `o` --> open new line below.
	* `I`, `A`, `O` --> versions for start/end of line or above.
* Navigation (Normal Mode):
	* `h` --> Left
	* `j` --> Down 
	* `k` --> Up
	* `l` --> Right
	* `gg` --> Go to top
	* `G` --> Go to bottom
	* `0` --> Start of line
	* `$` --> End of line
* Editing (Normal Mode):
	* `x` --> Delete character
	* `dd` --> Delete (cut) line
	* `yy` --> Copy (yank)
	* `p` --> Paste
	* `u` --> Undo
	* `Ctrl + r` --> Redo
* Saving and Exit Mode
	* `:w` --> Save (write)
	* `:q` --> Quit
	* `:wq` --> Save and Quit
	* `:q!` --> Quit without saving
* 1 character = 1 byte

