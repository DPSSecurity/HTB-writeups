# Dancing | Very Easy
Category/Tags: Network, Protocols, SMB, Reconnaissance, and Anonymous/Guest Access

## Decription:
This is the third box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to use Server Message Block (SMB) to obtain the flag.txt file.

## Solution:
### **Task 1**:
What does the 3-letter acronym SMB stand for?

Answer: `Server Message Block`

### **Task 2**:
What port does SMB use to operate at?

Run: `nmap -v -sT -sV <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>
>-sV = service version number<br>

SMB is a Microsoft proprietary protocol, so `microsoft-ds?` hints towards the use of SMB. This is important because the words `Server Message Block` are not listed explicitly.

Answer: `445`

### **Task 3**:
What is the service name for port 445 that came up in our Nmap scan?

Answer: `microsoft-ds`

### **Task 4**:
What is the ‘flag’ or ‘switch’ that we can use with the smbclient utility to ‘list’ the available shares on Dancing?

Run: `smbclient -h` to view the flags. We don’t need to connect to list the shares.

Answer: `Answer`

### **Task 5**:
How many shares are there on Dancing?

Run: `smbclient -L <IP of machine>` and when prompted for the username, press enter.

Answer: `4`

### **Task 6**:
What is the name of the share we are able to access in the end with a blank password?

Run: `smbclient \\\\<IP address of machine>\\WorkShares` and when connected, run `ls` to list files because we're searching for the flag.txt file.`

Answer: `WorkSpaces`

### **Task 7**:
What is the command we can use within the SMB shell to download the files we find?

Navigate through the folders inside the share using `ls <folder name>`. Once you find the flag.txt file, run `GET` to download the file to our local machine.

Answer: `GET`

## **Flag**:
Run: `EXIT`

Run: `cat flag.txt`
