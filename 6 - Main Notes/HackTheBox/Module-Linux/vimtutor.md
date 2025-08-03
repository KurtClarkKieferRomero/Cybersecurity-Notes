2025-07-31 23:51

Status: **Incomplete**

Tags: 

## vimtutor
#### Navigation
`h` - moves the cursor to the right
`j` - moves the cursor down
`k` - moves the cursor up
`l` - moves the cursor to the left

#### Exiting vim
Pressing the `ESC` key will get you back to `Normal` mode
Typing `q! <ENTER>` will exit the editor

#### Text Editing - DELETION
Using the navigation keys `h,j,k,l` you can navigate to the part you wanted to delete and press `x` key

#### Text Editing - INSERTION
Using the same navigation keys, you can navigate to the part you wanted to insert characters then press `i` key. At the bottom left, you can see `-- INSERT --` this means that you are now inserting keys in the 

#### Text Editing - APPENDING
This just `appends` or add to the right of the cursor using the `a` key. The same symbol is indicated with the insertion or `i` key

#### Editing a File
to edit the file use the command `vim <filename.txt>` to enter it using the vim and to save file changes and exit vim use the command `:wq` which means save and exit executed together

#### Deleting a word
To delete a word, you must navigate to the first letter of the word you want to delete then type `dw` to delete the whole word

#### Deleting a line to the right
To delete a whole line to the right, you must navigate to the first letter of the line you want to delete then type `d$` to delete the whole line in the cursor and on the right of the cursor

#### Operations and Motions
Operations are letters that do something and motion are like parameters to tell the operation what to do for example earlier we used the `dw` command which tells us that
	`d` delete operator
	`w` to the start of the current word including the last character
	so when you use `dw` on hippopotamus, you place the cursor on `h` then enter the command dw
Some notable motions
	`w` - until the start of the next word, EXCLUDING its first character.
    `e` - to the end of the current word, INCLUDING the last character.
    `$` - to the end of the line, INCLUDING the last character.

Adding numbers before the motion will do as it says, for example using `d2w` will delete two words from the start of the cursor

Using this knowledge the motion can be used also to navigate through a sentence with the same motions command `w, e, $` and using numbers before them will do what they said with a count

#### Operating on lines
typing `dd` will delete a whole line and you can still use numbers or count to manipulate the output, `2dd` will delete two lines

#### Undoing and Redoing
Type `u` case sensitive, will undo the last command while typing `U` case sensitive will fix a whole line. While typing `Ctrl R` Holding on the ctrl key and pressing R will redo the last undo

#### Put command
Using the `dd` command delete the whole line, and typing `p` will 'put' the latest deleted line used by the `dd` after the cursor

#### Replace command
Using the command `r` will replace the character where the cursor is at with the inputted character.

#### Change command
Using the command `cc` and `ce` will change the whole line and put you in the insert mode and will change the current character until the end of the word and put you in insert mode. 
The motions also works with the `c` command for example using `c$` will put you into insert mode to change the current cursor until the end of the line



### Reference
