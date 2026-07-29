# Windows Fundamentals Writeup

**Difficulty:** Easy  
**Room Link:** https://tryhackme.com/room/windowsfundamentals1xbx  
**Time to Complete:** 1-2 hours

---

## 📚 Overview

Windows Fundamentals is an introductory room that teaches you the basics of the Windows operating system. This writeup covers everything you need to know to complete this room, from understanding the Windows desktop to working with the command line.

---

## 🎯 Learning Objectives

By completing this room, you'll understand:
- ✅ Windows operating system structure
- ✅ Key Windows components and terminology
- ✅ How to navigate the Windows GUI
- ✅ Introduction to the Command Line (CMD and PowerShell)
- ✅ Basic Windows file system hierarchy
- ✅ User accounts and permissions basics
- ✅ Windows security fundamentals

---

## 📋 Task Breakdown & Solutions

### Task 1: What is Windows? - Fundamentals

**Question:** What term describes a collection of instructions that tell the computer to do something?

**Answer:** `Program`

**Explanation:** A program is a set of instructions written in code that a computer executes to perform specific tasks.

---

**Question:** If you have Windows 10 or Windows 11 installed, what year was it released?

**Answer:** 
- Windows 10: `2015`
- Windows 11: `2021`

**Explanation:** These are the official release years for these operating systems.

---

### Task 2: Windows Editions

**Question:** What Windows edition is used in most workplaces?

**Answer:** `Windows Pro` or `Enterprise`

**Explanation:** 
- **Windows Pro** - Used in small to medium businesses
- **Windows Enterprise** - Used in large organizations
- Both have advanced security and management features

**Key Editions:**
- **Windows Home** - For personal/home use
- **Windows Pro** - For small businesses and professionals
- **Windows Enterprise** - For large organizations
- **Windows Server** - For server operations

---

### Task 3: The Desktop

**Question:** What is displayed in the bottom-left of the screen on Windows?

**Answer:** `Taskbar` or `Start Button`

**Explanation:** The taskbar shows running applications and the Start menu button (Windows logo).

---

**Question:** What does the taskbar typically display?**

**Answer:** 
- Currently open applications
- System tray (time, volume, network status)
- Quick launch buttons
- Notification area

**Key Desktop Components:**
1. **Desktop** - Main work area with icons
2. **Taskbar** - Bottom panel showing open apps
3. **System Tray** - Bottom-right corner with system info
4. **Start Menu** - Access to programs and settings

---

### Task 4: The File System

**Question:** What is the root of the file system in Windows?

**Answer:** `C:\` (C drive)

**Explanation:** By default, Windows installs on the C: drive, which serves as the root/primary drive.

---

**Question:** What are the main directories under C:\?

**Answer:**
```
C:\
├── Users              (User profiles and personal files)
├── Windows            (Operating system files)
├── Program Files      (64-bit applications)
├── Program Files (x86)(32-bit applications)
└── ProgramData        (Application data)
```

**Important Directories:**
- `C:\Users` - Contains user profiles (Documents, Downloads, Desktop, etc.)
- `C:\Windows` - Core OS files (NEVER delete!)
- `C:\Program Files` - Installed applications
- `C:\Windows\System32` - Critical system files

---

### Task 5: User Accounts

**Question:** What are the types of user accounts in Windows?

**Answer:**
1. **Administrator** - Full system access
2. **Standard User** - Limited access
3. **Guest** - Temporary limited access

**Explanation:**
- **Administrator accounts** can install software, change system settings, and manage other users
- **Standard user accounts** can run programs but can't make system changes
- **Guest accounts** have very limited functionality

---

**Question:** Where do you find user account settings?

**Answer:** 
- **Windows 10/11:** Settings → Accounts
- **Alternative:** Control Panel → User Accounts

**Step-by-step to view users:**
1. Open Settings (Win + I)
2. Click on "Accounts"
3. View your current user account
4. Click "Other people" to see other accounts

---

### Task 6: User Account Control (UAC)

**Question:** What is UAC and what does it do?

**Answer:** User Account Control is a security feature that prompts for permission when making system-wide changes.

**Explanation:**
- UAC protects your computer from unauthorized changes
- When you try to install software or change settings, UAC asks for approval
- Prevents malware from making changes without permission
- Can be disabled but NOT recommended

**UAC Prompt Example:**
```
"Do you want to allow this app to make changes to your device?"
[Yes] [No]
```

---

### Task 7: File Properties & Attributes

**Question:** How do you view file properties in Windows?

**Answer:** Right-click on file → "Properties"

**Key Properties:**
- **Name** - File name
- **Type** - File type (.txt, .exe, .pdf, etc.)
- **Size** - File size in bytes/MB/GB
- **Location** - Full file path
- **Created/Modified** - Date and time stamps
- **Security** - Who can access this file

**To view file properties:**
1. Right-click on any file
2. Select "Properties"
3. View all details

---

### Task 8: Run Commands (CMD)

**Question:** What is the Run dialog and how do you open it?

**Answer:** Win + R (Windows logo key + R)

**Explanation:** The Run dialog allows you to execute commands or open programs quickly.

**Common Run Commands:**
```
cmd              - Open Command Prompt
powershell       - Open PowerShell
notepad          - Open Notepad
calc             - Open Calculator
mstsc            - Remote Desktop Connection
devmgmt.msc      - Device Manager
diskmgmt.msc     - Disk Management
eventvwr.msc     - Event Viewer
services.msc     - Services
taskmgr          - Task Manager
```

**How to use:**
1. Press Win + R
2. Type command name
3. Press Enter

---

### Task 9: Command Prompt (CMD)

**Question:** What is Command Prompt?

**Answer:** A command-line interface where you can type commands to control Windows.

**Opening CMD:**
1. Press Win + R
2. Type `cmd`
3. Press Enter
4. Or search "Command Prompt" in Start Menu

**Basic CMD Commands:**

```batch
dir              - List files and folders
cd <folder>      - Change directory
cd ..            - Go to parent directory
mkdir <name>     - Create new folder
echo <text>      - Display text
type <file>      - Display file contents
ipconfig         - Show network configuration
systeminfo       - Display system information
tasklist         - Show running processes
whoami           - Show current user
date /t          - Show current date
time /t          - Show current time
cls              - Clear screen
exit             - Close Command Prompt
```

**Example Usage:**
```batch
C:\> dir
C:\> cd Users
C:\Users> dir
C:\Users> ipconfig
C:\Users> whoami
```

---

### Task 10: PowerShell

**Question:** What is PowerShell?

**Answer:** A more advanced command-line interface with more powerful features than Command Prompt.

**Key Differences:**
| Feature | CMD | PowerShell |
|---------|-----|-----------|
| Scripting | Basic | Advanced |
| Objects | Text | Full objects |
| Flexibility | Limited | Extensive |
| Error Handling | Basic | Robust |
| Learning Curve | Easy | Moderate |

**Opening PowerShell:**
1. Press Win + R
2. Type `powershell`
3. Press Enter
4. Or search in Start Menu

**Basic PowerShell Commands:**
```powershell
Get-ChildItem      - List files (like dir)
Set-Location       - Change directory (like cd)
New-Item          - Create files/folders
Get-Process       - Show running processes
Get-ExecutionPolicy - Check script permissions
Get-NetIPConfiguration - Network info
Get-WmiObject Win32_OperatingSystem - OS info
```

---

### Task 11: Windows Security & Firewall

**Question:** Where is Windows Defender/Firewall located?

**Answer:** Settings → Privacy & Security → Windows Security

**Steps to access:**
1. Open Settings (Win + I)
2. Go to "Privacy & Security"
3. Click "Windows Security"
4. View different security options

**Windows Security Components:**
- **Virus & threat protection** - Antivirus/Malware
- **Firewall** - Network protection
- **App & browser control** - Protection settings
- **Device security** - Hardware security

---

### Task 12: Updates & Maintenance

**Question:** How do you check for Windows updates?

**Answer:** Settings → Update & Security → Windows Update

**Steps:**
1. Open Settings (Win + I)
2. Go to "System"
3. Click "About"
4. Scroll down to "Windows Update" or go to Settings → Update & Security

**Why Updates Matter:**
- ✅ Security patches (critical!)
- ✅ Bug fixes
- ✅ Performance improvements
- ✅ New features

---

## 🔍 Key Concepts Summary

| Concept | Description |
|---------|-------------|
| **File System** | C:\ drive with Users, Windows, Program Files |
| **User Accounts** | Admin, Standard, Guest with different permissions |
| **UAC** | Security prompts for system changes |
| **CMD** | Basic command-line interface |
| **PowerShell** | Advanced command-line with scripting |
| **Firewall** | Network protection tool |
| **Defender** | Built-in antivirus protection |

---

## 📝 Important Notes

1. **Never delete Windows system files** - Stay out of C:\Windows unless you know what you're doing
2. **Use Administrator account carefully** - Only when necessary
3. **Keep updates installed** - Security is critical
4. **Back up important data** - Before major changes
5. **Use strong passwords** - Protect your accounts

---

## 🎓 Best Practices

### ✅ DO:
- Keep Windows updated
- Use strong, unique passwords
- Enable Windows Defender
- Regular backups
- Use a Standard user account for daily use
- Lock your computer (Win + L)

### ❌ DON'T:
- Download unknown files
- Disable Windows Defender
- Run everything as Administrator
- Share your password
- Ignore UAC prompts
- Delete system files

---

## 🚀 Next Steps

After completing this room:
1. ✅ Explore the Windows GUI thoroughly
2. ✅ Practice basic CMD commands
3. ✅ Learn PowerShell scripting
4. ✅ Move to "Windows Exploitation Basics"
5. ✅ Study Windows privilege escalation

---

## 📚 Additional Resources

- [Microsoft Windows Documentation](https://docs.microsoft.com/en-us/windows/)
- [PowerShell Documentation](https://docs.microsoft.com/en-us/powershell/)
- [Windows Security Best Practices](https://www.microsoft.com/en-us/security/)

---

**Room Status:** ✅ Complete  
**Last Updated:** 2026-07-27  
**Difficulty Level:** Easy (Beginner Friendly)
