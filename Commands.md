# Commands

**Set Environment Variable for DDS**

$  `export NDDSHOME=~/rti/ndds.5.0.1/`

**View Serial Device Attributes**

$  `devcadm info -a -n /dev/ttyUSB0`

**To create a USB Serial Persisten name symlink, create a new rules file i.e.**

$  `sudo vi /etc/udev/rules.d/99-usb-serial.rules`

**View Current Process running**

$  `ps -ef`

**Look for a certain process running, i.e motion***

$  `ps -ef | grep motion*`

**Check for network connection or liveliness of a machine,** 
Use : `ipconfig` to find IP address

*Format*
$ `ping [address]`

*Pinging Youtube*
$ `ping youtube.com`

**List all directory entries including files that start with `.`**

$  `ls -la`

**Check Memory Usage**

$ `cat /proc/meminfo`

$ `less /proc/meminfo`

$ `more /proc/meminfo`

$ `egrep --color 'Mem|Cache|Swap' /proc/meminfo`

**Command History**

$ `CTRL - R`

$ `history`

$ `history | grep XXX`

**Check group user**

$ `getent group groupname`

**Add user to "dialout" group**

$ `sudo adduser second_user dialout`

## Git

**Add changes in the working directory to the staging area**

$  `git add <file>`

$  `git add <directory>`

**Add all changes in the working directory to the staging area**

$  `git add -A`

**Add a submodule**

$ `git submodule add [git clone url] [directory path]`

**Pull latest changes**

$ `git pull`

$ `git pull origin [branch]`

$ `git pull origin master`

**Pull latest changes for all submodules**

*Format*
$ `git submodule foreach git pull [origin alias] [branch]`

*Established branch*
$ `git submodule foreach git pull`

*From master branch*
$ `git submodule foreach git pull origin master`


