# Responder | Very Easy
Category/Tags: WinRM, Web, Network, Custom Applications, Protocols, XAMPP, SMB, Responder, PHP, Reconnaissance, Password Cracking, Hash Capture, Remote File Inclusion, and Remote Code Execution

## Description:
This is the fourth box in Starting Point Tier 1 Hack The Box presents aspriring cybersecurity professionals with. In this box, we are asked to .

## Solution:
### **Task 1**:
When visiting the web service using the IP address, what is the domain that we are being redirected to?

Answer: `unika.htb`

### **Task 2**:
Which scripting language is being used on the server to generate webpages?

Run: `nmap -sT -A -sC <IP address of machine>`

Port #80 is open and is running an Apache web server that uses the PHP scripting language.

Answer: `php`

### **Task 3**:
What is the name of the URL parameter which is used to load different language versions of the webpage?

At the top of the website, there is a drop down menu titled "EN". It includes hyperlinks that changes the webpages to French and German. Once you change languages, there's a new URL parameter present: page.

Answer: `page`

### **Task 4**:
Which of the following values for the `page` parameter would be an example of exploiting a Local File Include (LFI) vulnerability: "french.html", "//10.10.14.6/somefile", "../../../../../../../../windows/system32/drivers/etc/hosts", "minikatz.exe"

Answer: ``

### **Task 5**:
Which of the following values for the `page` parameter would be an example of exploiting a Remote File Include (RFI) vulnerability: "french.html", "//10.10.14.6/somefile", "../../../../../../../../windows/system32/drivers/etc/hosts", "minikatz.exe"

Answer: ``

### **Task 6**:
What does NTLM stand for?

Answer: ``

### **Task 7**:
Which flag do we use in the Responder utility to specify the network interface?

Answer: ``

### **Task 8**:
There are several tools that take a NetNTLMv2 challenge/response and try millions of passwords to see if any of them generate the same response. One such tool is often referred to as `john`, but the full name is what?.

Answer: ``

### **Task 9**:
What is the password for the administrator user?

Answer: ``

### **Task 10**:
We'll use a Windows service (i.e. running on the box) to remotely access the Responder machine using the password we recovered. What port TCP does it listen on?

Answer: ``

## **Flag**:

