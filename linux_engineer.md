# Linux Engineering: From Zero to Professional

## Overview
This comprehensive guide provides a complete roadmap for individuals with no prior IT experience to become Linux Engineers at professional level. The curriculum is designed with a progressive approach, beginning with absolute fundamentals and advancing to professional-level skills required in enterprise environments.

## Learning Journey Timeline
- **Absolute Beginners**: 1-2 months
- **Fundamentals**: 2-3 months
- **Intermediate Skills**: 3-4 months
- **Advanced Topics**: 3-4 months
- **Professional Level & Specialization**: 2-3 months
- **Total Estimated Time**: 11-16 months (studying 15-20 hours per week)

## Table of Contents

### 🔰 Absolute Beginners
- [Introduction to Computing](#introduction-to-computing)
- [What are Operating Systems?](#what-are-operating-systems)
- [Introduction to Linux](#introduction-to-linux)
- [Setting Up Your Linux Environment](#setting-up-your-linux-environment)
- [Basic Computer Networking](#basic-computer-networking)

### 🌱 Linux Fundamentals
- [Understanding the Linux Filesystem](#understanding-the-linux-filesystem)
- [Command Line Basics](#command-line-basics)
- [Working with Files and Directories](#working-with-files-and-directories)
- [Users, Groups and Permissions](#users-groups-and-permissions)
- [Package Management](#package-management)
- [Text Editing in Linux](#text-editing-in-linux)
- [Basic Shell Scripting](#basic-shell-scripting)

### 🚀 Intermediate Linux Skills
- [Advanced Command Line Usage](#advanced-command-line-usage)
- [Process Management](#process-management)
- [System Administration Tasks](#system-administration-tasks)
- [Intermediate Shell Scripting](#intermediate-shell-scripting)
- [Networking Fundamentals](#networking-fundamentals)
- [Storage Management](#storage-management)
- [System Monitoring](#system-monitoring)
- [Basic Security Principles](#basic-security-principles)

### 🏆 Advanced Linux Skills
- [Linux System Architecture](#linux-system-architecture)
- [Advanced Networking](#advanced-networking)
- [Advanced Security](#advanced-security)
- [Server Services Configuration](#server-services-configuration)
- [Automation with Bash](#automation-with-bash)
- [Configuration Management](#configuration-management)
- [Virtualization Fundamentals](#virtualization-fundamentals)
- [Containerization Basics](#containerization-basics)
- [Troubleshooting Skills](#troubleshooting-skills)

### 💼 Professional Linux Engineer
- [Enterprise Linux Administration](#enterprise-linux-administration)
- [High Availability and Clustering](#high-availability-and-clustering)
- [Infrastructure as Code](#infrastructure-as-code)
- [Container Orchestration](#container-orchestration)
- [CI/CD Integration](#cicd-integration)
- [Cloud Platform Integration](#cloud-platform-integration)
- [Advanced Monitoring and Logging](#advanced-monitoring-and-logging)
- [Performance Tuning](#performance-tuning)
- [Disaster Recovery and Backup Strategies](#disaster-recovery-and-backup-strategies)

### 📚 Career Development and Certification
- [Linux Certification Paths](#linux-certification-paths)
- [Building Your Linux Portfolio](#building-your-linux-portfolio)
- [Resume and Interview Preparation](#resume-and-interview-preparation)
- [Continuing Education](#continuing-education)
- [Professional Networking](#professional-networking)

## 🔰 Absolute Beginners

This section is designed for people with no prior experience in IT or computing. It lays the groundwork for your journey to becoming a Linux engineer.

## Introduction to Computing

### What is a Computer?

At its most basic level, a computer is a machine that can:
- Accept inputs (keyboard, mouse, touchscreen, etc.)
- Process data according to instructions (programs)
- Store data (RAM for temporary storage, drives for permanent storage)
- Provide outputs (display, print, sound, etc.)

### Computer Hardware Basics

#### Essential Components:
- **CPU (Central Processing Unit)**: The "brain" of the computer that executes instructions
- **Memory (RAM)**: Temporary storage used while the computer is running
- **Storage Devices**: Hard drives (HDD), Solid State Drives (SSD) for permanent storage
- **Motherboard**: The main circuit board connecting all components
- **Power Supply**: Provides electrical power to components
- **Input/Output Devices**: Keyboard, mouse, monitor, etc.

### Software Fundamentals

Software is a collection of instructions that tells the hardware what to do:

- **System Software**: Programs that manage computer hardware and provide a platform for running applications
  - Operating Systems (Windows, macOS, Linux)
  - Device drivers
  - Utilities

- **Application Software**: Programs that perform specific tasks for users
  - Web browsers
  - Word processors
  - Games
  - Specialized tools

### Binary and Computer Logic

Computers use binary (0s and 1s) for all operations:

- Binary is a base-2 number system (only uses 0 and 1)
- Each binary digit (bit) can be represented by an electrical signal (on or off)
- 8 bits = 1 byte
- Computer operations are based on logical operations (AND, OR, NOT)

```
Example: The number 42 in binary
42 ÷ 2 = 21 remainder 0
21 ÷ 2 = 10 remainder 1
10 ÷ 2 = 5 remainder 0
5 ÷ 2 = 2 remainder 1
2 ÷ 2 = 1 remainder 0
1 ÷ 2 = 0 remainder 1
Reading from bottom up: 101010
```

## What are Operating Systems?

### Definition and Purpose

An operating system (OS) is system software that manages computer hardware, software resources, and provides common services for computer programs:

- Acts as an intermediary between users and hardware
- Manages resources (CPU, memory, I/O devices)
- Provides an interface for users and applications
- Ensures security and stability

### Key Functions of Operating Systems

1. **Process Management**: Creates, schedules, and terminates processes
2. **Memory Management**: Allocates and deallocates memory
3. **File System Management**: Organizes and maintains files and directories
4. **Device Management**: Controls input/output devices
5. **Security**: Controls access to resources and data
6. **User Interface**: Provides ways for users to interact with the computer

### Types of Operating Systems

- **Windows**: Microsoft's proprietary OS (Windows 10, Windows 11, Windows Server)
- **macOS**: Apple's proprietary OS for Mac computers
- **Linux**: Open-source, Unix-like operating system
- **Unix**: Original multi-user, multitasking operating system
- **Mobile OS**: Android (Linux-based), iOS (Unix-based)
- **Embedded OS**: For specialized devices (IoT, appliances)

### Operating System Components

- **Kernel**: Core component that manages system resources
- **Shell**: Interface that accepts user commands
- **File System**: Organizes and stores files
- **Device Drivers**: Software that communicates with hardware
- **System Utilities**: Tools for system maintenance and configuration

## Introduction to Linux

### What is Linux?

Linux is an open-source, Unix-like operating system kernel created by Linus Torvalds in 1991. When people refer to "Linux," they typically mean a complete operating system built around the Linux kernel, which includes many utilities and applications.

### History of Linux

- **1969**: UNIX was developed at Bell Labs by Ken Thompson and Dennis Ritchie
- **1983**: Richard Stallman started the GNU Project to create a free Unix-like OS
- **1991**: Linus Torvalds created the Linux kernel
- **1992-Present**: Ongoing development by thousands of contributors worldwide

### Linux vs. Other Operating Systems

| Feature | Linux | Windows | macOS |
|---------|-------|---------|-------|
| **License** | Open-source | Proprietary | Proprietary |
| **Cost** | Mostly free | Paid | Comes with Apple hardware |
| **Customization** | Highly customizable | Limited | Limited |
| **Security** | Generally very secure | Vulnerable to malware | Generally secure |
| **User Interface** | Multiple options (GNOME, KDE, etc.) | Windows Explorer | macOS interface |
| **Software Installation** | Package managers | Installers/Store | App Store/Installers |
| **Market Share** | Dominates servers, low on desktop | Dominates desktop | Mid-range desktop share |
| **Updates** | User-controlled | Semi-forced | Semi-forced |

### Linux Distributions (Distros)

A Linux distribution is an operating system built on the Linux kernel, packaged with additional software:

#### Popular Distributions:

- **Debian-based**:
  - Ubuntu: User-friendly, great for beginners
  - Debian: Stable, secure, foundation for many distros
  - Linux Mint: User-friendly, Windows-like interface

- **Red Hat-based**:
  - Red Hat Enterprise Linux (RHEL): Enterprise-focused, paid support
  - CentOS/Rocky Linux/AlmaLinux: Free RHEL alternatives
  - Fedora: Cutting-edge, community version of Red Hat

- **Others**:
  - Arch Linux: Rolling release, highly customizable
  - SUSE/openSUSE: Enterprise and community versions
  - Gentoo: Source-based, highly optimizable

#### Choosing a Distribution

For beginners, these distributions are recommended:
- **Ubuntu**: Most beginner-friendly with extensive community support
- **Linux Mint**: Familiar interface for Windows users
- **Fedora**: If you want to learn skills applicable to Red Hat environments

For this guide, we'll primarily use **Ubuntu** for examples, but will note differences for Red Hat-based systems where relevant.

### The Linux Philosophy

Linux follows several key philosophies:

1. **Everything is a file**: Devices, processes, and system information are represented as files
2. **Small, single-purpose programs**: Programs should do one thing well
3. **Programs work together**: Chain simple programs to perform complex tasks
4. **Text configuration**: Most configuration is done via text files
5. **Open-source development**: Code is freely available and community-driven

### Linux in the Real World

Linux powers:
- **Over 90% of the world's top 500 supercomputers**
- **Most web servers** (Apache, Nginx run primarily on Linux)
- **Cloud infrastructure** (AWS, Google Cloud, Azure use Linux extensively)
- **Android devices** (Android is built on the Linux kernel)
- **Embedded systems** (routers, smart TVs, IoT devices)
- **Scientific and research computing**

### Exercise: Linux Exploration

1. Research 3 different Linux distributions and note their key features
2. Identify 5 real-world applications or services running on Linux
3. List 3 reasons why companies choose Linux for their server environments
4. Find and join an online Linux community forum or discussion group

## Setting Up Your Linux Environment

### Installation Options

There are several ways to get started with Linux:

#### 1. Virtual Machine (Recommended for Beginners)

Using a virtual machine allows you to run Linux inside your current operating system:

- **VirtualBox** (Free, works on Windows, macOS, Linux)
- **VMware Workstation Player** (Free for personal use, Windows and Linux)
- **VMware Fusion** (macOS, paid)
- **Hyper-V** (Windows 10/11 Pro, Enterprise, Education)

#### 2. Dual Boot

Install Linux alongside your existing OS:
- Requires partitioning your hard drive
- More complex setup
- Provides native performance
- Slight risk of data loss during installation

#### 3. Live USB

Run Linux without installing:
- Create a bootable USB drive
- Boot from USB to try Linux
- Changes aren't saved between sessions (unless configured)
- Good for testing distributions

#### 4. Cloud-based Linux

Use Linux in the cloud:
- AWS EC2, Google Cloud Compute, Azure VMs
- Free tiers available for learning
- No local installation required
- Good for learning server administration

#### 5. Windows Subsystem for Linux (WSL)

For Windows 10/11 users:
- Install Linux directly in Windows
- No need for virtualization
- Limited hardware access
- Good for command-line learning

### Installing Linux in a Virtual Machine

We'll go through installing Ubuntu on VirtualBox as a beginner-friendly option:

#### Step 1: Download Required Software

1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. Download [Ubuntu Desktop ISO](https://ubuntu.com/download/desktop) (LTS version recommended)

#### Step 2: Create a New Virtual Machine

1. Open VirtualBox and click "New"
2. Name your VM (e.g., "Ubuntu")
3. Select "Linux" as Type and "Ubuntu (64-bit)" as Version
4. Allocate at least 2GB (2048MB) of RAM
5. Create a virtual hard disk (VDI, dynamically allocated, 20GB+)

#### Step 3: Configure the Virtual Machine

1. Select your new VM and click "Settings"
2. Under "System":
   - Enable EFI (if available)
   - Set at least 2 processors
3. Under "Display":
   - Allocate at least 32MB of video memory
   - Enable 3D acceleration
4. Under "Storage":
   - Click the empty disk under Controller: IDE
   - Click the disk icon next to "Optical Drive"
   - Select "Choose a disk file" and browse to your Ubuntu ISO

#### Step 4: Install Ubuntu

1. Start the virtual machine
2. Select "Install Ubuntu"
3. Follow the on-screen instructions:
   - Choose your language and keyboard layout
   - Select "Normal installation"
   - Choose "Erase disk and install Ubuntu" (don't worry, this only affects the virtual disk)
   - Select your location and create a user account
   - Wait for installation to complete and restart

#### Step 5: Post-Installation Setup

1. Log in to your new Ubuntu system
2. When prompted, install available updates
3. Install VirtualBox Guest Additions:
   - In VirtualBox menu: Devices > Insert Guest Additions CD image
   - Run the installer from the mounted CD
   - Restart the VM

### Alternative: Using a Linux Cloud Instance

If you prefer to learn Linux server administration directly:

1. Create a free account on [AWS](https://aws.amazon.com/), [Google Cloud](https://cloud.google.com/), or [Azure](https://azure.microsoft.com/)
2. Launch a free-tier Linux instance:
   - AWS: Amazon Linux or Ubuntu
   - Google Cloud: Compute Engine with Ubuntu
   - Azure: Virtual Machine with Ubuntu
3. Connect via SSH:
   - Windows: Use PuTTY or Windows Terminal
   - macOS/Linux: Use terminal with `ssh` command

```bash
# Example SSH connection (replace with your own information)
ssh -i /path/to/your-key.pem username@your-instance-ip
```

### Exercise: Setting Up Your Linux Environment

1. Install VirtualBox and create an Ubuntu virtual machine
2. Complete the Ubuntu installation process
3. Install updates and Guest Additions
4. Explore the desktop environment
5. Open a terminal and try some basic commands (we'll cover these next!)

## Basic Computer Networking

Understanding basic networking is essential for Linux administration:

### Network Fundamentals

#### IP Addressing

- **IP Address**: Unique identifier for devices on a network
  - IPv4: 32-bit address (e.g., 192.168.1.1)
  - IPv6: 128-bit address (e.g., 2001:0db8:85a3:0000:0000:8a2e:0370:7334)
- **Subnet Mask**: Defines which portion of an IP address refers to the network (e.g., 255.255.255.0)
- **Default Gateway**: Router address that connects to other networks
- **DNS Server**: Translates domain names to IP addresses

#### Networking Components

- **Router**: Connects different networks together
- **Switch**: Connects devices within the same network
- **Firewall**: Controls incoming and outgoing network traffic
- **DHCP**: Assigns IP addresses automatically
- **DNS**: Domain Name System - translates domain names to IP addresses
- **Network Interface Card (NIC)**: Hardware that connects a device to a network

#### Networking Protocols

- **TCP/IP**: The fundamental suite of protocols used for internet communication
- **HTTP/HTTPS**: For web browsing (Hypertext Transfer Protocol)
- **SSH**: Secure Shell for remote access
- **FTP/SFTP**: File Transfer Protocol and its secure version
- **SMTP/POP3/IMAP**: Email protocols

#### Network Topology

- **LAN (Local Area Network)**: Network in a limited area (home, office)
- **WAN (Wide Area Network)**: Network spanning a large geographic area
- **VPN (Virtual Private Network)**: Secure connection over public networks
- **Internet**: Global network of interconnected networks

### Basic Network Commands

We'll explore these in more detail later, but these are key commands for networking in Linux:

```bash
# Display network interfaces
ifconfig     # Traditional command
ip addr      # Modern command

# Test connectivity to a host
ping google.com

# Trace the route to a host
traceroute google.com

# Look up DNS information
nslookup google.com
dig google.com

# Display network connections
netstat -tuln   # Traditional command
ss -tuln        # Modern command
```

### Exercise: Basic Networking

1. Identify your computer's IP address and subnet mask
2. Find your default gateway
3. Use `ping` to test connectivity to a website
4. Use `traceroute` to see the path to a website
5. Look up the IP address of a website using `nslookup` or `dig`

## 🌱 Linux Fundamentals

This section builds on the basics, introducing you to the core skills needed for Linux administration.

## Understanding the Linux Filesystem

### Filesystem Hierarchy Standard

Linux follows the Filesystem Hierarchy Standard (FHS), which defines the directory structure and contents:

```
/          # Root directory - top of the filesystem hierarchy
├── bin    # Essential command binaries
├── boot   # Boot loader files and kernel
├── dev    # Device files
├── etc    # System configuration files
├── home   # User home directories
├── lib    # Essential shared libraries
├── media  # Mount points for removable media
├── mnt    # Temporary mount points
├── opt    # Optional application software
├── proc   # Virtual filesystem for process information
├── root   # Home directory for the root user
├── run    # Run-time variable data
├── sbin   # System binaries
├── srv    # Data for services provided by the system
├── sys    # Virtual filesystem for system information
├── tmp    # Temporary files
├── usr    # User utilities and applications
└── var    # Variable data (logs, spool files, etc.)
```

### Key Directories Explained

- **/bin**: Contains essential command binaries (executable programs) that need to be available in single-user mode
- **/boot**: Files needed for booting, including the Linux kernel and boot loader configuration
- **/dev**: Device files representing hardware devices (e.g., /dev/sda for the first hard drive)
- **/etc**: System-wide configuration files
- **/home**: User home directories (e.g., /home/username)
- **/lib**: Essential shared libraries needed by programs in /bin and /sbin
- **/opt**: Optional software and add-on packages
- **/proc**: Virtual filesystem providing process and kernel information
- **/root**: Home directory for the root (administrative) user
- **/sbin**: System administration binaries
- **/srv**: Data for services provided by the system
- **/sys**: Interface to kernel objects (similar to /proc)
- **/tmp**: Temporary files (typically cleared on reboot)
- **/usr**: Secondary hierarchy containing non-essential utilities, applications, and files
- **/var**: Variable data files, including logs, spool files, and temporary files

### Filesystem Types

Linux supports various filesystem types:

- **ext4**: Fourth Extended Filesystem - the default on many Linux distributions
- **XFS**: High-performance journaling filesystem, default on some distributions like RHEL
- **Btrfs**: B-tree filesystem with advanced features like snapshots and pooling
- **ZFS**: Advanced filesystem with volume management, data integrity features
- **NTFS/FAT32**: Windows filesystems (limited support for compatibility)

### Mount Points

In Linux, accessing storage devices requires "mounting" them to a directory in the filesystem:

```bash
# List mounted filesystems
mount

# Mount a USB drive (replace with actual device and mount point)
sudo mount /dev/sdb1 /mnt/usb

# Unmount a filesystem
sudo umount /mnt/usb
```

### File Types

Linux has several types of files:

- **Regular files**: Normal data files (text, images, executables)
- **Directories**: Containers for other files
- **Links**: 
  - Symbolic links (similar to shortcuts in Windows)
  - Hard links (multiple directory entries pointing to the same data)
- **Device files**: Represent hardware devices
  - Block devices (storage devices like hard drives)
  - Character devices (serial devices, terminals)
- **Named pipes**: Allow communication between processes
- **Sockets**: Enable inter-process communication

### Exercise: Exploring the Filesystem

1. Open a terminal and navigate through the filesystem hierarchy
2. List the contents of key directories (/bin, /etc, /home)
3. Check what filesystems are mounted on your system
4. Identify different file types in the system

## Command Line Basics

### Understanding the Terminal

The terminal (or console) is a text-based interface for interacting with the operating system:

- **Terminal emulator**: Application that provides access to the shell (e.g., GNOME Terminal, Konsole)
- **Shell**: Command interpreter that executes commands (e.g., Bash, Zsh)
- **Command prompt**: Where you enter commands (typically ends with $ for regular users, # for root)

### Opening a Terminal

- In Ubuntu: Press Ctrl+Alt+T or search for "Terminal" in the applications menu
- In most Linux distributions: Look for "Terminal" or "Console" in the system menu

### Shell Basics

The most common shell is Bash (Bourne Again SHell):

```bash
username@hostname:~$ command [options] [arguments]
```

Where:
- **username**: Your login name
- **hostname**: Your computer's name
- **~**: Current directory (~ represents your home directory)
- **$**: Regular user prompt (# for root/admin)
- **command**: The program you want to run
- **options**: Modify the command's behavior (usually start with - or --)
- **arguments**: What the command operates on (files, directories, etc.)

### Basic Shell Navigation

```bash
# Print working directory (current location)
pwd

# List directory contents
ls

# List with details
ls -l

# List including hidden files
ls -a

# Change directory
cd /path/to/directory

# Go to home directory
cd
# or
cd ~

# Go up one directory
cd ..

# Go to previous directory
cd -
```

### Getting Help

There are several ways to get help with commands:

```bash
# Display manual page for a command
man ls

# Brief help for a command
ls --help

# Information about a command
info ls

# Show what a command does (often with examples)
whatis ls
```

### Command History

Bash keeps a history of commands you've entered:

```bash
# Show command history
history

# Run the previous command
!!

# Run command number 42 from history
!42

# Search history (press Ctrl+R and start typing)
# Press Ctrl+R again to cycle through matches
```

### Tab Completion

The Tab key helps you complete commands and filenames:

1. Start typing a command or filename
2. Press Tab once to complete if there's only one match
3. Press Tab twice to show all possibilities if there are multiple matches

### Command Line Shortcuts

- **Ctrl+C**: Interrupt (kill) the current process
- **Ctrl+Z**: Suspend the current process
- **Ctrl+D**: End of input (log out from shell)
- **Ctrl+L**: Clear the screen (same as `clear` command)
- **Ctrl+A**: Move cursor to beginning of line
- **Ctrl+E**: Move cursor to end of line
- **Ctrl+U**: Cut from cursor to beginning of line
- **Ctrl+K**: Cut from cursor to end of line
- **Ctrl+W**: Cut the word before the cursor

### Exercise: Command Line Basics

1. Open a terminal and identify the parts of the prompt
2. Practice navigating with `cd` and viewing directories with `ls`
3. Check your current location with `pwd`
4. Look up the manual page for a command like `ls` or `cd`
5. Try tab completion with partial commands and filenames
6. Use the history feature to recall and reuse commands

## Working with Files and Directories

### Creating and Managing Directories

```bash
# Create a directory
mkdir my_directory

# Create nested directories
mkdir -p parent/child/grandchild

# Remove an empty directory
rmdir my_directory

# Remove a directory and its contents (BE CAREFUL!)
rm -r my_directory
```

### Creating and Viewing Files

```bash
# Create an empty file
touch myfile.txt

# Display file contents
cat myfile.txt

# View large files one page at a time
less myfile.txt

# View the first 10 lines of a file
head myfile.txt

# View the last 10 lines of a file
tail myfile.txt

# Follow a file as it grows (useful for logs)
tail -f /var/log/syslog
```

### Copying, Moving, and Removing Files

```bash
# Copy a file
cp source.txt destination.txt

# Copy a directory and its contents
cp -r source_dir destination_dir

# Move/rename a file
mv oldname.txt newname.txt

# Move a file to a different directory
mv file.txt /path/to/directory/

# Remove a file
rm file.txt

# Remove multiple files
rm file1.txt file2.txt

# Remove files interactively (with confirmation)
rm -i file.txt
```

### Finding Files

```bash
# Find files by name in the current directory and subdirectories
find . -name "*.txt"

# Find files by type
find /home -type f  # Regular files
find /home -type d  # Directories

# Find files by size
find /var -size +10M  # Files larger than 10 MB

# Find files by owner
find /home -user username

# Find files modified in the last 7 days
find /home -mtime -7

# Execute a command on found files
find . -name "*.txt" -exec ls -l {} \;
```

### File Compression and Archives

```bash
# Create a tar archive
tar -cvf archive.tar file1 file2 directory1

# Extract from a tar archive
tar -xvf archive.tar

# Create a compressed tar archive with gzip
tar -czvf archive.tar.gz directory/

# Extract from a compressed tar archive
tar -xzvf archive.tar.gz

# Zip files
zip -r archive.zip directory/

# Unzip files
unzip archive.zip
```

### Viewing File Information

```bash
# View file details
ls -l filename

# Determine file type
file filename

# View file size
du -h filename

# View disk usage of directories
du -sh directory/
```

### Exercise: Working with Files and Directories

1. Create a directory structure for a project
2. Create several files using `touch` and `echo`
3. Copy and move files between directories
4. Find specific files based on name, type, or size
5. Create an archive of your project files
6. Practice viewing file contents with different commands

## Users, Groups and Permissions

### User Management

In Linux, every user has:
- A unique username
- A numeric user ID (UID)
- A primary group
- A home directory
- A login shell

#### Key User-Related Files

- **/etc/passwd**: User account information
- **/etc/shadow**: Encrypted passwords
- **/etc/group**: Group information

#### User Management Commands

```bash
# Add a new user
sudo adduser username
# or (more basic version)
sudo useradd username

# Set or change a user's password
sudo passwd username

# Modify an existing user
sudo usermod -options username

# Delete a user
sudo deluser username
# or (with home directory removal)
sudo deluser --remove-home username

# View user information
id username

# Switch to another user
su - username

# Run a command as another user
sudo -u username command

# List all users
cat /etc/passwd
```

### Group Management

Groups organize users for access control purposes:

```bash
# Create a new group
sudo addgroup groupname
# or
sudo groupadd groupname

# Add a user to a group
sudo adduser username groupname
# or
sudo usermod -aG groupname username

# Remove a user from a group
sudo deluser username groupname
# or
sudo gpasswd -d username groupname

# Change a user's primary group
sudo usermod -g groupname username

# List a user's groups
groups username

# Delete a group
sudo delgroup groupname
# or
sudo groupdel groupname

# List all groups
cat /etc/group
```

### File Permissions

Linux uses a permission system to control access to files and directories:

#### Permission Types

- **Read (r)**: View the contents of a file or list directory contents
- **Write (w)**: Modify a file or create/delete files in a directory
- **Execute (x)**: Execute a file (if it's a program) or access a directory

#### Permission Classes

- **User (u)**: The owner of the file
- **Group (g)**: Users in the file's group
- **Others (o)**: All other users

#### Viewing Permissions

```bash
ls -l filename
```

Output example:
```
-rwxr-xr--  1 user group  4096 Apr 15 14:30 filename
```

Where:
- First character:
  - `-`: Regular file
  - `d`: Directory
  - `l`: Symbolic link
- Next 9 characters: Permissions for user (rwx), group (r-x), and others (r--)
- Number: Number of hard links
- user: File owner
- group: File group
- 4096: File size in bytes
- Apr 15 14:30: Last modification time
- filename: File name

#### Changing Permissions

```bash
# Symbolic method
chmod u+x file.sh       # Add execute permission for the owner
chmod g-w file.txt      # Remove write permission for the group
chmod o=r file.txt      # Set others to only have read permission
chmod a+r file.txt      # Add read permission for all (user, group, others)

# Octal (numeric) method
chmod 755 file.sh       # rwxr-xr-x (owner:rwx, group:r-x, others:r-x)
chmod 644 file.txt      # rw-r--r-- (owner:rw-, group:r--, others:r--)
chmod 600 private.key   # rw------- (owner:rw-, no permissions for group or others)

# Recursive change for directories
chmod -R 755 directory/
```

#### Common Permission Patterns

- **755 (rwxr-xr-x)**: Standard for executable files and directories
- **644 (rw-r--r--)**: Standard for regular files
- **700 (rwx------)**: Private executable
- **600 (rw-------)**: Private file (like SSH keys)

#### Changing Ownership

```bash
# Change the owner of a file
sudo chown username file.txt

# Change the group of a file
sudo chgrp groupname file.txt

# Change both owner and group
sudo chown username:groupname file.txt

# Recursive ownership change
sudo chown -R username:groupname directory/
```

### Special Permissions

#### SUID (Set User ID)

When set on an executable, it runs with the permissions of the file owner, not the user who runs it:

```bash
chmod u+s file
# or 
chmod 4755 file  # The 4 adds SUID
```

#### SGID (Set Group ID)

Similar to SUID but for groups. When set on a directory, new files in that directory inherit the directory's group:

```bash
chmod g+s directory
# or
chmod 2755 directory  # The 2 adds SGID
```

#### Sticky Bit

Primarily used on directories to prevent users from deleting files owned by others:

```bash
chmod +t directory
# or
chmod 1777 directory  # The 1 adds the sticky bit
```

### Access Control Lists (ACLs)

ACLs provide more granular permissions beyond the basic owner/group/others model:

```bash
# Install ACL support (if needed)
sudo apt install acl  # Ubuntu/Debian
sudo dnf install acl  # Fedora/RHEL

# View ACLs
getfacl file.txt

# Set an ACL (give user john read-write access)
setfacl -m u:john:rw file.txt

# Set a default ACL (for new files in a directory)
setfacl -d -m g:developers:rwx directory/
```

### Exercise: Users, Groups, and Permissions

1. Create two new users and a new group
2. Add both users to the new group
3. Create a shared directory owned by the group
4. Set permissions so that:
   - Both users can read, write, and execute in the directory
   - New files in the directory belong to the group
   - Other users can read but not write to the directory
5. Test creating files as each user
6. Experiment with changing file permissions

## Package Management

Linux distributions use package management systems to install, update, and remove software.

### Package Managers

Different distributions use different package managers:

#### Debian-based (Ubuntu, Debian, Linux Mint)

Uses **APT** (Advanced Package Tool):

```bash
# Update package lists
sudo apt update

# Upgrade installed packages
sudo apt upgrade

# Upgrade the distribution
sudo apt dist-upgrade

# Install a package
sudo apt install package-name

# Remove a package
sudo apt remove package-name

# Remove a package and its configuration files
sudo apt purge package-name

# Search for a package
apt search keyword

# Show package information
apt show package-name

# List installed packages
apt list --installed

# Clean up downloaded package files
sudo apt autoremove
sudo apt clean
```

#### Red Hat-based (RHEL, CentOS, Fedora)

Uses **DNF** (or older systems use **YUM**):

```bash
# Update package lists and upgrade packages
sudo dnf upgrade

# Install a package
sudo dnf install package-name

# Remove a package
sudo dnf remove package-name

# Search for a package
dnf search keyword

# Show package information
dnf info package-name

# List installed packages
dnf list installed

# List available updates
dnf check-update

# Clean up cached package data
sudo dnf clean all
```

### Software Repositories

Repositories are servers that host collections of packages:

#### Managing Repositories

**Debian-based:**
```bash
# Repository configuration files are in:
/etc/apt/sources.list
/etc/apt/sources.list.d/

# Add a repository
sudo add-apt-repository ppa:repository-name/ppa

# After adding repositories, update package lists
sudo apt update
```

**Red Hat-based:**
```bash
# Repository configuration files are in:
/etc/yum.repos.d/

# Add a repository
sudo dnf config-manager --add-repo repository_url

# Enable a repository
sudo dnf config-manager --enable repository

# Disable a repository
sudo dnf config-manager --disable repository
```

### Package Dependencies

Modern package managers automatically handle dependencies (other packages required by the software):

```bash
# Resolve dependencies for a package without installing it
apt-cache depends package-name   # Debian-based
dnf repoquery --requires --resolve package-name   # Red Hat-based
```

### Installing Software from Source

Sometimes you need to install software not available in repositories:

```bash
# Install build essentials
sudo apt install build-essential   # Debian-based
sudo dnf group install "Development Tools"   # Red Hat-based

# Basic source installation process
tar -xzvf package-name.tar.gz
cd package-name
./configure
make
sudo make install
```

### Alternative Package Managers

Some software is distributed using universal package managers:

#### Snap (by Canonical/Ubuntu)

```bash
# Install snap
sudo apt install snapd   # Debian-based
sudo dnf install snapd   # Red Hat-based

# Install a snap package
sudo snap install package-name

# Update all snap packages
sudo snap refresh

# List installed snaps
snap list

# Remove a snap
sudo snap remove package-name
```

#### Flatpak

```bash
# Install Flatpak
sudo apt install flatpak   # Debian-based
sudo dnf install flatpak   # Red Hat-based

# Add Flathub repository
flatpak remote-add --if-not-exists flathub https://flathub.org/repo/flathub.flatpakrepo

# Install a Flatpak
flatpak install flathub app-id

# Run a Flatpak application
flatpak run app-id

# Update Flatpaks
flatpak update

# List installed Flatpaks
flatpak list
```

### Exercise: Package Management

1. Update your system's package lists and install any available updates
2. Search for and install a text editor (like 'nano' or 'vim')
3. Find information about the installed package
4. Remove the package and verify it was removed
5. Add a new repository and install software from it
6. Try installing a Snap or Flatpak application

## Text Editing in Linux

Text editing is a fundamental skill for Linux administration as configuration files are plain text.

### Common Text Editors

#### nano

Beginner-friendly, easy to use:

```bash
# Open a file
nano filename.txt
```

**Basic nano commands:**
- **Ctrl+O**: Save file
- **Ctrl+X**: Exit
- **Ctrl+G**: Help
- **Ctrl+K**: Cut line
- **Ctrl+U**: Paste line
- **Ctrl+W**: Search
- **Ctrl+\**: Search and replace

#### vim (or vi)

Powerful but steeper learning curve:

```bash
# Open a file
vim filename.txt
```

**vim operates in different modes:**

- **Command mode** (default): For navigation and commands
  - `h`, `j`, `k`, `l`: Move cursor left, down, up, right
  - `i`: Enter insert mode
  - `Esc`: Return to command mode
  - `:w`: Save
  - `:q`: Quit
  - `:wq` or `ZZ`: Save and quit
  - `:q!`: Quit without saving

- **Insert mode**:
