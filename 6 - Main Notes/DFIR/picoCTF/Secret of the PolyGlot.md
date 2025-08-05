2025-08-05 11:41

##### Description:
This CTF Challenge is focused on identifying the metadata of a "PDF" file. Or actually just opening it with a viewer tool

### Terminal:
The image was downloaded using `wget` and the file was downloaded. I used the command `file` to find out what kind of file is it. Although the file itself was named `flag.pdf` the file presented is a type of `PNG` which is an image. I used `atril` for pdf viewer and `zsteg` for PNG. `zsteg` did help me understand what `png` viewer to used and it popped out with `made with GIMP` and I used gimp to open the image
	`wget <link>`
	`file flag2of2.pdf`
	`zsteg flag2of2.pdf`
	`gimp flag2of2.pdf` - I got only the first part of the flag, so I think of opening it with a pdf viewer
	`atril flag2of2.pdf`
After noting both the two parts of the flag, I note it using `nano` and combined it.

#### Note
I think a few extra steps on viewing the file like `zsteg` and `gimp` is overkill, but it is a good method to use whatever tool I have in hand. I realized that it is better to just use `ristretto` which is an image viewer

## Next Application(s)
[[CanYouSeeMe]]