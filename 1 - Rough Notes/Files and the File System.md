**File System**
	Is like an index for all the files in your computer system which is like a direct call or reference to it

*Main Parts*
- Files
- Directories/Folders
- Metadata

**Files**
	These are used to store data and have two parts
		- Filename - Name of the file
		- Type - What kind if data is stored in that file
**Directories/Folders**
	Are collections of files grouped together in some way
**Metadata**
	Data about the file like its length, time created. Kind of like the file properties

A thing to note: When a file is created, the data is stored at some position in the memory. To call or use that file, you must use the *filename* which is just a refence to that data. Think of it as a address (filename) to the house (file). For you to find the house, you can use the address you know.
*Deleting Files*
	When you delete a file, the data stored is erased but the location of that file or the 'address' is still there. The computer just removes the calling operation on that certain file but until you put something 'new' there, the data can be restored

A file is constructed through *Blocks* which is the smallest part of the data. There is a *header block* and a *footer block* which is the start and the end of the file respectively.

**File Carving**
	Refers to the technique to extract data from a disk drive without having the normal file system to easily recover the files. It is a method of recovering files when there is 'not a reference' to them in the computer.

*Deleting Files v2*
	Files that get deleted also has an marked location in the disk. It is marked with unallocated and can be overwritten. Though this, you can recover files, most or all of the data inside of it.