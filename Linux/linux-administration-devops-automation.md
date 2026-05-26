====================================================
# LINUX FOR DEVOPS - PART 2
### Linux Administration, DevOps & Automation

====================================================

###  PERMISSIONS

Read = r = 4 → Permission to view file contents

Write = w = 2 → Permission to modify file contents

Execute = x = 1 → Permission to run file/program

Example:

-rwxr-xr-x

Explanation:

First character (-) → File type

rwx → Owner permissions (Read + Write + Execute)

r-x → Group permissions (Read + Execute)

r-x → Others permissions (Read + Execute)

----------------------------------------------------

Permission values:

777 → Full access for owner, group and others

Example:
chmod 777 file.txt

----------------------------------------------------

755 → Owner has full access, others can read and execute

Example:
chmod 755 script.sh

----------------------------------------------------

644 → Owner has read/write, others only read

Example:
chmod 644 file.txt

----------------------------------------------------

Commands:

chmod 755 file.sh → Changes file permission to 755

Example:
chmod 755 deploy.sh

----------------------------------------------------

chmod +x script.sh → Adds execute permission

Example:
chmod +x backup.sh

----------------------------------------------------

chown user file.txt → Changes file owner

Example:
chown nandy report.txt

----------------------------------------------------

chown user:group file.txt → Changes owner and group

Example:
chown nandy:devops report.txt

----------------------------------------------------

chgrp developers file.txt → Changes group ownership

Example:
chgrp devops file.txt

====================================================

### USER MANAGEMENT

useradd nandy → Creates new user account

Example:
sudo useradd nandy

----------------------------------------------------

passwd nandy → Sets password for user

Example:
sudo passwd nandy

----------------------------------------------------

userdel nandy → Deletes user account

Example:
sudo userdel nandy

----------------------------------------------------

userdel -r nandy → Deletes user with home directory

Example:
sudo userdel -r nandy

----------------------------------------------------

groupadd devops → Creates new group

Example:
sudo groupadd devops

----------------------------------------------------

usermod -aG devops nandy → Adds user into group

Example:
sudo usermod -aG devops nandy

====================================================

###  PROCESS MANAGEMENT

ps → Shows current running processes

Example:
ps

----------------------------------------------------

ps -ef → Shows complete process details

Example:
ps -ef

Output:
UID PID PPID CMD
root 250 nginx

----------------------------------------------------

top → Shows real-time process usage

Example:
top

Shows:

• CPU usage
• Memory usage
• Running processes

----------------------------------------------------

htop → Advanced interactive process monitor

Example:
htop

----------------------------------------------------

kill processid → Stops process normally

Example:
kill 3456

----------------------------------------------------

kill -9 processid → Forcefully kills process

Example:
kill -9 3456

====================================================

###  NETWORK COMMANDS

ping google.com → Checks network connectivity

Example:
ping google.com

----------------------------------------------------

curl google.com → Fetches webpage/API content

Example:
curl https://google.com

----------------------------------------------------

wget fileurl → Downloads files from internet

Example:
wget https://example.com/file.zip

----------------------------------------------------

netstat -tuln → Displays listening ports and connections

Options:

t → TCP
u → UDP
l → Listening
n → Numeric values

Example:
netstat -tuln

----------------------------------------------------

ss -tuln → Faster replacement for netstat

Example:
ss -tuln

----------------------------------------------------

traceroute google.com → Displays path packets travel

Example:
traceroute google.com

----------------------------------------------------

nslookup google.com → Finds DNS information

Example:
nslookup google.com

----------------------------------------------------

ip a → Displays network interfaces and IP addresses

Example:
ip a

====================================================

### PACKAGE MANAGEMENT

Ubuntu:

sudo apt update → Updates package list

Example:
sudo apt update

----------------------------------------------------

sudo apt upgrade → Upgrades installed packages

Example:
sudo apt upgrade

----------------------------------------------------

sudo apt install nginx → Installs package

Example:
sudo apt install nginx

----------------------------------------------------

sudo apt remove nginx → Removes package

Example:
sudo apt remove nginx

----------------------------------------------------

sudo apt autoremove → Removes unused packages

Example:
sudo apt autoremove

====================================================

### COMPRESSION

tar -cvf file.tar folder → Creates tar archive

Options:

c → Create
v → Verbose
f → File

Example:
tar -cvf backup.tar project

----------------------------------------------------

tar -xvf file.tar → Extracts tar archive

Options:

x → Extract
v → Verbose
f → File

Example:
tar -xvf backup.tar

----------------------------------------------------

gzip file.txt → Compresses file

Example:
gzip report.txt

Output:
report.txt.gz

----------------------------------------------------

gunzip file.txt.gz → Decompresses file

Example:
gunzip report.txt.gz

----------------------------------------------------

unzip file.zip → Extracts zip file

Example:
unzip project.zip

====================================================

### SHELL SCRIPT INTRODUCTION

Example:

#!/bin/bash

echo "Hello DevOps"

name="Nandy"

echo $name

Explanation:

#!/bin/bash → Defines bash shell interpreter

echo → Prints output

name="Nandy" → Creates variable

echo $name → Displays variable value

Output:

Hello DevOps
Nandy

====================================================

### SHELL SCRIPT WITH CONDITION

Example:

#!/bin/bash

num=10

if [ $num -gt 5 ]
then
echo "Greater"
else
echo "Smaller"
fi

Explanation:

if → Starts condition

-gt → Greater than

then → Executes if condition is true

else → Executes if condition is false

fi → Ends if statement

Output:

Greater

====================================================

### REAL DEVOPS SCENARIO

Problem:

Website is down

##### Step 1:

SSH into server

ssh ubuntu@IP

Explanation:
Connects to remote Linux server

----------------------------------------------------

##### Step 2:

Check process

ps -ef

Explanation:
Checks whether application process is running

----------------------------------------------------

##### Step 3:

Check logs

cd /var/log

tail -f application.log

Explanation:
Monitors logs in real time to identify errors

----------------------------------------------------

##### Step 4:

Restart service

sudo systemctl restart nginx

Explanation:
Restarts Nginx web server

----------------------------------------------------

##### Step 5:

Verify status

sudo systemctl status nginx

Explanation:
Checks whether service is active and running

====================================================