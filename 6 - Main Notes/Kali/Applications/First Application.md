##### Description:
Trying to access or modify a text file that is limited in permission. Note that this is still in the virtualBox environment

### Terminal:
`touch Passwords.txt`
`mousepad Passwords.txt`
	While editing and trying to save, the file says its in read-only mode
`ls -l Passwords.txt`
	It shows `-------rw-` this means that the file is in read and write for the `others` maybe root
`chmod 666 Passwords.txt`
	It then says you have no permission, further cementing that the file is created by the root and it has only the read and write permissions
`sudo chmod 666 Passwords.txt`
`ls -l Passwords.txt`
	It now shoes `-rw-rw-rw-` this means that the file is read and write for all the users
`mousepad Passwords.txt`
	I can now edit and save the file

#### Note
This is my first breakthrough from learning kali, which lets me change the file permissions, look at file permissions, and edit the content of the text file (also create it).

## Next Application(s)
[[Second Application]]