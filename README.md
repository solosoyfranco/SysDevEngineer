# Linux Systems Developer Engineer
### General questions



* What did you learn yestarday/this week?
    
        I'm currently learning about Evi Nemeth, Unix and linux system administrator handbook, ansible, prometheus

* Talk about your preferred development/administration environment, (OS, Editor, Browsers, Tools, etc.)
    
        After years of using Windows, Linux, and MacOS, my preferred operating system is Fedora, because it's more reliable, secure, and backed by a great company.
        Editor: VSC, it's great because all the extensions and plugins from the community.
        Browsers: Firefox and Brave browser, for personal browsing, and Google Chrome for work-related tabs, choosing that for compatibility when browsing the web (chrome web engine).
        Tools: fail2ban, grsync, htop, ohmyzsh, KVM

* Tell me about the las major Linux Project you finished.

        Automate the installation process of the Type 1 hypervisor (Debian-based) called proxmox VE. With PCI KVM pass-through, network link aggregation, LXC template update, swap memory, cluster, backups, etc.


* Tell me about the biggest mistake you've made in [some recent time period] and how you would do it differently today. What did you learn from this experience? 
        
        Haven't used GIT and LINT (shellcheck) for scripting before. It is much more functional than taking notes in the cloud.


* Why we must choose you?
        
        This position requires me to do things I have experience and that I like to do. Also I'm a pleasant guy to be around. :) 


* What function does DNS play on a network?

        Domain Name System, DNS servers converts URLs and domain names into IP addresses that computer can understand and use. They translate what a user types into a browser into something the machine can use to find a webpage.

* What is HTTP?

        HyperText Transfer Protocol, is an application-layer for transmitting hypermedia documents, such as html. It was designed for communication between web browsers and web servers, but it can also be used for other purposes.

* What is an HTTP proxy and how does it work?

        An HTTP proxy acts as a high-performance content filter on traffic received by an HTTP client and HTTP server. The HTTP proxy protocol routes client requests from web browsers to the internet and supports rapid data caching.

* Describe briefly how HTTPS works.

        HTTPS occurs based upon the transmission of TLS/SSL certificates, which verify that a particular provider is who they say they are. When a user connects to a webpage, the webpage will send over its SSL certificate which contains the public key necessary to start the secure session. it uses the 443 port to send the encrypted traffic.

* What is SMTP? Give the basic scenario of how a mail message is delivered via SMTP.

        SMTP or Simple Mail Transfer Protocol is an application that is used to send, receive, and relay outgoing emails between senders and receivers. When an email is sent, it's transferred over the internet from one server to another using SMTP. In simple terms, an SMTP email is just an email sent using the SMTP server.
        A SMTP client contacts the destination host's SMTP server on port 25 across the connection, to deliver the mail. The SMTP server is an always-on listening mode. 

* What is RAID? What is RAID0, RAID1, RAID5, RAID10?

        Redundant Array Independent Disks, is a way of storing the same data in different places on multiple hard disks, for the purposes of data redundancy, performance improvement, or both.
        RAID 0 (disk striping) is just getting all space available across multiple storage devices. 
        RAID 1 (mirroring) The disks in the cluster are organized in pairs for mirroring the data.
        RAID 5 uses disk striping with parity, data and parity are striped  evenly across all of the disks, no single disk is a bottleneck. Allows to reconstruct data in case of a disk failure.
        RAID 10 (1+0) combines disk mirroring and disk striping to protect data, minimum of four disks and stripes data across mirrored pairs. As long as one disk in each mirrored pair is functional, data can be retrieved.

* What is a level 0 backup? What is an incremental backup?

        A level 0 copies all blocks in the data file, is used as a staring point for an incremental backup strategy.
        An Incremental backup only copies data that has been changed or created since the previous backup activity.

* Describe the general file system hierarchy of a Linux system

        /bin   -> Essential user command binaries (essential commands.. ls, cp, cat)
        /boot  -> Static files of the boot loader (kernels, initrd)
        /dev   -> Device files (/dev/disk0)
        /etc   -> Host specific system configuration 
        /home  -> User home directories 
        /lib   -> Shared libraries
        /media -> Removable media
        /mnt   -> Temporarily mounted filesystem
        /opt   -> Add-on application software package
        /sbin  -> System binaries
        /srv   -> Data for service from system
        /tmp   -> Temporary files
        /usr   -> User utilities and application
        /proc  -> Process information
        /var   -> variable files (logs, spool files, tmp emails)

        
* Which difference have between public and private SSH key?

        The private key is secret, known only to the user, and should be encrypted and stored safely. The public key can be shared freely with any SSH server to which the user whishes to connect.
        


### Simple Linux Questions:

* What is the name and the UID of the administrator user?

        The UID of the administrator user refers to a unique positive integer that is assigned by the system to each user. 
        root is considered the super user and has the highest access level on a system, with 0=UID

* How to list all files, including hidden ones, in a directory?

        ``` ls -al ```

* What is the Unix/Linux command to remove a directory and its contents?

        ``` rm -r ./DIRECTORY/ ```

* Which command will show you free/used memory? Does free memory exists on linux?

        There are many commands, which display the free or used memory on Linux. The easiest way to track memory usage on Linux is by using the ``` free ``` command. Linux and other Unix based operating systems generally show less free memory as might be available. That is why Swap (a special type of memory) is available for use when the RAM is full.
        Free memory does exist on Linux, the only portion of memory considered "free" by Linux is that which is not used fo anything at all. This does not include the memory space which is used but readily available.

* How to search for the string "my konfu is the best" in files of a directory recursively?

        ``` grep -R "my konfu is the best" ./DIRECTORY/ ```

* How to connect to a remote server or what is SSH?

        SSH, also known as Secure Shell or Secure Socket shell, is a cryptographic network protocol that gives users (administrators) a secure way to access over an unsecured network.
        ``` ssh username@servername_or_ip ```

* How to get all environment variables and how can you use them?

        Running the command ``` env ``` will print all currently used environment variables

* I get "command not found" when I run ```ifconfig -a```. What can be wrong?

        It can mean a handful of things:
                1- The program is not installed.
                2- The executable is not found anywhere in the PATH.
                3- The program was configured by the system administrator to only be executable by root. So a non-sudo user will not be able to execute it.


* What happens if I type TAB-TAB?

        The first TAB press will attempt to auto complete whatever command is being written in the terminal. On the second TAB press, if the command cannot be further autocompleted due to more than one possible matching command, a prompt will appear on the terminal to list all possible suggestions. If no autocomplete is posible at all, then the second TAB press will do nothing.

* What command will show the available disk space on the Unix/Linux system?

        ``` df -h ```

* What commands do you know that can be used to check DNS records?

        ``` nslookup, dig, host```
        Though not the intended use for it, ``` ping ```

* What Unix/Linux commands will alter a files ownership, file permissions?

        ``` chmod ``` will change the permissions of a file.
        ``` chown ``` will change the owner of a file.

* What does ```chmod +x FILENAME``` do?

        This command will add the executable bit for every user on that particular file.

* What does the permission 0750 on a file mean?

        This permission list will set full permissions to the owner of a file, read and execute permissions to those in the group of the file, and no permissions for the other users.

* What does the permission 0750 on a directory mean?

        This permission list will allow the owner of a directory to do whatever operation they wat within it, grant read and execute permissions to files within the directory to members of the group of the directory, and no permissions to other users.

* How to add a new system user without login permissions?

        There are a couple of ways to do this:
                - User with a home directory and without shell (login)
                  - ``` sudo adduser USERNAME --shell=/bin/false ```
                - User without a home directory and shell
                  - ``` sudo add user USERNAME --shell=/bin/false --no-create-home ```
                - User account without a password and without shell so the user can't log in.
                  - ``` sudo add user USERNAME --system ```


* How to add/remove a group from a user?

        ``` usermod -G groupname username ``` 

* What is a bash alias?

        A bash alias are essentially shortcuts that can save you from having to remember long commands.

* How do you set the email address of the root/a user?

        If you have a service like postfix installed on the server, one way to change the email address of any user is by making an entry in /etc/aliases
        ``` root example@gmail.com ```

* What does CTRL-C do?

        Interrupt the process currently being run by sending a SIGINT  to the process.

* What does CTRL-D do?

        Sends an ``` exit() ``` to whatever process is running, but doesn't interrupt it. Commonly used to exit a shell.

* What does CTRL-Z do?

        Instead of interrupting the process like CTRL-C, CTRL-Z will suspend the process and put it into the background.

* What is in /etc/services?

        A human readable mapping of what port common networked services typically listen on.

* How to redirect STDOUT and STDERR in bash? (>/dev/null 2>&1)

        STDOUT goes to output 1. STDERR goes to output 1.
        So one can run a command like ``` cat file.txt 1> output.txt ``` to redirect the standart output of the cat command to output.txt. Running ``` cat  file.txt > output.txt ``` does the same thing.

        If one wants to ignore an error their command may throw, they can do something like ``` command 2> /dev/null ``` to not see any errors printed out.

        What 2>&1 means, is to make a copy of file descriptor 1 using file descriptor 2. So whenever the command outputs to STDERR the user will receive it in STDOUT.

* What is the difference between UNIX and Linux.

        Linux is built on top of an older operating system called UNIX by a bloke by the name of Linus Torvalds. With the combined efforts of Richard Stallman, and Linus Torvalds, Linux was created as an open source alternative to UNIX.

* What is the difference between Telnet and SSH?

        They are both commands used to manage servers remotely, but telnet is unencrypted and shouldn't be used. 

* Explain the three load averages and what do they indicate. What command can be used to view the load averages?

        The load average can be seen with ``` htop ```.
        The three load average are 1 minute, 5 minute and 15 minute intervals of how heavily the CPU of a server is being used.
        A rule of thumb is that the load average of a server should not exceed the number of cores its processor has.

* Can you name a lower-case letter that is not a valid option for GNU ```ls```?

        When running ``` man ls ``` you can see there is no option for -e.

* What is a Linux kernel module?

        Modules are pieces of code that can be loaded and unloaded into the kernel upon demand. They extend the functionality of the kernel without the need to reboot the system. 

* Walk me through the steps in booting into single user mode to troubleshoot a problem.

        If the server does not boot correctly, you can boot into a shell using GRUB. When the server is booting up and the BIOS is still loading, press whatever key is prompted on the screen to enter the GRUB menu.
        Once in the GRUB menu you can select "Advanced options" and select a kernel to boot into recovery mode. From here you can accept the prompt to open a root shell session.
        If GRUB can't save you, make a YUMI key.

* Walk me through the steps you'd take to troubleshoot a 404 error on a web application you administer.

        It depends on the type of content being served, and the type of web application being run.
        If it's simple HTML files, or other static content on Apache/NGiNX web server, then I will simple see if the file exists in the directory being requested, and permissions are readable.
        Some general troubleshooting will be... check the httpd service status, check logs, look for any error or warning, check firewall and ports open, ping connection, check the interface config, check cables and physical networking connections, restart server.

* What is ICMP protocol? Why do you need to use?

        ICMP stands for Internet Control Message Protocol. It's mostly used to send error messages and operation information between network devices.


### Medium Linux Questions

* What do the following commands do and how would you use them?
  * ``` tee ``` = Receives input and redirects it to both the terminal and an output one or more files.
  * ``` awk ``` = Allows scanning of input (file or STDIN) for patterns. Useful for things like manipulating data and generating reports.
  * ``` tr ``` = Used to translating or delete certain characters. Useful for things like transform uppercase to lowercase, squeezing repeating characters, deleting specific characters and basic fin and replace.
  * ``` cut ``` =  Used to remove a columns from a file.
  * ``` tac ``` = Prints a file but with the line numbers reversed. Opposite of CAT command.
  * ``` curl ``` = Short for Client URL, tool that transfer data to or from a server, using various network protocols.
  * ``` wget ``` = Utility for downloading files from the web.
  * ``` watch ``` = Used to run any command at regular intervals and displays the output of the command on the terminal window.
  * ``` head ``` =  Looks at the first n rows of an input. By default displays only the first 10 lines of the file specified.
  * ``` tail ``` = It's the complementary of  the HEAD command, prints the last n number of data of the given input. By default it prints the last 10 lines of the specified files.
  * ``` less ``` = Read the contents of a text file one page(one screen) at a time. 
  * ``` cat ``` = Reads data from the file and gives their content as output. Help us to create, view, concatenate files.
  * ``` touch ``` = Used to create, change and modify timestamps of a file. Creates a file without any content.
  * ``` sar ``` =  Stands for System Activity Report, Used to see resource usage(CPU, Memory, disk IO) of the server at a point in time.
  * ``` netstat ``` = Prints network information about the server, such as ports in use, network interfaces, routing tables.
  * ``` tcpdump ``` = Its a packet sniffing and packet analyzing tool. Records all of the packets going over a network interface.
  * ``` lsof ``` = Stands for List Of Open File. Provides a list of files that are opened.


* What does an ```&``` after a command do? 

        This is know as job control under unix. ```&``` after a command is meant to run the command in the background. This way a long running command is not blocking. If the parent process dies, this background command will still die as well.

* What does ```& disown``` after a command do?

        The difference between  ``` command & ``` and ``` command & disown ``` is that disowning the process results in it no longer showing up in the list of jobs attached to a shell. 
        However, in both cases the command will start a process which is still owned by the terminal that started it. So if the terminal is closed, the process will die in both cases.

* What is a packet filter and how does it work?

        A packet filter inspects packet headers on a network interface. This can be implemented on a firewall, or on a linux server directly. The filter looks at the contents of each packet, and compares it to a list of rules for acceptable traffic. If the packet is considered acceptable, then it is allowed through the network interface.


* What is Virtual Memory?

        Virtual memory in Linux is the ability to use a disk to extend Memory. There are a couple of ways to do this: 
        -Create a swap space
        -Create a swap file
        -Write a program which takes advantage of memory mapped IO.

* What is swap and what is it used for?

        Swap is a portion of the disk that the server uses as an extension to memory when the server is running out of memory.
        A good reason to use swap is to prevent a server from crashing if it begins to run out of memory. Instead it will try to extend memory using dedicated space on the disk, and continue operations, at a considerably slower speed.

* What is A record, an NS record, a PTR record, a CNAME record, an MX record?

        - A record: The A stands for address. Maps a hostname to an IP address.
        - NS record: a Name Server record which indicates which DNS server(s) are authoritative for a specific domain. Basically, NS records tell the internet where to go to find out a domain's IP address.
        - PTR record: A DNS pointer record (PTR short) provides the domain name associated with an IP  address. A PTR record is exactly the opposite of the "A record", maps an IP address in reverse to a hostname.
        - CNAME record: The "canonical name" (cname) creates an "alias" name which maps typically to an A record, but can also be an alias of another alias.
        - MX record: A DNS "mail exchange" (MX) record directs email to a mail server.

* Are there any other RRs and what are they used for?

        There are plenty of other DNS resource records:
        - AAAA: match a domain to an IPv6 address.
        - TXT: allow to enter text into the DNS. Originally intended fo human-readable notes.
        - SOA: "start of authority" record stores important information about a domain or zone such as the email address of the administrator, when the domain was las updated, and how long the server should wait between refreshes.
        - SRV: The "service" record specifies a host and port for specific services such as voice over IP (VoIP), instant messaging, and so on. 
        - SPF: a Sender Policy Framework record is a type of DNS TXT record that lists all the servers authorized to send emails from a particular domain.

* What is a Split-Horizon DNS?

        Split Horizon DNS is the ability to return different results to DNS queries based on the IP address of the requester. 
        This is beneficial if you have a service (A) running on a public IP address within a corporate (firewalled) network, that must be accessed by another service (B) running on a private IP address within the corporate network. Instead of service B resolving service A to a public IP address and thus needing to go out of the firewall to route to it, is possible using Split-Horizon DNS to get service B to get a different result which is the private IP address of service A.

* What is the sticky bit?

        The sticky bit on a file is used to grant it additional properties in therms of permissions. In a typical file, there is octal notation to denote the permissions it has. A file can have permissions set to 755 for example. However, there is a fourth octal bit which is not often talked about, which is the sticky bit at the beginning. The file actually has permissions of 0755.
        The sticky bit can be set by doing ``` chmod +t file.txt ```. What this particular permission does is prevent anyone but the owner of the file from renaming or deleting this file.

* What does the immutable bit do to a file?

        The immutable bit on a file is set by running ``` chmod +i file.txt. ```. It prevents the file from being modified, deleted, renamed or linked to.

* What is the difference between hardlinks and symlinks? What happens when you remove the source to a symlink/hardlink?

        - A symlink can cross filesystems, but a hardlink cannot.
        - A symlink has a different inode for the link, whereas the hardlink uses the same inode. 
        - If you delete the source file, the symlink becomes a "dead link" that points to nowhere. The hard link will continue to point to the old file because it wasn't wiped from the hard drive, so the hard link can still be used to read the content of the old file.

* What is an inode and what fields are stored in an inode?

        An inode contains metadata about a file but not the file itself.
        It contains information such as:
        - The block at which file is found.
        - The permissions of that file.
        - The number of the inode (there is a limit of inodes on a per-filesystem basis)

* How to force/trigger a file system check on next reboot?

        Is not recommended to run ``` fsck ``` command on a mounted file system. The simplest way to force fsck filesystem check on a root partition is to create an empty file called forcefsck in the partition root directory.
        ``` touch /forcefsck ```
        The empy file created by the command above will override any other settings for the fsck and force fsck to check the filesystem on the next system reboot.
        
        To configure file system check on "N" number of reboots, run the following command ``` tune2fs -c 1 /dev/sda1 ``` which will change the maximum number of times a filesystem has been mounted before requiring a check. To disable ``` tune2fs -c 0  /dev/sda1 ```

* What is SNMP and what is it used for?

        Stands for Simple Network Management Protocol. It is mostly used for monitoring devices over the network. So long as the correct MIBs are presented, it is possible to use an SNMP walk to collect metrics from given devices.

* What is a runlevel and how to get the current runlevel?

        A runlevel is a description of what is running on a server at a particular runlevel.
        There are 6 standard levels, but more can be added:
        - 0 - Shutdown. The server will shut down at this runlevel
        - 1 - Single-user mode, no networking.
        - 2 - Multi-user mode, no networking.
        - 3 - Multi-user mode, with networking.
        - 4 - User-definable.
        - 5 - Multi-user mode, with networking and GUI.
        - 6 - Reboot. The server will restart at this runlevel.

        To get the current (and previous) runlevel, just run the ``` runlevel ``` command.

* What is SSH port forwarding?

        SSH port forwarding (also referred to as SSH tunneling) is simply routing the local network traffic through SSH to remote hosts. Is useful for transporting network data of services that use an unencrypted protocol, such as VNC or FTP, accessing geo-restricted content, or bypassing intermediate firewalls. Basically, you can forward any TCP port and tunnel the traffic over a secure SSH connection.

* What is the difference between local and remote port forwarding?

        - Local SSH port forwarding allows connecting from your local computer to a remote server. Your set up a tunnel from localhost on port 1234 to remote host on port 4321. Then you can access the remote host on port 4321 by making a request against port 1234 locally.

        - Remote SSH port forwarding allows connecting from a remote to server to your local computer.Then you can run a similar command to local port forwarding which allow accessing an application running on localhost port 1234 by making a request to the remote server on port 4321.


* What are the steps to add user to a system without using useradd/adduser?

        1. Create an entry for the user in /etc/passwd
        2. Create an entry for the user in /etc/shadow
        3. Create an entry for the user in /etc/group
        4. Create a home directory and make sure it is owned by the correct user and group

* What is MAJOR and MINOR numbers of special files?

        Special files, such as files which represents devices, have major and minor numbers which represent which drivers are responsible for that class of device, and what specific device is of that class, respectively.

* Describe the mknod command and when you'd use it.

        From the man page, ``` mknod ``` is used to create block or character special files found in /dev.
        These days this command is not used because ``` udev ``` automatically handle the creation and removal of devices in /dev.

* Describe a scenario when you get a "filesystem is full" error, but 'df' shows there is free space.

        One possibility for this error is running out of inodes on a filesystem. This can happen when many tiny files are written to the filesystem that don't take up much space but do each take up an inode.
        Also its possible that a process has opened a large file which has since been deleted. You'll have to kill that process to free up the space. You may be able to identify the process by using  ``` lsof +L 1 ``` command.

* Describe a scenario when deleting a file, but 'df' not showing the space being freed

        If a process currently has a file open, an you delete the file, the space is still considered in use on the filesystem. Killing the process with the file open fixes this.

* Describe how 'ps' works.

        Stands for Process Status. ``` ps ``` reads from /proc to know about all running processes and information about said processes.

* What happens to a child process that dies and has no parent process to wait for it and what's bad about this?

        When a child process dies and has no parent process waiting for it, it is considered a orphaned process, similar to zombie process. Orphaned Processes are sign of resource leakage and will eventually cause the system to slow down.
        It is possible to run out of PIDs which can be assigned if too many orphans or zombies have been made.

* Explain briefly each one of the process states.

        You can find the process states with ``` ps aux ``` command, in the STAT column, you'll see lots of values. A linux process can be in a number of different states. The most common state codes you'll see are described below:
        - R: Running or runnable, it is just waiting for the CPU to process it.
        - S: Interruptible sleep, waiting for an event to complete, such as input from the terminal.
        - D: Uninterruptible sleep, processes that cannot be killed or interrupted with a signal usually to make them go away you have to reboot or fix the issue.
        - T: Stopped, a process that has been suspended/stopped.
        - Z: Zombie, terminated processes that are waiting to have their statuses collected.

* How to know which process listens on a specific port?

        They are different ways of finding the process/service listening on a particular port. Using port 80 as example.
        - ``` ss -tlpn | grep 80 ```
        - ``` netstat -ltnp | grep -w ':80' ``` 
        - ``` lsof -i :80 ``` 


* What is a zombie process and what could be the cause of it?

        A zombie process i s process started by a parent, which has completed running, but the parent process has failed to catch the exit call from the child.
        The cause for a zombie process could be a poorly programmed piece of software, or by sending a ``` kill -9 ``` signal to the parent process. Sending a ``` kill -9 ``` signal kill the process, but does not clean up child processes.

* You run a bash script and you want to see its output on your terminal and save it to a file at the same time. How could you do it?

        ``` ./script.sh | tee output.txt ```

* Explain What echo "1" > /proc/sys/net/ipv4/ip_forward does.

        This will change the settings for ip forwarding at runtime. Since it is putting "1" into this file, we can assume that it is enabling ip forwarding. A better way to do this would be to find the equivalent kernel configuration and put it into ``` /etc/sysctl.conf.

* Describe briefly the steps you need to take in order to create and install a valid certificate for the site https://foo.example.com

        Assuming this is running on a webserver such as NGINX or Apache.
        1. Create a certificate signing request (CSR) for foo.example.com
        2. Present the CSR to valid certificate authority , and generate a new TLS certificate and private key
        3. Put the new issued certificate and private key into the webserver hosting foo.example.com. Make sure you put the files into appropriate directories with appropriate file permissions.
        4. Configure the webserver to use TLS and specify which certificate and key files to use.
        5. Reload the webserver configuration.

* Can you have several HTTPS virtual hosts sharing the same IP?
        
        Yes it can be done with Apache or NGINX.

* What is the wildcard certificate?

        A wildcard certificate is an SSL certificate that can secure any number of subdomains with a single certificate. You may want a wild certificate in cases where you need to support multiple subdomains but don't want to configure them all individually.

* Which Linux file types do you know?

        In Linux technically everything is a file.
        The standard file types are regular files and directories.
        Regular files, Directory, block file, character file, pipe files, symbolic links, socket files.

* What is the difference between a process and a thread? And parent and child processes after a fork system call?

        A process is the program being executed in memory. A thread is a separate instruction set being executed within a process. 
        
        ``` fork() ``` is the system call used to start another process. The process which called ``` fork() ``` is the parent. The child is different, because it can be killed or finish  execution without the parent also being killed or finishing. However, if the parent is killed, then the child is supposed to be reaped as well. Child processes inherit most attributes from the parent process.

* What is the difference between exec and fork?

        The fork() system call is used to create an exact copy of a running process and the crated copy is the child process and the running process is the parent process. Where exec() system call is used to replace a process image with a new process image. 
        So, there is no concept of parent and child processes in exec() system call.

* What is "nohup" used for?

        ``` nohup command arguments ``` stands for no "hangup" is a command that ignores the HUP signal. Usually, when we log out, all the running programs and processes are hangup or stopped.


* What is the difference between these two commands? 
  * ```myvar=hello```
  * ```export myvar=hello```

        Both commands create a variable called myvar local to the shell in which they were created. The difference is that using ``` export ``` makes this variable available to child processes started by that shell.



* How many NTP servers would you configure in your local ntp.conf?

        Having 3 or more servers is ideal as it allows for NTP on a client to smooth out the jitter between NTP servers. Most distributions default to a minimum of 4.

* What does the column 'reach' mean in ```ntpq -p``` output?

        Reach is a base 10 number representing how many successful connections have been made to a particular NTP server.
        Reach is actually tracked by 8 octal bits which are constantly left shifted. Each successful connection left shifts the reach number, and sets the right most bit to 1. Each filed connection does the same left shift, and sets the rightmost bit to 0.
        The sum of the bit values is represented in decimal form, and is a quick overview of how many successful connections of the past 8 connections have been made to an NTP server.

* You need to upgrade kernel at 100-1000 server, how you would do this?

        The easiest way to do this is by running an Ansible playbook with sudo to upgrade the kernel and providing the 1000 server as the inventory.
        On a Debian based system this would be (simplified):
        1. ``` sudo apt update ```
        2. ``` sudo apt dist-upgrade -y ```
        3. ``` sudo reboot ```

        Another approach will be with a simple txt file and a bash script.
        ``` for server in $(cat servers_list.txt) ; do ssh root@${server} 'bash -s' < ./update_kernel.sh ; done ``` 
 
 source: https://devdojo.com/bobbyiliev/executing-bash-script-on-multiple-remote-server


* How can you get Host, Channel, ID, LUN of SCSI disk?

        Assuming the SCSI disk is actually connected then all of this information can be found with ``` cat /proc/scsi/scsi ```

* How can you limit process memory usage?

        ``` ulimit options limit ``` , provides control over the resources available to the shell and processes it creates.

* What is bash quick substitution/caret replace (^x^y)?

        That particular feature is called quick substitution, its documentation can be found in the "Event Designators section of the Bash Manual.
        ``` !!:gs/x/y/ ```

* Do you know of any alternative shells? If so, have you used any?

        I've heard of shells like "fish" and ksh. But I have only used "zsh", with the framework "oh-my-zsh".


* What is a tarpipe (or, how would you go about copying everything, including hardlinks and special files, from one server to another)?

        It's a construct for copying directory trees. In the Linux/Unix shell run two "tar" commands, one creating and the other extracting in different folders like this:
        ``` (cd src && tar -c ) | (cd dst && tar -xp) ```

        In modern systems there are multiples ways to do this, like ``` cp -rp ``` or ``` rsync -a ``` to archive one directory to another.

* How can you tell if the httpd package was already installed?

        ```httpd``` is the name for the Apache web server on RedHat based systems. So ``` yum list installed ``` is a good start.

* How can you list the contents of a package?

        List the contents of a installed package  ```dpkg -L installed_package``` 
        List the contents of a non-installed package ```dpkg -c filename.deb```
        

* How can you determine which package is better: openssh-server-45.3p1-118.1.el6_8.x86_64 or openssh-server-6.6p1-1.el6.x86_64 ?

        These packages are following the RPM naming convention.
        The name of the package is ```openssh-server```. The versions are ```5.3p1-118.1el6_8``` and ```6.6p1-1.el6```. the OS version (RHEL6.8 vs RHEL 6), they both use the ```x86_64``` OS architecture. 
        If we follow the principle of "newer is better" then the second option is "better".

* Can you explain to me the difference between block based, and object based storage?

        Block storage is the oldest and simplest form of data storage. Stores data in fixed sized chunks called "blocks".

        Compared to block storage, object storage is much newer. Objects are stored in a flat address space and there is no limit to the number of objects stored, making it much easier to scale out.



### Hard Linux Questions

* What is a tunnel and how you can bypass a http proxy?

        HTTP tunneling is used to create a network link between two computers  in conditions of restricted network connectivity including firewalls, NATs and ACLs, among other restrictions. The tunnel is created by an intermediary called a proxy server which is usually located in a DMZ.

        You can't bypass a proxy if it is configured correctly. You can get around a proxy, but it requires significant work and a external server. 
        Ways are using ssh-tunneling over https, or a VPN also simulating https connections. 


* What is the difference between IDS and IPS?

        IDS (Intrusion Detection Systems) and IPS (Intrusion Prevention Systems) go hand in hand when it comes to network integrity of organizations.
        The main thing that differentiates IDS from IPS is that IDS is for monitoring networks while IPS is all about control systems.


* What shortcuts do you use on a regular basis?

        TAB is my ultimate friend for autocomplete. Ctrl+C for interrupt and abort. Ctrl+L is the equivalent to clear console. Ctrl+A move the cursor to the beginning of the line. Ctrl+E moves the cursor to the end of the line. Ctrl+R back search. Ctrl+/ undo. Ctrl+W: delete last word of command & close current tab.


* What is the Linux Standard Base?

        The Linux Standard Base (LSB) was a joint project by several Linux distributions under the organizational structure of the Linux foundation to standardize the software system structure, including the Filesystem Hierarchy standard used in the Linux Kernel.


* What is an atomic operation?

        Atomic operations provide instructions which complete oin one instruction cycle. Since atomic instructions complete in one single instruction cycle, they are not interrupted by other CPUs trying to access the same memory location. This prevents race conditions.
        Linux provides two types of atomic operations - 
          - Atomic operations on integer variables
          - atomic operation that operate on individual bits


* Your freshly configured http server is not running after a restart, what can you do?

        Make sure the service ir running. 
        ```sudo systemctl restart apache2``` or ```httpd``` for Redhat environments.
        Check your server configuration.
        ```sudo apache2ctl -t``` or ```httpd -t```
        Check logs
        ```sudo ls /var/log/apache2/``` or ```/httpd/```
        Check other services, databases, firewall, network connections, or file permissions.
        

* What kind of keys are in ~/.ssh/authorized_keys and what it is this file used for?

        This file containers a list of public keys, one-per-line, that are authorized to login into this account.
        This file is used to authenticate using SSH keys. A user must have an SSH key pair on their local computer. On the remote server, the public key must be copied to a file within the user's home directory at ```~/.ssh/authorized_keys```

* I've added my public ssh key into authorized_keys but I'm still getting a password prompt, what can be wrong?

        A couple of things to look around...
        - open configuration tile ```/etc/ssh/ssh_config```
        - look for ```PreferredAuthentications```
        - make sure ```password``` comes after ```publickey``` 
          - ```PublickeyAuthentication``` should be set to YES.
        - make sure to configure the right permissions on ```~/.ssh/``` 

* Did you ever create RPM's, DEB's or solaris pkg's?

        Yes, I have compiled projects which I download from Github. No own project so far

* What does ```:(){ :|:& };:``` do on your system?

        The ```:(){ :|:& };:``` is nothing but a bash function. This function get executed recursively. It is often used by sysadmin to test user process limitations on server. Linux process limits can be configured via ```/etc/security/limits.conf``` and PAM to avoid bash fork() bomb.
        The fork bomb is a form of denial-of-service (DoS) attack against a Linux or Unix-based system. Once a successful fork bomb has been activated in a system it may not be possible to resume normal operation without rebooting the system as the only solution to a fork bomb is to destroy all instances of it.

* How do you catch a Linux signal on a script?

        With a built-in bash command ```trap [action] [signal]``` that is used to execute a command when the shell receives any signal. For example, the most common signal of bash is SIGINT (signal interrupt). 

* Can you catch a SIGKILL?

        You cannot, at least not for the process being killed.

* What's happening when the Linux kernel is starting the OOM killer and how does it choose which process to kill first?

        If memory is exhaustively used up by processes, to the extent which can possibly threaten the stability of the system, then the OOM killer comes into the picture. The OOM killer has to select the best process to kill. Best here refers to a process which will free up the maximum memory upon killing and is also the least important to the system.

* Describe the linux boot process with as much detail as possible, starting from when the system is powered on and ending when you get a prompt.

        The following are the 6 high level stages of a typical Linux boot process:
        1. BIOS: Basic input/output system executes MBR
        2. MBR: Master Boot Record, executes GRUB
        3. GRUB: Grand Unified Bootloader executes Kernel
        4. Kernel: Kernel executes /sbin/init
        5. Init: Init executes runlevel programs
        6. Runlevel: Runlevel programs are executed from /etc/rc.d/rc*.d/

* What's a chroot jail?

        A chroot (short for change root) is a Unix operation that change the apparent root directory to one specified by the user.It allows you to run a program (process) with a root directory other than /. The program cannot see or access files outside the designated directory tree.

* When trying to unmount a directory it says it's busy, how to find out which PID holds the directory?

        Use ``` lsof | grep /media/busymediahere ```to find out what is using the mount.

* What's LD_PRELOAD and when it's used?

        If you set LD_PRELOAD to the path of a shared object, that file will be loaded before any other library (including the C runtime). 

* You ran a binary and nothing happened. How would you debug this?

        There is a set of tools which would be using to debugging the binaries.
        - ```file```: Help to determine the file type.
        - ```ldd```: Print shared object dependencies.
        - ```ltrace```: A library call tracer.
        - ```hexdump```: Display file contents in ASCII, decimal, hexadecimal or octal.
        - ```strings```: print the strings of printable characters in files.

* What are cgroups? can you specify a scenario where you could use them?

        A control group (cgroup)  is a Linux kernel feature that limits, accounts for, and isolates the resource (CPU, memory, disk I/O, network and so on) of a collection of processes. So basically you use cgroups to control how much of a given key resource (CPU, memory, network and disk) can be accessed or used by a process or set of processes.

* How can you remove/delete a file with file-name consisting of only non-printable/non-typeable-characters?

        First ensure that the name is right with: ```ls -ld $'\177```', if it shows the right file, then use rm: ```rm $'\177'```
        Another approach is to use ```rm -i -- *``` . With the -i option requires confirmation before removing a file, so you can skip all files you want to keep.

* How can you increase or decrease the priority of a process in Linux?


        You can change the priority of a running process to a value lower or higher than the base scheduling priority by using the ```nice``` command from the terminal.


### Expert Linux Questions:

* A running process gets ```EAGAIN: Resource temporarily unavailable``` on reading a socket. How can you close this bad socket/file descriptor without killing the process?
* What do you control with swappiness?

        Swappiness is the kernel parameter that defines how much (and how often) your Linux kernel will copy RAM contents to swap. This parameter's default value is "60" and it can take anything from "0" to "100". The higher value of the swappiness parameter, the more aggressively you kernel will swap.

* How do you change TCP stack buffers? How do you calculate it?

        

* What is Huge Tables? Why isn't enabled by default? Why and when use it?
* What is LUKS? How to use it?


### Networking Questions:

* What is localhost and why would ```ping localhost``` fail?
* What is the similarity between "ping" & traceroute" ?  how is traceroute able to find the hops.
* What is the command used to show all open ports and/or socket connections on a machine?
* Is 300.168.0.123 a valid IPv4 address?
* Which IP ranges/subnets are "private" or "non-routable" (RFC 1918)?
* What is a VLAN?
* What is ARP and what is it used for?
* What is the difference between TCP and UDP??
* What is the purpose of a default gateway?
* What is command used to show the routing table on a Linux box?
* A TCP connection on a network can be uniquely defined by 4 things. What are those things?
* When a client running a web browser connects to a web server, what is the source port and what is the destination port of the connection?
* How do you add an IPv6 address to a specific interface?
* You have added an IPv4 and IPv6 address to interface eth0. A ping to the v4 address is working but a ping to the v6 address give you the response ``` sendmdg: operation not permitted ```. What could be wrong?
* What is SNAT and when should it be used?
* Explain how could you ssh login into a Linux system that DROPs all new incoming packets using a SSH tunnel.
* How do you stop a DDoS attack?
* How can you see content of an ip packet?
* What is IPoAC (RFC 1149)?
* What will happen when you bind port 0?


### MySQL Questions:

* How do you create a user?
* How do you provide privileges to a user?
* What is the difference between a "left" and a "right" join?
* Explain briefly the differences between InnoDB and MyISAM.
* Describe briefly the steps you need to follow in order to create a simple master/slave cluster.
* Why should you run "mysql_secure_installation" after installing MySQL?
* How do you check which jobs are running?
* How would you take a backup of MySQL database?



### DevOps Questions:

* Can you decribe your workflow when you create a script?
* What is GIT?
* What is a dynamically/statically linked file?
* What does "./configure && make && make install" do?
* What is puppet/chef/ansible used for?
* What is Nagios/Zenoss?NewRelic used for?
* What is Jenkins/TeamCity/GoCI used for?
* What is the difference between Containers and VMs?
* How do you create a new postgres user?
* What is a virtual IP address? What is a cluster?
* How do you print all strings of printable characters present in a file?
* How do you find shared library dependencies?
* What is Automake and Autoconf?
* ./configure shows an error that libfoobar is missing on you system, how could you fix this, what could be wrong?
* What are the advantages/disadvantages of script vs compiled program?
* What's the relationship between continuous delivery and DevOps?
* What are the important aspects of a system continuous integration and deployment?
* How would you enable network file sharing within AWS that would allow EC2 instances in multiple availability zones to share data?


### Fun Questions:

* A careless sysadmin executes the following command: ``` chmod 444 /bin/chmod ``` - what do you do to fix this?
* I've lost my root password, what can i do?
* I've rebooted a remote server but after 10 minutes I'm still not able to ssh into it, what can be wrong?
* If you were stuck on a desert island with only 5 command-line utilities, which would you choose?
* You come across a random computer and it appears to be a command console for the universe. What is the first thing you type?
* Tell me about a creative way that you've used SSH?
* You have deleted by error a running script, what could you do to restore it?
* What will happen on 19 January 2038?
* How to reboot server when reboot command is not responding?


### Demo Time:

* Unpack test.tar.gz without man pages or google.
* Remove all "*.pyc" files from test dir recursively?
* Search for "my konfu is the best" in all *.py files.
* Replace the occurrence of "my konfu is the best" with "I'm a linux jedi master" in all *.txt files.
* Test if port 443 on a machine with IP address X.X.X.X is reachable.
* Get http://myinternal.webserver.local/test.html via telnet.
* How to send an email without a mail client, just on the command line?
* Write a ``` get_prim ``` method in python/perl/bash/pseudo.
* Find all files which have been accessed within the last 30 days.
* Explain the following command ``` (date ; ps -ef | awk '{print $1}' | sort | uniq | wc -l) >> Activity.log ```
* Write a script to list all the differences between two directories.
* In a log file with contents as ``` <TIME> : [MESSAGE] : [ERROR_NO] - Human readable text ``` display summary/count of specific error numbers that occurred every hour or a specific hour.



source: https://github.com/chassing/linux-sysadmin-interview-questions/blob/master/README.md