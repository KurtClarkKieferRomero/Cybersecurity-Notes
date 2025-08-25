[[GAMES LEVEL GOAL]]
## LEVEL 0
****
Remember This always: `banditx@bandit.labs.overthewire.org -p 2220`
Where x is the number of your bandit
You can use the command `~.` to forcibly close the SSH connection you have currently on

## LEVEL 0 -> 1
****
The level 1 password is: *ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If*
Level 1 has this for username and info
* USERNAMES are somegame0, somegame1, ...
* Most LEVELS are stored in /somegame/.
* PASSWORDS for each level are stored in /etc/somegame_pass/.
**Steps**
	- I entered level 1 through the use of `ls` command that shows the files and directories i am currently working at. It shows `readme`
	- Then I used the `cat` command to display the content of the file or the `readme` file in there

## LEVEL 1 -> 2
****
The level 2 password is: *263JGJPfgU6LtdEvgfWU1XP5yac29mFx*
**Steps**
	- I use the `ls` command to find the file name of that the current file is named `-` which conflicts with many commands such as `cd`, `cat`, and etc. 
	- First, I search on 'how to open file names with -' in google and found out about this [website](https://medium.com/@.Qubit/how-to-create-open-find-remove-dashed-filename-in-linux-27ee297d1740)
	- This provided me a way to create, to concatenate and lastly to open such files with name starting with a `-`
	- The solution is to *prefix the path* which uses the `./` that simply states "use this directory right HERE"
	- Then I run the command `cat ./-` which means "In this directory open the file named `-`"

## LEVEL 2 -> 3
****
The level 3 password is: *MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx*
**Steps**
	- I entered the password and use the command `ls` to find or see the directories and file name. I saw `spaces in this filename` named-file
	- The thing when accessing this type of file is that it has spaces in its file name, which makes the command `cat` read every word after the spaces or white lines
	- Same with the previous level, I search on google how to properly open file names with spaces, and I found this [website](https://stackoverflow.com/questions/23019471/how-can-i-go-to-a-directory-whose-file-name-has-spaces-between-them-in-the-linux)
	- Basically, wrap the file name in `'file name'` single quotes or `"file name"` double quotes
	- Then I run the command `cat 'spaces in this filename'` which means "open the file with the filename inside this single quotes"

## LEVEL 3 -> 4
****
The level 4 password: *2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ*
**Steps**
	- I entered the password and use the command `ls` to find a directory named `inhere` which when I `cd inhere` and tried using `ls` command, it shows nothing
	- The instruction say that the file is hidden, which means it's filename is hidden
	- I used the command `ls -la` which means "List the files in here with the long description and list ALL of them" the `-la` shows the file info and even the hidden files
	- It shows the hidden file named `...Hiding-From-You`
	- I entered the `cat` command followed with the `./` which I learned to make the file name absolute, even used the single quotes method but eventually I tried not using the quotes or prefixing the path, It still worked with the command `cat ...Hiding-From-You`

## LEVEL 4 -> 5
****
The level 5 password is: *4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw*
**Steps**
	- I entered the password and use the command `ls` to find a directory named `inhere` which again I used `ls` to see many file names from 00 to 07 and with the format of `-file00`
	- I tried using `cat` command to find the hidden password on each file but that will be inefficient and time consuming
	- I tried searching about the `du` command which shows this [website](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) 
	- I found out that using the `-ah` command shows all the file even the directory and the `h` is for human-readable file
	- but it shows it in the same pattern with the same files
	- I figured to try opening the file `-file05` and it displays random symbols and I tried opening the last file which is `-file07` which contains the password
	- I figured that the order of the human-readable file is descending to which the last order in the system is the directory followed bu the `-file07` 
		`4.0K    ./-file05`
		`4.0K    ./-file03`
		`4.0K    ./-file06`
		`4.0K    ./-file02`
		`4.0K    ./-file01`
		`4.0K    ./-file09`
		`4.0K    ./-file00`
		`4.0K    ./-file04`
		`4.0K    ./-file08`
		`4.0K    ./-file07`
		`44K     .`
	- Since the filename is using `-` again, I again prefix the path before entering the name like `cat ./-file07`
	**NOTE:** The method I used was incorrect, I should have used the command `file` which means to determine the file type of the given file name or all using `*`. The correct command was to use the `file ./*` which shows you the REAL password containing file which is containing the ASCII text in THIS DIRECTORY because of the command `./`

## LEVEL 5 -> 6
****
The level 6 password is: *HWasnPhtq9AVKe0dmk45nxy20cvUa6EG*
**Steps**
	- Same things I did before this level
	- I used `ls` and found out that there are 20 directories with all of them having 7 files with almost the same name
	- I was tasked to find a specific file so I tried first using the command 
	`du -ba ./directoryName` which is really inefficient because imagine sifting through 20 directories but how about finding it in a 100. I did this with brute force
	- That command says "List me all the files in bytes in whole form inside the given directory" since I was trying to find a file that is the size of `1033` and I land on `./maybehere07` because I saw `.file2` with the same size as I was trying to find
	- So the next is I try to find the file permissions using the command `ls -la` which means "List all permissions of files inside this directory" and found out that the file is not executable
	- Then I try to find if the file is human-readable and not some weird data. using the command `file -h ./*` which means "List all the file type of files here in this directory" and found out that it is in `ASCII text with long binaries` which I instinctively used `cat` command
	- It finally outputted the password and even tried to enter it in the bandit6 which is correct
	**NOTE:** The correct command to find the specific file you want with correct parameters is using the `find` command (recursively) with its parameters. Here is the [man](https://manpages.ubuntu.com/manpages/jammy/en/man1/find.1.html) page of the `find` command. Finally, the correct command is
	`find inhere/ -type f -size 1033c ! -executable`
		-`inhere/` states that find it in that directory
		- `-type f` means that f is for files meaning find only file types
		- `-size 1033c` means that find only the files that has a size of 1033c which c is for bytes
		- `! -executable` means find the files that are NOT executable
		- In conclusion, find a specific file(s) inside the directory `inhere/` that is a `file` type with a size of `1033 bytes` and `not executable`

## LEVEL 6 -> 7
****
The level 7 password is: *morbNTDkSW6jIlUc0ymOdMaLnOlFVAaj*
**Steps**
	- This level is different because it's instruction requires me to look into different directories meaning in that whole container
	- I tried the command `ls` which shows nothing but the instructions said that it is owned by `bandit7` and used the command `ls /home` which shows different directories regarding the overthewire bandit game
	- The command I used to find the specific file is `find` with the different parameters given:
		- `/` which means find in `root` directory
		- `-user bandit7` which finds a file with the ownership given
		- `-group bandit6` which find a file with the group given
		- `-type f` which specify that we are trying to find a normal `file`
		- `-size 33c` which means find the file that is `33 bytes` in size
		- Completing the command: `find / -user bandit7 -group bandit6 -type f -size 33c`
		It showed many directories with permission denied
	- I used GPT to ask why does it outputs with `permission denied` files and was instructed to add a command `2>/dev/null` which tells me that "Every output that releases or say its an `standard error` get sent to the void or don't show at all"
		- `2` means `stderr` or standard error
		- `>` means redirect to...
		- `/dev/null` a directory that is a void, anything that goes here does not show or releases an output
	- The final command used is: `file -user bandit7 -group bandit6 -type f -size 33c 2>/dev/null` which worked and shows the directory where all the parameters are met and no error or `permission denied` outputted to the terminal
	- I used the `cat` command and typed `cat /var/lib/dpkg/info/bandit7.password`

## LEVEL 7 -> 8
****
The level 8 password is: *dfwvzFQi4mU0wfNbFOe9RoWskMLg7eEc*
**Steps**
	- I used the command `ls` to verify if the file named `data.txt` is indeed in the directory and I found out that it's true
	- When I tried to use the command `cat data.txt` it showed many entries of names that is associated with a string that looks like the password in the next level. That means I need to find a specific word and find the password associated with it
	- I used the command `grep -i millionth data.txt` which means "find a specific word in data.txt with the word `millionth` and IGNORE case sensitive"
	- Before this I used the command `grep --help` which helps me find the use of grep and how can I use it.
## LEVEL 8 -> 9
****
The level 9 password is: *4CKMh1JI91bUIZZPXDqGanal4xvAg0JM*
**Steps**
	- I tried using `grep` to the file but I don't know how can I use it properly
	- I check other commands given to me by the page and it has `sort and uniq` which intrigues me to use it
	- I used `man sort` and `man uniq` to check what it do
	- After finding out the proper command is `sort data.txt | uniq -u` which tells me that sort the passwords inside the `data.txt` file and find the only one occurrence of a password with the `-u` options
## LEVEL 9 -> 10
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	- I tried using `grep` but the file only outputs a binary match meaning its just a bunch of gibberish without using other command
	- After reading the Level goal, I tried using `grep` again with `grep -oE "\="` which means find an exact occurrence of an `=` sign but still it only outputs `binary match found`
	- Using what the level goal said and commands that need to be used to solve, I then used `strings` which provides me with random things but after scrolling up I found the password which really occurred with many `=======`
## LEVEL 10 -> 11
****
The level 10 password: *dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr*
**Steps**
	 - After using `ls` It is the same `data.txt` then by the level goal I need to use `base64` command which I did
	 - I used the command `base64 -d data.txt` then it outputs the password
## LEVEL 11 -> 12
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
## LEVEL 12 -> 13
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
## LEVEL 13 -> 14
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
## LEVEL 14 -> 15
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
## LEVEL 15 -> 16
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
## LEVEL 16 -> 17
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
## LEVEL 17 -> 18
****
The level 10 password: *FGUW5ilLVJrxX9kMYMmlN4MgbpfMiqey*
**Steps**
	
