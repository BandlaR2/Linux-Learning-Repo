````md
# Linux Project Completion and Advanced Commands

## Overview
This section focuses on completing the static website deployment project and learning Linux tools used for file management, text editing, package management, and user privileges.

## Topics Covered

### File Management Commands

#### View file contents
```bash
cat index.html
```
Displays file content.

#### View multiple files
```bash
cat index.html file.txt
```
Displays contents of multiple files.

#### Add line numbers
```bash
cat -n index.html
```
Shows line numbers.

#### Merge files
```bash
cat file1 file2 > newfile.txt
```
Combines files into a new file.

---

### File Creation

Create file:

```bash
touch file.txt
```

Create multiple files:

```bash
touch file1.txt file2.txt file3.txt
```

---

### Remove Files

Delete file:

```bash
rm file.txt
```

Delete with confirmation:

```bash
rm -i file.txt
```

Delete directory:

```bash
rm -r foldername
```

---

### Secure File Transfer (SCP)

Copy local file to EC2:

```bash
scp -i mykey.pem file.zip ec2-user@IP:/home/ec2-user/
```

Copy EC2 file to local system:

```bash
scp -i mykey.pem ec2-user@IP:/home/ec2-user/file.txt .
```

---

### Extract ZIP Files

```bash
unzip file.zip
```

Extracts compressed files.

---

### Move Files

```bash
mv source destination
```

Move website files:

```bash
mv mywebsite/* /usr/share/nginx/html/
```

---

## Text Editors

### Nano
Simple editor for beginners.

Open file:

```bash
nano index.html
```

Commands:

- Save → CTRL + O
- Exit → CTRL + X

---

### Vi

Open file:

```bash
vi index.html
```

Commands:

- Insert mode → i
- Save and exit → :wq
- Exit without saving → :q!

---

### Vim

Open file:

```bash
vim index.html
```

Commands:

- Insert mode → i
- Save and exit → :wq

---

## Package Management

### Yum (Amazon Linux/CentOS)

Update system:

```bash
sudo yum update -y
```

Install package:

```bash
sudo yum install nano -y
```

Remove package:

```bash
sudo yum remove nano -y
```

---

### APT (Ubuntu/Debian)

Update:

```bash
sudo apt update
sudo apt upgrade -y
```

Install:

```bash
sudo apt install apache2 -y
```

Remove:

```bash
sudo apt remove nano -y
```

---

## Sudo Commands

Run command with administrator access:

```bash
sudo yum install nginx -y
```

Check user details:

```bash
id
```

Check sudo permissions:

```bash
sudo -l
```

Edit sudo file:

```bash
sudo visudo
```

Add user privileges:

```bash
ec2-user ALL=(ALL) ALL
```

---

## Technologies Used

- Linux
- AWS EC2
- Nginx
- SSH
- Nano
- Vim
- Yum

---

## Outcome

- Hosted static website successfully
- Learned file operations
- Learned text editors
- Understood package managers
- Managed user permissions with sudo
````
