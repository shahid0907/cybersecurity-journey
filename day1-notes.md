# Day 1 — Linux, Networking, Python Basics
**Date: Aug 7, 2026**

## Linux Commands

### Navigation
| Command | What it does |
|---|---|
| pwd | Prints your current location (which folder you're in) |
| ls | Lists files/folders in current directory |
| ls -la | Lists everything including hidden files, with details (permissions, size, date) |
| cd foldername | Moves into a folder |
| cd .. | Moves up one level (parent folder) |
| cd ~ | Jumps straight to home directory |
| mkdir name | Creates a new folder |
| touch file | Creates a new empty file |
| cp source dest | Copies a file |
| mv source dest | Moves a file, or renames it if destination is same folder |
| rm file | Deletes a file (permanently — no recycle bin) |
| rm -r folder | Deletes a folder and everything inside it |

### Viewing File Contents
| Command | What it does |
|---|---|
| cat file | Prints entire file content at once — good for small files |
| less file | Opens file in scrollable viewer (q to quit) — good for large files/logs |
| head file | Shows first 10 lines of a file |
| tail file | Shows last 10 lines of a file |
| tail -f file | Watches a file live as new lines get added (live log monitoring) |
| wc -l file | Counts number of lines in a file |

### Searching
| Command | What it does |
|---|---|
| find /path -name "file" | Searches for a file by name, starting at a given path |
| grep "word" file | Searches inside a file for lines containing "word" |
| grep -r "word" . | Searches for "word" inside every file in current folder (recursive) |
| which program | Shows the file path of an installed command/program |

### System Info
| Command | What it does |
|---|---|
| whoami | Shows your current username |
| hostname | Shows this machine's name |
| uname -a | Shows kernel/system version info |
| date | Shows current date and time |
| uptime | Shows how long the system has been running |
| df -h | Shows disk space usage (human-readable) |
| free -h | Shows RAM/memory usage |

### Processes & Permissions
| Command | What it does |
|---|---|
| ps aux | Lists all currently running processes |
| top | Live-updating view of running processes (q to quit) |
| chmod +x file | Adds execute permission (needed to run scripts) |
| sudo command | Runs a single command with admin/root privileges |
| history | Shows list of previously typed commands |
| clear | Clears the terminal screen |
| man command | Opens the manual/help page for a command |

## File Permissions
- Format: -rwxrwxr-x → type + owner perms + group perms + other perms
- r = read, w = write, x = execute (or "enter" for a folder)
- First character: - = regular file, d = directory
- New files default to rw- for owner/group, no execute — must add x manually with chmod +x

## Python Basics
| Concept | What it means |
|---|---|
| python3 file.py | Runs a Python script from the terminal |
| nano file.py | Opens terminal text editor to write code (Ctrl+O save, Ctrl+X exit) |
| input("prompt") | Pauses program, waits for user input, returns it as text |
| print(x) | Displays x on screen |
| variable = value | Stores a value under a name you can reuse |
| + (on strings) | Joins two pieces of text together |
| int(x) | Converts text into a whole number (so you can do math) |
| str(x) | Converts a number back into text (so it can join with other text) |

### Script written today:
name = input("What's your name? ")
print("Welcome to the terminal, " + name)
age = input("How old are you? ")
print("In one year you'll be " + str(int(age) + 1))

## Networking — IP Addresses
| Term | Meaning |
|---|---|
| IP address | Unique numeric label identifying a device on a network (e.g. 192.168.1.15) |
| Private IP | Used inside local networks — 192.168.x.x, 10.x.x.x, 172.16-31.x.x. Not directly reachable from internet |
| Public IP | Address your whole network uses to reach the internet, assigned by ISP |
| ip a | Command to view all network interfaces and their assigned IPs |
| lo | Loopback interface — machine talking to itself (127.0.0.1) |
| eth0 / wlan0 | Your real network interface (wired/wireless) |

## Today's Progress
- 30 Linux commands practiced
- First Python script written and run
- IP addressing concept learned
- Started TryHackMe: Linux Fundamentals Part 1
- Set up GitHub account + first repo

**Next session:** finish TryHackMe room, push first commit, learn chmod numeric shortcuts (755, 644)
