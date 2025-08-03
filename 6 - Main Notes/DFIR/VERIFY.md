2025-08-03 19:24

##### Description:
The CTF Challenge was all about using a SHA256 checksum text that works like verifying files by checking the first half using the available text then finding the next half using commands

### Terminal:
The Challenge required me to connect through `ssh` so I cannot download the files but I still created a directory to put the flag in. After that I use the `man` command on the command `sha256sum` which tells me that the command just verifies if the file has been tampered with. Given the `checksum.txt` I need to find the corresponding correct file within the `files` directory inside the `ssh`. For that I need to `cat` the `checksum.txt` to verify if its in a encrypted thing, and yes it is.
	`ssh ...`
	`man sha256sum`
	`cat checksum.txt`
	`ls files`
	`sha256sum files/* | grep -f checksum.txt`
I used the command `ls` to find that there are many files inside the `files` directory, that means I need to find and check the `sha256` of each files hence the command `sha256sum files /*` and use `grep -f checksum.txt` to match the correct half of the sha256. The `-f checksum.txt` simply means "using the type of file and find the matching content inside the `checksum.txt`"

#### Note
This command is new to me so its a hurdle to use it right away because I don't know its function. I googled the command and how is it used

## Next Application(s)
[[Scan Surprise]]