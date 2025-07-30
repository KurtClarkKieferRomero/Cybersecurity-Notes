2025-07-07 13:47

Status: **Complete**

Tags: 
[[Kali Linux]]
[[Basics]]
[[File Manipulation cmd]]
## Viewing, Editing and Creating Files
`echo`
	does the same as echo in JavaSript, it can also echo different things and variables such as $USER, $SHELL. But it can also be used to write something in a specific file
		`echo "Hello" > Hello.txt` will put the string 'hello' to a text file named 'Hello.txt'
`cat`
	`cat` in this scenario is used to print out the file or display the contents of it. But it can also be used to combine different text files or text-based files
		`cat Hi.txt` will print out the contents of the text file

`replacing >`
	the `>` means that whatever the string before it *replace* everything to the file its going to
		`echo "please dont change me" > Hi.txt`
		`echo "get replaced loser" > Hi.txt` 
		You created a file that has the original contents of the first one but after using the `>` you replaced the contents of the previous file

`appending >>`
	the `>>` means that whatever the string before it *append or add* everything to the file its going to
		`echo "please dont change me" > Hi.txt`
		`echo "You will surely not be replaced" >> Hi.txt` 
		The same as before but you added a new line of a new text because of `>>`

`touch`
	creates a file instantly and its empty with 0 bytes
		`touch menot.txt`

`nano (or vi, vim)`
	After typing the command and the text file, you will be inside a text editor (that is inside a terminal) where you can add, change, delete or whatever you want to do with a text file
		`touch EditMe.txt`
		`nano EditMe.txt`
		after you created a file you can now edit the file using text editor with `nano`

`mousepad (old gedit)`
	The same as nano but instead of being a terminal-based editor, you can edit it in a *graphical* interface just like a notepad in windows.
		`touch GraphEdit.txt`
		`mousepad GraphEdit.txt`

[[First Application]]
### Reference
