2025-06-30 15:10

Status: **Complete**

Tags: 
[[Kali Linux]]
[[Basics]]
[[Commands]]
[[User cmd]]
## User Privileges
typing ls -la will net you with different listings of files or directory
if a file name starts with '-' it means that it is a *file*
if a file name starts with 'd' it means that it is a *directory*
for example

	drwxr-xr-x
	drwxr-xr-x
	-rw-------
	rw-r--r--

lets take `d rwx r-x r-x` to read what it means
`d` - means its a *directory*
`rwx` - means the *owner* has permissions to *read write execute*
`r-x` - means the *group* has permissions to *read and execute only*
`r-x` - means that *others* has permission to *read and execute only*

To change permissions of the file or directory you can use `chmod` command
it has many parameters but the important are:
	`r` - read
	`w` - write
	`x` - execute
	Symbolic Mode
	`u` - user(owner)
	`g` - group
	`o` - others
	`a` - all (users + group + others)
	`+` - add permission
	`-` - remove permission
	`=` - set exact permission
	For example
	'chmod u+r hello.txt' means change permission of user and add read capabilities
	'chmod a=rwx hello.txt' means change permission of all and set it to read write execute capabilities

*Octal mode* provides you with using numbers to better change the permissions

Then you can add them to assign the overall permissions that is 
User | Group | Others
ex. 7 6 0
means that
`User` has Read + Write + Execute
`Group` has Read + Write only
`Others` has no permissions

**Adding Users**
command `adduser` adds user with a name and a password
	`adduser nalah` gives a name and will ask for a password

**Switching to another User**
command `su` or switch user is used to switch to another user. Note that if you are not in *root* you are required to input their password

**the sudo**
`sudo` command is a powerful tool that can be used to gain higher privileges than what you are currently working on, but you must be part of the "sudoer's file" to even use `sudo` as a command

**Commands to note**
`cat` means concatenate but it also used to display the contents of a file
`/etc/fileHere` is a directory containing configuration files,
### Reference
YouTube video link: https://www.youtube.com/watch?v=lZAoFs75_cs