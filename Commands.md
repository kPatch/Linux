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

*For master branch*

$ `git submodule foreach git pull origin master`

** Reconcile detached HEAD with master/origin**

1. Create a branch that points to the commit currently pointed to by your detached HEAD

$ `git branch temp`

$ `git checkout temp`

2. You should compare the current commit with the normal branch on which you expected to be working

$ `git log --graph --decorate --pretty=oneline --abbrev-commit master origin/master temp`

$ `git diff master temp`

$ `git diff origin/master temp`

3. If your new branch `temp` looks good, you may want to update `master` to point to it

$ `git branch -f master temp`

$ `git checkout master`

You can abbreviate these two commmand by typing in:

$ `git checkout -B master temp`

4. You can delete the temporary branch

$ `git branch -d temp`

5. Push the reestablished history

$ `git push origin master`

*You may need to use `--force` *

