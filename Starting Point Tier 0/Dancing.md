# Dancing | Very Easy
Category/Tags: Network, Protocols, SMB, Reconnaissance, and Anonymous/Guest Access

## Decription:
This is the third box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to use Server Message Block (SMB) to obtain the flag.txt file.<br>

## Solution:
### **Task 1**:
What does the 3-letter acronym SMB stand for?<br>
Answer: `Server Message Block`

### **Task 2**:
What port does SMB use to operate at?<br>
Run:
`nmap -v -Pn -sT -sV <IP address of machine>`

SMB is a Microsoft proprietary protocol, so `microsoft-ds?` hints towards the use of SMB. This is important because the words `Server Message Block` are not listed explicitly.

Answer: `445`

### **Task 3**:
What is the service name for port 445 that came up in our Nmap scan?<br>
Answer: `microsoft-ds`

### **Task 4**:
What is the ‘flag’ or ‘switch’ that we can use with the smbclient utility to ‘list’ the available shares on Dancing?<br>
Run: `smbclient -h` to view the flags. We don’t need to connect to list the shares.

Answer: `Answer`

### **Task 5**:
How many shares are there on Dancing?<br>
Run: 
`smbclient -L <IP of machine>`

When prompted for the username, enter enter.<br>

Answer: `4`

### **Task 6**:
What is the name of the share we are able to access in the end with a blank password?<br>
Run:
`smbclient \\\\<IP address of machine>\\WorkShares`

We know this because the first 3 shares are default shares.

When connected, run to list files because we're searching for flag.txt:
`ls`

Answer: `WorkSpaces`

### **Task 7**:
What is the command we can use within the SMB shell to download the files we find?<br>
Navigate through the folders inside the share using `ls <folder name>`. Once you find the flag.txt file, run `GET` to download the file to our local machine.

Answer: `GET`

### **Flag**:
Run: `EXIT`<br>
Run: `cat flag.txt`<br>
