# Linux
Repository contains info about Linux systems


Distros Linux

Ubuntu: https://ubuntu.com/download/desktop
Mint: https://linuxmint.com/download.php
Arch Linux: https://www.archlinux.org/download/
RedHat: https://www.redhat.com/en
CentOS: https://www.centos.org/
Fedora: https://getfedora.org/
Suse: https://www.suse.com/

=====================================================================

Linux Kernel: Is an interface between hardware and software
Shell: Its like a container, interface between users and Kernel/OS, CLI is a Shell
NIC (Network Interface Card)
=====================================================================

Commands Linux

whoami: to see the current user

pwd: name of your current directory

cd: change directory, example: cd name_directory, to go back cd ..

/: directory root

ls: list all content of current directory
ls -ltr: list all content in order

clear: clean the screen

mkdir: create a new directory/folder, example: mkdir name_folder
mkdir -p: create a folder structure, example: mkdir -p folder1/folder2/folder3
rmdir: remove a directory

echo: write a message on screen, example: echo Hello World! > hello_world.txt

cat: command to read an file, example: cat name_filel

cp: create or copy a file to a specific folder
cp -r: copy all content to a specific folder, example: cp -r origin_folder destiny_folder

mv: rename or move a file, example rename: mv file1.txt file2.txt, example mv: file.txt ../folder2/. 

ren: rename a directory

rm: delete a file or directory, example rm file.txt; example rm -rf name_folder

touch: create a file empty, example: touch name_file

man: manual, example: man touch, man clear

> : directed this instruction for a exit, example pwd > file.txt
>> : add this instruction for a file, example Hello World >> file.txt

ifconfig: to see ip machine

passwd: change password user, ex: passwd userid

find or locate: main commands used to find files/directorie, example find . -name "george.txt"

wildcards: Is a character that can be used as a substitute for any of a class of characters in a search
s:
* - represents zero or more characters
? - represents a single character
[] - represents a range of characters
\ - as an escape character
^ - the beginning of the line
$ - the end of the line
example: abc{1..9}-xyz

pipes: Is used by the sheel to connect the ooutput of one command directly to the input of another command. 
Example: 
ls -ltr | more 
ll | more
ls -ltr | tail -1 

&: execute a program in background: example firefox &
top: view all process running
kill -9: finish a process, example: kill -9 name_process
sudo su: change terminal for root user
apt-get install: install a program, example: sudo apt-get install name_program

sudo shutdown -r now: restart the computer
sudo shutdown -h now: turn off the computer
exit: exit terminal

Help commands:
whatis name_command
name_command --help
man name_command

cat: command to read a content a specific file
more: command to see one page at a time, example more name_file
less: command to see one page at a time and navigate using page up or page down
head: command to see the head of file, example: head name_file or head -2 name-file
tail: command to see the tail fo file, example: tail name_file or tail -100 name_file

date: command to see the date of system operational system

cut: show the first or more characters in a file, example: cut -c1 name_file, cut -c1-3 name_file
awk: separate each column in a file, example: awk '{print $1}' name_file
grep: search a text in a file, example: grep Hello name_file
sort: show the file sorted, example: sort name_file, or sort -r name_file
uniq: remove all duplicates in a file, example: uniq name_file
wc: count lines in a file, example: wc name_file

diff: compare two files line by line
cmd: compare two files byte by byte

tar:
- command to zip a file: tar cvf name_file.tar name_directory_to_zip
- command to unzip a file: tar xvf name_file.tar   

gzip (gzip -d or gunzip): 
- command to compress a file: gzip name_fie_to_compress
- command to uncompress a file: gzip -d name_file_to_uncompress

hostnamectl: command to change the name of hostname, example: hostnamectl - set-hostname name_new_hostname

alias: examnple: alias ls="ls -al"

history: show all commands executed

ethtool enp0s3

yum: command to install/update/upgrade/remove packages and updates

ftp: example ftp ftp.redhat.com

tracerout: command to used to map the journey, example traceroute www.google.com
netstat -rnv
=================================================================

User Account Management

Commands:

useradd: to create a new user, example: useradd name_user, to check if user was created use: id name_ser
useradd -g superheroes -s /bin/bash -c "user description"-m -m /home/ironman ironman
  
groupadd: to create a new group, example: groupadd name_group, to check if a group was created use: cat /etc/group
userdel: to delete a user, example: userdel -r name_user
groupdel: to delete a group, example: groupdel name_group
usermod: to modify a user account, example: usermod -G name_group name_user
chgrp: to modify the group, example: chgrp -R name_group name_user

Files
/etc/passwd
/etc/group
/etc/shadow

==================================================================

Switch users and sudo access

Commands:
su - username
sudo command
visudo

File
/etc/sudoers

=================================================================

Monitor Users
who:  How many people are they and user id their terminal ID

last: Last command tells you all the details of every uses that have been logged in from since the day one
last | awk '{print $1}' | sort | uniq
w
finger
id

==================================================================

Linux File Editor

- vi: Visual Editor
- ed: Standard line Editor
- ex: Extended line Editor
- emacs: A full screen editor 
- pico: Beginner's editor
- vim: Advance version of vi
 
Commands vi:
i: insert
Esc: Escape out of any mode
r: replace
d: delete
:q! : quit without saving
:wq : quit and save

==================================================================

System Utility Commands

date: show the date 
uptime: tell you how long been the system up for and how many user have been logged
hostname: show the hostname
uname: give you more detail about the linux, example: uname -a
which: tell you location of the command, example: which pwd
cal: show the calendar, example: cal 11 1981 or cal 1981
bc: basic program calculator 

===================================================================

File Syste Structured Description

/bin: Linux commands
/boot: Contains files that aren't used by the operating system, but by its bootloader
/etc: Additional programs and data files
/lib: C programming library directory
/mnt: Mount directory, usually reserved for mounting filesystems
/opt: Optional add-on applications
/root: Root home directory. It is not same as /
/sbin: System binaries
/proc: Running process
/tmp: Temporary directory
/home: User directories
/var: Directory for system logs
/dev: Contains references to all the preripheral hardware
/media: cdrom
/run: Directory is the companion directoruy to /var/run 

==================================================================

File System Paths

Absolute path: Always begin with a "/", this indicates that the path starts at the root directory. Ex.: cd /var/lo/samba
Relative path: Not begin with a "/". It identifies a location relative to your current position. Ex.: cd /var  cd log cd samba:

===================================================================

Permission on files:

There are 3 types of permissions: read (r), write (w), execute running a program (x)
Each permission can be controlled at three levels: u (user), g (group) and o (other)
421     421     421
rwx     rwx     rwx

chmod 777 name_file: insert all permissions in this file 
chmod g-w jerry: remove write to file "jerry" for the  group 
chmod a-r jerry: remove read to file "jerry" for the all (use, group and others)
chdmod u+r jerry: add read to file "jerry" for the user: 
chmod +x: permission to execute script owner   group   all
chmod +x: permission to execute script
chmod -R 777 *: using recursive

chown bruno name_file: change owner file
chgrp root name_file: change group file

=================================================================

Processes and Jobs

Application = Service: Word, Gimp, Apache Server
Script: Shell scripts or Commands are list of instructions
Process: Is a process ID associated with an application
Daemon: Is could tell you when I compare it with the process as something that continuously runs in the background or doens't stops.
Threads: A process starts a thread
Job: Is a scheduler

systemclt or service: command used to start/stop an application, or to see the status, example: systemctl start/stop/restart/status ntpd
ps: Allow you to see what are the process running in your Linux System, example: ps -ef | grep ntpd
top: command to see all process running, you'll see first based on its load
kill: command to kil the process using your PID
crontab: command to schedule applications or process

=================================================================

System Monitoring

top: show the process are running
df: show information about your disk partition, example: df -h
dmesg: give you the output of the system related warning error messages failures or anything  
iostat: give you information aboout communicating with our system peripheral devices or system internal devices ssassas
netstat: give you information about your gateway and subnet
free: give you your physical memory and your swap space
cat /proc/cpuinfo
cat /proc/meminfo

================================================================

System Maintenance Commands

shutdown: command to power-off or reboot the  machine
init 0-6
reboot
halt

=================================================================

Virtual-Box

Host-only Adapter = Allows communication between your PC and the Virtual Machine
Bridged Adapter = Allow communication between your PC and VM plus allos communication to the internet

==================================================================
