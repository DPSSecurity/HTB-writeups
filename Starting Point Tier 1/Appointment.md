# Appointment | Very Easy
Category/Tags: Web, Databases, Injection, Apache, MariaDB, PHP, SQL, Reconnaissance, and SQL Injection

## Decription:
This is the first box in Starting Point Tier 1 Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to complete a SQL injection attack.<br>

## Solution:
### **Task 1:**
What does the acronym SQL stand for?<br>
Answer: `Structured Query Language`

### **Task 2:**
What is one of the most common type of SQL vulnerabilities?<br>
Answer: `SQL injection`

### **Task 3:**
What is the 2021 OWASP Top 10 classification for this vulnerability?<br>
Read the [OWASP Top 10 from 2021](https://owasp.org/Top10/) to find the answer. It's the third entry on the list.<br>

Answer: `A03:2021-Injection`

### **Task 4:**
What does Nmap report as the service and version that are running on port 80 of the target?<br>
Run:
`nmap -v -sT -A <IP address of machine>`
>-v = verbose<br>
>-sT = TCP scan<br>
>-A = Operating System version<br>

Answer: `Apache httpd 2.4.38 ((Debian))`

### **Task 5:**
What is the standard port used for the HTTPS protocol?<br>
Answer: `443`

### **Task 6:**
What is a folder called in web-application terminology?<br>
Answer: `Directory`

### **Task 7:**
What is the HTTP response code is given for 'Not Found' errors?<br>
Answer: `404`

### **Task 8:**
Gobuster is one tool used to brute force directories on a webserver. What switch do we use with Gobuster to specify we're looking to discover directories, and not subdomains?<br>
First, visit the website by entering the machine's IP address into your browser's URL bar.
Then, run:
`gobuster -h` to view flags.

Answer: `Dir`

### **Task 9:**
What single character can be used to comment out the rest of a line in MySQL?<br>
Answer: `#`

### **Task 10:**
If user input is not handled carefully, it could be interpreted as a comment. Use a comment to login as admin without knowing the password. What is the first word on the webpage returned?<br>
To login, we need to complete the SQL injection.<br>
I Googled SQL injections to find which one uses the comment character `#`.<br>

Username: admin `#<br>
Password: password<br>
*Anything can be entered in the Password field*<br>

Answer: `Congratulations`

### **Flag:**
On the web page after you login!
