====================================================
# LINUX FOR DEVOPS - PART 1
### Linux Fundamentals & Core Commands

====================================================

### BASIC SYSTEM COMMANDS

pwd → Shows current working directory
Example:
pwd
Output:
/home/ubuntu

----------------------------------------------------

whoami → Displays currently logged-in username
Example:
whoami
Output:
ubuntu

----------------------------------------------------

hostname → Displays server/computer name
Example:
hostname
Output:
dev-server01

----------------------------------------------------

date → Shows current system date and time
Example:
date
Output:
Tue May 26 18:45:30 IST 2026

----------------------------------------------------

uptime → Shows how long system is running with load details
Example:
uptime
Output:
18:45 up 5 days, 2 users

----------------------------------------------------

uname → Displays operating system name
Example:
uname
Output:
Linux

----------------------------------------------------

uname -a → Shows complete system details
Example:
uname -a
Output:
Linux ubuntu-server 6.8 x86_64 GNU/Linux

====================================================

### FILE NAVIGATION COMMANDS

ls → Lists files and folders in current directory
Example:
ls
Output:
project file1.txt test.sh

----------------------------------------------------

ls -l → Shows detailed file information
Example:
ls -l
Output:
-rw-r--r-- 1 ubuntu ubuntu 500 file1.txt

----------------------------------------------------

ls -a → Displays all files including hidden files
Example:
ls -a
Output:
. .. .git .bashrc file1.txt

----------------------------------------------------

ls -lh → Shows file sizes in human-readable format
Example:
ls -lh
Output:
-rw-r--r-- 1 ubuntu ubuntu 2K file.txt

----------------------------------------------------

cd foldername → Moves into specified directory
Example:
cd project

----------------------------------------------------

cd .. → Moves one directory backward
Example:
cd ..

----------------------------------------------------

cd ~ → Moves to user's home directory
Example:
cd ~

----------------------------------------------------

tree → Displays folder structure in tree format
Example:
tree
Output:

project
├── file1.txt
├── images
└── scripts

----------------------------------------------------

find . -name file.txt → Searches for file in current directory and subdirectories
Example:
find . -name test.txt
Output:
./documents/test.txt

----------------------------------------------------

locate nginx.conf → Quickly searches file path in database
Example:
locate nginx.conf
Output:
/etc/nginx/nginx.conf

====================================================

### FILE OPERATIONS

touch file.txt → Creates empty file
Example:
touch notes.txt

----------------------------------------------------

mkdir project → Creates a new folder
Example:
mkdir project

----------------------------------------------------

mkdir project1 project2 → Creates multiple folders
Example:
mkdir devops docker

----------------------------------------------------

cp file1 file2 → Copies file content to another file
Example:
cp data.txt backup.txt

----------------------------------------------------

cp -r folder1 folder2 → Copies folder and all files recursively
Example:
cp -r project backup_project

----------------------------------------------------

mv old.txt new.txt → Renames or moves file
Example:
mv file1.txt file2.txt

----------------------------------------------------

rm file.txt → Deletes file
Example:
rm notes.txt

----------------------------------------------------

rm -r folder → Deletes folder with files
Example:
rm -r project

----------------------------------------------------

rm -rf folder → Forcefully deletes folder without confirmation
Example:
rm -rf temp

Warning:
Very dangerous command. Can permanently delete data.

====================================================

### TEXT VIEW COMMANDS

cat file.txt → Displays complete file content
Example:
cat notes.txt

Output:
Hello
Linux Learning
DevOps

----------------------------------------------------

head file.txt → Shows first 10 lines of file
Example:
head notes.txt

----------------------------------------------------

head -5 file.txt → Shows first 5 lines
Example:
head -5 logfile.txt

----------------------------------------------------

tail file.txt → Shows last 10 lines
Example:
tail logfile.txt

----------------------------------------------------

tail -f logfile.txt → Continuously monitors live log updates
Example:
tail -f /var/log/syslog

Use Case:
DevOps engineers use this to monitor application logs.

----------------------------------------------------

less file.txt → Opens file page by page
Example:
less largefile.txt

Controls:
Space → Next page
b → Previous page
q → Exit

====================================================

### TEXT EDITORS

nano file.txt → Opens file using Nano editor
Example:
nano app.conf

Commands:

CTRL + X → Exit editor

CTRL + O → Save file

CTRL + K → Cut line

CTRL + U → Paste line

----------------------------------------------------

vim file.txt → Opens file in Vim editor
Example:
vim app.conf

Commands:

i → Enter insert mode

Esc → Return to command mode

:w → Save file

:q → Exit

:wq → Save and quit

:q! → Exit without saving

dd → Delete line

yy → Copy line

p → Paste line

====================================================