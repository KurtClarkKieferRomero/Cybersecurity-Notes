2025-09-24 19:04

##### Description:
There is an image file with an image of picoCTF.

### Terminal:
I checked the file type of an image using `file` and yes, its an `PNG` then opening the image but seeing only the `picoCTF` image. So I used `strings` command and after scrolling I found a `secret/png` text, so I thought that maybe it is an image packaged with a directory. So I tried zipping it by renaming it and using the `cp` command

```
file flag.png
strings flag.png
strings flag.png | grep pico
cp flag.png flag.zip
ls
unzip flag.zip
```

after unzipping I saw a directory in the name of `secret` which houses a `png` file with the same 
#### Note


## Next Application(s)