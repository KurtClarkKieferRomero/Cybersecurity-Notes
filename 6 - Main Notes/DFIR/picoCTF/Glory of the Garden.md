2025-08-05 15:50

##### Description:
The CTF Challenge is an image and the description is it 'contains more than it seems'

### Terminal:
The same thing as always `wget` `ls` `file`. I hop onto using the `exiftool` but did not find anything useful or encrypted text. But after using the `strings` command it showed itself not even encrypted. Then I just used `grep` to extract the text then redirect it to a `flag.txt`
	`wget <file link>`
	`ls`
	`file garden.jpg`
	`exiftool garden.jpg`
	`strings garden.jpg`
	`strings garden.jpg | grep -oE "picoCTF\{[^}]*\} > flag.txt`

#### Note
I'm getting the hang of using the basic commands and using the essential commands like `ls` and `file`


## Next Application(s)
[[DISKO 2]]