FreshJuice Hub — Cybersecurity Awareness Pentesting Lab
A safe, beginner-friendly pentesting lab designed for teaching phishing, malware awareness, website reconnaissance, and reverse-shell simulation.
This lab helps students understand:
How attackers trick users with fake websites
How phishing pages look in the real world
How downloading random ZIP files leads to compromise
How to analyze a suspicious website
How to perform Nmap & Gobuster scanning
How malware callbacks / reverse shells work (safe simulation)
This project is 100% safe — there is NO real malware.
Everything is simulated for educational purposes.

Project Structure
freshjuice-hub-lab/
│── index.html
│── shop.html
│── deals.html
│── order.html
│── contact.html
│── style.css
│
└── files/
    ├── malware.zip     (Safe ZIP for demonstration)
    └── malware.txt     (Explains how malware spreads)

🧑‍🏫 1. Overview for Students

Welcome to the FreshJuice Hub Pentesting Lab.

This is your practice environment where you will learn:

✔️ How fake websites trick users
✔️ How phishing pages steal credentials
✔️ How websites can be hosted locally
✔️ How to perform reconnaissance on a target
✔️ How malware callbacks simulate reverse-shells
✔️ How to protect yourself from these attacks

2. How to Run This Lab (Windows / Mac / Linux)
Step 1 — Download the Lab
Option A (Recommended):
git clone https://github.com/marufrigan/freshjuice-hub-lab.git

Option B:
Click Code → Download ZIP
Extract on your computer

Step 2 — Enter the Project Folder
cd freshjuice-hub-lab

Step 3 — Start the Web Server
Windows / Mac / Linux:
python3 -m http.server 8080

If Python is installed as python, use:

python -m http.server 8080

Step 4 — Open the Website in Browser
**http://localhost:8080**


Congratulations — your phishing website is now running!

🎯 3. Part A — Website Analysis Tasks
📝 Task 1: Explore the fake website

Look at:

Product pages

Deals

Discount button

Login page

Download buttons

Write down:

What looks “trustworthy”?

What looks suspicious?

🔍 Task 2: Analyze the Fake Login Page

Enter test credentials:

test@example.com
password123


Explain:

How phishing pages steal credentials

What clues show it’s fake

Why users fall for it

📦 Task 3: Download the malware.zip

Inside the ZIP, open malware.txt.

It tells the story:

How attackers hide malware

How simply opening a file can be risky

Why awareness is important

⚔️ 4. Part B — Attacker Reconnaissance (Using Kali Linux)

Make sure your Windows/Mac system is running the fake website.

Find your system IP:

Windows:
ipconfig

Mac/Linux:
ifconfig


Example IP:

192.168.1.150

🔎 Task 4: Run Nmap Scan

From Kali:

nmap -sV -sC -p 8080 192.168.1.150


Answer:

What service is running?

What version of Python server?

What ports are open?

🗂️ Task 5: Directory Enumeration with Gobuster
gobuster dir -u http://192.168.1.150:8080 -w /usr/share/wordlists/dirb/common.txt


Find:

Hidden directories

Secret files

Write reflections:

Why do attackers scan directories?

Why is this dangerous for real companies?

🕵️‍♂️ 5. Part C — Malware Callback Simulation (SAFE)

This is the highlight of the lab.
No real malware — just a reverse-shell demonstration.

🧑‍💻 On Kali (Attacker): Start Listener
nc -lvp 4444


You will see:

listening on [any] 4444 ...

🧑‍🎓 On Victim Machine (Simulated Callback)

Open a second Kali terminal and send the callback:

nc <kali-ip> 4444


Example:

nc 192.168.1.97 4444


Now type commands:

hello
whoami
ls
pwd


These commands appear on attacker terminal — just like a real compromise.

Learning Outcome

Students learn:

How opening files triggers malicious connections

How reverse shells work

Why network monitoring matters

How attackers interact with a compromised device

🔐 6. Safety Notice

This project is 100% safe: No real malware

No dangerous scripts. No automation
Only educational simulations

The goal is awareness, not exploitation.

📘 7. Learning Outcomes Summary

By completing this lab, students will learn:

✔ Social engineering and phishing concepts
✔ Local website hosting
✔ Reconnaissance techniques (Nmap, Gobuster)
✔ Risks of downloading unknown files
✔ Reverse-shell behavior
✔ How attackers think
✔ How to protect systems

🏁 8. Credits

Developed by Maruf Farhan
For cybersecurity education and awareness.

Use responsibly and ethically.
