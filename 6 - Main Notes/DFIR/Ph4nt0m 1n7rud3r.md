2025-08-03 17:15

##### Description:
The CTF challenge was to find the attackers payload and decode it. The file contained `pcap` file which is a packet capture that can be analyzed by wireshark

### Terminal:
I used `wget` to download the `pcap` file then I used the command `file` to verify the type of file it is and surely it is a `pcap` file. Then I used the `strings` command to extract information on the `pcap` file and at first I didn't notice that there was a `base64` code and surely it is not what I want.
	`wget https://challenge-files.picoctf.net/c_verbal_sleep/586d0206891cc683bae1160ad6b0e05d7e10e7b2df122c0441ab06581038dd32/myNetworkTraffic.pcap`
	`file myNetworkTraffic.pcap`
	`strings myNetworkTraffic.pcap`
After doing all of that, I hop onto using `wireshark` which is a packet analyzer tool which has GUI to interact with. The tool shows many stream of TCPs that's showing only SYN and not many more information. If I try to follow the stream, it leads to something that is not readable. Then I used ChatGPT to find or show me how to extract ASCII text from the `pcap` stream, but then it only shows the gibberish. I give up and used the hint, it helps me realize that I need to filter by time, and looking at the packet bytes of the lower end of TCP stream I can see a pattern that has a string that ends with `...==` then I go to google to just find the solution and sure enough they translated the `...==` text to base64. Using that knowledge I selected every stream in the chronological order then `right click` the stream, `show bytes` then I `copy-pasted` it in a `txt` file using `nano.` After collecting the end of the `base64` bytes that I could find, I used the `base64 -d` command to decode the fragmented `base64` texts.
	`nano fragmentedflag.txt`
	`base64 -d fragmentedflag.txt`
	`base64 -d fragmentedflag.txt > flag.txt`
The last command I just use to redirect the flag into a `flag.txt` to save it

#### Note
LEARN I mean LEARN the wireshark tool, and also just get handsy on the file, find some patterns or just brute force your way to it

## Next Application(s)
[[VERIFY]]