# Crocodile | Very Easy
Category/Tags: Web, Network, Custom Applications, Protocols, Apache, FTP, Reconnaissance, Web Site Structure Discovery, Clear Text Credentials, and Anonymous/Guest Access

## Description:
This is the third box in Starting Point Tier 1 Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to .

## Solution:
### **Task 1**:
What Nmap scanning switch employs the use of default scripts during a scan?<br>

Answer: `-sC`

### **Task 2**:
What service version is found to be running on port 21?<br>
Run: `nmap -A -sC` to scan the box.

Answer: `vsftpd 3.0.3`

### **Task 3**:
What FTP code is returned to us for the "Anonymous FTP login allowed" message?<br>
Our previous scan returns the code.

Answer: `230`

### **Task 4**:
After connecting to the FTP server using the ftp client, what username do we provide when prompted to log in anonymously?<br>
Run: `ftp -v <IP address of machine>` to connect.<br>
When prompted, enter: `anonymous`. We know this because our previous scans told us the FTP server allows Anonymous login.

Answer: `anonymous`

### **Task 5**:
After connecting to the FTP server anonymously, what command can we use to download the files we find on the FTP server?<br>

Answer: `GET`

### **Task 6**:
What is one of the higher-privilege sounding usernames in 'allowed.userlist' that we download from the FTP server?<br>
Run: `ls` to view the files present. Then run: `GET allowed.userlist` and `GET allowed. `EXIT`.<br>
`cat allowed.userlist` to view the user list.

Answer: `admin`

### **Task 7**:
What version of Apache HTTP Server is running on the target host?<br>
The scan we ran during Task 2 returns this information.

Answer: `Apache httpd 2.4.41`

### **Task 8**:
What switch can we use with Gobuster to specify we are looking for specific filetypes?<br>
Run: `gobuster dir -h` to view the flags.

Answer: `-x`

### **Task 9**:
Which PHP file can we identify with directory brute force that will provide the opportunity to authenticate to the web service?<br>
Run: `gobuster dir -u <IP address of machine> -x php -w /usr/share/wordlists/dirb/common.txt`.

Answer: `login.php`

### **Flag**:
Navigate to the website by using the IP address of your machine, plus /login.php. Use the login creds in the files downloaded from the FTP server.

Answer: `c7110277ac44d78b6a9fff2232434d16`
