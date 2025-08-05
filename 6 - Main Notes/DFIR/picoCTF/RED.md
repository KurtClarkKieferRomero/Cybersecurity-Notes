2025-07-30 00:17
##### Description:
the CTF challenge contains a PNG. Here is the link https://play.picoctf.org/practice/challenge/460?category=4&page=1
### Terminal:
Same thing as the previous application, use `wget` to get the image link and download it inside a new directory. Then I immediately used `strings` command to find any string hidden in the image and I got a simple poem that is also a hint on what to do next
	`wget the link`
	`strings red.png`
		`IHDR`
		`tEXtPoem`
		`Crimson heart, vibrant and bold,`
		`Hearts flutter at your sight.`
		`Evenings glow softly red,`
		`Cherries burst with sweet life.`
		`Kisses linger with your warmth.`
		`Love deep as merlot.`
		`Scarlet leaves falling softly,`
		`Bold in every stroke.x`
		`IDATx`
		`IEND`
	As you can notice the starting letter in each sentences spells out **CHECKLSB** meaning to check the *Least Significant Bit* of the image
To do that, we need a `stegonography` tool and download it in the net to identify the `png` because `steghide` doesn't recognize `png` type. I searched the internet for the `zsteg` and also found a YouTube video that demonstrates how to use the `zsteg` on `png` [here](https://www.youtube.com/watch?v=OPRGfJJ8bmU&list=PL1H1sBF1VAKUOp_TVZiOTGt4nB74So8sv&index=10). After installing `zsteg` I used the `man` command to find out how to find the `LSB` of an image, and sure enough, it shows it right away using the option `zsteg --lsb filename`
	`sudo gem install zsteg`
	`man zsteg`
	`zsteg --lsb red.png`
After using the command, it outputs this
```
meta Poem           .. text: "Crimson heart, vibrant and bold,\nHearts flutter at your sight.\nEvenings glow softly red,\nCherries burst with sweet life.\nKisses linger with your warmth.\nLove deep as merlot.\nScarlet leaves falling softly,\nBold in every stroke."            
b1,rgba,lsb,xy      .. text: "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ=="                                                                                 
b2,g,lsb,xy         .. text: "ET@UETPETUUT@TUUTD@PDUDDDPE"
b2,rgb,lsb,xy       .. file: OpenPGP Secret Key
b2,rgba,lsb,xy      .. file: OpenPGP Secret Key
b2,abgr,lsb,xy      .. file: OpenPGP Secret Key
b4,b,lsb,xy         .. file: 0421 Alliant compact executable not stripped
```
Notice the text after the poem. I didn't know what to do first and I googled how to decode `OpenPGP Secret Key` but it leads to a deeper rabbit hole. I then noticed that the text maybe is encrypted and googled "How to decode random encrypted text in Linux." The first thing it showed was a link that tells me its just a base64. Then I googled "base64 decoder" and used the website to decode that specific string and it already showed the flag. After that I searched google on how to decode base64 on the terminal and also gave me the way to use the `base64` command. I also used the `man` command to find out how to use it myself
	 `echo "cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==cGljb0NURntyM2RfMXNfdGgzX3VsdDFtNHQzX2N1cjNfZjByXzU0ZG4zNTVffQ==" | base64 -d | grep -oE 'picoCTF\{[^}]*\}' | head -n 1 | strings > red_FLAG.txt`
The `grep` and `head` command was chatGPT'd but it just means "start from the word picoCTF then from inside the curly braces (don't include them) extract it until the last curly brace" and the `head` command was "Extract only one instance" because the `base64` decoded many instances of the flag where I only want one. The `strings > red_FLAG.txt` just means turn the final output into strings and create a file and redirect it to `red_FLAG.txt`
#### Note
You really need to google even use ChatGPT to figure out your proper commands, there is no shame in that. The way you figure out on how to solve this is the key element to this challenge, I even used a hint yet it does not help me and got it on my own. Also don't forget to use the internet to find things like the `base64` decoder to help you. Also always use `man` command if you are not familiar with the command you are using

### References
`zsteg` github: https://github.com/zed-0xff/zsteg
John Hammond YT video about LSBs: https://www.youtube.com/watch?v=OPRGfJJ8bmU&list=PL1H1sBF1VAKUOp_TVZiOTGt4nB74So8sv&index=10
Where I got the idea to decode unknown algorithm (but its just base64): https://askubuntu.com/questions/178521/how-can-i-decode-a-base64-string-from-the-command-line
base64 decoder website: https://www.base64decode.org
## Next Application(s)

**Previous**
[[DISKO 1]]