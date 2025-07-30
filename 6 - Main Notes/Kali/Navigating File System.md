2025-06-28 15:05

Status: Complete

Tags: 
[[Kali Linux]]
[[Basics]]
[[Commands]]
[[File System cmd]]
## Navigating File System
**Commands for FS navigation**
~pwd (present working directory)
	shows where you at, or currently working at

~cd (change directory)
	 changes the directory
	 You can go up to another folder using '~' before a slash to indicate you want to "jump" to the directory you wanted
		 'cd ~/Music' Also case sensitive
	The '..' indicates going back to the parent directory you are currently working with

~ls (list files)
	List files inside the directory you are currently in
	You can also list files inside a directory without going into it
		'ls /dekstop'
	You can also list hidden folders with the command '-la' (list all) in the current directory
		'ls -la'

~mkdir, rmdir (make directory, remove directory)
	mkdir creates a directory (or a folder)
		'mkdir folderName'
	You can also create a hidden folder by adding '.' before it
		'mkdir .hiddenFolder'
	rmdir removes the directory (or a folder)
		'rmdir folderName'
~cp, rm, mv, locate (copy, remove, move, locate files)
	'cp' Command means copy something
		'cp text.txt ~/Desktop'
	'rm' removes the file
		'rm text.txt'
	'mv' moves the file to another directory
		'mv text.txt ~/Desktop'
~updatedb (updatedb)
	'updatedb' Updates the db, meaning you will see the changes you have made
~passwd (change password)
	'passwd' Changes the password of the current user BUT must have super do command 'sudo'
		'sudo passwd > ilak' sudo lets you have higher autorization
~man (manual)
	'man' is useful command to see what the command do. You can always do this command if you ever have doubts on what parameters to use
		'man ls' will show you the parameters you can give to ls

### Reference
YouTube titled "Linux for Ethical Hackers" by freeCodeCamp: https://www.youtube.com/watch?v=lZAoFs75_cs