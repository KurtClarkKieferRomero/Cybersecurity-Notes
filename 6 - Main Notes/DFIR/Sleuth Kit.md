2025-08-05 16:55

Status: **Incomplete**

Tags: 
[[Image Carving]]
## Sleuth Kit
**Commands to know**

| Command    | Description                                                                                                                                                                                                                                                                   |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `md5sum`   | Checks the hash md5 of a certain file. This is used to match the md5 to a specific disk image                                                                                                                                                                                 |
| `img_stat` | Gains more information about the disk image                                                                                                                                                                                                                                   |
| `mmls`     | Displays the partition layout of the volume system. This helps figuring out the `START` and `END` offset of the partition to identify which of the partitions you are currently working on. Note the units of byte sector                                                     |
| `fstat -o` | Basically gets the file system information given an offset. The `-o` states `offset`                                                                                                                                                                                          |
| `fls -o`   | Prints out files and directories inside the disk. If a name displays before a `_` it means its deleted for example `_notDeleted`. Note that it only lists from the `root` directory. If specified with an `inode` You will go inside the corresponding `inode` to a directory |
| `help`     | Not exactly a command but to find a `--help` of a command in sleuthkit arsenals, just type out the command                                                                                                                                                                    |


### Reference
YouTube video from DFIRScience - https://www.youtube.com/watch?v=R-IE2j04Chc