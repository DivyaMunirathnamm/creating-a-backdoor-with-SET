# creating-a-backdoor-with-SET
creating a backdoor with SET - Ethical Hacking Techniques course

# AIM:
To Create a backdoor with Social Engineering Toolkit (SET)

## DESIGN STEPS:

### Step 1:

Install kali linux either in partition or virtual box or in live mode


### Step 2:

Investigate on the various categories of tools as follows:

### Step 3:

Open terminal and try execute some kali linux commands

### Architecture Diagram

```
+----------------+        +------------------------+        +----------------------+
| Attacker's PC  | -----> | SET (Credential        | -----> | Fake Login Page      |
| (Kali Linux)   |        | Harvester via Apache)  |        | (Hosted by SET)      |
+----------------+        +------------------------+        +----------------------+
       |                                                             |
       |                                                             v
       |   1. Configure SET with phishing site (e.g., Gmail clone)   |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Victim's Browser     |
       | <------------------------------------------------| Clicks Phishing Link|
       |                                                 +----------------------+
       |                                                             |
       |                                                             v
       |     2. Victim Enters Credentials → Sent to SET/Attacker    |
       |                                                             |
       |                                                             v
       |                                                 +----------------------+
       |                                                 | Credentials Captured |
       |                                                 | in Apache log/SET DB |
       |                                                 +----------------------+

```

## EXECUTION STEPS AND ITS OUTPUT:
Social Engineering attacks are the various cons used by the hackers to trick people into providing sensitive data to the attackers.

**Steps to Use SET for Phishing (Credential Harvester Attack Method)**

**1. Open terminal:**
```bash
sudo setoolkit
```
<img width="997" height="751" alt="image" src="https://github.com/user-attachments/assets/403d94ca-5a36-4588-899a-037d44eaef46" />


**2. Navigate:**
```bash
1) Social-Engineering Attacks  
2) Website Attack Vectors  
3) Credential Harvester Attack Method
```
<img width="991" height="303" alt="image" src="https://github.com/user-attachments/assets/39635ccd-16a1-4cf2-bfa6-c32a2de90e29" />
<img width="989" height="644" alt="image" src="https://github.com/user-attachments/assets/55ba5744-6b41-4cc9-90c9-a8a4ae6cd4a5" />
<img width="936" height="369" alt="image" src="https://github.com/user-attachments/assets/3389ff02-cc58-4261-9108-0f37702cf3cd" />



**3. Enter your IP address as the attacker server.**

<img width="946" height="631" alt="image" src="https://github.com/user-attachments/assets/939f5f5e-5ec5-42a8-b9e1-b660afa8343c" />



**4. Choose:**
```bash
2) Site Cloner
```
<img width="999" height="627" alt="image" src="https://github.com/user-attachments/assets/5fcca61f-2629-4414-b8d9-2706213091ef" />


**5. Enter the URL of the legitimate site ```(e.g., https://accounts.google.com)```**
<img width="991" height="504" alt="image" src="https://github.com/user-attachments/assets/0ddcdf77-3dd7-4f84-a9e5-79f54a2e5f00" />

**6. Send the generated link to the victim.**

**7. Once the victim logs in → their credentials are stored in:**
```bash
/var/www/html/
```



## RESULT:
The Social Engineering Toolkit (SET) is used to create backdoor is  examined successfully
