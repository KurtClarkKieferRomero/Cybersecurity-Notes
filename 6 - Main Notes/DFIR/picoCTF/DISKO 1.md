2025-07-27 22:38

##### Description:
The picoCTF challenge offered is: https://play.picoctf.org/practice/challenge/505?category=4&page=1

### Terminal:
First I created a directory to house all my Forensics CTF. I have done this to make them all in one place.
	`mkdir -p ./Forensics` This tells that if the directory is not yet created, create it
Then I go back to the picoCTF page and copy the link address of the image file. Using that link I go to the directory `Forensics` and created another directory for the specific CTF challenge named `DISKO1` and used the command `wget` to get a download link from the internet and download it in that directory
	`cd Forensics`
	`mkdir DISKO1`
	`wget https://artifacts.picoctf.net/c/537/disko-1.dd.gz`
From that, I started to use `Autopsy` which is a program that lets you analyze disk images and started using to analyze the disko-1.dd. But before that I used the command `gunzip` to uncompress the `.gz` file and get the image properly
	`gunzip disko-1.dd.gz`
	`file disko-1.dd.gz` - I used this command to verify if the file is actually a image and it is labeled as `DOS/MBR`
After verifying I go to terminal and enter the command `sudo Autopsy` there should be a localhost link that is running and will have you go through the steps of the process and enable you to analyze the files. In another terminal, I get the path directory of the .dd file
	`sudo Autopsy`
	`realpath disko-1.dd`
After getting the path, I pasted it in the autopsy and followed the normal procedure, then I go to use the keyword search function and search for the word `picoCTF` which already shows a file that has it. Then I extracted it and since its a `.raw` file I turned it into a string then use grep to extract the exact word I need or flag
	`ls /home/kali/Downloads`
	`strings /home/kali/Downloads/vol1-Unit58162.raw | grep -oE "picoCTF{.*?}" > flag.txt`
This just means that whatever the vol1.raw file, turn it into a string and find a specific word and extract it specifically word with `picoCTF` and whatever is inside the bracket, until you hit the last ASCII text before the closing curly brace then redirect or save it to `flag.txt`
#### Note
I did this very inefficient as I think this can be solved without even using `Autopsy`. The way to do it is just use `strings` command and `grep` piped `|` together.

## Next Application(s)
[[RED]]