# Sequel | Very Easy
Category/Tags: Vulnerability Assessment, Databases, MySQL, SQL, Reconnaissance, and Weak Credentials

## Description:
This is the second box in Starting Point Tier 1 Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to access a SQL database to obtain the flag.

## Solution:
### **Task 1**:
During our scan, which port do we find serving MySQL?

Run: `nmap -v -sT -sV -A <IP address of machine>`<br>
>-v = verbose<br>
>-sT = TCP scan<br>
>-sV = service version number<br>
>-A = Operating System version<br>

Answer: `3306`

### **Task 2**:
What community-developed MySQL version is the target running?

Answer: `MariaDB`

### **Task 3**:
When using the MySQL command line client, what switch do we need to use in order to specify a login username?

Run: `mysql -help` to view the flags.

Answer: `-u`

### **Task 4**:
Which username allows us to log into this MariaDB instance without providing a password?

Answer: `root`

### **Task 5**:
In SQL, what symbol can we use to specify within the query that we want to display everything inside a table?

Answer: `*`

### **Task 6**:
In SQL, what symbol do we need to end each query with?

Answer: `;`

### **Task 7**:
There are three databases in this MySQL instance that are common across all MySQL instances. What is the name of the fourth that's unique to this host?

Run: `mysql -u root -h <IP address of machine>`

Run: `SHOW DATABASES;`

Run: `USE htb;`

Answer: `htb`

## **Flag**:
Run: `SHOW tables;` to list all tables in the htb databases. We are searching for the flag.

Run: `SELECT * FROM USERS;` to view all entries in the USERS tables in the htb database.

Run: `SELECT * FROM CONFIG;` to view all entries in the CONFIG tables in the htb database.

The flag is inside the CONFIG table!
