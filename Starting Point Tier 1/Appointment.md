# Appointment | Very Easy
Category/Tags: Web, Databases, Injection, Apache, MariaDB, PHP, SQL, Reconnaissance, and SQL Injection

## Decription:
This is the first box in Starting Point Tier 1 Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to complete a SQL injection attack.

## Solution:
### **Task 1:**
What does the acronym SQL stand for?

Answer: `Structured Query Language`

### **Task 2:**
What is one of the most common type of SQL vulnerabilities?

Answer: `SQL injection`

### **Task 3:**
What is the 2021 OWASP Top 10 classification for this vulnerability?

Read the [OWASP Top 10 from 2021](https://owasp.org/Top10/) to find the answer. It's the third entry on the list.

Answer: `A03:2021-Injection`

### **Task 4:**
What does Nmap report as the service and version that are running on port 80 of the target?

Run: `nmap -v -sT -A <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>
>-A = Operating System version<br>

Answer: `Apache httpd 2.4.38 ((Debian))`

### **Task 5:**
What is the standard port used for the HTTPS protocol?

Answer: `443`

### **Task 6:**
What is a folder called in web-application terminology?

Answer: `Directory`

### **Task 7:**
What is the HTTP response code is given for 'Not Found' errors?

Answer: `404`

### **Task 8:**
Gobuster is one tool used to brute force directories on a webserver. What switch do we use with Gobuster to specify we're looking to discover directories, and not subdomains?

First, visit the website by entering the machine's IP address into your browser's URL bar.

Then, run: `gobuster -h` to view flags.

Answer: `Dir`

### **Task 9:**
What single character can be used to comment out the rest of a line in MySQL?

Answer: `#`

### **Task 10:**
If user input is not handled carefully, it could be interpreted as a comment. Use a comment to login as admin without knowing the password. What is the first word on the webpage returned?

To login, we need to complete the SQL injection.

I Googled SQL injections to find which one uses the comment character `#`.

>Username: admin `#<br>
>Password: password<br>

*Anything can be entered in the Password field*

Answer: `Congratulations`

## **Flag:**
It is present on the web page after you login!
