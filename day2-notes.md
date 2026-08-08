# Day 2 — Git/GitHub, chmod Permissions, Python, Networking
Date: Aug 8, 2026

## Git & GitHub

Git = program on your computer that tracks changes to files
GitHub = website that stores an online copy of your git project
Local copy = your project files sitting on your Kali machine
Remote copy = your project files sitting on GitHub's website
git push = uploads your local changes to GitHub
git pull = downloads GitHub's changes to your local machine
Personal Access Token = a special "substitute password" used only for git, since GitHub blocks normal passwords for security
git remote set-url origin URL = connects your local folder to GitHub using your token, so future pushes don't ask for login again

Key lesson: nothing syncs automatically — you must run git add . then git commit -m "message" then git push every time you want changes to appear on GitHub.

## File Permissions — chmod Numeric Shortcuts

Each permission has a value:
r (read) = 4
w (write) = 2
x (execute) = 1

Add them up per group (owner / group / others):
7 = rwx (read+write+execute)
6 = rw- (read+write)
5 = r-x (read+execute)
4 = r-- (read only)

Common combos:
chmod 644 file = owner: rw-, group: r--, others: r-- = Normal files/documents
chmod 755 file = owner: rwx, group: r-x, others: r-x = Scripts/programs
chmod 777 file = owner: rwx, group: rwx, others: rwx = Full access for everyone, avoid, security risk

## Python

Wrote a simple calculator script:

num1 = int(input("Enter first number: "))
num2 = int(input("Enter second number: "))

print("Sum:", num1 + num2)
print("Difference:", num1 - num2)
print("Product:", num1 * num2)

int(input(...)) = takes typed input and converts it to a number directly
+, -, * = math operators
print("label:", value) = prints text and a variable together, comma adds a space automatically

## Networking — Ports

Port = a "door number" on a device, lets multiple services run on the same IP address
IP:Port = example 192.168.1.15:22 = an address plus a specific service on it

Port 22 = SSH (remote login)
Port 21 = FTP (file transfer)
Port 25 = SMTP (email sending)
Port 53 = DNS
Port 80 = HTTP (websites)
Port 443 = HTTPS (secure websites)
Port 3389 = RDP (Windows remote desktop)

sudo ss -tulnp = shows all ports currently open/listening on your machine

Why it matters: Nmap scans check which ports are open on a target, open ports mean running services and potential attack surface. SOC analysts also watch for suspicious port activity in logs.

## Today's Progress
- Fixed GitHub authentication (token-based push working)
- Learned chmod numeric permissions (644, 755, 777)
- Wrote calculator script in Python
- Learned about ports and common port numbers

Next session: Finish TryHackMe Linux Fundamentals room, continue Month 1 topics (users, SSH, cron jobs)
