---
title: "Basic Linux Commands For DevOps"
datePublished: Sun May 26 2024 11:57:09 GMT+0000 (Coordinated Universal Time)
cuid: clwnhiq3q00040aldgucqdchs
slug: basic-linux-commands-for-devops
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1716733390977/abb96725-5916-4cd7-939a-ef2306bcbf32.jpeg
tags: linux, devops, devop, linux-for-beginners, linux-basics, devops-articles, linux-commands, devops-trends, devops-journey, devopscommunity

---

### Basic Linux Commands for DevOps

#### Introduction

As a DevOps professional, having a strong command of Linux is crucial. Linux is the backbone of many server environments and cloud platforms, and understanding the basic commands can significantly improve your efficiency and productivity. This article will cover some fundamental Linux commands that every DevOps practitioner should know.

#### File and Directory Management

1. `ls` - List Directory Contents
    
    ```bash
    ls
    ls -l
    ls -a
    ```
    
    The `ls` command lists the files and directories within the current directory. The `-l` flag provides detailed information, while `-a` includes hidden files.
    
2. `cd` - Change Directory
    
    ```bash
    cd /path/to/directory
    cd ~
    cd ..
    ```
    
    The `cd` command changes the current directory. Use `~` to navigate to the home directory and `..` to move up one directory level.
    
3. `mkdir` - Make Directory
    
    ```bash
    mkdir new_directory
    mkdir -p /path/to/new_directory
    ```
    
    The `mkdir` command creates a new directory. The `-p` flag allows the creation of nested directories.
    
4. `rm` - Remove Files or Directories
    
    ```bash
    rm file.txt
    rm -r directory
    ```
    
    The `rm` command deletes files. Use the `-r` flag to remove directories and their contents recursively.
    
5. `cp` - Copy Files or Directories
    
    ```bash
    cp source_file destination_file
    cp -r source_directory destination_directory
    ```
    
    The `cp` command copies files or directories. The `-r` flag allows recursive copying of directories.
    
6. `mv` - Move or Rename Files or Directories
    
    ```bash
    mv old_name new_name
    mv file.txt /new/path/
    ```
    
    The `mv` command moves files or directories and can also be used to rename them.
    

#### File Content Manipulation

1. `cat` - Concatenate and Display Files
    
    ```bash
    cat file.txt
    ```
    
    The `cat` command displays the contents of a file.
    
2. `less` - View File Contents One Page at a Time
    
    ```bash
    less file.txt
    ```
    
    The `less` command allows you to view file contents one page at a time, useful for large files.
    
3. `head` and `tail` - View Beginning or End of Files
    
    ```bash
    head file.txt
    tail file.txt
    tail -f log.txt
    ```
    
    The `head` command displays the first few lines of a file, while `tail` shows the last few lines. The `-f` flag for `tail` continuously monitors the file for new content, useful for log files.
    
4. `grep` - Search Text Using Patterns
    
    ```bash
    grep 'pattern' file.txt
    grep -r 'pattern' /path/to/directory
    ```
    
    The `grep` command searches for text patterns within files. The `-r` flag allows recursive searching within directories.
    
5. `awk` and `sed` - Text Processing
    
    ```bash
    awk '{print $1}' file.txt
    sed 's/old/new/g' file.txt
    ```
    
    `awk` is a powerful text-processing command used for pattern scanning and processing. `sed` is a stream editor for filtering and transforming text.
    

#### System Monitoring and Management

1. `ps` - Report Process Status
    
    ```bash
    ps
    ps aux
    ```
    
    The `ps` command displays information about running processes. The `aux` option provides detailed information about all processes.
    
2. `top` - Display Linux Tasks
    
    ```bash
    top
    ```
    
    The `top` command provides a real-time view of system processes and resource usage.
    
3. `htop` - Interactive Process Viewer
    
    ```bash
    htop
    ```
    
    `htop` is an improved, interactive version of `top` with more features and a user-friendly interface.
    
4. `df` - Report File System Disk Space Usage
    
    ```bash
    df -h
    ```
    
    The `df` command displays the amount of disk space used and available on filesystems. The `-h` flag makes the output human-readable.
    
5. `du` - Estimate File Space Usage
    
    ```bash
    du -sh /path/to/directory
    ```
    
    The `du` command estimates the disk space used by files and directories. The `-sh` option provides a summary in human-readable format.
    
6. `free` - Display Memory Usage
    
    ```bash
    free -h
    ```
    
    The `free` command shows the total, used, and free memory. The `-h` flag makes the output human-readable.
    

#### Networking

1. `ping` - Send ICMP Echo Requests
    
    ```bash
    ping google.com
    ```
    
    The `ping` command checks the connectivity between the host and the specified destination.
    
2. `netstat` - Network Statistics
    
    ```bash
    netstat -tuln
    ```
    
    The `netstat` command displays network connections, routing tables, interface statistics, masquerade connections, and multicast memberships.
    
3. `curl` - Transfer Data from or to a Server
    
    ```bash
    curl http://example.com
    ```
    
    The `curl` command transfers data from or to a server, using various protocols such as HTTP, HTTPS, FTP, and more.
    
4. `wget` - Non-Interactive Network Downloader
    
    ```bash
    wget http://example.com/file.zip
    ```
    
    The `wget` command retrieves files from the web.
    
5. `ssh` - Secure Shell
    
    ```bash
    ssh user@hostname
    ```
    
    The `ssh` command connects to a remote host via the Secure Shell protocol.
    

#### Package Management (Example for Ubuntu/Debian)

1. `apt-get` - APT Package Handling Utility
    
    ```bash
    sudo apt-get update
    sudo apt-get install package_name
    sudo apt-get remove package_name
    ```
    
    The `apt-get` command is used for handling packages in Debian-based distributions. `update` refreshes the package list, `install` installs a package, and `remove` removes a package.
    

#### Conclusion

These are just some of the basic Linux commands that every DevOps professional should be familiar with. Mastering these commands will help you navigate and manage Linux systems more efficiently, allowing you to focus on automating processes and improving workflows. As you gain more experience, you'll discover many more powerful commands and tools that Linux offers.