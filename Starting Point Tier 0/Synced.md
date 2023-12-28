# Synced | Very Easy
Category/Tags: Rsync, Network, Protocols, Reconnaissance, and Anonymous/Guest Access

## Description:
This is the final box Hack The Box presents aspriring cybersecurity professionals in Starting Tier 0. In this box, we are asked to transfer the flag.txt file from a share using rsync.

## Solution:
### **Task 1**:
What is the default port for rsync?

I Googled `default rsync port` to find the answer.

Answer: `873`

### **Task 2**:
How many TCP ports are open on the remote host?

Run: `nmap -v -sT -sV <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>
>-sV = service version number<br>

Answer: `1`

### **Task 3**:
What is the protocol version used by rsync on the remote machine?

Answer: `31`

### **Task 4**:
What is the most common command name on Linux to interact with rsync?

Answer: `rsync`

### **Task 5**:
What credentials do you have to pass to rsync in order to use anonymous authentication?<br>
>anonymous:anonymous<br>
>anonymous<br>
>None<br>
>rsync:rsync<br>

The answer can be found in the rsync man page.

Answer: `None`

### **Task 6**:
What is the option to only list shares and files on rsync? (No need to include the leading -- characters)

The answer can be found in the rsync man page, again.

Answer: `list-only`

## **Flag**:
List the shares on the server: `rsync rsync://<IP address of machine>`

`public` is the only share present.

List the files on the `public` share: `rsync --list-only rsync://<IP address of machine>`

Download the flag.txt file to our local machine: `rsync rsync://10.129.228.37/public/flag.txt flag.txt`
