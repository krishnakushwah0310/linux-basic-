##  Table of Contents:
1. **What is Linux?**
2. **CentOS Installation in VirtualBox**
3. **Linux Distributions**
4. **Linux Filesystem Structure**
5. **Basic Linux Commands**
6. **Understanding the Linux Terminal**
7. **Working with Files and Directories**
8. **Permissions and Ownership**
9. **Package Management**
10. **Process Management**
11. **Networking Commands**
12. **Shell Scripting Basics**

---

##  1. **What is Linux?**

Linux is an open-source operating system (OS) that's based on the Linux kernel. It's used in servers, desktops, mobile devices, and embedded systems. Unlike Windows or macOS, Linux is free to use, modify, and distribute. It’s known for being secure, stable, and versatile.

---

##  2.**CentOS Installation in VirtualBox**

## 📹 **Installation Video**
To watch the full installation video, click on the link below:  
### *[CentOS Installation in VirtualBox](https://www.youtube.com/watch?v=ZqyVrfW2c6g)*


---


Follow the steps below to successfully install CentOS in VirtualBox. This guide will walk you through each step with clear instructions.

---

### *Step 1: Download CentOS ISO*
1. Visit the [CentOS website](https://www.centos.org/download/).
2. Download the *ISO image* that corresponds to your system architecture (e.g., x86_64).
   - Choose the *Minimal ISO* for a lighter installation or the *DVD ISO* for a complete installation.

---

### *Step 2: Create a New Virtual Machine in VirtualBox*
1. *Open VirtualBox* and click on *New* to start creating a new VM.
2. Set the *Name* of your VM (e.g., "CentOS VM").
3. Choose *Linux* for the *Type* and *Red Hat (64-bit)* for the *Version*.
4. Set *Memory (RAM)* allocation: 2GB or more is recommended for optimal performance.
   - Example: 2048MB (2GB) or 4096MB (4GB) depending on your system’s capacity.

---

### *Step 3: Configure the Virtual Machine’s Storage*
1. *Go to the Storage tab* in VM settings.
2. Under *Controller: IDE, click **Empty*.
3. *Attach the CentOS ISO*:
   - Click the *disk icon* next to *Optical Drive* and select *Choose a disk file*.
   - Browse and select the *CentOS ISO* you downloaded in Step 1.

---

### *Step 4: Start the Virtual Machine*
1. *Click Start* to boot the VM from the attached CentOS ISO.
2. The CentOS installation screen should now appear. Select *Install CentOS* and press *Enter* to begin the installation process.

---

### *Step 5: Install CentOS*
1. *Language and Keyboard Layout*:
   - Select your desired *Language* and *Keyboard Layout*.
2. *Installation Destination*:
   - Select the hard disk where CentOS will be installed (usually the default one).
   - You can choose *Automatic Partitioning* for simplicity.
3. *Network Configuration*:
   - Set up your *Network* and ensure it’s *enabled* for internet access.
4. *User Configuration*:
   - Set a *root password* and create a *user account* with administrative privileges.
5. Once the installation completes, click *Reboot*.

---

### *Step 6: Post-Installation Setup*
1. *Initial Boot*:
   - After rebooting, log in using the credentials you created during the installation.
2. *Update CentOS*:
   - Open the *Terminal* and run the following command to update CentOS:
     
     sudo yum update -y
     
3. *Install Additional Software*:
   - Install any necessary software packages using yum or dnf (for newer CentOS versions).

---

### *Additional Tips*
- *Enable Network Adapter*:
   - If you don’t have internet access, ensure your *network settings* are configured correctly. Use *NAT* or *Bridged Adapter* to enable internet.
- *Install VirtualBox Guest Additions*:
   - For better integration (shared folders, enhanced graphics), install *VirtualBox Guest Additions* after logging into CentOS.
   - You can find the option to install it in *Devices > Insert Guest Additions CD image*.

---

###⚡ *Congratulations!* 
You have successfully installed CentOS on VirtualBox! Enjoy exploring your new virtual machine and getting familiar with CentOS.

---

##  3. **Linux Distributions**

A Linux **distribution** (or **distro**) is a version of Linux that includes the Linux kernel and various software packages to make the OS functional.

- **Ubuntu**: User-friendly, great community support.
- **Debian**: Known for its stability.
- **CentOS/RedHat**: Used in enterprise environments.
- **Fedora**: Cutting-edge features, often used by developers.

---

##  4. **Linux Filesystem Structure**

In Linux, everything is a file, and the entire filesystem is organized in a hierarchical tree-like structure, starting from the root directory (/). 

#### Common directories:
- /: The root directory, where everything starts.
- /bin: Essential command binaries.
- /etc: Configuration files.
- /home: User home directories.
- /var: Variable files, such as logs and mail.
- /tmp: Temporary files.
- /dev: Device files.
- /usr: User applications and utilities.

---

##  5. **Basic Linux Commands**

Here are some basic commands that every Linux user should know:

- **ls**: Lists files in the current directory.
  - Example: ls -l (detailed listing)
  
- **pwd**: Prints the current working directory.
  
- **cd**: Changes the current directory.
  - Example: cd /home/user/ (navigate to /home/user/)
  
- **cp**: Copies files or directories.
  - Example: cp file1.txt /home/user/
  
- **mv**: Moves or renames files.
  - Example: mv oldfile.txt newfile.txt
  
- **rm**: Removes files or directories.
  - Example: rm file.txt
  
- **cat**: Displays the contents of a file.
  - Example: cat file.txt
  
- **man**: Displays the manual for a command.
  - Example: man ls

---

##  6. **Understanding the Linux Terminal**

The **terminal** is the command-line interface (CLI) in Linux. It's where you type commands to interact with the system.

- **Prompt**: The terminal shows a prompt indicating it’s ready to accept commands.
  Example: username@hostname:~$
  
- **Root User**: The system administrator account with full privileges, denoted by root. You can switch to root by using sudo or su.

- **Bash**: The default shell for most Linux systems. It allows users to interact with the OS via commands.

---

##  7. **Working with Files and Directories**

#### Navigating Directories:

- **ls**: Lists files and directories.
- **cd**: Change directories.
- **pwd**: Print working directory.

#### File Operations:

- **cp**: Copy files and directories.
- **mv**: Move or rename files and directories.
- **rm**: Remove files or directories.

#### Example:

bash
mkdir myfolder          # Creates a directory
cd myfolder             # Navigates into the folder
touch file.txt          # Creates an empty file
ls                       # Lists files
rm file.txt              # Deletes the file



---

##  8. **Permissions and Ownership**

Linux uses a system of permissions to control who can read, write, and execute files.

- **Owner**: The user who created the file.
- **Group**: Users who belong to the same group.
- **Others**: Everyone else.

#### Commands to manage permissions:

- **chmod**: Change file permissions.
  - Example: chmod +x file.sh (gives execute permission)
  
- **chown**: Change file owner and group.
  - Example: chown user:group file.txt

- **chgrp**: Change the group ownership of a file.
  - Example: chgrp group file.txt

#### Understanding Permissions:
File permissions are displayed as a string of characters like -rwxr-xr--. The first character denotes the file type, followed by three sets of three characters each representing owner, group, and others' permissions.

- **r**: Read
- **w**: Write
- **x**: Execute

---

##  9. **Package Management**

In Linux, software is managed through **package managers**. Package managers allow you to install, update, and remove software.

#### For Ubuntu/Debian (APT):
- **apt-get install <package>**: Install a package.
- **apt-get update**: Update package lists.
- **apt-get upgrade**: Upgrade installed packages.

#### For CentOS (YUM):
- **yum install <package>**: Install a package.
- **yum update**: Update installed packages.

---

##  10. **Process Management**

Processes in Linux are managed through commands that allow you to see running programs and control their execution.

- **ps**: Lists current running processes.
  - Example: ps aux (shows all processes)
  
- **top**: Displays real-time system information and running processes.
  
- **kill**: Terminates a process.
  - Example: kill 1234 (kills process with PID 1234)

- **nohup**: Runs a command even if the terminal is closed.
  - Example: nohup command &

---

##  11. **Networking Commands**

Linux provides various networking tools for configuration and troubleshooting:

- **ifconfig**: Shows or configures network interfaces.
- **ping**: Tests connectivity to a host.
  - Example: ping google.com
  
- **netstat**: Displays network connections and listening ports.
- **ssh**: Secure shell for remote login.
  - Example: ssh username@hostname

---

##  12. **Shell Scripting Basics**

Shell scripting allows you to automate tasks using a sequence of commands.

#### Basic Script Example:

bash
#!/bin/bash
echo "Hello, World!"



- **#!/bin/bash**: Specifies the shell to use.
- **echo**: Prints text to the terminal.

#### Making a script executable:

bash
chmod +x script.sh    # Makes the script executable
./script.sh           # Runs the script

---

##      **by krishna kushwah**          *[LinkedIn](https://www.linkedin.com/in/krishna-kushwah-382812317/)*
