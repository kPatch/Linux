# Commands

Set Environment Variable for DDS
`export NDDSHOME=~/rti/ndds.5.0.1/`

View Serial Device Attributes
`devcadm info -a -n /dev/ttyUSB0`

To create a USB Serial Persisten name symlink, create a new rules file i.e.
`sudo vi /etc/udev/rules.d/99-usb-serial.rules`

View Current Process running
`ps -ef

Look for a certain process running, i.e motion*
`ps -ef | grep motion*`

Check for network connection or liveliness of a machine, use : `ipconfig` to find IP address
`ping youtube.com`

List all directory entries including files that start with .
`ls -la`

## Git

Add changes in the working directory to the staging area
`git add <file>`
`git add <directory>`

Add all changes in the working directory to the staging area
`git add -A`

