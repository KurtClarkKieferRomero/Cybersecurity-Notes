2025-07-30 23:45

Status: **Incomplete**

Tags: 
[[Basics]]
[[Linux]]
## Linux Fundamentals
**Linux** is an Operating System just like windows. This OS is used more in cybersecurity. Linux can come in many different distributions called *distros* which are modified and tailored to various needs and preferences

Linux was created by *Linus Torvalds* a Finnish student that wants a free operating system kernel.

Linux is generally considered more secure than other operating system.

Note that Operating System (OS) manages the communication between hardware and software part of computers.

The five core principle of Linux
	- **Everything is a file:** All config files even in the OS are stored in one or more text files
	- **Small, single-purpose programs:** Linux tools can be combined to work together
	- **Ability to chain programs together to perform complex tasks:** Enables to carry different programs tasks such as processing, filtering and more
	- **Avoid captive user interfaces:** Linux is designed to work mainly with the shell or terminal which handles greater control than GUIs
	- **Configuration data stored in text file:** As previously mentioned, almost all files are registered on the system

#### File System
Linux File system consist of many directories containing configuration files for the whole system. 

Take `/bin` for example, it houses all the command you can use in the terminal while `/sbin` houses the administrator or privileged commands.

In the `/usr` directory, houses the different users in the Linux

in the `/home` directory is where we always work at Desktops, Downloads and more

In the `/etc` sometimes referred to as 'etsy' houses most of the configuration of the network, protocols and other generic configurations that are set in the computer

#### Terminal
Serves as a gateway to communicating and interacting with the shell that communicates with the Kernel of the system. It can be also used to remotely communicate to other terminals

#### Shell
The most commonly used shell in Linux is called *Bourne-Again Shell (BASH)* and is a port of the GNU project.

#### Bash Prompt
it is structured like this
`<username>@<hostname><current working directory>$`
`kali@kali[~]$`
	Note that *~* refers to the `home` directory of the current user and also the default folder when we log in. You can interpret it as `/home/<user>` when you type the command `pwd`
`kali@kali[/home/Desktop]$`
	Note that the *$* refers us to be the `user`. Once we become `root` it changes to a `hash` or *#*
`root@kali[~]#`

#### PS1
the `PS1` variable in Linux customizes how the terminal looks. You can change what is visible, your username, the computer's name, your current working directory. You can also change the colors of the corresponding information

Using tools like `script` or reviewing the `.bash_history` file (located in the user's home directory), you can **record** all the commands you have used and organize them by *date and time*, which aids in documentation and analysis

#### Getting Help
Using the `man` and `--help` command helps you understand the command you are using. This is really important when diving into new commands you don't know or when you want to know the specific parameters to throw the command with (sometimes the parameters are also called `options`, `patterns`, so on)
Note that sometimes, some command take the `-help` instead of the earlier `help` command.
Syntax
	`man <tool>`
	`<tool> --help`
Sometimes you can shorten the output of the help command using the `curl` or `-h` command

Another useful tool to use is `apropos` which gives you the *shortened* description of the command
	`apropos sudo`

#### Navigating nano text editor
The interface is shown with Carets(`^`) and a character for example: `^G Get Help`. 

The `^` means just `Ctrl +` whichever the character is next to it so `^G` means `Ctrl + G` will get you help

the `M-` is a meta-key sequence that can accept `alt, cmd, esc` *twice* then the character associated with it.
### Reference
[[Linux Cheat Sheet.pdf]]