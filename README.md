# 🍊 FreshJuice Hub — Cybersecurity Awareness Pentesting Lab

A safe, beginner-friendly penetration testing lab designed for teaching:

- Phishing awareness  
- Fake website analysis  
- Reconnaissance (Nmap, Gobuster)  
- Malware awareness  
- Reverse-shell callback simulation (safe)  

This project is **100% safe** — there is **NO real malware**.  
Everything is simulated for educational purposes only.

---

# 📁 Project Structure

freshjuice-hub-lab/
│── index.html
│── shop.html
│── deals.html
│── order.html
│── contact.html
│── style.css
│
└── files/
├── malware.zip (Safe ZIP for demo)
└── malware.txt (Explains malware behaviour)



# 🎓 1. Overview for Students

Welcome to the **FreshJuice Hub Pentesting Lab**.

In this lab, you will learn:

- ✔ How fake websites trick users  
- ✔ How phishing login pages steal credentials  
- ✔ How websites can be hosted locally  
- ✔ How attackers perform website reconnaissance  
- ✔ How downloading files can compromise a system  
- ✔ How malware callbacks / reverse shells work (simulation only)  
- ✔ How to protect yourself from these attacks  

---

# 🖥️ 2. How to Run This Lab (Windows / Mac / Linux)

## **Step 1 — Download the Lab**

### Option A (Recommended)

git clone https://github.com/marufrigan/freshjuice-hub-lab.git
Option B
Click Code → Download ZIP

Extract the ZIP

Step 2 — Enter the Project Folder

cd freshjuice-hub-lab
Step 3 — Start the Local Web Server

Windows / Mac / Linux:

python3 -m http.server 8080
If Python is installed as python:


python -m http.server 8080
Step 4 — Open Website in Your Browser
Visit:


http://localhost:8080
You should now see the FreshJuice Hub fake website.

🔎 3. Part A — Website Analysis Tasks
🧪 Task 1: Explore the Website
Review the following pages:

index.html (home page)

shop.html

deals.html

order.html

contact.html

Fake login form

Fake download button

Write down:

What looks genuine?

What looks suspicious?

Would an average user trust it?

🧪 Task 2: Analyze the Fake Login Page
Enter test credentials such as:


test@example.com
password123
Discuss:

Why phishing login forms are dangerous

Signs of a suspicious login page

How attackers collect credentials

🧪 Task 3: Download the Fake Malware ZIP
Inside files/malware.zip, open:

malware.txt

This explains:

How attackers hide malware

Why opening unknown files is dangerous

How reverse-shell callbacks occur in real attacks

⚔️ 4. Part B — Reconnaissance from Kali Linux (Attacker)
Find the victim machine IP:

Windows
cmd
ipconfig
Mac/Linux

ifconfig
Example:

192.168.1.150
🛠 Task 4 — Nmap Scan
From Kali:


nmap -sV -sC -p 8080 192.168.1.150
Answer:
What service is running?
What version of Python is detected?
What ports are open?

🛠 Task 5 — Directory Enumeration (Gobuster)

gobuster dir -u http://192.168.1.150:8080 -w /usr/share/wordlists/dirb/common.txt
Find:
Hidden pages
Sensitive files
Developer paths
Explain why directory enumeration is dangerous for real companies.

🕵️‍♂️ 5. Part C — Safe Reverse-Shell Callback Simulation
This simulation demonstrates how malware communicates with attackers.
No real malware is used.

👨‍💻 On Kali (Attacker): Start Listener

nc -lvp 4444
👨‍🎓 Simulate the “malware callback”
Open a new terminal in Kali:

nc <kali-ip> 4444
Example:

nc 192.168.1.97 4444
Now type:


hello
whoami
ls
pwd
These commands appear on the listener — showing how attackers gain remote access.

🛡 6. Learning Outcomes
By completing this lab, you will understand:

✔ Phishing techniques

✔ Fake website indicators

✔ Website recon (Nmap, Gobuster)

✔ Social engineering risks

✔ Malware infection chain

✔ Reverse-shell behavior

✔ Defensive strategies

🧠 7. Safety Notice
This project is 100% safe.
It contains:

No real malware

No harmful scripts

Only educational simulations

Use only in controlled environments for ethical learning.

👤 Credits
Developed by Maruf Farhan
For cybersecurity education and awareness.

