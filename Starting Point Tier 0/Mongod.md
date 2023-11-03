# Mongod | Very Easy
Category/Tags: MongoDB, Web, Databases, Reconnaissance, Misconfiguration, and Anonymous/Guest Access

## Description:
This is the sixth (and third VIP!) box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to .

## Solution:
### **Task 1**:
How many TCP ports are open on the machine?<br>
Run:
`nmap -v -sT -sV -p 1-65535`
>-v = verbose<br>
>-sT = TCP scan<br>
>-sV = service version number<br>
>-p 1-65535 = scans the port range 1-65535 because, by default, nmap scans the top ports (0-1000) and if we only scan those ports, it'll return closed<br>

Answer: `2`

### **Task 2**:
Which service is running on port 27017 of the remote host?<br>
Our previous scan returns this information in the `VERSION` column.

Answer: `MongoDB 3.6.8`

### **Task 3**:
What type of database is MongoDB? (Choose: SQL or NoSQL)<br>
I Googled the question to find the answer.<br>

Answer: `NoSQL`

### **Task 4**:
What is the command name for the Mongo shell that is installed with the mongodb-clients package?<br>
I Googled `mongodb-clients package mongo shell` to find the answer.<br>

Answer: `mongo`

### **Task 5**:
What is the command used for listing all the databases present on the MongoDB server? (No need to include a trailing ;)<br>
