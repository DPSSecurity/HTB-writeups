# Fawn | Very Easy
Category/Tags: FTP, Network, Protocols, Reconnaissance, and Anonymous/Guest Access

## Decription:
This is the second box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to use the File Transfer Protocol (FTP) to obtain the flag.txt file.<br>

## Solution:
### **Task 1:**
What does the 3-letter acronym FTP stand for?<br>

Answer: `File Transfer Protocol`

### **Task 2:**
Which port does the FTP service listen on usually?<br>

Run a port scan on the machine to figure out the port number FTP runs on: `nmap -v -sT <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>

Answer: `21`

### **Task 3:**
What acronym is used for the secure version of FTP?<br>

Answer: `SFTP`

### **Task 4:**
What is the command we can use to send an ICMP echo request to test our connection to the target?<br>

Answer: `ping`

### **Task 5:**
From your scans, what version is FTP running on the target?<br>

Run: `nmap -v -sT -sV <IP address of machine>`<br>
>-sV = service version number<br>

Answer: `vsftpd 3.0.3`

### **Task 6:**
From your scans, what OS type is running on the target?<br>

Run: `nmap -v -sT -sV -A <IP address of machine>`<br>
>-A = Operating System version<br>

*Notice how this scan also returns flag.txt!* 

Answer: `Unix`

### **Task 7:**
What is the command we need to run in order to display the ‘ftp’ client help menu?<br>

Answer: `ftp -h`

### **Task 8:**
What is username that is used over FTP when you want to log in without having an account?<br>

Answer: `Anonymous`

We know this before the previous nmap scan returns an interesting line: ftp-anon: Anonymous FTP login allowed (FTP code 230).

### **Task 9:**
What is the response code we get for the FTP message ‘Login successful’?<br>

Run: `ftp anonymous@<IP address of machine> 21` and when prompted, press enter for a blank password.<br>

Answer: `230`

### **Task 10:**
There are a couple of commands we can use to list the files and directories available on the FTP server. One is dir. What is the other that is a common way to list files on a Linux system.<br>

Answer: `ls`

### **Task 11:**
What is the command used to download the file we found on the FTP server?<br>

Run: `GET flag.txt` to download the flag.txt file to our local machine. We know flag.txt exists because of the nmap scap ran during Task 6.<br>

Answer: `GET`

## **Flag:**
Run: `EXIT` to log off the FTP server and return back to our local machine.<br>

Run: `cat flag.txt`<br>
