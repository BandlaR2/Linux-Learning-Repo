````md
# Linux System Administration and Management

## Overview
Linux system administration involves managing files, users, permissions, processes, networking, and system resources. These concepts are widely used in Cloud, DevOps, and server administration.

---

# 1. File and Directory Permissions

Linux permissions control who can access files and what actions they can perform.

## Permission Types

- `r (Read)` → View file content
- `w (Write)` → Modify file content
- `x (Execute)` → Run file as program

Permissions apply to:

- `u` → User/Owner
- `g` → Group
- `o` → Others

### View Permissions

```bash
ls -l
```

Example:

```bash
-rw-r--r-- 1 ec2-user ec2-user file.txt
```

Explanation:

- `-` → Regular file
- `rw-` → Owner has read and write
- `r--` → Group has read
- `r--` → Others have read

### Change Permissions

```bash
chmod 755 file.sh
```

Explanation:

- `7` → Read + Write + Execute
- `5` → Read + Execute
- `5` → Read + Execute

Add execute permission:

```bash
chmod u+x file.sh
```

### Change Ownership

```bash
chown user file.txt
```

Changes file owner.

```bash
chgrp developers file.txt
```

Changes file group.

### ACL (Advanced Permissions)

View ACL:

```bash
getfacl file.txt
```

Set ACL:

```bash
setfacl -m u:user:rw file.txt
```

Allows specific permissions to a user.

---

# 2. User and Group Management

Linux supports multiple users sharing the same system.

## Create User

```bash
sudo useradd aj
```

Creates user account.

## Set Password

```bash
sudo passwd aj
```

Assigns password.

## Switch User

```bash
su aj
```

Switches to another user.

## Delete User

```bash
sudo userdel -r aj
```

Deletes user and home directory.

## Create Group

```bash
sudo groupadd developers
```

Creates group.

## Add User to Group

```bash
sudo usermod -aG developers aj
```

- `-a` → Append
- `-G` → Secondary group

Check groups:

```bash
groups aj
```

Shows all groups of user.

---

# 3. Compression and Archiving

Compression reduces file size while archiving combines multiple files.

## Extract ZIP

```bash
unzip file.zip
```

Extracts compressed file.

## Create ZIP

```bash
zip backup.zip file.txt
```

Compresses file.

Compress folder:

```bash
zip -r backup.zip project/
```

- `-r` → Recursive

## Create TAR Archive

```bash
tar -cf backup.tar folder/
```

- `c` → Create
- `f` → Filename

Compress TAR using GZIP:

```bash
tar -czf backup.tar.gz folder/
```

- `z` → Gzip compression

Extract TAR:

```bash
tar -xzf backup.tar.gz
```

- `x` → Extract

---

# 4. Process Management

Processes are running applications or services.

## View Processes

```bash
ps -e
```

Shows running processes.

## Search Process

```bash
ps aux | grep nginx
```

Explanation:

- `ps aux` → Display all processes
- `grep nginx` → Search nginx

## Real-time Monitoring

```bash
top
```

Displays:

- CPU usage
- Memory usage
- Running processes

Exit:

```bash
Q
```

## Stop Process

```bash
kill PID
```

Terminates process.

Force stop:

```bash
kill -9 PID
```

Forcefully stops process.

## Process Tree

```bash
pstree
```

Shows parent-child relationship.

---

# 5. Networking Commands

Used for checking connectivity and network details.

## View Network Interfaces

```bash
ifconfig
```

Displays:

- IP address
- MAC address
- Network interface

## Test Internet Connection

```bash
ping google.com
```

Checks connectivity.

Stop:

```bash
CTRL + C
```

## View Network Statistics

```bash
netstat -t
```

Shows active TCP connections.

## Remote Access

```bash
ssh -i key.pem ec2-user@IP
```

Connects securely to remote server.

## Download Files

```bash
wget URL
```

Downloads file from internet.

## DNS Information

```bash
dig google.com
host google.com
```

Displays IP and DNS details.

## View Hostname

```bash
hostname
```

Shows system hostname.

---

# 6. System Information Commands

Used to monitor system health and resources.

## System Information

```bash
uname -a
```

Displays:

- Operating system
- Kernel version
- Architecture

## Check Uptime

```bash
uptime
```

Displays:

- Running time
- Number of users
- Load average

## Current User

```bash
whoami
```

Displays current user.

## Logged-in Users

```bash
who
```

Displays active users.

## Disk Usage

```bash
df -h
```

Displays:

- Total storage
- Used storage
- Available storage

Check directory size:

```bash
du -sh folder/
```

- `s` → Summary
- `h` → Human readable

## Memory Usage

```bash
free -h
```

Displays:

- Total RAM
- Used RAM
- Free RAM
- Swap memory

---

# Technologies Used

- Linux
- AWS EC2
- Nginx
- SSH

---

# Outcome

- Learned file permissions and ownership
- Managed users and groups
- Worked with archives and compression
- Monitored system processes
- Used networking commands
- Monitored system resources
````
