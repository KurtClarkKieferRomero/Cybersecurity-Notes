2025-08-03 20:10

##### Description:
This CTF challenge have me scan a QR code image inside a file

### Terminal:
This challenge introduced a new tool for QR code scanning called `zbarimg` which is a tool for scanning images. I downloaded the image and I tried using `strings` to find if the metadata of the image can be extracted.
	`wget <imagefile.png>`
	`strings flag.png`
	`sudo apt install zbar-tools`
	`zbarimg flag.png`
After using the `zbarimg` command, It showed the flag in image form so I took the text from there by typing it
	`echo "picoCTF{flag here} > flag.txt` 
#### Note


## Next Application(s)
[[Secret of the PolyGlot]]