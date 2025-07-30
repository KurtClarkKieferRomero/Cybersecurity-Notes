2025-07-24 16:03

Status: **Complete**

Tags: 
[[Digital Forensics]]
[[Kali Linux]]
## Introduction to Digital Forensics
What is *Digital Forensics*
	Digital forensics is the **process of identifying, preserving, analyzing, and presenting digital evidence** from electronic devices such as computers, smartphones, or servers. It plays a critical role in cybercrime investigations by helping uncover:
	- Suspicious or deleted files
	- Malware traces
	- Unauthorized access
	- Evidence of data breaches

What is *Computer Forensics*
	Computer forensics is a **subfield of digital forensics** that focuses specifically on investigating computers and storage media. It emphasizes the **legal admissibility** of digital evidence and involves:
	- Lawful data collection and analysis
	- Evidence preservation and chain of custody
	- Report creation for courts and authorities

Key Differences

|   Aspect    |  Digital Forensics  |      Computer Forensics      |
| :---------: | :-----------------: | :--------------------------: |
|    Scope    | All Digital Devices | Mainly Computers and Storage |
| Legal Focus |       Broader       |    Strong Legal Emphasis     |
| Tools Used  |        Wider        |    Often desktop-focused     |
**Common Use Cases**
- Recovering deleted files
- Investigating ransomware attacks
- Tracing unauthorized access
- Analyzing memory dumps
- Extracting data from a corrupted disk
- Parsing document metadata in malware-infected files

**Tools To install**
****
Install the tools needed and here are the *steps*
1. Making sure `pipx` is installed:
	`sudo apt update`
	`sudo apt install pipx python3-venv -y`
	`pipx ensurepath`
2. Restart the terminal by closing and opening it again
3. Install the tools
	`pipx install volatility3`
	`pipx install analyzeMFT
	`pipx install oletools`
	`pipx install python-registry`
4. Check if the proper tools are installed using the commands
	`which volatility3`
	`which oleid`
	 So on...

The tools used are

| Tools             | Description                                             |
| ----------------- | ------------------------------------------------------- |
| `volatility3`<br> | Analyze memory dumps (RAM)                              |
| `analyzeMFT`      | Parse the NTFS Master File Table                        |
| `oletools`        | Analyze MS Office/OLE malware                           |
| `python-registry` | Read offline Windows Registry hives                     |
| `autopsy`         | GUI frontend for SleuthKit; Full Digital Forensic suite |





### Reference
- Kali Linux official tools list: https://www.kali.org/tools
- Volatility3 documentation: https://volatility3.readthedocs.io/
- AnalyzeMFT GitHub: https://github.com/dkovar/analyzeMFT
- Oletools docs: https://github.com/decalage2/oletools