# cloud-engineering

## Installation
* Download virtual box, install and set up
* Download and install vagrant in vagrantup.com
* Install boxes - on vagrant site go tofind boxes and search for focal64(ubuntu/focal64)
* Create folder for vagrant e.g user/user/vagrant/boxes/ubuntu20.04-LTS
* open terminal and cd to the above created directory
* Go back to vagrant site and see how to install boxes under "simple and powerful" command line
* $vagrant init ubuntu/focal64
* $nano Vagrantfile - edit the file to set up type: "dhcp" for network ip address
* $vagrant up - to start the machine
* $vagrant ssh - to login
* $ifconfig - to check the ip address  

## Linux Command
(~) is home directory
(/) is root of file system for linux operating system
* man man
* man <option>
* uname -a - type of system/linux version
* date - system date and time
* uptime - how long the system has been up
* whoami - who is the login user
* export varname=value - set variable
* echo $varname - displace the variable value
* ps - view running process
* top - get detailed info about running process
* df -h - tell you about your storage
* press ctr q or type exit - to exit running process
* pwd - print working directory
* cd <DIR> - change directory
* cd - takes you back to user home directory from anywhere you are - same as cd ~
* cd ~ - to switch to user home directory.
* cd / - takes you to the root directory of file system.
* ls | ls -a | ls -l | ls -h | ls -al | ls -alh - list
* ls -a - for all files including hiden files.
* ls -l - for files with directories and permisions.
* ls -h - display the files and folder i uman redable format.
* mkdir <DIR> - make directory
* mkdir -p Test/test_child -  the -p is used to make parent directory and you can make grand parents with it too.
* touch filename - create a file
* cp file1 file2 - copy file from 1 to 2
* cp -r dirname dirname2 - to copy a directory
* mv file1 fil2 - cut and past from file 1 to 2 or rename file 1 to 2
* mv dirname dirname2 - move dirname to dirname 2 or rename the directory.
* rm filename - delete the file
* rmdir directory_name - remove empty directory.
* rmdir -p Test/test_child - remove a parent directory or a non empty directory.
* rm -rf dirname - to remove a directory also.
* file filename - give information about a file.
* cat filename - display the content of file
* head filename - display first 10 content of the file
* tail filename - display the last 10 content of the file
* man commandname - full documentation on how to use the command
* commandname --h - quick help on how to use the command
* command --help - quick help on how to use the command
* head filename - output the first 10 lines of the file
* head -5 filename - output the first 5 lines of the file
* tail filename - output the last 10 lines of the file
* tail -5 filename - output the last 5 lines of the file
* cat filename - display the file content
* cat filename | grep Omobayode - display only the lines that has Omobayode in it
* cat filename filename2 - display the files content at once
* cat filename filename2 > filename3 - concatenate the two files content into filename3 and if filename3 doesnot exit it will create it.
* cat > filename - let you create a file and write the content into it at once. Press "ctr d" to save the content when you are done.
* cat file.txt > file2.txt - copy the content of file to file2.
* echo content > filename -  write the content into the filename and if the file doesnot exit create it.
* echo $HOME - shows you the user home directory
* more filename - to see the content of the file page by page, use spacebar to move to the next page and q to quit.
* less filename - to see the content of the file page by page with higher overview, use spacebar to move to the next page and q to quit.

## Change Time Zone
* timedatectl system current time status
* timedatectl list-timezone - list all the available time zone on the system
* sudo timedatectl set-timezone Africa/Lagos - set the time zone to lagos time zone

## Editing Files
* Using Vim  
$vim text.txt - use vim to open text.txt and it enters the command mode.
Press i - for insert mode when you are done editing press esc to go back to command mode and use :wq to write out your changes and quit. :w - write out, :q - quit, :q!, force quit without asking to save the changes made to the file.
* Using nano  
The comman to write out and quit(exit) is bellow the text editor when opened.
$nano text.txt

## Networking
* ifconfig - configure a network interface
* ip - show/manipulate routing, network devices, interfaces and tunnels
* ip a - pull up all ip informations
  
## apt
* sudo - super user do (execute a command as another user) 
* sudeo su - to switch to the root user
* apt - advanced package management tool(facilitate the process of installing and uninstalling linux software packages.)
* sudo apt update - Update the Package Index
* sudo apt list --upgradable - to see the list of ungradable packages
* sudo apt upgrade - Upgrade Packages
* sudo apt search packageName - search for a package
* sudo apt install <packageName> - Install a Package
* sudo apt remove <packageName> - Remove a Package
* apt help - To get help on apt
* $ sudo add-apt-repository <repo directory> - install app using package repository
* apt install apache2 - Install apache
* curl localhost - To see the server in the terminal  
Apache web service is the sutware that respon and sed the website file to our browser.
  
Configuration of the Advanced Packaging Tool (APT) system repositories is stored in the /etc/apt/sources.list file and the /etc/apt/sources.list.d directory.  
A makefile contains instructions for how an application should be compiled.

## Groups & Users  
Everything in linux is represented as file.  
-rw-r--r-- 1 root root 1031 Nov 18 09:22 /etc/passwd  
The first dash (-) indicates the type of file (d for directory, s for special file, and - for a regular file).
* cat /etc/passwd - To get users and their groups (username : password : user ID : Group ID : homeDIR : shellUsed)
* useradd <username> - To create user
* useradd -m <username> - To create user with home directory
* useradd -g <primarygroupname> <username> - to create user with primary group name.
* userdel username - to delete a user.
* groups <username> - To get the usergroup. (Output - username: usergroupName)
* id -gn <username> - To get the groupname of the user
* id <username> - To get the user and group id with the groupname
* usermod -g <groupname> <username> - make the group user primary group.
* usermod -G <groupname> <username> - Add user to another group (to a new supplementary group)
* usermod -G <groupname1>,<groupname2> <username> - Add user to multiple groups  
  
MANAGING GROUPS  
  Groups are stored in /etc/group - cat /etc/group (output - groupName : password : group ID : Users)
  * groupadd groupname - to create a group
  * groupmod -n grouprename groupname - to rename thr groupname where -n stands for new-name
  * members groupname - list users in a group
  * groupdel groupname - to delete a group
  
  ## File Permission  
  Linux has two authorization levels Ownership and Permission. 
  
  USER TYPES
  Flile owners: Three user types
  1. owner (u) -The user who created the file is the owner of the file.  
  2. Group (g)- all user in the group have the same file permision  
  3. other (o) - other users who has access to the file(everybody else)  
  4. all users (a)
  
  PERMISSIONS
  Linux uses file permission to distinquish these three users.  
  Every file directory has three permissions.  
  * Read - 4
  * Write - 2
  * Execute - 1
  * no permission - 0  
  
  
  
  ACTIONS  
  we can perform these three actions on the permisions
  * remove -
  * add +
  * replace =
  
  TO SET FILE PERMISSIONS
  * chown - choose owner(to assign file to user)
  * chmod - CHange MODe (changes the permissions (attributes) of a file or directory)
  * chmod 750 dirname/filename - user(owner) - full permisions(7), group -read and execute permissions(5), others - no permissions(0).
  * chmod o-w filename - remove write permision for other users
  * chmod a+rw - give read and write permission to all users
  * chmod g+x - give add execute permision to g users
  * chmod a=x - replace permission for all user with only execute permission.
  * chmod a= filename or chmod 000 filename - replace/give permissions for all users to no permissions.
  * chmod a=rwx filename or chmod 777 filename - replace/give full permissions to all users.
  * chmod u+x,g=rw,o-w filename - add execute permissions to user(owner), replace groupuser permissions with read and write, remove write permission from other users.
  
## SystemD
* systemctl or systemctl list-units- list of all applications(units)
* systemctl --failed - List failed units
* systemctl status apache2 - xcheck application(apache2) status 
* systemctl stop apache2 - stop application(apache2)
* journalctl -u apache2 - See application(apache2) log info
* systemctl reboot <application>
* systemctl poweroff <application>
* systemctl suspend <application>
* systemctl hibernate <application>  
system log info are stores in /var/log. /var/log/journal is the journal log info directory
  
  
