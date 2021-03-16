# Trials of Odin: A Difficulty Enhancement Mod

This mod was created to increase the difficulty, add some mechanics, and make Valheim dangerous again!

## Implemented Features:

### Base Features

- Configurable boss scaling that :
  - Takes a value from the config, and uses that to overwrite the default game scaling.
  - Scaling is applied to health, damage, and movement speed.
  - Scaling is also based on number of players. Higher player count around boss spawn = much harder bosses.
  - Optional config to force scaling to set number of players.
- Toggleable boss rage mode that increases boss attack frequency below half health.
- Toggleable increased base enemy difficulty. Enemies have a 95% chance of spawning lvl 1-4, 4% chance of spawning 5-7, and 1% chance of spawning 8-10. Loot is based on those "Tiers" that they fall into. Max loot that can be dropped is that of a 2\* enemy.

### Event System

- Toggleable Event System Overhaul: Events can now be bound to the player so that they only receive events they've "unlocked"

### Iron Man Mode

- Toggleable Iron Man Mode: Once your character dies, you get logged out & that character is deleted forever. Try a true Iron Man Run!
- Toggleable Iron Man Lite: Once your character dies, instead of being deleted, inventory is destroyed & stats are reset to zero. At least you get to keep your base?
- Toggleable World Breaker Mode: **ONLY** for the hardcore. On death, logs you out, deletes your character & your world. **HAS NOT BEEN TESTED IN MULTIPLAYER, WOULD NOT RECOMMEND. TRY AT YOUR OWN RISK.**
- Iron Man Mode must be enabled for Iron Man Lite or World Breaker to function.

## Planned Features

- Allow bosses to spawn their corresponding events during boss fights.
- Increase portal construction cost to add 5 Bronze Bars.
- Anything else **_sadistic_** I can come up with, or that you recommend!

#### Config Format

---

```
[TrialsOfOdin.Base]

## Enable/Disable increased difficulty
# Setting type: Boolean
# Default value: true
IncreaseBaseDifficulty = true

## Difficulty Percentage increase per player (40% default value)
# Setting type: Single
# Default value: 0.4
BaseDifficultyIncreaseFactor = 0.4

## Enable/Disable Speed Increase
# Setting type: Boolean
# Default value: true
IncreaseSpeedWithDifficulty = true

## Difficulty Percentage increase per player (40% default value)
# Setting type: Boolean
# Default value: true
EnableRageMode = true

## Enable/Disable allowing bosses to spawn their associated event during the boss fight.
# Setting type: Boolean
# Default value: false
EnableBossAdds = false

## Force Difficulty Increase (used to force difficulty when in Multiplayer)
# Setting type: Boolean
# Default value: false
ForceDifficulty = false

## Force Number of Players (used to force number of players in Multiplayer)
# Setting type: Int32
# Default value: 1
ForcedPlayerCount = 1

## Enable/Disable Increase all mobs (except bosses) by 1 star.
# Setting type: Boolean
# Default value: true
IncreaseMobDifficulty = true

[TrialsOfOdin.EventSystem]

## Enable/Disable tying events to players.
# Setting type: Boolean
# Default value: true
FixEventSystem = true

[TrialsOfOdin.IronMan]

## Enable/Disable Iron Man Mode: Lose all items & Delete Character on Death (Off by default)
# Setting type: Boolean
# Default value: false
IronMan = false

## Enable/Disable Iron Man Lite Mode: Lose all items, stats reset to 0 on Character Death. Use in conjunction with Iron Man Mode above (Off by default)
# Setting type: Boolean
# Default value: false
IronManLite = false

## Enable/Disable WorldBreaker mode: On death, destroys world as well.
# Setting type: Boolean
# Default value: false
WorldBreaker = false
```

---

### Enjoy the Trials of Odin. He's always watching...

---

## Installation (manual)

If you are installing this manually, do the following

1. Extract the archive into a folder. **Do not extract into the game folder.**
2. Move the contents of `plugins` folder into `<GameDirectory>\BepInEx\plugins`.
3. Run the game.

---

### Changelog:

---

- **V1.3.5**: Changed Game Version checking to check actual version as opposed to string. Tweaked internal difficulty scaling on damage (increased). Fixed health scaling for non-boss enemies. Added same move speed scaling from bosses to regular enemies, as well as added move scaling for flying enemies... Beware the **_Rocketsquito_**. Fixed potential loot drop issues. Fixed bug when enemies died they would change colors. Event system fix still in-progress. Hope to have working with next update.
- **V1.3.4**: Added support for Game Version _0.147.3_.
- **V1.3.3**: Fixed issue where loot was not spawning for some enemies.
- **V1.3.2**: Actually fixed potential compatability issue with V+ this time.
- **V1.3.1**: Fixed potential compatability issues with V+.
- **V1.3.0**: I was an idiot before. Stars will now show up appropriately. 0* for bottom tier, 1* for mid tier, & 2\* for high tier. Enemies will also now have the appropriate coloring for their tier as well. Also slightly adjusted loot so that it won't overspawn loot.
- **V1.2.1**: Fixed error causing stars to show up incorrectly.
- **V1.2.0**: Changed weighted values to be 95/4/1 for low/med/high levels respectively. Added config values for percent chances & level ranges. In multiplayer these should definitely be synced.
- **V1.1.1**: Enemies have a 60% chance of spawning lvl 2-4, 30% chance of spawning 5-7, and 10% chance of spawning 8-10. Loot is based on those "Tiers" that they fall into. Max loot that can be dropped is that of a 2\* enemy.
- **V1.1.0**: New algorithm for setting mob levels. Ranges from 1-10 on a weighted scale.
- **V1.0.6**: Missed one line because I'm an idiot...
- **V1.0.5**: Checks for dedicated server didn't work. Learned about ZDOs. Now saving custom values of Characters (Monsters) to ZDO network object. Should fix issues on multiplayer servers with ultra-high level mobs & over-looting.
- **V1.0.4**: Added checks for dedicated servers.
- **V1.0.3**: Updated Changelog incorrectly. Reflected appropriately now.
- **V1.0.2**: Added checks for whether host or not on a lot of things. Also WorldBreaker now checks if total players is 1 and if it is enabled it will delete the world. **STILL DO NOT RECOMMEND USING ON SERVER**.
- **V1.0.1**: Updated icon
- **V1.0.0**: Initial Release
