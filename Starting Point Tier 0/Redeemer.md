# Redeemer | Very Easy
Category/Tags: Redis, Vulnerability Assessment, Databases, Reconnaissance, and Anonymous/Guest Access

## Description:
This is the fourth box Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to connect to a Redis database to obtain the flag. This box will require reading Redis docs.<br>

## Solution:
### **Task 1**:
Which TCP port is open on the machine?<br>
Run:
`nmap -v -sT -p 1–65535 <IP address of machine>`
>-v = verbose<br>
>-sT = TCP scan<br>
>-p 1-65535 = scans the port range 1-65535 because, by default, nmap scans the top ports (0-1000) and if we only scan those ports, it'll return closed<br>

Answer: `6379`

### **Task 2**:
Which service is running on the port that is open on the machine?<br>
Answer: `redis`

### **Task 3**:
What type of database is Redis? Choose from the following options: (i) In-memory Database, (ii) Traditional Database<br>
I read the [Redis docs](https://redis.io/docs/about/) to find the answer.<br>

Answer: `in-memory database`

### **Task 4**:
Which command-line utility is used to interact with the Redis server? Enter the program name you would enter into the terminal without any arguments.<br>
I read the [Redis installation docs](https://redis.io/docs/install/install-redis/) to find the answer.<br>

Answer: `redis-cli`

### **Task 5**:
Which flag is used with the Redis command-line utility to specify the hostname?<br>
I read the [Redis command docs](https://redis.io/commands/info/) to find the answer.<br>

Answer: `redis-cli -h`

### **Task 6**:
Once connected to a Redis server, which command is used to obtain the information and statistics about the Redis server?<br>
I read the [Redis command docs](https://redis.io/commands/info/) to find the answer.<br>

Answer: `INFO`

### **Task 7**:
What is the version of the Redis server being used on the target machine?<br>
Connect to the Redis database:
`redis-cli -h <IP address of machine>`

Once connected, run:
`INFO` and then page up to the `#Server` section to view the version.<br>
Next time, you can run `INFO Server` to view this information without needing to page up.<br>

Answer: `5.0.7`

### **Task 8**:
Which command is used to select the desired database in Redis?<br>
I read the [Redis command docs](https://redis.io/commands/info/) to find the answer.<br>

Answer: `SELECT`

### **Task 9**:
How many keys are present inside the database with index 0?<br>
Run: `INFO keyspace` to view the databases and keys.<br>

*Notice how it returns `db0:keys=4`. This is how we know which database to select and how many keys it has.*

Answer: `4`

### **Task 10**:
Which command is used to obtain all the keys in a database?<br>
First, select the database by running:
`SELECT 0`

Then, run:
`KEYS *` to view the keys.

Answer: `KEYS *`

### **Flag**:
While connect still, run:
`GET flag` to select and print the flag.
