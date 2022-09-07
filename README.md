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
* ls | ls -al | ls -l - list
* mkdir <DIR> - make directory
* touch filename - create a file
* cp file1 file2 copy file from 1 to 2
* mv file1 fil2 - cut and past from file 1 to 2 or rename file 1 to 2
* rm filename - delete the file
* cat filename - display the content of file
* head filename - display first 10 content of the file
* tail filename - display the last 10 content of the file
* man commandname - full documentation on how to use the command
* commandname --h - quick help on how to use the command
* command --help - quick help on how to use the command

## Change Time Zone
* timedatectl system current time status
* timedatectl list-timezone - list all the available time zone on the system
* sudo timedatectl set-timezone Africa/Lagos - set the time zone to lagos time zone

## Editing Files
* Using Vim  
$vim text.txt - use vim to open text.txt  
Press i - for insert mode when you are done editing press esc and use :wq to write and quit
* Using nano
$nano text.txt

## Groups & Users  
-rw-r--r-- 1 root root 1031 Nov 18 09:22 /etc/passwd  
The first dash (-) indicates the type of file (d for directory, s for special file, and - for a regular file).
* cat /etc/passwd - To get users and their groups 
* useradd <username> - To create user
* useradd -m <username> - To create userwith home directory
* useradd -g <primarygroupname> <username> - Add primary group name to user
* groups <username> - To get the group name
* id -gn <username> - To get the group name
* id <username> - To get the useer and group id with the group name
* usermod -G <groupname> <username> - Add user to another group
* usermod -G <groupname1>,<groupname2> <username> - Add user to multiple groups


## apt
* sudo apt install <packageName> - Install a Package
* sudo apt remove <packageName> - Remove a Package
* sudo apt update - Update the Package Index
* sudo apt upgrade - Upgrade Packages
* apt help - To get help on apt
* $ sudo add-apt-repository <repo directory> - install app using package repo
* apt install apache2 - Install apache
* curl localhost - To see the server in the terminal  
  Apache web service is the sutware that respon and sed the website file to our browser.
  
Configuration of the Advanced Packaging Tool (APT) system repositories is stored in the /etc/apt/sources.list file and the /etc/apt/sources.list.d directory.  
A makefile contains instructions for how an application should be compiled.
