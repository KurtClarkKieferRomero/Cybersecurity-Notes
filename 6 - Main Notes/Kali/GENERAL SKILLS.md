2025-07-27 16:54

Status: **Incomplete**

Tags: 
[[Basics]]
## GENERAL SKILLS
#### What is a command prompt?
- Also called a Terminal or Bash and is used to execute commands
- Very simple user interface. Type in commands, and it interprets and runs the operation in the computer
#### SSH? Shashawa?
- SSH stands for "**Secure Shell**" which grants you safe access to unsafe networks. It is used to remotely login to a computer and execute commands
- To use SSH to remote login:
	On windows: use client like *PuTTY*
	On Mac or Linux: in the terminal type `ssh {user}@{host}`. User refers to the account you want to access and host is the domain or IP address of the computer you are trying to access

#### Swiss Army Knife: Netcat
- `Netcat` is a tool that can help you read or write data over the internet and is called "The Swiss Army Knife of Information Security"
- `Netcat` can use and do file transfer, chatting, port scanning and can even serve as both a client and a server
- the basic syntax for `netcat` commands is `nc [-options] [destination] [port]`
	- *Options* is/are an optional argument or "flag" that you can use to change the behavior or the command
	- *Destination* is the IP address of the computer you are trying to contact
	- *Port* is the endpoint and helps identify the type of communication happening

#### The Terminal
- Terminal is used to execute different command and functionalities
	**Basic commands**
	- `pwd` - Present working directory which tells you where you are currently
	- `ls` - List all the files in current directory, to see hidden files use `ls -a`
	- `cd` - change directory which helps you move around different directory
	- `mkdir & rmdir` - make and remove directory helps you create and delete directories or folders
	- `rm` - remove or delete files and to delete the directory use the `rm -r`
	- `touch` - used to create a file
	- `man & --help` - Helps you know more about the command
	- `cp` - used to copy files
	- `mv` - use to move and rename files
	- `locate` - used to locate file and give their directory
	**Intermediate commands**
	- `echo` - used to input data into a text file
	- `cat` - used to output or display the data in the file
	- `nano, vi, jed` - a text editor program that is inside the shell
	- `sudo` - SuperUser Do to make the command be administrative and execute it as root
	- `df` - used to see available disk  space in each partitions
	- `du` - to know a file or directory disk usage specifically
	- `tar` - tarballs or compress files or uncompress files
	- `zip, unzip` - use to zip files into .zip or unzip .zip files
	- `uname` - to show the information about the linux distro
	- `apt-get` - apt to work with packages and apt-get to install packages
	- `chmod` - change the permissions of a file
	- `hostname` - to change the hostname of the user
	- `ping` - use to check connection to a server
	*Other Commands*
	- `clear` - use to clear the shell
	- TAB - used to autocomplete commands
	- Ctrl + C - ised to stop any command and to force stop use Ctrl + Z
	- exit - Used to exit the terminal
	- `sudo halt & sudo reboot` - Used to power off and reboot the computer
- Be careful on using the `rm -rf` command as it recursively, forcibly, deletes the directories on where you are
- Root privileges is essentially a command that makes you execute it with a higher privileges
- You can use the terminal and the text editor, no matter what you still need to configure things both way
- 

### Reference
- picoCTF: https://picoctf.org/learning_guides/Book-1-General-Skills.pdf
- Basic linux commands: https://maker.pro/linux/tutorial/basic-linux-commands-for-beginners