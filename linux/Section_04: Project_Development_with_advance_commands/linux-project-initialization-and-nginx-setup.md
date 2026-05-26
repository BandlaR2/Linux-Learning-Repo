# Linux Project Development with Advanced Commands

## Overview
This project focuses on learning Linux administration and file system concepts through a practical approach using Nginx on an Amazon Linux EC2 instance.

## Topics Covered

### System Control Commands
- Understanding `systemctl`
- Managing Linux services (daemons)
- Starting and stopping services
- Enabling services at boot
- Checking service status

### Nginx Service Management Commands

Check service status:

```bash
systemctl status nginx
```

Start service:

```bash
systemctl start nginx
```

Stop service:

```bash
systemctl stop nginx
```

Restart service:

```bash
systemctl restart nginx
```

Enable service at boot:

```bash
systemctl enable nginx
```

Disable service at boot:

```bash
systemctl disable nginx
```

Check enable status:

```bash
systemctl is-enabled nginx
```

---

### File Navigation Commands

Change directory:

```bash
cd
```

Display current directory:

```bash
pwd
```

List files and folders:

```bash
ls
```

List hidden files:

```bash
ls -la
```

Move to parent directory:

```bash
cd ..
```

Move to root directory:

```bash
cd /
```

---

### Linux File System Hierarchy

Important Linux directories:

- `/` → Root directory
- `/bin` → Executable commands
- `/boot` → Boot files
- `/dev` → Device files
- `/etc` → Configuration files
- `/home` → User directories
- `/root` → Root user directory
- `/tmp` → Temporary files
- `/usr` → User programs
- `/var` → Logs and changing data

---

### Nginx HTML Directory

Default location:

```bash
/usr/share/nginx/html
```

Navigate:

```bash
cd /usr/share/nginx/html
```

List files:

```bash
ls
```

Read file content:

```bash
cat index.html
```

---

## Technologies Used

- Linux
- AWS EC2
- Nginx
- SSH

## Outcome

- Learned Linux service management
- Understood Linux navigation commands
- Explored Linux file system hierarchy
- Located Nginx web files
- Prepared environment for website deployment