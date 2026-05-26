````md
# Linux Project Initialization

## Project Overview
This project helps us learn Linux through a practical scenario by hosting a static blog website on an Amazon Linux EC2 instance using Nginx. Instead of only studying commands, we perform real-world tasks used by Cloud and DevOps engineers.

---

# Linux Command Categories

Linux commands are grouped into categories based on their purpose.

## 1. System Information
These commands provide information about the system.

Examples:

```bash
whoami
hostname
df -h
```

Explanation:

- `whoami` → Displays the current logged-in user.
- `hostname` → Displays the system name.
- `df -h` → Shows available disk space in a readable format.

---

## 2. Navigation Commands

Used for moving through directories.

Examples:

```bash
pwd
ls
cd
```

Explanation:

- `pwd` → Print Working Directory; shows current location.
- `ls` → Lists files and folders.
- `cd` → Changes directory.

Example:

```bash
cd /home
```

Moves to the home directory.

---

## 3. File Operations

Used to create and manage files.

Examples:

```bash
touch
mkdir
cp
mv
rm
```

Explanation:

- `touch` → Creates empty file
- `mkdir` → Creates folder
- `cp` → Copies files
- `mv` → Moves or renames files
- `rm` → Deletes files

Example:

```bash
touch test.txt
mkdir project
```

---

## 4. File Permissions

Used to control file access.

Examples:

```bash
chmod
chown
```

Explanation:

- `chmod` → Changes permissions
- `chown` → Changes ownership

Example:

```bash
chmod 777 file.txt
```

Gives read, write, and execute permissions.

---

## 5. User and Group Management

Used to create and manage users.

Examples:

```bash
useradd
userdel
groupadd
```

Explanation:

- `useradd` → Creates user
- `userdel` → Deletes user
- `groupadd` → Creates group

---

## 6. Text Processing

Used to search and process text.

Examples:

```bash
grep
awk
sort
```

Explanation:

- `grep` → Searches specific text
- `awk` → Extracts fields
- `sort` → Sorts content

Example:

```bash
grep nginx file.txt
```

Searches for nginx inside file.

---

## 7. Process Management

Used to monitor running applications.

Examples:

```bash
ps
top
kill
```

Explanation:

- `ps` → Displays running processes
- `top` → Displays real-time system activity
- `kill` → Stops process

Example:

```bash
kill 1234
```

Stops process with ID 1234.

---

## 8. Package Management

Used to install software packages.

Example:

```bash
yum install nginx -y
```

Explanation:

- `yum` → Package manager in Amazon Linux
- `install` → Installs package
- `nginx` → Package name
- `-y` → Automatically confirms installation

---

## 9. Networking

Used for network-related operations.

Examples:

```bash
ping
curl
netstat
```

Explanation:

- `ping` → Checks connectivity
- `curl` → Transfers data
- `netstat` → Displays network information

---

## 10. Compression and Archiving

Used for compressing files.

Examples:

```bash
zip
unzip
tar
```

Explanation:

- `zip` → Compress files
- `unzip` → Extract ZIP files
- `tar` → Archive files

---

## 11. System Control

Used for managing services.

Example:

```bash
systemctl
```

Actions:

```bash
systemctl start nginx
systemctl stop nginx
systemctl restart nginx
systemctl status nginx
```

Explanation:

- `start` → Starts service
- `stop` → Stops service
- `restart` → Restarts service
- `status` → Displays current state

---

# Resources Required

### 1. Amazon Linux EC2 Instance
A virtual server running on AWS used for project setup.

### 2. Nginx Web Server
Nginx is software used to deliver website content to users.

Reasons for using Nginx:

- Fast performance
- Lightweight
- Supports high traffic
- Popular in cloud environments

### 3. SSH Terminal

SSH allows secure access to the EC2 server.

Examples:

- Windows → PowerShell
- Linux → Terminal
- macOS → Terminal

---

# Step-by-Step Project Setup

## Step 1: Check Current User

Command:

```bash
whoami
```

Output:

```bash
ec2-user
```

Explanation:

Shows which user is currently logged in.

---

## Step 2: Check Current Directory

Command:

```bash
pwd
```

Output:

```bash
/home/ec2-user
```

Explanation:

Displays current working location.

---

## Step 3: Switch to Root User

Command:

```bash
sudo su
```

Explanation:

- `sudo` → Run command with admin privileges
- `su` → Switch user

Prompt changes:

```bash
$
```

to

```bash
#
```

`#` indicates root access.

---

## Step 4: Verify Current Directory

Command:

```bash
pwd
```

Explanation:

Checks whether directory changed.

---

## Step 5: Install Nginx

Command:

```bash
yum install nginx -y
```

Explanation:

Downloads and installs Nginx from online repositories.

---

# Final Outcome

Successfully:

- Connected to EC2 using SSH
- Learned Linux command categories
- Verified user and directory
- Switched to root user
- Installed Nginx
- Prepared Linux environment for static website hosting
````
