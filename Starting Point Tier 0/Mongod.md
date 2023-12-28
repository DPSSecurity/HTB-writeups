# Mongod | Very Easy
Category/Tags: MongoDB, Web, Databases, Reconnaissance, Misconfiguration, and Anonymous/Guest Access

## Description:
This is the sixth (and third VIP!) box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to connect to a Mongo database to obtain the flag.

## Solution:
### **Task 1**:
How many TCP ports are open on the machine?

Run: `nmap -v -sT -sV -p 1-65535 <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>
>-sV = service version number<br>
>-p 1-65535 = scans the port range 1-65535 because, by default, nmap scans the top ports (0-1000) and if we only scan those ports, it'll return closed<br>

Answer: `2`

### **Task 2**:
Which service is running on port 27017 of the remote host?

Our previous scan returns this information in the `VERSION` column.

Answer: `MongoDB 3.6.8`

### **Task 3**:
What type of database is MongoDB? (Choose: SQL or NoSQL)

I Googled the question to find the answer.

Answer: `NoSQL`

### **Task 4**:
What is the command name for the Mongo shell that is installed with the mongodb-clients package?

I Googled `mongodb-clients package mongo shell` to find the answer.

You may need to install the `mongodb-clients` package to proceed when you type `mongo` into your CLI.

Answer: `mongo`

### **Task 5**:
What is the command used for listing all the databases present on the MongoDB server? (No need to include a trailing ;)

First, connect to the target machine's database by running: `mongo <IP address of machine>`

Then, list the commands available on the server: `help`

Answer: `show dbs`

### **Task 6**:
What is the command used for listing out the collections in a database? (No need to include a trailing ;)

In the previous task, notice the database named: `sensitive_information`

Select the database: `use sensitive_information`

Then, run the command to list collections in a database: `show collections`

Answer: `show collections`

### **Task 7**:
What is the command used for dumping the content of all the documents within the collection named flag in a format that is easy to read?

Answer: `db.flag.find().pretty()`

## **Flag**:
The previous answer/command will reveal the flag.
