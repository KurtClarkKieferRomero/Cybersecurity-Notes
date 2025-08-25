2025-08-23 17:05

##### Description:
One of the employees at your company has their computer infected by malware! Turns out every time they try to switch on the computer, it shuts down right after they log in. The story given by the employee is as follows:

1. They installed software using an installer they downloaded online
2. They ran the installed software but it seemed to do nothing
3. Now every time they bootup and login to their computer, a black command prompt screen quickly opens and closes and their computer shuts down instantly.

See if you can find evidence for the each of these events and retrieve the flag (split into 3 pieces) from the correct logs!Download the Windows Log file [here](https://challenge-files.picoctf.net/c_verbal_sleep/123d9b79cadb6b44ab6ae912f25bf9cc18498e8addee851e7d349416c7ffc1e1/Windows_Logs.evtx)

### Terminal:
I installed python-evtx which is a Event Viewer that can be used to get info and dump it into a `.txt or .XML` file which is now readable and can be used by other applications. I used the `.txt` format because it will be easier and I just used `grep` but that gave me a really hard time because I don't know what event should I look for. Then I turn to ChatGPT to ask what process ID are the ones given by the description. Then I try to use `grep` but I am not successful. I then turn to use an environment where I can see the Logs much better and installed sublime. I don't want to put here how I installed sublime, the website itself provides a great CLI things to use. After viewing the `.txt` file with sublime, I tried to already search for the things like "shutdown, ran, download" but the things shown are too much and already a hassle to scroll because the log contains 116k lines. So I just started to scroll from the top and see if anything is amiss or different. Then I found the "Totally Legit Software" installation from the user. From the I followed the the logs from the point and searched for "Totally Legit" word then I found some instances of the flag which contains 2. The last one is hard and I did not bother to search for it and search it online
	`wget <file>`
	`file <filename>`
The file showed `.evtx` which is a Windows 10/11 Events Logger. I installed python-evtx which the command for is `evtx_dump.py <evtx file> > <txt file>`. Which dumps the information on the `.txt` file
	`evtx_dump.py <file> XML.txt`
	`subl XML.txt`
From that point its just copy and paste on the terminal and using `echo <encoded stuff> | base64 -d > flag.txt` 


#### Note
I cheated here again and went to YouTube but I normally don't know which file to use. I am getting there

## Next Application(s)