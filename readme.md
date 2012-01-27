#Node-Info
Stuff we're figuring out as we explore node.js.

##Hosting

###Hosting on Windows Server 2k8 R2 w/o IIS
This is the easy way to get a website built on node.js up and running on a Windows machine.  To use IIS, see the instructions below (tbd) (to save your sanity, make sure the IIS role is turned off on the server).

Basically, since node.js on Windows runs as a single .exe, you just need to create a service that will host the .exe and run your site.

This isn't as easy as it should be using built-in Windows tools, which is why we use [NSSM - the Non-Sucking Service Manager](http://nssm.cc/).

Steps:

1. Install NSSM.
2. Crank up the NSSM Gui
3. Choose the node .exe
4. For the command-line argument put the path to your node.js app (server.js)
5. Give it a name (this will show up in the Services Manager)
6. Click Ok

(This can also be done via the command line if you wish to script it)

That's it.  You now have a service installed  in the services manager for your app.  Go to the Services MMC console and start the service.  Your node app will now run in the background, restart if it stops for some reason, and start automatically if the system reboots itself.

### Hosting using IIS



##Databases

###Mongo using the mongo driver

###Mongo using the Mongoose ODM 