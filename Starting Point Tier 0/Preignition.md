# Preignition | Very Easy
Category/Tags: Web, Custom Applications, Apache, Reconnaissance, Web Site Structure Directory, and Default Credentials.

## Description:
This is the sixth (and second VIP!) box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to 

## Solution:
### **Task 1**:
Directory Brute-forcing is a technique used to check a lot of paths on a web server to find hidden pages. Which is another name for this? (i) Local File Inclusion, (ii) dir busting, (iii) hash cracking.<br>
Answer:`dir busting`

### **Task 2**:
What switch do we use for nmap's scan to specify that we want to perform version detection?<br>
I've explained this before in the [Fawn box writeup](https://github.com/DPSSecurity/HTB-writeups/blob/main/Starting%20Point%20Tier%200/Fawn.md).

Answer:`-sV`

### **Task 3**:
What does Nmap report is the service identified as running on port 80/tcp?<br>
Run:
`nmap -v -sT -sV <IP address of machine>`
>-v = verbose
>-sT = TCP scan
>-sV = service version number

Answer:`-sV`

### **Task 4**:
What server name and version of service is running on port 80/tcp?<br>
Our previous scan returns this information in the `VERSION` column.

Answer:`nginx 1.14.2`

### **Task 5**:
What switch do we use to specify to Gobuster we want to perform dir busting specifically?<br>
Run:
`gobuster -h` to view the flags. You may need to install Gobuster to proceed.

Answer:`dir`

### **Task 6**:
When using gobuster to dir bust, what switch do we add to make sure it finds PHP pages? <br>
Run:
`gobuster dir -h` to view the `dir` flags.

Answer:`-x php`

### **Task 7**:
When using gobuster to dir bust, what switch do we add to make sure it finds PHP pages? <br>
Run:
`gobuster dir -x php`

Answer:`-x php`
