# Shell Scripting Basics

## Overview
This module introduces Shell Scripting in Linux and explains how scripts automate repetitive tasks. Shell scripts allow multiple commands to execute automatically in sequence, improving efficiency in system administration and DevOps tasks.

## Topics Covered

### Understanding Shell
Shell acts as an interface between the user and the Linux kernel.

Types of shells:
- Bash (Bourne Again Shell)
- Z Shell (Zsh)
- C Shell (CSH)
- Korn Shell (KSH)

---

### Why Use Shell Scripting?

- Automates repetitive tasks
- Saves time
- Reduces human errors
- Executes multiple commands automatically
- Useful in Cloud and DevOps environments

---

### Creating a Basic Shell Script

Example:

```bash
#!/bin/bash
echo "Hello World"
```

Explanation:

- `#!/bin/bash` → Defines Bash interpreter
- `echo` → Prints output to terminal

---

### Creating Script File

Create file:

```bash
vim myscript.sh
```

Grant execute permission:

```bash
chmod +x myscript.sh
```

Run script:

```bash
./myscript.sh
```

Alternative execution:

```bash
bash myscript.sh
```

---

### File and Folder Automation Script

Example:

```bash
#!/bin/bash

mkdir -p folder1 folder2
touch folder1/file1.txt
touch folder2/file2.txt
```

Functions:

- `mkdir` → Creates directory
- `touch` → Creates file
- `-p` → Creates parent directories if required

---

### System Information Script

Example:

```bash
#!/bin/bash

echo "Hostname: $(hostname)"
echo "Current User: $(whoami)"
echo "Uptime: $(uptime -p)"
df -h
free -h
```

Displays:

- Hostname
- Current user
- System uptime
- Disk usage
- Memory usage

---

### Shell Scripting Best Practices

- Use meaningful file names
- Add comments using `#`
- Use variables

Example:

```bash
name="John"
echo "Hello $name"
```

- Use conditions

```bash
if [ -f file.txt ]
then
echo "File exists"
fi
```

- Use loops

```bash
for file in *.txt
do
echo $file
done
```

- Handle errors

```bash
command || echo "Failed"
```

---

## Technologies Used

- Linux
- Bash Shell
- Vim
- SSH

## Outcome

- Learned Shell scripting basics
- Created executable scripts
- Automated file operations
- Created system information scripts
- Understood scripting best practices