2025-07-05 15:35

Status: **Complete**

Tags: 
[[Kali Linux]]
[[Basics]]
[[Commands]]
[[Networking cmd]]

## Networking Commands
**Refresher on OSI Model**
I refer to it as **A**ng **P**apaya **S**a **T**inola **N** **D**i **P**a Luto

| **Layer #** | **Name**     | **What it Does**                             | **Example**                 |
| :---------: | ------------ | -------------------------------------------- | --------------------------- |
|      7      | Application  | Apps that use the network                    | Browser, Discord, SSH, FTP  |
|      6      | Presentation | Translate data formats (Encrypt or Compress) | SSL/TLS, JPEG, MP3          |
|      5      | Session      | Starts/Ends connections between apps         | Session tokens, sockets     |
|      4      | Transport    | Moves Data                                   | TCP (Reliable), UDP (Fast)  |
|      3      | Network      | Finds paths (routing) and uses IP Addresses  | IP, ICMP (ping), ARP        |
|      2      | Data Link    | Deals with MAC Address and uses Frames       | Ethernet, Wi-Fi (MAC Layer) |
|      1      | Physical     | Hardware and signals                         | Cables, Wi-Fi signal, NIC   |

`ifconfig`
	Pretty much the same as `ipconfig` on windows that shows ip configuration and connection. Shows ip, Mac and packet status

`iwconfig`
	shows `ipconfig` information but for wireless and their status. 

`ping`
	sends packets of data and if it returns with a reply, you have a connection with what you are pinging

`arp`
	`arp` means address resolution protocol and used to view and manipulate system's ARP table. ARP is used to map IP address to a MAC address in a local network that means, Layer 3 will establish communication with Layer 2. In a nutshell it just asks "*Who has this IP address, Give me your MAC*"
		`arp -a` shows all ARP entries
		`arp -d 192.168.100.26` Deletes ARP entry for given IP
		`arp -s 192.168.100.26 00:11:22:33:44:55` Add a static ARP entry

`netstat`
	short for network statistics that shows current network connections, open ports and routing table
		`netstat` - shows basic network connections
		`netstat -tuln` - shows listening ports (TCP/UDP, no DNS names)
		`netstat -anp` - connections with program names and PIDs
		`netstat -r` - Routing table
		`netstat -i` - Info about your network interfaces

`route`
	tells you where your traffic exits and the two important things to see are *see table*. This means that destination 10.0.2.0 exits through a gateway of 0.0.0.0 which is your network. This can show you multiple networks that are connected on the same device
	
| Destination | Gateway  |
| ----------- | -------- |
| default     | 10.0.2.2 |
| 10.0.2.0    | 0.0.0.0  |


### Reference
YouTube titled "Linux for Ethical Hackers" by freeCodeCamp: https://www.youtube.com/watch?v=lZAoFs75_cs