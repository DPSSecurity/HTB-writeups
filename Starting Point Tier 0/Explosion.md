# Explosion | Very Easy
Category/Tags: Network, Programming, RDP, Reconnaissnace, and Weak Credentials

## Description:
This is the fifth (and first VIP!) box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to connect to a Windows Server using RDP to obtain the flag.

## Solution:
### **Task 1**:
What does the 3-letter acronym RDP stand for?

Answer: `Remote Desktop Protocol`

### **Task 2**:
What is a 3-letter acronym that refers to interaction with the host through a command line interface?

Answer: `CLI`

### **Task 3**:
What about graphical user interface interactions?

Answer: `GUI`

### **Task 4**:
What is the name of an old remote access tool that came without encryption by default and listens on TCP port 23?

Answer: `Telnet`

### **Task 5**:
What is the name of the service running on port 3389 TCP?

Run: `nmap -v -sT -sV <IP address of machine>`

Answer: `ms-wbt-server`

### **Task 6**:
What is the switch used to specify the target host's IP address when using xfreerdp?

Run: `xfreerdp -h` to view the flags.

We are searching for `Server hostname`.

Answer: `/v:`

### **Task 7**:
What username successfully returns a desktop projection to us with a blank password?

We need to RDP to the server to test usernames.

Run: `xfreerdp /u:Administrator /v:<IP address of machine>:3389`

FreeRDP will open a GUI window. This is the Windows Server!

Answer: `Administrator`

## **Flag**:
While connected still, open the flag.txt file on the desktop to obtain the flag!
