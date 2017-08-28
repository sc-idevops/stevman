#Backup File Server
-----
One of my more clever concepts was repurposing an old desktop computer to serve as a file server that all of the computers on the local network send their weekly backups to.
All you need is a lot of storage space, consider the following:
* Number of users
* Content of Backups
* How long to keep backups
After analyzing this you can see you'll quickly need several TB to safely store backups for an office. Here is how you go about doing it.
###System Requirements
* Any Processor or RAM configuration will do. This isn't a gaming PC, it's a very basic server.
* A UPS would be nice to have so you don't have to worry about losing power and the server being offline
* Several HDD of several TB worth of space to store all this stuff. It sounds like a lot but remember you are storing the data of an office's worth of PCs. Don't worry, we can combine disks using Linux's logical volume management, or RAID if you prefer though I never particularly used RAID.
##Installing Linux
-----
Once you have a suitable old desktop PC we can begin installing a fresh OS. I typically use the latest LTS of Ubuntu because why make life harder than it needs to be?
You can choose a server install or a minimal XFCE install, its up to you if you want a GUI or not. Either way you'll be using less than 300MB of RAM. 

During installation make sure you select the tasks of:
1. SSH Server
2. File Server
3. Standard System Utilities

SSH is important for remote management (which is its own chapter at this point)

