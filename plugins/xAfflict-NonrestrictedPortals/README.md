_____________________________________________________________________________________________________________________________________
**What is it?:**

Nonrestricted Portals is a mod that allows players to take any kind item through portals. The mod removes restrictions placed on portals that would normally force you to drop certain items before entering. Players can also specify the percentage of the amount of items kept when going through portals for each individual item.

_____________________________________________________________________________________________________________________________________
**Why install it?:**

Because Valheim has so many resources that are separated by tons of land, water, and biomes, it makes grinding certain resources a pain. Having to go from one point ﻿to another takes forever and wastes time. The developers fixed this by adding in portals. But then, they blacklisted certain items which forced players to play the walking ﻿simulator again.

If you think being able to take every item across portals is too overpowered or easy, then you can edit the configuration file to only allow, for example, 50% of the original quantity. This can be set for all items, or specific items. Or you can set a base percent for all items and have it be overridden by specified percents for specific items.

_____________________________________________________________________________________________________________________________________
**How do you install it?:**

1) ﻿Go to [BepInExPack Valheim](https://valheim.thunderstore.io/package/denikson/BepInExPack_Valheim/)
2) Download it and follow the installation manual
3) Drag the unzipped Nonrestricted Portals folder into -> <Steam Location>\steamapps\common\Valheim\BepInEx\plugin

The next time you start your game, the mod will be enabled. To disable it, just remove it from the mods folder.

_____________________________________________________________________________________________________________________________________
**How do you use it?:**

By default, the mod will let you take 100% of previously restricted items through a portal. You can set the mod to only allow, for example, 50% of the original quantity of that item. This means that if you take 20 metal ore through the portal, you would only keep 10 of it. You can also set a few outliers. Along with every restricted item being at 50%, you can also set specific items to override that percent. This feature is provided to help balance out the gameplay and give the mod more customization.

The configuration files are located at -> <Steam Location>\steamapps\common\Valheim\BepInEx\plugin\﻿Unrestricted Portals\Config

The General.txt is for the base percentage. This is for every item. The percentage can be overridden by entries in the Items.txt.
The Items.txt is for specific item entries. It will override the base percentage inside of the General.txt.

The percentage must be inclusive of 0 - 100. If it isn't, then the mod won't change anything for the item(s). If the base percent is 50% for all items, but the overridden percent for tin ore is 200%, then the base percent will take priority. If the base percent is 200% for all items, but the overriden percent for tin ore is 50%, then the overriden percent will take ﻿priority.

Make sure you use the correct syntax or it won't work. See below for examples.

Items.txt:
[name = "item_copperore", percentage = "50%"]
[name = "item_tinore", percentage = "50%"]

General.txt:
Restricted Items Kept Percentage: 200%

A list of item names can be found [here](https://pastebin.com/ykQdT8Kr).

_____________________________________________________________________________________________________________________________________