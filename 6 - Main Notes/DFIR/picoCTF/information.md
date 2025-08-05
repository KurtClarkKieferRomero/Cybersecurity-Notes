2025-08-05 15:37

##### Description:
This CTF Challenge was the same as the previous one [[CanYouSeeMe]] which is an image file without any description

### Terminal:
The same as always `wget`, `ls`, `file`. Then I used `strings` to maybe search the image for strings but to no avail. Then I used `exiftool` to see the image's metadata. I already saw a encrypted text but I glanced over it because I though it was not the flag itself. Then I opened the image to see something but its just a cat loafing on the laptop's keyboard. Then I go to one of the hints and it leads me to see the image's description. So I go back and use the `exiftool` again and copied the encrypted text and then use `base64` to decode the text and sure enough it provided me with the flag
	`wget <file link>`
	`ls`
	`file cat.jpg`
	`strings cat.jpg`
	`exiftool cat.jpg`
	`echo "<encrypted text> | base64 -d > flag.txt`

#### Note
Sometimes trust your gut or if something is out of the ordinary react to and to use it already

## Next Application(s)
[[Glory of the Garden]]