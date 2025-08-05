2025-08-05 15:25

##### Description:
This CTF challenge provided no info but it says it hides somewhere because of the title. It also provided a `jpg` file

### Terminal:
This challenge I again used `wget` then I used `unzip` to unzip the file as it was in `.zip` then after that the `jpg` file types was shown but from my previous experience I still used `file` command to find out if the file is really as it seems and yes it is a `jpg` file. I used `strings` to maybe get something out but its full of encrypted data. Then I used `zsteg` but it fails because it only analyzes `png` files. Then I turn to `exiftool` which is releases information about a certain file and it's metadata.
	`wget <file link>`
	`ls`
	`unzip unknown.zip`
	`ls`
	`file ukn_reality.jpg`
	`strings ukn_reality.jpg`
	`zsteg ukn_reality.jpg`
	`exiftool ukn_reality.jpg`
After using `exiftool` the URL attribute of the file is encrypted in a `base64`. I copied the encrypted text and used `grep` to extract the text and redirect it to `decode.txt`. After that I use `base64 -d` to decode the text and sure enough it is the flag.
	`exiftool ukn_reality.jpg | grep -oE "<encrypted text>" > decode.txt`
	`base64 -d decode.txt > flag.txt`
#### Note
I did not even open the file or view it using any viewer tool in my system. It is good to just mess with the file because you might find something off like I did

## Next Application(s)
[[information]]