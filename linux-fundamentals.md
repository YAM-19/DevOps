# Linux Fundamentals and Shell Scripting

## 1. Introduction to Linux

Linux is an open-source operating system widely used in cloud computing, server administration, and DevOps engineering.

It is commonly used on production servers because of its flexibility, stability, security features, and extensive command-line tools.

### What is an Operating System?

An operating system (OS) acts as a bridge between software applications and computer hardware.

It manages:
- CPU (Central Processing Unit)
- RAM (Random Access Memory)
- Storage
- Input and output devices
- Running applications and processes

Examples of operating systems include Linux, Windows, and macOS.

## 2. Why Linux Is Important in DevOps

Linux is widely used in DevOps because:

- It is open-source and available for free.
- It provides powerful command-line tools.
- It supports automation through shell scripting.
- It is widely used on cloud servers and virtual machines.
- It integrates with tools such as Docker, Kubernetes, Jenkins, and Ansible.
- It is suitable for server administration and deployment automation.

## 3. Linux Architecture

The main components of Linux architecture are:

### Kernel
The kernel is the core of the operating system. It manages hardware resources, memory, CPU scheduling, and device communication.

### System Libraries
System libraries provide functions that applications use to interact with the kernel.

### Shell
The shell interprets commands entered by the user and passes the required operations to the operating system.

Examples include Bash and Zsh.

### User Applications and Processes
These are programs and tasks running on the operating system.

Examples include text editors, web servers, and monitoring tools.

## 4. Command-Line Interface (CLI)

A command-line interface allows users to interact with the operating system by typing commands.

Linux servers often use the CLI because it is efficient for remote administration, automation, and troubleshooting.

## 5. Basic Linux Commands

### Navigation and Directory Listing

**Print Working Directory**
```bash
pwd
```
Displays the current working directory.

**List Files and Directories**
```bash
ls
```
Displays files and directories in the current location.

```bash
ls -l
```
Displays detailed file information.

```bash
ls -a
```
Displays hidden files as well.

**Change Directory**
```bash
cd /path/to/directory
```
Moves to the specified directory.

```bash
cd ..
```
Moves to the parent directory.

```bash
cd ~
```
Moves to the user's home directory.

### File Management

**Create a File**
```bash
touch notes.txt
```
Creates an empty file if it does not exist.

**Edit a File**
```bash
vi notes.txt
```
Opens the file using the Vi editor.

To edit in Vi:
1. Press `i` to enter insert mode.
2. Type your content.
3. Press `Esc`.
4. Type `:wq` and press Enter to save and exit.

**Read a File**
```bash
cat notes.txt
```
Displays the contents of a file.

**Create a Directory**
```bash
mkdir myfolder
```
Creates a directory named `myfolder`.

## 6. Linux System Monitoring Commands

### Check Memory Usage
```bash
free -h
```
Displays RAM and swap usage in a human-readable format.

### Check CPU Count
```bash
nproc
```
Displays the number of processing units available to the system.

### Check Disk Space
```bash
df -h
```
Displays filesystem disk usage in a human-readable format.

### Monitor Running Processes
```bash
top
```
Displays running processes and resource usage, including CPU and memory.

Press `q` to exit the `top` interface.

## 7. Introduction to Shell Scripting

Shell scripting involves writing a series of shell commands in a file so they can be executed together.

It is useful for:
- Automating repetitive tasks.
- Managing files and directories.
- Monitoring system resources.
- Automating deployments.
- Performing routine server administration.

### Example: First Shell Script

Create a script:
```bash
vi hello.sh
```

Add the following content:
```bash
#!/bin/bash

echo "Hello, DevOps!"
echo "Welcome to Linux Shell Scripting"
```

Save and exit the editor.

Give the script execute permission:
```bash
chmod +x hello.sh
```

Run the script:
```bash
./hello.sh
```

Expected output:
```text
Hello, DevOps!
Welcome to Linux Shell Scripting
```

### Understanding the Script

- `#!/bin/bash` specifies Bash as the interpreter.
- `echo` prints text to the terminal.
- `chmod +x` adds execute permission.
- `./hello.sh` runs the script from the current directory.

## 8. Practical Hands-On Exercises

Practice these commands on a Linux machine or virtual machine:

1. Display the current directory using `pwd`.
2. List files using `ls -l`.
3. Create a directory named `devops-practice`.
4. Navigate into that directory using `cd`.
5. Create a file named `linux-notes.txt`.
6. Write and read file contents.
7. Check memory using `free -h`.
8. Check CPU count using `nproc`.
9. Check disk usage using `df -h`.
10. Create and execute your first shell script.

## 9. Key Takeaways

- Linux is an important operating system for DevOps engineers.
- The kernel manages hardware and system resources.
- The shell provides a way to execute commands.
- Linux commands help with navigation, file management, and system monitoring.
- Shell scripts automate repetitive tasks and improve operational efficiency.
- Regular hands-on practice is essential for learning Linux and DevOps.

## 10. Conclusion

Linux fundamentals and shell scripting are essential skills for cloud and DevOps engineering. Understanding these concepts provides a foundation for working with cloud servers, automation tools, containers, and CI/CD pipelines.
