2025-09-24 21:06

##### Description:
The CTF Challenge gave a `flag.zip and dump.pcap` the flag.zip is encrypted with a password and is hinting to not use any password crackers

### Terminal:
After checking both files with the `file` command, I tried unzipping the `flag.zip` file but it is password-protected. So I worked first with the `dump.pcap` file and tried using `wireshark` on it which provides a stream of hidden messages. But I ultimately used `strings` to get the hidden messages and clearer. After noticing some fishy messages, I read that the flag is split into the other locked `.zip` file. Going through the stream of messages, I saw a decodable text and tried copying the whole thing to `cyberchef` after decoding it with `base64` command it provided me with jumbled and gibberish. I tried everything on the given stream but the text `AABBHHPJGTFRLKVGhpcyBpcyB0aGUgc2VjcmV0OiBwaWNvQ1RGe1IzNERJTkdfTE9LZF8=` is the only one that looks like decodable. I tried using `ChatGPT` and instructed it to be only in hint mode. It said it is in `base64` but its too long and try removing characters from the front or end. So I did, removed some of the letters from the front and it slowly shows half of the flag until It comes up with `VGhpcyBpcyB0aGUgc2VjcmV0OiBwaWNvQ1RGe1IzNERJTkdfTE9LZF8=` which translate into `picoCTF{R34DING_LOKd_` It is cut off. So the other half will be on the `.zip` file, I'm still trying to find the correct password but I tried using the first half the flag as the password and it worked
```
ls
file flag.zip
file dump.pcap
unzip flag.zip
--Tried typing a random password but fails
wireshark dump.pcap
strings dump.pcap
echo VGhpcyBpcyB0aGUgc2VjcmV0OiBwaWNvQ1RGe1IzNERJTkdfTE9LZF8= | base64 -d
--...picoCTF{R34DING_LOKd_
unzip flag.zip
--Entered "picoCTF{R34DING_LOKd_"
--flag txt file was created
```

#### Note


## Next Application(s)