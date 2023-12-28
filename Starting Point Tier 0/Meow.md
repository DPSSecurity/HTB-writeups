# Meow | Very Easy
Category/Tags: Telnet, Network, Protocols, Reconnaissance, Weak Credntials, and Misconfiguration

## Decription:
This is the very first box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to connect to the system using Telnet.<br>

## Solution:
### **Task 1:**
What does the acronym VM stand for?<br>

Answer: `Virtual Machine`

### **Task 2:**
What tool do we use to interact with the operating system in order to issue commands via the command line, such as the one to start our VPN connection? It’s also known as a console or shell.<br>

Answer: `Terminal`

### **Task 3:**
What service do we use to form our VPN connection into HTB labs?<br>

Answer: `openvpn`

### **Task 4:**
What tool do we use to test our connection to the target with an ICMP echo request?<br>

Answer: `ping`

### **Task 5:**
What is the name of the most common tool for finding open ports on a target?<br>

Answer: `nmap`

### **Task 6:**
What service do we identify on port 23/tcp during our scans?<br>

Run: `nmap -v -sT <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>

Answer: `Telnet`

### **Task 7:**
What username is able to log into the target over telnet with a blank password?<br>

Run: `telnet <IP address of machine>` and when prompted for the username, enter root.<br>

Answer: `root`

## **Flag**:
When connected, run to list files because we're searching for flag.txt: `ls -alh`<br>

When flag.txt is located, run: `cat flag.txt`<br>
