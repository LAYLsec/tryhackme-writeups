# 🐧 TryHackMe: Linux Fundamentals Part 1 — Walkthrough & Solutions

This room is tailored for beginners stepping into the world of cybersecurity and ethical hacking, introducing basic navigation and terminal commands inside an in-browser Linux machine.


### Task 1: Introduction

* **Overview:** A brief introduction to what you will learn in the room.
* **Question:** Let's get started!
* **Answer:** `No answer needed` (Click 'Complete')


### Task 2: A Bit of Background on Linux

* **Overview:** Covers what Linux is, its history, and where it's used (e.g., websites, car entertainment systems, traffic lights).
* **Question:** Research: What year was the first release of a Linux operating system?
* **Answer:** `1991`


### Task 3: Interacting With Your First Linux Machine (In-Browser)

* **Overview:** Deploy the machine using the green **"Start Machine"** button to access the terminal directly in your browser.
* **Question:** I've deployed my first Linux machine!
* **Answer:** `No answer needed`


### Task 4: Running Your First few Commands

Introduces two fundamental terminal commands:

* `echo`: Prints text to the screen.
* `whoami`: Displays your current logged-in username.
* **Question 1:** If we wanted to output the text “TryHackMe”, what would our command be?
* **Answer:** `echo TryHackMe`


* **Question 2:** What is the username of who you're logged in as on your deployed Linux machine?
* **Answer:** `tryhackme`




### Task 5: Interacting With the Filesystem!

Teaches core filesystem navigation commands:

* `ls`: Lists files and directories.
* `cd`: Changes directory.
* `cat`: Outputs the content of a file.
* `pwd`: Prints the working directory path.
* **Question 1:** On the Linux machine that you deploy, how many folders are there?
* **Answer:** `4`


* **Question 2:** Which directory contains a file?
* **Answer:** `folder4`


* **Question 3:** What is the contents of this file?
* **Answer:** `Hello World!`


* **Question 4:** Use the cd command to navigate to this file and find out the new current working directory. What is the path?
* **Answer:** `/home/tryhackme/folder4`




### Task 6: Searching for Files

Covers advanced searching utility tools:

* `find`: Searches for files across directories.
* `grep`: Searches for specific text inside files.
* **Question 1:** Use grep on "access.log" to find the flag that has a prefix of "THM". What is the flag?
* **Answer:** `THM{ACCESS}`


* **Question 2:** And I still haven't found what I'm looking for!
* **Answer:** `No answer needed`




### Task 7: An Introduction to Shell Operators

Explains terminal redirection and operational symbols:

* `&`: Runs commands in the background.
* `&&`: Chains commands sequentially (runs the second command only if the first succeeds).
* `>`: Redirects command output to a file, overwriting existing content.
* `>>`: Appends output to the end of a file without overwriting.


### Task 8 & 9: Conclusions & Next Steps

* Wraps up the basics of Linux terminal operations.
* **Answer:** `No answer needed` to complete the room and move on to **Linux Fundamentals Part 2**.


For a visual walkthrough of setting up and navigating this room, you can check out [Learn the Linux Fundamentals Part 1 video tutorial](https://www.youtube.com/watch?v=DuGR9uCiRyM).
