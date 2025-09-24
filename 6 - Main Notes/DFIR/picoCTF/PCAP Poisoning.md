2025-09-24 18:57

##### Description:
Given a PCAP file and nothing else

### Terminal:
I used the command `file` to determine the file type to be sure and it is a `.pcap` file. After doing that I used the `strings` command to maybe pull some strings inside the `pcap` file and the flag actually shows up. I was not satisfied because maybe there are some other ways to do the CTF challenge so I open `wireshark` to investigate the `packets`. In the first few lines of packets it already shows some hint regarding the flag which when you click and inspect says "Flag is close", seeing the hint, I saw a packet containing `user root password toor..` so I used the `Follow Stream` method to see the whole packet and after analyzing it, it contained the flag

#### Note
Its good to see already the flag using the `strings` command but doing so undermines the whole CTF challenge, but it also happens sometimes

## Next Application(s)