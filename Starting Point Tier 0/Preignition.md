# Preignition | Very Easy
Category/Tags: Web, Custom Applications, Apache, Reconnaissance, Web Site Structure Directory, and Default Credentials.

## Description:
This is the sixth (and second VIP!) box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to enumerate a website's directories to find the correct page so we login to obtain the flag.

## Solution:
### **Task 1**:
Directory Brute-forcing is a technique used to check a lot of paths on a web server to find hidden pages. Which is another name for this? (i) Local File Inclusion, (ii) dir busting, (iii) hash cracking.

Answer:`dir busting`

### **Task 2**:
What switch do we use for nmap's scan to specify that we want to perform version detection?

I've explained this before in the [Fawn box writeup](https://github.com/DPSSecurity/HTB-writeups/blob/main/Starting%20Point%20Tier%200/Fawn.md).

Answer: `-sV`

### **Task 3**:
What does Nmap report is the service identified as running on port 80/tcp?

Run: `nmap -v -sT -sV <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>
>-sV = service version number<br>

Answer: `-sV`

### **Task 4**:
What server name and version of service is running on port 80/tcp?

Our previous scan returns this information in the `VERSION` column.

Answer: `nginx 1.14.2`

### **Task 5**:
What switch do we use to specify to Gobuster we want to perform dir busting specifically?

Run: `gobuster -h` to view the flags. You may need to install Gobuster to proceed.

Answer: `dir`

### **Task 6**:
When using gobuster to dir bust, what switch do we add to make sure it finds PHP pages?

Run: `gobuster dir -h` to view the `dir` flags.

Answer: `-x php`

### **Task 7**:
What page is found during our dir busting activities?

Run: `gobuster dir -w /usr/share/wordlists/rockyou.txt -u <IP address of machine>` to dir bust the website. We will start with common.txt. because it's a smaller, faster wordlist.

Answer: `admin.php`

### **Task 8**:
What is the HTTP status code reported by Gobuster for the discovered page?

Answer: `200`

## **Flag**:
Go to the webpage by pasting the machine's IP address into your browser and adding `/admin.php` to the end of the URL.

Test a common default creds login:<br>
>Username: `Admin`<br>
>Password: `Admin`<br>

The flag is on the website after you login!
