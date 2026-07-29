# Linux Fundamentals Writeup

**Difficulty:** Easy  
**Room Link:** https://tryhackme.com/room/linuxfundamentalspart1  
**Time to Complete:** 1-2 hours  
**Prerequisites:** None (Complete Beginner Friendly)

---

## 📚 Overview

Linux Fundamentals is an introductory room designed for complete beginners with zero Linux experience. You'll learn the basics of navigating a Linux terminal, understanding file systems, and executing common commands. This room covers Part 1 of the Linux Fundamentals series and provides hands-on experience with an in-browser Linux machine.

---

## 🎯 Learning Objectives

By completing this room, you'll understand:
- ✅ What Linux is and why it's important
- ✅ How to interact with a Linux terminal
- ✅ Basic Linux commands and their usage
- ✅ Linux file system structure and navigation
- ✅ How to search for files and content
- ✅ Introduction to shell operators and command chaining
- ✅ File permissions basics

---

## 📋 Task-by-Task Solutions

### Task 1: Introduction

**Objective:** Get started with Linux Fundamentals

**Answer:** Click the "Complete" button to proceed.

**What You'll Learn:**
- Basic terminal commands
- File system navigation
- File searching and filtering
- Introduction to shell operators

---

### Task 2: A Bit of Background on Linux

**Objective:** Understand what Linux is and its history

**Question 1:** Research: What year was the first release of a Linux operating system?

**Answer:** `1991`

**Explanation:** Linus Torvalds released the first version of Linux on September 17, 1991.

---

**Key Linux Facts:**

| Fact | Details |
|------|---------|
| **Creator** | Linus Torvalds |
| **Release Year** | 1991 |
| **Type** | Free, open-source operating system |
| **Usage** | Servers, websites, smartphones (Android), IoT devices, supercomputers |
| **Examples in Daily Life** | Traffic lights, car entertainment systems, ATMs, websites |

**Why Linux is Popular:**
1. ✅ **Free and Open Source** - Anyone can use and modify it
2. ✅ **Secure** - Strong user permissions and access control
3. ✅ **Stable** - Can run for years without restarting
4. ✅ **Flexible** - Used everywhere from phones to supercomputers
5. ✅ **Community Support** - Large community of developers

---

### Task 3: Interacting With Your First Linux Machine (In-Browser)

**Objective:** Deploy and access your first Linux machine

**Steps:**
1. Look for the green "Start Machine" button
2. Click it to deploy the Linux machine
3. Wait for it to load (usually 30-60 seconds)
4. You'll see a terminal window in your browser
5. You can now type commands directly

**Question:** I've deployed my first Linux machine!

**Answer:** Click "Complete" when the machine is running

**What You'll See:**
```
Welcome to TryHackMe!
[user@machine ~]$
```

The terminal is ready for commands!

---

### Task 4: Running Your First Few Commands

**Objective:** Learn basic terminal commands for output and user identification

#### Command 1: `echo` - Print Text to Screen

**What it does:** Displays text/output on the terminal

**Syntax:** `echo <text>`

**Example:**
```bash
echo Hello World
echo TryHackMe
echo "This is a longer text"
```

**Question 1:** If we wanted to output the text "TryHackMe", what would our command be?

**Answer:** `echo TryHackMe`

**Explanation:** Simply type `echo` followed by the text you want to display.

---

#### Command 2: `whoami` - Show Current User

**What it does:** Displays the username of the currently logged-in user

**Syntax:** `whoami`

**Example:**
```bash
whoami
```

**Sample Output:**
```
tryhackme
```

**Question 2:** What is the username of who you're logged in as on your deployed Linux machine?

**Answer:** `tryhackme`

**Explanation:** On TryHackMe machines, the default user is typically "tryhackme"

---

**Quick Command Reference:**

| Command | Purpose | Example |
|---------|---------|---------|
| `echo` | Display text | `echo Hello` |
| `whoami` | Show current user | `whoami` |
| `pwd` | Show current directory | `pwd` |
| `ls` | List files | `ls` |
| `cd` | Change directory | `cd /home` |

---

### Task 5: Interacting With the Filesystem!

**Objective:** Learn navigation and file interaction commands

#### Command 1: `pwd` - Print Working Directory

**What it does:** Shows the full path of the current directory you're in

**Syntax:** `pwd`

**Example:**
```bash
pwd
```

**Sample Output:**
```
/home/tryhackme
```

**Explanation:** `/home/tryhackme` is the home directory for the user "tryhackme"

---

#### Command 2: `ls` - List Files and Folders

**What it does:** Shows all files and folders in the current directory

**Syntax:** `ls` or `ls <directory>`

**Example:**
```bash
ls              # List current directory
ls /home        # List /home directory
ls -la          # Show all files including hidden (-a = all, -l = long format)
```

**Sample Output:**
```
folder1  folder2  folder3  folder4
```

**Question 1:** On the Linux machine that you deploy, how many folders are there?

**Answer:** `4`

**Explanation:** When you first deploy the machine, there are 4 folders visible: folder1, folder2, folder3, and folder4.

---

#### Command 3: `cd` - Change Directory

**What it does:** Navigate to a different folder/directory

**Syntax:** `cd <directory>`

**Example:**
```bash
cd folder1           # Go to folder1
cd /home/tryhackme   # Go to absolute path
cd ..                # Go to parent directory
cd ~                 # Go to home directory
cd -                 # Go to previous directory
```

---

#### Command 4: `cat` - Display File Contents

**What it does:** Shows the entire contents of a text file

**Syntax:** `cat <filename>`

**Example:**
```bash
cat file.txt
cat /home/tryhackme/documents/secret.txt
```

---

**Task 5 Questions & Answers:**

**Question 1:** On the Linux machine that you deploy, how many folders are there?

**Answer:** `4`

**Question 2:** Which directory contains a file?

**Answer:** `folder4`

**Step-by-step:**
```bash
# Check each folder for files
ls folder1      # Empty
ls folder2      # Empty
ls folder3      # Empty
ls folder4      # Contains a file!
```

**Question 3:** What is the contents of this file?

**Answer:** `Hello World!`

**Step-by-step:**
```bash
cd folder4      # Navigate to folder4
cat file       # Display file contents
# Output: Hello World!
```

**Question 4:** Use the cd command to navigate to this file and find out the new current working directory. What is the path?

**Answer:** `/home/tryhackme/folder4`

**Step-by-step:**
```bash
cd folder4      # Navigate to folder4
pwd             # Show current path
# Output: /home/tryhackme/folder4
```

---

### Task 6: Searching for Files

**Objective:** Learn how to search for files and text within files

#### Command 1: `find` - Search for Files

**What it does:** Searches for files in directories

**Syntax:** `find <path> -name <filename>`

**Example:**
```bash
find . -name "flag.txt"          # Search in current directory
find /home -name "*.log"         # Find all .log files in /home
find / -name "secret" 2>/dev/null # Search entire system, hide errors
```

---

#### Command 2: `grep` - Search Within Files

**What it does:** Searches for specific text/patterns inside files

**Syntax:** `grep <pattern> <filename>`

**Example:**
```bash
grep "password" file.txt         # Find "password" in file.txt
grep "THM" access.log            # Find lines containing "THM"
grep -i "hello" file.txt         # Case-insensitive search
```

---

**Task 6 Questions & Answers:**

**Question 1:** Use grep on "access.log" to find the flag that has a prefix of "THM". What is the flag?

**Answer:** `THM{ACCESS}`

**Step-by-step:**
```bash
# First, find the access.log file
find . -name "access.log"

# Then, search for lines containing "THM"
grep "THM" access.log

# Output will show:
# THM{ACCESS}
```

**Question 2:** And I still haven't found what I'm looking for!

**Answer:** Click "Complete" to proceed to the next task

---

### Task 7: An Introduction to Shell Operators

**Objective:** Learn how to chain commands and redirect output

#### Shell Operators Explained:

**Operator 1: `;` (Semicolon) - Command Separator**

**What it does:** Runs commands one after another (regardless of success/failure)

**Syntax:** `command1 ; command2`

**Example:**
```bash
echo "Hello" ; echo "World"
# Output:
# Hello
# World
```

---

**Operator 2: `&&` (AND) - Conditional Execution**

**What it does:** Runs the second command ONLY if the first command succeeds

**Syntax:** `command1 && command2`

**Example:**
```bash
cd folder1 && ls              # List only if cd succeeds
mkdir new_folder && cd new_folder  # Create and enter folder
```

---

**Operator 3: `||` (OR) - Alternative Execution**

**What it does:** Runs the second command ONLY if the first command fails

**Syntax:** `command1 || command2`

**Example:**
```bash
cd invalid_folder || echo "Folder not found"
# If cd fails, echo message
```

---

**Operator 4: `>` (Redirect Output)**

**What it does:** Saves command output to a file (overwrites if exists)

**Syntax:** `command > filename`

**Example:**
```bash
echo "Hello" > output.txt      # Create file with "Hello"
ls -la > file_list.txt         # Save file list to file
```

---

**Operator 5: `>>` (Append Output)**

**What it does:** Adds output to the end of a file (doesn't overwrite)

**Syntax:** `command >> filename`

**Example:**
```bash
echo "New line" >> output.txt  # Add to existing file
```

---

**Operator 6: `&` (Background Process)**

**What it does:** Runs a command in the background

**Syntax:** `command &`

**Example:**
```bash
long_running_command &         # Runs in background
# Terminal stays responsive
```

---

**Quick Reference Table:**

| Operator | Name | Function | Example |
|----------|------|----------|---------|
| `;` | Semicolon | Run commands in sequence | `cmd1 ; cmd2` |
| `&&` | AND | Run next if previous succeeds | `cmd1 && cmd2` |
| \|\| | OR | Run next if previous fails | `cmd1 \|\| cmd2` |
| `>` | Redirect | Save output (overwrite) | `cmd > file` |
| `>>` | Append | Add output to file | `cmd >> file` |
| `&` | Background | Run in background | `cmd &` |

---

### Task 8: Continuing Your Learning

**Objective:** Wrap up Part 1 and prepare for Part 2

**Answer:** Click "Complete" to finish Part 1

**What's Next:**
- ✅ Move to Linux Fundamentals Part 2
- ✅ Learn more advanced commands
- ✅ Understand file permissions
- ✅ Learn about users and groups
- ✅ Practice more complex operations

---

## 🔍 Key Commands Cheat Sheet

### Navigation & Viewing:
```bash
pwd              # Print working directory
cd <folder>      # Change directory
ls               # List files
ls -la           # List with details (including hidden files)
cat <file>       # Display file contents
```

### File Operations:
```bash
mkdir <folder>   # Create folder
touch <file>     # Create empty file
cp <src> <dst>   # Copy file
mv <src> <dst>   # Move/rename file
rm <file>        # Delete file
```

### Searching:
```bash
find . -name "file"    # Find file
grep "text" <file>     # Search in file
grep -i "text" <file>  # Case-insensitive search
```

### Useful Commands:
```bash
echo "text"      # Display text
whoami           # Show current user
date             # Show date/time
history          # Show command history
clear            # Clear screen
```

---

## 📝 Important Linux Concepts

### File System Hierarchy:
```
/
├── home/           (User home directories)
├── root/           (Root user home)
├── etc/            (System configuration)
├── var/            (Variable data, logs)
├── tmp/            (Temporary files)
├── bin/            (Essential programs)
└── usr/            (User programs)
```

### Absolute vs Relative Paths:
- **Absolute Path:** Full path from root → `/home/tryhackme/folder`
- **Relative Path:** Path from current location → `folder/subfolder`

### Special Symbols:
- `~` - Home directory
- `.` - Current directory
- `..` - Parent directory
- `/` - Root directory

---

## 🎓 Tips for Success

### ✅ DO:
- Take your time to understand each command
- Practice typing commands yourself
- Use `man <command>` to get help
- Experiment with different options
- Keep a notebook of useful commands

### ❌ DON'T:
- Copy-paste everything (type it out!)
- Skip the practice questions
- Assume you understand without trying
- Delete important system files
- Ignore error messages

---

## 🚀 Next Steps

**After Completing This Room:**
1. ✅ Move to Linux Fundamentals Part 2
2. ✅ Learn file permissions
3. ✅ Understand users and groups
4. ✅ Practice with scripts
5. ✅ Explore advanced Linux features

---

## 📚 Additional Resources

- [Linux Man Pages Online](https://man7.org/linux/man-pages/)
- [Linux Command Line Cheat Sheet](https://linux.die.net/)
- [TryHackMe Linux Fundamentals Part 2](https://tryhackme.com/room/linuxfundamentalspart2)
- [TryHackMe Linux Fundamentals Part 3](https://tryhackme.com/room/linuxfundamentalspart3)

---

## 💡 Common Questions & Troubleshooting

**Q: I don't see any files when I use `ls`**
- A: The directory might be empty, or files might be hidden. Try `ls -la` to show hidden files.

**Q: The command says "command not found"**
- A: The command doesn't exist or isn't installed. Check spelling and try `man <command>` for help.

**Q: My file didn't save**
- A: Make sure you used `>` to redirect output. Without it, text just displays on screen.

**Q: How do I go back to the previous directory?**
- A: Use `cd -` to return to the previous directory you were in.

---

**Room Status:** ✅ Complete  
**Last Updated:** 2026-07-29  
**Difficulty Level:** Easy (Beginner Friendly)  
**Estimated Time:** 1-2 hours

---

**Ready to move on to Part 2?** You've now learned the fundamentals! 🎉
