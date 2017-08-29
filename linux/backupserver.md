# Backup File Server
One of my more clever concepts was repurposing an old desktop computer to serve as a file server that all of the computers on the local network send their weekly backups to.

All you need is a lot of storage space. Consider the following:
* Number of users
* Content of Backups
* How long to keep backups

After analyzing this, you can see you'll quickly need several TB to safely store backups for an office. Here is how you go about doing it.
## System Requirements
* Any Processor or RAM configuration will do. This isn't a gaming PC, it's a very basic server.
* A UPS would be nice to have, so you don't have to worry about losing power and the server being offline
* Several HDD of several TB worth of space to store all this stuff. It sounds like a lot, but remember, you are storing the data of an office worth of PCs. Don't worry, we can combine disks using Linux's logical volume management, or RAID if you prefer, though I never particularly used RAID.
## Installing Linux
Once you have a suitable old desktop PC, we can begin installing a fresh OS. I typically use the latest LTS of Ubuntu, because why make life harder than it needs to be?
You can choose a server install or a minimal XFCE install, it's up to you if you want a GUI or not. Either way you'll be using less than 300MB of RAM. 
I recommend having the server install security updates for you automatically. This way you will always be protected regardless if you apply updates daily or not.
#### Tasks 
During installation make sure you select the tasks of:
1. SSH Server
2. File Server
3. Standard System Utilities

SSH is important for remote management (which is its own chapter at this point).
After installation is complete make a new user account for each backup person. this will help seperate the backups into their own /home directory.

### Samba
Next we need to edit samba's config file so that all /home is browsable and writable for authorized users. 
Don't forget to restart samba after you make changes!
`sudo service smbd restart`

### SSH
Edit sshd's config file to only allow your authorized keypair to connect. Also specify your user being the only one that can login. This will help keep things secure than just using a password.


__personal reminder: don't forget to git clone and initialize your personal configs for a new server__

