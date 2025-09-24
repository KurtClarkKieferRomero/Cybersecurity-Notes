2025-09-24 21:23

##### Description:
The CTF Challenge provided a `pcap and SSH key` in ASCII text. Since it's hard, I opened the hints and it said open it in `wireshark` and question on "How do you decrypt a TLS key"

### Terminal:
I checked both files if they are what they are. I used `wireshark` and saw many streams but this time it has TLSv1.2 as an encryption method to sending packets. During this time, I searched on the internet "how to decrypt TLS stream with a key" and clicked on this [website](https://blog.didierstevens.com/2020/12/14/decrypting-tls-streams-with-wireshark-part-1). Using the website, I followed and click on one of the TLS stream in `wireshark`

```
wireshark capture.pcap
-- right click > Protocol Preferences > Transport Layer Security > Open TLS Preferences > TLS debug file > Browse > **added the path to my pico.key
```

After doing that I came back to the stream and saw some TLS stream was decrypted by the debug file I used.

```
--right click > follow > TLS stream
Until I found the correct picoCTF flag
```
#### Note
Always use what information is on hand, don't be ashamed to use hints. It will not give you the answer and sometimes it will stump you even more. This is specially more crucial if you are new to the field of the CTF you are solving

## Next Application(s)