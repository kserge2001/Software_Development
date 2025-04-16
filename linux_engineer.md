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
  - Type to insert text
  - Arrow keys to navigate
  - `Esc` to return to command mode

- **Visual mode**:
  - `v`: Enter visual mode for character selection
  - `V`: Enter visual line mode
  - Use movement keys to select text

**Basic vim commands:**
```
# Navigation
h, j, k, l    # Move cursor left, down, up, right
w             # Move to start of next word
b             # Move to start of previous word
0             # Move to start of line
$             # Move to end of line
gg            # Move to first line of file
G             # Move to last line of file

# Editing
i             # Insert before cursor
a             # Append after cursor
o             # Open new line below
O             # Open new line above
x             # Delete character under cursor
dd            # Delete current line
yy            # Copy (yank) current line
p             # Paste after cursor
u             # Undo
Ctrl+r        # Redo

# Searching
/pattern       # Search forward for pattern
?pattern       # Search backward for pattern
n              # Find next occurrence
N              # Find previous occurrence

# Saving/Quitting
:w             # Save
:q             # Quit (if no changes)
:wq or ZZ      # Save and quit
:q!            # Quit without saving
```

#### emacs

Another powerful editor with extensive features:

```bash
# Open a file
emacs filename.txt
```

**Basic emacs commands:**
- **Ctrl+x Ctrl+s**: Save file
- **Ctrl+x Ctrl+c**: Exit
- **Ctrl+g**: Cancel current command
- **Ctrl+k**: Kill (cut) line
- **Ctrl+y**: Yank (paste) line
- **Ctrl+s**: Search forward
- **Ctrl+r**: Search backward

### Command-Line Text Processing

#### grep - Search for patterns in files

```bash
# Search for a pattern in a file
grep "pattern" filename

# Case-insensitive search
grep -i "pattern" filename

# Recursive search in directory
grep -r "pattern" directory/

# Show line numbers
grep -n "pattern" filename

# Show only filenames with matches
grep -l "pattern" *

# Invert match (show lines that don't match)
grep -v "pattern" filename
```

#### sed - Stream editor for filtering and transforming text

```bash
# Replace first occurrence on each line
sed 's/old/new/' filename

# Replace all occurrences on each line
sed 's/old/new/g' filename

# Replace on specific lines (e.g., line 3)
sed '3s/old/new/' filename

# Delete lines
sed '5d' filename      # Delete line 5
sed '/pattern/d' filename  # Delete lines matching pattern

# Edit file in-place (save changes)
sed -i 's/old/new/g' filename
```

#### awk - Powerful text processing language

```bash
# Print specific columns (fields)
awk '{print $1, $3}' filename  # Print 1st and 3rd fields

# Filter lines based on condition
awk '$3 > 50 {print $0}' filename  # Print lines where 3rd field > 50

# Use custom field separator
awk -F: '{print $1, $7}' /etc/passwd  # Print username and shell

# Calculate sum
awk '{sum += $1} END {print "Sum:", sum}' filename
```

#### cut - Extract sections from lines of files

```bash
# Extract characters by position
cut -c 1-5 filename  # Extract first 5 characters

# Extract fields by delimiter
cut -d":" -f1,7 /etc/passwd  # Extract 1st and 7th fields
```

#### sort - Sort lines of text files

```bash
# Sort alphabetically
sort filename

# Sort numerically
sort -n filename

# Sort in reverse
sort -r filename

# Sort by specific field
sort -k2 filename  # Sort by 2nd field
```

#### uniq - Report or filter out repeated lines

```bash
# Remove duplicate lines (input must be sorted)
sort filename | uniq

# Count occurrences of lines
sort filename | uniq -c

# Show only duplicate lines
sort filename | uniq -d
```

### Exercise: Text Editing

1. Open, edit, and save a file using nano
2. Learn basic vim commands:
   - Create a new file
   - Insert text
   - Save and exit
   - Search and replace text
3. Practice text processing:
   - Use grep to find patterns in log files
   - Use sed to replace text in configuration files
   - Use awk to extract and process data from CSV files

## 🚀 Intermediate Linux Skills

This section covers more advanced topics for Linux system administration.

## Advanced Command Line Usage

### Redirection and Pipes

#### Input/Output Redirection

```bash
# Redirect output to a file (overwrite)
command > output.txt

# Redirect output to a file (append)
command >> output.txt

# Redirect error output to a file
command 2> error.txt

# Redirect both standard output and error
command > output.txt 2>&1
# Modern syntax
command &> output.txt

# Redirect input from a file
command < input.txt

# Redirect input from a string
command <<< "string input"

# Here document (multi-line input)
command << EOF
line 1
line 2
line 3
EOF
```

#### Pipes

Pipes connect the output of one command to the input of another:

```bash
# Chain commands with pipes
command1 | command2 | command3

# Examples
cat /var/log/syslog | grep "error" | less
ls -la | grep "\.txt$" | sort
ps aux | grep "firefox" | wc -l
```

### Command Substitution

Execute a command and use its output as part of another command:

```bash
# Using backticks (older style)
echo "Current date: `date`"

# Using $() (preferred modern style)
echo "Current date: $(date)"

# Nested command substitution
echo "Files in directory $(basename $(pwd)): $(ls | wc -l)"
```

### Expansion and Globbing

#### Pathname Expansion (Globbing)

```bash
# Match any string
ls *.txt          # All .txt files in current directory

# Match a single character
ls file?.txt      # Matches file1.txt, fileA.txt, etc.

# Match any character in a set
ls file[123].txt  # Matches file1.txt, file2.txt, file3.txt

# Match any character not in a set
ls file[!123].txt # Matches any character except 1, 2, 3

# Match a range
ls file[a-z].txt  # Matches files with lowercase letters

# Extended globbing (bash)
shopt -s extglob   # Enable extended globbing
ls !(*.txt)        # All files except .txt files
```

#### Brace Expansion

```bash
# Generate sequences
echo {1..5}        # Outputs: 1 2 3 4 5
echo {a..e}        # Outputs: a b c d e

# Generate sequences with steps
echo {1..10..2}    # Outputs: 1 3 5 7 9

# Multiple sets
echo file{1,3,5}.txt    # Outputs: file1.txt file3.txt file5.txt

# Nested brace expansion
echo {a,b}{1,2}    # Outputs: a1 a2 b1 b2

# Practical examples
mkdir -p project/{src,lib,doc}/{main,test}  # Creates directory structure
cp file.txt{,.bak}  # Copies file.txt to file.txt.bak
```

### Regular Expressions

Regular expressions (regex) are patterns for matching text:

#### Basic Regex Patterns

- `.` - Match any single character
- `^` - Match start of line
- `$` - Match end of line
- `*` - Match zero or more of the previous character
- `+` - Match one or more of the previous character (extended regex)
- `?` - Match zero or one of the previous character (extended regex)
- `[]` - Match any character inside brackets
- `[^]` - Match any character not inside brackets
- `()` - Group patterns (extended regex)
- `|` - Alternation (OR) (extended regex)

```bash
# grep with basic regex
grep "^The" file.txt     # Lines starting with "The"
grep "end$" file.txt     # Lines ending with "end"
grep "a..b" file.txt     # "a" followed by any two chars, then "b"

# grep with extended regex
grep -E "word1|word2" file.txt   # Lines containing word1 or word2
grep -E "[0-9]+" file.txt        # Lines containing one or more digits
```

### Aliases and Functions

#### Creating Aliases

```bash
# Create a temporary alias
alias ll='ls -la'

# Make aliases permanent by adding to ~/.bashrc
echo 'alias ll="ls -la"' >> ~/.bashrc
echo 'alias update="sudo apt update && sudo apt upgrade"' >> ~/.bashrc

# Remove an alias
unalias ll
```

#### Creating Shell Functions

```bash
# Simple function
myfunc() {
    echo "Hello, $1!"
}

# Usage
myfunc "World"  # Outputs: Hello, World!

# Function with multiple commands
extract() {
    if [ -f "$1" ] ; then
        case "$1" in
            *.tar.bz2)   tar xjf "$1"     ;;
            *.tar.gz)    tar xzf "$1"     ;;
            *.bz2)       bunzip2 "$1"     ;;
            *.rar)       unrar e "$1"     ;;
            *.gz)        gunzip "$1"      ;;
            *.tar)       tar xf "$1"      ;;
            *.zip)       unzip "$1"       ;;
            *)           echo "Cannot extract '$1'" ;;
        esac
    else
        echo "'$1' is not a valid file"
    fi
}

# Make functions permanent by adding to ~/.bashrc
```

### Job Control

#### Managing Background and Foreground Processes

```bash
# Run a command in the background
command &

# List current jobs
jobs

# Bring a background job to the foreground
fg %job_number

# Send a foreground job to the background
# First press Ctrl+Z to suspend, then:
bg %job_number

# Resume a suspended job in the background
bg

# Kill a job
kill %job_number
```

#### Running Commands After Logout

```bash
# Using nohup
nohup command &

# Using screen
screen
# Then run your command, press Ctrl+A then D to detach

# Using tmux
tmux
# Then run your command, press Ctrl+B then D to detach
```

### Exercise: Advanced Command Line

1. Experiment with I/O redirection:
   - Redirect command output to a file
   - Append to an existing file
   - Redirect errors to a separate file
2. Create a pipeline of at least three commands
3. Use command substitution in a practical scenario
4. Create useful aliases and functions in your ~/.bashrc
5. Practice job control:
   - Run commands in the background
   - Move between foreground and background
   - Use screen or tmux for persistent sessions

## Process Management

Understanding how to monitor and control processes is essential for system administration.

### Viewing Running Processes

```bash
# Display all running processes
ps aux

# Display processes in a tree format
ps auxf

# Display processes for a specific user
ps -u username

# Display processes in real-time
top

# Interactive process viewer (more user-friendly than top)
htop  # May need to install: sudo apt install htop

# Show process information by PID
ps -fp PID
```

### Process States

Linux processes can be in several states:

- **R (Running)**: Currently running or ready to run
- **S (Sleeping)**: Waiting for an event to complete
- **D (Uninterruptible sleep)**: Waiting for I/O operation
- **T (Stopped)**: Process has been suspended
- **Z (Zombie)**: Terminated process that still has an entry in the process table

### Process Control

#### Sending Signals to Processes

```bash
# Terminate a process gracefully (SIGTERM)
kill PID

# Force terminate a process (SIGKILL)
kill -9 PID
# or
kill -KILL PID

# Pause a process (SIGSTOP)
kill -STOP PID

# Resume a paused process (SIGCONT)
kill -CONT PID

# Send HUP signal (often used to reload configuration)
kill -HUP PID

# List all signals
kill -l
```

#### Terminating Processes by Name

```bash
# Kill all processes with a specific name
pkill process_name

# Kill processes by pattern
pkill -f pattern

# Send a specific signal (e.g., SIGKILL)
pkill -9 process_name
```

### Process Priorities

The "niceness" value (-20 to 19) determines process priority. Lower values = higher priority.

```bash
# Start a process with a specific priority
nice -n 10 command

# Change priority of a running process
renice +10 -p PID

# Run a process with the highest priority (requires root)
sudo nice -n -20 command
```

### Background and Foreground Processes

```bash
# Run a command in the background
command &

# Resume a suspended process in the background
bg %job_number

# Bring a background process to the foreground
fg %job_number

# Send a foreground process to the background
# First press Ctrl+Z to suspend, then:
bg
```

### Process Monitoring Tools

```bash
# System and process monitor
htop

# System monitor with more details
glances  # sudo apt install glances

# Process visualization
pstree

# Check process start time and resource usage
ps -eo pid,user,start_time,cmd,%cpu,%mem

# Monitor file system events
sudo apt install inotify-tools
inotifywait -m /path/to/monitor
```

### Cron Jobs and Scheduled Tasks

Cron allows you to schedule commands to run at specific times:

```bash
# Edit your user's crontab
crontab -e

# List your cron jobs
crontab -l
```

Crontab format:
```
# minute hour day-of-month month day-of-week command
# * * * * * command (runs every minute)
# 0 * * * * command (runs every hour at minute 0)
# 0 0 * * * command (runs at midnight every day)
# 0 0 * * 0 command (runs at midnight every Sunday)
```

Examples:
```
# Run backup script at 2:30 AM daily
30 2 * * * /home/user/scripts/backup.sh

# Run system updates every Monday at 3 AM
0 3 * * 1 apt update && apt upgrade -y

# Run a script every 5 minutes
*/5 * * * * /path/to/script.sh
```

#### Systemd Timers (Modern Alternative to Cron)

```bash
# Create a service unit
sudo nano /etc/systemd/system/myscript.service
```

```ini
[Unit]
Description=My Service

[Service]
Type=oneshot
ExecStart=/path/to/script.sh

[Install]
WantedBy=multi-user.target
```

```bash
# Create a timer unit
sudo nano /etc/systemd/system/myscript.timer
```

```ini
[Unit]
Description=Run My Service Daily

[Timer]
OnCalendar=*-*-* 02:30:00
Persistent=true

[Install]
WantedBy=timers.target
```

```bash
# Enable and start the timer
sudo systemctl enable myscript.timer
sudo systemctl start myscript.timer

# List all timers
systemctl list-timers
```

### Exercise: Process Management

1. Monitor system processes using `top` and `htop`
2. Find specific processes using `ps` and `pgrep`
3. Experiment with process priorities using `nice` and `renice`
4. Set up cron jobs to run commands at scheduled times
5. Practice killing processes using different signals

## System Administration Tasks

This section covers common administration tasks for managing Linux systems.

### System Information

```bash
# Display system and kernel information
uname -a

# Display Linux distribution information
cat /etc/os-release
lsb_release -a

# Display hardware information
sudo lshw

# Display CPU information
cat /proc/cpuinfo
lscpu

# Display memory information
cat /proc/meminfo
free -h

# Display disk information
df -h
sudo fdisk -l
lsblk

# Display PCI devices
lspci

# Display USB devices
lsusb

# Display block devices
lsblk

# Show environment variables
env

# Display loaded kernel modules
lsmod
```

### User Management

```bash
# Add a new user
sudo adduser username

# Add a user to sudo group
sudo usermod -aG sudo username

# Switch to another user
su - username

# Change user password
sudo passwd username

# Lock/unlock user account
sudo passwd -l username  # Lock
sudo passwd -u username  # Unlock

# View user login history
last
lastlog

# Remove a user
sudo deluser username
sudo deluser --remove-home username  # Also remove home directory
```

### Service Management

#### Systemd (Modern Linux Systems)

```bash
# Start a service
sudo systemctl start service_name

# Stop a service
sudo systemctl stop service_name

# Restart a service
sudo systemctl restart service_name

# Reload configuration without restarting
sudo systemctl reload service_name

# Enable service to start at boot
sudo systemctl enable service_name

# Disable service from starting at boot
sudo systemctl disable service_name

# Check service status
systemctl status service_name

# List all services
systemctl list-units --type=service

# List all running services
systemctl list-units --type=service --state=running

# View service logs
journalctl -u service_name

# Follow service logs in real-time
journalctl -u service_name -f
```

#### SysVinit (Older Systems)

```bash
# Start a service
sudo service service_name start

# Stop a service
sudo service service_name stop

# Restart a service
sudo service service_name restart

# Check service status
sudo service service_name status

# Enable service to start at boot
sudo update-rc.d service_name defaults

# Disable service from starting at boot
sudo update-rc.d service_name disable
```

### Log Management

#### System Logs

```bash
# View system messages
cat /var/log/syslog

# View authentication logs
sudo cat /var/log/auth.log

# View kernel logs
sudo dmesg

# Follow logs in real-time
tail -f /var/log/syslog

# View boot logs (systemd)
journalctl -b

# View logs for a specific service
journalctl -u service_name

# Filter logs by time
journalctl --since "2023-04-15" --until "2023-04-16 03:00"
journalctl --since "1 hour ago"
```

#### Log Rotation

Log rotation helps manage log files by archiving and compressing old logs:

```bash
# Configuration files are in /etc/logrotate.d/
sudo nano /etc/logrotate.d/custom_logs
```

Example logrotate configuration:
```
/var/log/myapp/*.log {
    daily
    rotate 7
    compress
    delaycompress
    missingok
    notifempty
    create 640 user group
    postrotate
        service myapp reload
    endscript
}
```

### Storage Management

#### Disk Partitioning

```bash
# List disks and partitions
sudo fdisk -l
lsblk

# Create partitions using fdisk
sudo fdisk /dev/sdX
# Use interactive commands: n (new), p (primary), w (write)

# Format a partition
sudo mkfs.ext4 /dev/sdX1  # Create ext4 filesystem
sudo mkfs.xfs /dev/sdX2   # Create XFS filesystem
```

#### Mounting Filesystems

```bash
# Create a mount point
sudo mkdir /mnt/mydisk

# Mount a filesystem
sudo mount /dev/sdX1 /mnt/mydisk

# Mount with specific options
sudo mount -o rw,noexec /dev/sdX1 /mnt/mydisk

# Unmount a filesystem
sudo umount /mnt/mydisk

# Auto-mount at boot (edit /etc/fstab)
sudo nano /etc/fstab
```

Example /etc/fstab entry:
```
/dev/sdX1 /mnt/mydisk ext4 defaults 0 2
```

#### Logical Volume Management (LVM)

LVM adds a layer of abstraction between physical disks and filesystems, enabling flexible storage management:

```bash
# Install LVM tools
sudo apt install lvm2  # Debian/Ubuntu
sudo dnf install lvm2  # Fedora/RHEL

# Create physical volumes
sudo pvcreate /dev/sdX1 /dev/sdY1

# Create a volume group
sudo vgcreate myvg /dev/sdX1 /dev/sdY1

# Create a logical volume
sudo lvcreate -n mylv -L 10G myvg

# Format the logical volume
sudo mkfs.ext4 /dev/myvg/mylv

# Mount the logical volume
sudo mount /dev/myvg/mylv /mnt/lvm

# Extend a volume group
sudo vgextend myvg /dev/sdZ1

# Extend a logical volume and resize the filesystem
sudo lvextend -L +5G /dev/myvg/mylv
sudo resize2fs /dev/myvg/mylv
```

#### RAID Configuration

RAID (Redundant Array of Independent Disks) provides redundancy or performance improvements:

```bash
# Install mdadm tool
sudo apt install mdadm  # Debian/Ubuntu
sudo dnf install mdadm  # Fedora/RHEL

# Create a RAID 1 array (mirroring)
sudo mdadm --create /dev/md0 --level=1 --raid-devices=2 /dev/sdX1 /dev/sdY1

# Create a RAID 5 array (striping with parity)
sudo mdadm --create /dev/md0 --level=5 --raid-devices=3 /dev/sdX1 /dev/sdY1 /dev/sdZ1

# Check RAID status
cat /proc/mdstat
sudo mdadm --detail /dev/md0

# Format and mount the RAID array
sudo mkfs.ext4 /dev/md0
sudo mount /dev/md0 /mnt/raid

# Save RAID configuration
sudo mdadm --detail --scan | sudo tee -a /etc/mdadm/mdadm.conf
```

### Exercise: Storage Management

1. Create and format a new partition
2. Mount the partition and configure it to auto-mount at boot
3. Set up a basic LVM configuration
4. Monitor disk usage and identify large files or directories
5. Create a simple RAID array (if you have multiple disks available)

## Networking Fundamentals

Networking is a critical aspect of Linux administration. This section covers the essentials of Linux networking.

### Network Configuration

#### Viewing Network Information

```bash
# Show network interfaces
ip addr
ifconfig  # Legacy command

# Show routing table
ip route
route -n  # Legacy command

# Show DNS configuration
cat /etc/resolv.conf

# Show hostname and DNS domain
hostname
hostname -f  # Fully qualified domain name

# Display all network connections
netstat -tuln  # Legacy command
ss -tuln      # Modern command

# Show network statistics
netstat -s
ss -s
```

#### Configuring Network Interfaces

**Temporary Configuration:**

```bash
# Set IP address
sudo ip addr add 192.168.1.10/24 dev eth0

# Delete IP address
sudo ip addr del 192.168.1.10/24 dev eth0

# Set interface up/down
sudo ip link set eth0 up
sudo ip link set eth0 down

# Add a route
sudo ip route add 10.0.0.0/24 via 192.168.1.1

# Add default route
sudo ip route add default via 192.168.1.1
```

**Persistent Configuration:**

On Ubuntu/Debian (using Netplan):
```bash
# Edit Netplan configuration
sudo nano /etc/netplan/01-netcfg.yaml
```

Example Netplan configuration:
```yaml
network:
  version: 2
  renderer: networkd
  ethernets:
    eth0:
      dhcp4: no
      addresses: [192.168.1.10/24]
      gateway4: 192.168.1.1
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]
```

```bash
# Apply Netplan configuration
sudo netplan apply
```

On RHEL/CentOS/Fedora:
```bash
# Edit network interface configuration
sudo nano /etc/sysconfig/network-scripts/ifcfg-eth0
```

Example ifcfg-eth0:
```
TYPE=Ethernet
BOOTPROTO=none
IPADDR=192.168.1.10
PREFIX=24
GATEWAY=192.168.1.1
DNS1=8.8.8.8
DNS2=8.8.4.4
DEFROUTE=yes
IPV4_FAILURE_FATAL=no
NAME=eth0
DEVICE=eth0
ONBOOT=yes
```

```bash
# Apply configuration
sudo systemctl restart NetworkManager
```

#### Network Diagnostics

```bash
# Ping a host
ping google.com

# Trace route to a host
traceroute google.com
mtr google.com  # More detailed traceroute

# DNS lookup
nslookup google.com
dig google.com
host google.com

# Check if a port is open
telnet host port
nc -zv host port

# Check network bandwidth
sudo apt install iperf3  # Install iperf3
iperf3 -s  # Run as server
iperf3 -c SERVER_IP  # Run as client

# Check which process is using a port
sudo lsof -i :80
sudo netstat -tulpn | grep 80
sudo ss -tulpn | grep 80
```

### Firewall Configuration

#### Uncomplicated Firewall (UFW) on Ubuntu/Debian

```bash
# Install UFW
sudo apt install ufw

# Check status
sudo ufw status

# Enable/disable UFW
sudo ufw enable
sudo ufw disable

# Allow/deny service by name
sudo ufw allow ssh
sudo ufw deny http

# Allow/deny port
sudo ufw allow 22/tcp
sudo ufw deny 80/tcp

# Allow from specific IP address
sudo ufw allow from 192.168.1.5

# Allow from specific IP to specific port
sudo ufw allow from 192.168.1.0/24 to any port 3306

# Delete rules
sudo ufw delete allow 80/tcp

# Reset rules
sudo ufw reset
```

#### Firewalld on RHEL/CentOS/Fedora

```bash
# Check status
sudo firewall-cmd --state

# List allowed services
sudo firewall-cmd --list-services

# List all open ports
sudo firewall-cmd --list-ports

# Add a service
sudo firewall-cmd --add-service=http --permanent

# Add a port
sudo firewall-cmd --add-port=8080/tcp --permanent

# Remove a service
sudo firewall-cmd --remove-service=http --permanent

# Apply changes
sudo firewall-cmd --reload

# Add rich rule
sudo firewall-cmd --add-rich-rule='rule family="ipv4" source address="192.168.1.0/24" service name="ssh" accept' --permanent
```

### Network Services

#### SSH (Secure Shell)

```bash
# Install SSH server
sudo apt install openssh-server  # Debian/Ubuntu
sudo dnf install openssh-server  # Fedora/RHEL

# Start SSH server
sudo systemctl start sshd
sudo systemctl enable sshd

# Connect to a remote server
ssh username@hostname

# Connect with specific port
ssh -p 2222 username@hostname

# Connect with identity file
ssh -i /path/to/key.pem username@hostname

# Generate SSH key pair
ssh-keygen -t rsa -b 4096

# Copy SSH key to remote server
ssh-copy-id username@hostname

# SSH config file
nano ~/.ssh/config
```

Example SSH config:
```
Host myserver
    HostName 192.168.1.10
    User username
    Port 22
    IdentityFile ~/.ssh/id_rsa
```

#### DHCP (Dynamic Host Configuration Protocol)

```bash
# Install DHCP server
sudo apt install isc-dhcp-server  # Debian/Ubuntu
sudo dnf install dhcp-server      # Fedora/RHEL

# Configure DHCP server
sudo nano /etc/dhcp/dhcpd.conf
```

Example dhcpd.conf:
```
subnet 192.168.1.0 netmask 255.255.255.0 {
  range 192.168.1.100 192.168.1.200;
  option domain-name-servers 8.8.8.8, 8.8.4.4;
  option domain-name "example.local";
  option routers 192.168.1.1;
  option broadcast-address 192.168.1.255;
  default-lease-time 600;
  max-lease-time 7200;
}
```

#### DNS Server (BIND)

```bash
# Install BIND
sudo apt install bind9 bind9utils  # Debian/Ubuntu
sudo dnf install bind bind-utils   # Fedora/RHEL

# Configure BIND
sudo nano /etc/bind/named.conf.local
```

Example zone configuration:
```
zone "example.local" {
    type master;
    file "/etc/bind/zones/db.example.local";
};
```

### Exercise: Network Configuration

1. Set up a static IP address on your network interface
2. Configure your system to use Google DNS servers (8.8.8.8, 8.8.4.4)
3. Set up basic firewall rules to allow SSH and HTTP
4. Generate SSH keys and configure SSH for passwordless login
5. Use network diagnostic tools to troubleshoot connectivity issues

## Basic Security Principles

Security is a critical aspect of Linux administration. This section covers essential security practices.

### User Account Security

```bash
# Set password complexity requirements
sudo nano /etc/pam.d/common-password

# Set password expiration
sudo chage -M 90 username  # Set max days
sudo chage -l username     # List password info

# Lock unused accounts
sudo passwd -l username

# Remove unused accounts
sudo userdel username

# Configure password policies
sudo apt install libpam-pwquality  # Debian/Ubuntu
sudo dnf install libpwquality      # Fedora/RHEL

# Edit password policy configuration
sudo nano /etc/security/pwquality.conf
```

Example password policy settings:
```
# Minimum password length
minlen = 12

# Require at least one uppercase character
ucredit = -1

# Require at least one lowercase character
lcredit = -1

# Require at least one digit
dcredit = -1

# Require at least one special character
ocredit = -1

# Remember 5 previous passwords
remember = 5
```

### File and Directory Security

```bash
# Find files with insecure permissions
find /home -type f -perm -o+w

# Find SUID/SGID files
find / -type f -perm /6000 -ls 2>/dev/null

# Set secure permissions for sensitive files
chmod 600 ~/.ssh/id_rsa           # Private key
chmod 644 ~/.ssh/id_rsa.pub       # Public key
chmod 600 ~/.ssh/authorized_keys  # Authorized keys
chmod 644 ~/.ssh/known_hosts      # Known hosts

# Set secure directory permissions
chmod 700 ~/.ssh                  # SSH directory
chmod 750 /home/username          # Home directory
```

### System Security Updates

```bash
# Update package lists
sudo apt update      # Debian/Ubuntu
sudo dnf check-update # Fedora/RHEL

# Install security updates only
sudo apt-get -s dist-upgrade | grep "^Inst" | grep -i security # Check security updates
sudo unattended-upgrade -d # Debian/Ubuntu

# Enable automatic security updates
sudo apt install unattended-upgrades
sudo dpkg-reconfigure unattended-upgrades
```

### Securing SSH

```bash
# Edit SSH configuration
sudo nano /etc/ssh/sshd_config
```

Recommended SSH settings:
```
# Disable root login
PermitRootLogin no

# Use SSH key authentication only
PasswordAuthentication no

# Limit user access
AllowUsers user1 user2

# Change default port (adds security by obscurity)
Port 2222

# Restrict to specific IP addresses
ListenAddress 192.168.1.10

# Set idle timeout (5 minutes)
ClientAliveInterval 300
ClientAliveCountMax 0

# Disable empty passwords
PermitEmptyPasswords no

# Disable X11 forwarding if not needed
X11Forwarding no

# Use strong ciphers and MACs
Ciphers chacha20-poly1305@openssh.com,aes256-gcm@openssh.com
MACs hmac-sha2-512-etm@openssh.com,hmac-sha2-256-etm@openssh.com
```

```bash
# Restart SSH service after configuration changes
sudo systemctl restart sshd
```

### Firewall Configuration

```bash
# Basic UFW setup (Ubuntu/Debian)
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow 22/tcp
sudo ufw allow 80/tcp
sudo ufw allow 443/tcp
sudo ufw enable

# Basic firewalld setup (RHEL/CentOS/Fedora)
sudo firewall-cmd --permanent --add-service=ssh
sudo firewall-cmd --permanent --add-service=http
sudo firewall-cmd --permanent --add-service=https
sudo firewall-cmd --reload
```

### Security Auditing

```bash
# Install security auditing tools
sudo apt install lynis rkhunter chkrootkit # Debian/Ubuntu
sudo dnf install lynis rkhunter chkrootkit # Fedora/RHEL

# Run security audit
sudo lynis audit system

# Check for rootkits
sudo rkhunter --check
sudo chkrootkit

# Scan for vulnerabilities
sudo apt install nmap
sudo nmap -sV -p1-65535 localhost
```

### Intrusion Detection

```bash
# Install fail2ban to prevent brute force attacks
sudo apt install fail2ban  # Debian/Ubuntu
sudo dnf install fail2ban  # Fedora/RHEL

# Configure fail2ban
sudo nano /etc/fail2ban/jail.local
```

Example fail2ban configuration:
```
[sshd]
enabled = true
port = ssh
filter = sshd
logpath = /var/log/auth.log
maxretry = 3
bantime = 3600
```

```bash
# Start and enable fail2ban
sudo systemctl enable fail2ban
sudo systemctl start fail2ban

# Check fail2ban status
sudo fail2ban-client status
sudo fail2ban-client status sshd
```

### SELinux and AppArmor

#### SELinux (Security-Enhanced Linux)

Used primarily on Red Hat-based systems:

```bash
# Check SELinux status
getenforce

# Set SELinux mode
sudo setenforce 0  # Permissive mode
sudo setenforce 1  # Enforcing mode

# Configure SELinux
sudo nano /etc/selinux/config

# List SELinux contexts
ls -Z

# Change file context
sudo chcon -t httpd_sys_content_t /var/www/html/index.html

# Restore default context
sudo restorecon -v /var/www/html/index.html
```

#### AppArmor

Used primarily on Debian-based systems:

```bash
# Check AppArmor status
sudo aa-status

# List AppArmor profiles
sudo apparmor_status

# Put a profile in enforce mode
sudo aa-enforce /etc/apparmor.d/usr.sbin.nginx

# Put a profile in complain mode
sudo aa-complain /etc/apparmor.d/usr.sbin.nginx
```

### Exercise: Security Hardening

1. Configure password policies for your system
2. Secure SSH by disabling root login and using key-based authentication
3. Set up a basic firewall allowing only necessary services
4. Install and configure fail2ban to prevent brute force attacks
5. Run a security audit using Lynis and address high-priority findings

## System Monitoring

Monitoring is essential for maintaining system health and diagnosing issues.

### Real-time Monitoring Tools

```bash
# System activity reporter
sar 1 10  # Sample every 1 second for 10 samples

# Process viewer
top
htop  # More user-friendly version

# I/O monitoring
iostat -xz 1

# Memory usage
free -m
watch -n 1 free -m  # Update every second

# Network monitoring
netstat -tulpn
ss -tulpn

# Disk usage
df -h
du -sh /var/*  # Size of directories in /var

# System overview
glances  # Must install: sudo apt install glances

# Watch command for any command
watch -n 5 'ps aux | grep nginx'  # Monitor nginx processes every 5 seconds
```

### Log Monitoring

```bash
# View system messages
tail -f /var/log/syslog

# View authentication logs
tail -f /var/log/auth.log

# View Apache/Nginx access logs
tail -f /var/log/apache2/access.log
tail -f /var/log/nginx/access.log

# Monitor logs with journalctl (systemd)
journalctl -f  # Follow all logs
journalctl -u nginx -f  # Follow nginx service logs

# Search logs for errors
grep -i error /var/log/syslog
```

### Process Monitoring

```bash
# Find CPU/memory intensive processes
ps aux --sort=-%cpu | head -10  # Top 10 CPU consumers
ps aux --sort=-%mem | head -10  # Top 10 memory consumers

# Track process activity
pstree -p  # Process tree
pgrep nginx  # Find PIDs of nginx processes

# Monitor specific process
top -p $(pgrep -d ',' nginx)
```

### Advanced Monitoring Tools

#### Prometheus and Grafana

Modern monitoring stack for metrics collection and visualization:

```bash
# Install Prometheus
wget https://github.com/prometheus/prometheus/releases/download/v2.37.0/prometheus-2.37.0.linux-amd64.tar.gz
tar xvfz prometheus-*.tar.gz
cd prometheus-*

# Run Prometheus
./prometheus --config.file=prometheus.yml

# Install Node Exporter for system metrics
wget https://github.com/prometheus/node_exporter/releases/download/v1.3.1/node_exporter-1.3.1.linux-amd64.tar.gz
tar xvfz node_exporter-*.tar.gz
cd node_exporter-*
./node_exporter

# Install Grafana
sudo apt-get install -y apt-transport-https software-properties-common
wget -q -O - https://packages.grafana.com/gpg.key | sudo apt-key add -
echo "deb https://packages.grafana.com/oss/deb stable main" | sudo tee -a /etc/apt/sources.list.d/grafana.list
sudo apt-get update
sudo apt-get install grafana
sudo systemctl start grafana-server
sudo systemctl enable grafana-server
```

#### Nagios/Icinga

Traditional monitoring systems for availability and performance:

```bash
# Install Nagios
sudo apt install nagios4  # Debian/Ubuntu

# Install Icinga2
sudo apt install icinga2 icingaweb2  # Debian/Ubuntu
```

### Custom Monitoring Scripts

Example disk space alert script:
```bash
#!/bin/bash

THRESHOLD=90
EMAIL="admin@example.com"

df -h | grep -vE '^Filesystem|tmpfs|cdrom' | awk '{ print $5 " " $1 }' | while read output;
do
  usep=$(echo $output | awk '{ print $1}' | cut -d'%' -f1 )
  partition=$(echo $output | awk '{ print $2 }' )
  if [ $usep -ge $THRESHOLD ]; then
    echo "ALERT: Running out of space \"$partition ($usep%)\" on $(hostname) as on $(date)" | \
    mail -s "Disk Space Alert: $usep% on $(hostname)" $EMAIL
  fi
done
```

### Setting Up Monitoring as a Service

```bash
# Create a systemd service for a monitoring script
sudo nano /etc/systemd/system/disk-monitor.service
```

Example systemd service:
```ini
[Unit]
Description=Disk Space Monitoring Service
2890
