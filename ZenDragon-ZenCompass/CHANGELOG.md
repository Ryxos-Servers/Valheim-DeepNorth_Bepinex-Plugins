v1.8.0
- update for Valheim (Deep North)
- recompile for Zen.ModLib v1.14.0

v1.7.1
- added a config option to enable/disable malfunction for each nav tool separately.
- minor optimizations.

v1.7.0
- reworking the Sunstone to make it more intuitive for new players.
  - it tracks the sun position, not time of day.
  - it shows the sun position in bad weather, but not at night.
  - you can use the position of the sun to figure out your heading.
  - however, without time tracking you will have to figure out an alternative way of knowing if it is sunrise or sunset. (movement?)
  - crafted requirements changed to just a single Ruby with Stonecutter instead of Forge.
  - This essentially moves the Sunstone into a Swamp biome discovery since you need iron to make a Stonecutter. 
  - Therefore, you can track the Sun position even when you have no shadows and can not see the sun in the swamp.
- The Compass still tracks time of day and is unchanged.
- removed the "up is noon" config, it's just confusing legacy and extra complexity for not much utility.
- internal improvements to how malfunction is handled.
- had to reorganize configs because they were getting a bit too complicated:
  - The "General" section was split into "Appearance" and "Behavior" sections.  Update your configs as needed.
- these are just the new defaults, prior behaviors can be restored via configs.

v1.6.2
- revert default behavior for sunstone back to how it was before v1.6.1, show time of day instead of sun position via the sun ring. config option to show sun position instead if desired.
- reworked configs to use enum flags instead of bools for all compass/sunstone params, if you changed them from defaults then you will need to redo your configs.
- added configs to control time tracking rotation of sun position on the ring.
- added configs to control wind and time of day tracking per nav tool.

v1.6.1
- changed the behavior of Sunstone to reflect the sun position more accurately:
  - it now tracks the sun position instead of time of day, so it's a better tool for navigation.
  - additionally, it does not show the sun position in the dark. It's a SUN stone after all.
- updated Compendium with relevant entries.

v1.6.0
- adjust compass sun tracking to orientation reflect the sun position correctly across the southern sky. noon is now down instead of up.
- recompile for Zen.ModLib v1.10.12

v1.5.1
- Change config defaults for crafting the Sunstone and Compass.
- recompile for Zen.ModLib v1.10.7

v1.5.0
- add help info to Compendium
- recompile for Zen.ModLib v1.10.0

v1.4.12
- recompile for Zen.ModLib v1.9.5

v1.4.11
- IMPORTANT FIX: When Player Death mode was set to Keep or Destroy it was incorrectly targeting the item list inverted: all items in the inventory EXCEPT the compass.  It now correctly targets only the compass as was intended.
- recompile for Zen.ModLib v1.9.1

v1.4.10
- minor optimization and code cleanup: use transpiler instead of matching the GiveBoost function inside UpdateDespawn when automatically removing death pins. More logical for the intent of what is happening and prevents accidental side effects if some other area of code or a mod calls GiveBoost() later.
- no functional changes.

v1.4.9
- fix: does not malfunction for admin in god mode.

v1.4.8
- add config: track wind indicator.  can now toggle it off if desired.

v1.4.7
- adjust internal calculations to detect the current attached ship or mount. needed for ZenMap v1.1.0 feature to track mounts.

v1.4.6
- add Portuguese (Brazilian) translations

v1.4.5
- add config options for toggling the heading gear-arrow visibility.
- sunstone heading arrow now defaults to off

v1.4.4
- add config options for disabling the craftable Compass item and/or Sunstone item.

v1.4.3
- reduce the size of the Sunstone drop item so that it's not so huge.

v1.4.2
- minor adjustment to default recipes for Sunstone and Compass, no functional changes. (Check your configs if you want to use the new defaults)

v1.4.1
- add craftable item: Sunstone.  This is a primitive navigation tool, use it to navigate via sun position and wind direction.  It is imprecise but better than nothing.  Available to craft in the early game, before the compass.
- Crafting configs updated, check your configs.

v1.4.0
- identical to v1.4.1, just added screenshots to v1.4.1 readme.

v1.3.2
- bugfix: would not always detect if the compass was equipped if you had more than one compass in your inventory.

v1.3.1
- added an option for hiding the north/south needle. when used in conjunction with the rotating compass option; a deeper state of immersion is possible where you have to use the time of day, sun position, and wind direction to figure out your orientation.

v1.3.0
- identical to v1.3.1, just forgot to update the README.

v1.2.5
- add German language
- add Russian language

v1.2.4
- fix: when shifting into a dark environment, such as thunderstorm, the icon ring was not shifting into dark mode correctly.
- Recompiled for Valheim v0.221.4, Call to Arms

v1.2.3
- Add a config option to disable the auto shrink when radar is empty.

v1.2.2
- fix: prevent ship power rudder/sails indicator icon from displaying over the map.

v1.2.1
- add config: Display Scale

v1.2.0
- updated for Zen.ModLib v1.2.0
- recompile for BepInEx v5.4.2332
- recompile for JVL v2.26.0

v1.1.11
- change the compass item icon
- update to use Zen.ModLib v1.1.20

v1.1.10
- add a translation file

v1.1.9
- added clarifying instructions to config option for disabling compass biome/weather malfunction conditions.

v1.1.8
- add support for dark mode when in environments which are always dark, even if it's daytime.
- enable dark mode when in a dungeon if you have the compass configured to operate underground. (not recommended for immersion, but up to you)
- sun no longer appears on compass if you are in a dungeon and you have enabled indoor compass use.
- minor performance tweak.

v1.1.7
- update readme, no code changes.

v1.1.6
- Update config defaults for a more challenging early-game so that the first portion of the game can be experienced without a compass.
  - IronNails:1 added to crafting materials requirement
  - Workbench level 5 requirement which means obsidian is required from the mountains.
- These changes have no effect on existing config files. They are just new defaults.
- If you would like easier requirements: Remove the IronNails and lower the workbench level.

v1.1.5
- Update for Zen.ModLib v1.1.0

v1.1.4
- fix: hide the wind indicator when malfunctioning.

v1.1.3
- fix: sync compass item crafting reqs.

v1.1.2
- fixed config sync
- fixed bug: was not turning camera in nomap mode to look at the boss location when interacting with vegvisir.
- fixed bug: compass should not show when in dungeon if config set.

v1.1.1
- removed BepInEx from dependency, Zen.ModLib handles it.

v1.1.0
- Refactored to use shared lib Zen.ModLib
- Add new config option: MalfunctionConditions to specify biome:weather to cause the compass to malfunction.  Defaults: Mistlands:All, All:SnowStorm, Ocean:ThunderStorm
- Add new config option: MalfunctionTransitionDelay - specify how long must pass for the malfunction condition to be met/unmet before malfunction state changes.
- Removed config option: MalfunctionMistlands, MalfunctionSnowstorm
- Fix: Prevent in world shouts from being seen beyond the default nomap range if in nomap mode.

v1.0.22
- prevent stamina and eitr bars from being in the wrong location.

v1.0.21
- add compatibility for mods that create extra utility slots in the player inventory so that the compass item can detect when it is equipped in a modded utility slot.

v1.0.20
- fix: radar not displaying

v1.0.19
- update logging and configs subsystem

v1.0.18
- cleanup logs

v1.0.17
- UPDATE FOR VALHEIM v0.220.3

v1.0.16
- compatibility fix for MinimalStatusEffects by Randy Knapp, or any other mod that repositions ship hud elements.

v1.0.15
- changed log level of death pin removal so that the Vanilla nullref error that happens after looting a tombstone doesn't look like it's being caused by this mod.  because it isn't. it's a vanilla issue but having my log entry show up just before the red text can lead to confusion. 

v1.0.14
- automatic remove death pin when looting tombstone.
- config file section headers changed.  you will need to re-apply any custom config settings after applying this update.

v1.0.13
- fixed UI scaling issue.

v1.0.12
- Bugfix: would not allow editing configs when connecting to vanilla servers.

v1.0.11 
- Update README, no code changes.

v1.0.10 
- Initial release
