# Description
Normally, the game limits all network transmissions to 50kbps.

This is bad for a multitude of reasons. Imagine a scenario where 5 players are uploading at the max rate, 50kbps.

The server will only be able to send all 5 players updates at 50kbps. It is receiving 250 but cannot reciprocate that.

This mod will modify the data rate that the game uses for network actions. This allows you to use your network to the best potential.

It is best to have all clients and the server running the mod.

However, it is still beneficial to only run this only on the server. 
It may even be beneficial to only run it on your client but this is untested by myself. There is no harm in doing so however.

# Configuration
There is a configuration file for this mod. You can change the multiplier that is used.

The configuration file is generated after you run the game once after installation.

The default is 10. This means the default rate * 10, which is ~500kbps. This is more than enough for most scenarios.

If you are running a server with many players and install this there, you may wish to increase the multiplier to 20 or 30 to allow the server room to sync all the players information.

# Installation
* Ensure BepInEx is installed
* Download this mod and put it into the BepInEx/plugins folder

That's it! This fixed all of my group's problems and many others have let me know that it's a game changer.

Enjoy the game!