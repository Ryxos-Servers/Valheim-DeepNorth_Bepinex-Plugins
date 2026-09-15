v1.3.0
- update for Valheim (Deep North)
- recompile for Zen.ModLib v1.14.0

v1.2.0
- add config: show hover icons on static stacks and piles and treasure chest.
- moved config to show valuables hotkey from Containers section to General section, update your configs if you changed the default.

v1.1.1
- add config: when you hold left alt it will display the total for all valuables in the container or treasure piles & chests.
- recompile for Zen.ModLib v1.11.14

v1.1.0
- identical to v1.1.1, just forgot to update the readme.

v1.0.1
- recompile for Zen.ModLib v1.9.5

v1.0.0
- add a question mark icon for containers that are not player crafted instead of displaying nothing.
- recompiled for Zen.ModLib v1.9.3 

v0.6.3
- update translations strings.

v0.6.2
- recompile for binary compatibility with Zen.ModLib v1.8.1

v0.6.1
- internal optimizations.
- interface updated for Zen.ModLib v1.7.1 interop messages.

v0.6.0
- add listeners for Zen.ModLib v1.7.0 interop messages

v0.5.4
- fix: plant hover text color coded based on status ailments. hot, cold, wrong biome, etc.

v0.5.3
- fix: when a feast was empty it would display -1/10, now it displays nothing.

v0.5.2
- added additional logging for the v0.5.1 patch and streamlined error handling in that edge case.  no major functionality changes.

v0.5.1
- compatibilty: OdinsKingdom was not including icon data for the fuel item on its fireplaces. This patch prevents the icon from being displayed when the data is missing.

v0.5.0
- update for Zen.ModLib v1.5.0

v0.4.13
- fix: Oven was showing the hover icon even when fuel remaining was 0

v0.4.12
- recompiled for changes to Zen.ModLib v1.3.6

v0.4.11
- minor cosmetic fix: when displaying the sums of items in containers, if there is only one of the items in the container do not display "1" it is redundant because the icon itself indicates at least one. Two or more of the same items are required for the number to display, otherwise just show the icons without a number under it.

0.4.10
- use v0.4.11 instead.

v0.4.9
- improved logic for PetRock so that it displays the rock icon too, not just the item on its head.

v0.4.8
- add Feasts and PetRock support for icons

v0.4.7
- simplify messaging, no longer display a distinction between "No empty slots" and "It's full."  Instead, just show "It's full" when there are no empty slots and every slot is 100% full stack.  The subtle nuance was not worth the added complexity, verbiage, and potential for confusion.

v0.4.6
- change config default: Show "Hold to stack" to true, was set to false by accident in the prior version.

v0.4.5
- add a config option to disable the summary text on containers
- add a config option to disable the queue text on smelters
- add Polish translation

v0.4.4
- added Translation strings for localization
  - add German
  - add Russian

v0.4.3
- added an option to reformat the Hover Text on plants/crops to make them look nicer.
- recompiled for Valheim v0.221.4, Call to Arms

v0.4.2
- update: Beehive Honey icons now show individual honey icons for each unit of honey in the beehive instead of n/m.
- update: Sap Collectors get a meter.

v0.4.1
- add compatibility for StationsAreContainers
- updated for Zen.ModLib v1.2.5

v0.4.0
- updated for Zen.ModLib v1.2.0
- recompile for BepInEx v5.4.2332
- recompile for JVL v2.26.0

v0.3.0
- new config option to toggle the display of capacity info on fireplaces and smelters.
- changed fuel section config option names to better reflect meaning and intent. If you had changed your configs from the defaults in this section, please check them after this update to make sure they are set how you would like.

v0.2.19
- fix: change the behavior when Fuel config option AdjustFuelBurnRate config option is false so that it is compatible with other mods that adjust the burn rate.

v0.2.18
- Update description of a config option to remove outdated info.  No code changes.
- Update to use Zen.ModLib v1.1.20

v0.2.17
- cleanup transparency artifacts from icons

v0.2.16
- Removed old info from the readme that was no longer needed regarding the 2000-second days.  No code changes.

v0.2.15
- add skull icon to the tombstone hover info (NOTE: if you pair with `ZenPlayer` you can see the cause of death and how long the player lived)
- moved UI.Meter creation code into `Zen.ModLib v1.1.11` so that other ZenMods can use it.

v0.2.14
- moved the ItemDrop stack size display onto the icon instead of next to the name text.

v0.2.13
- clamp fuel meter to 0-1 because some mods do silly things like increase the fuel without increasing the max fuel. Therefore, you end up with percentages greater than 100% for fuel remaining, which is silly.
- add an option for showing the shield generator power level meter (default: true)
- change Smelter meters to width 10 instead of 5.
- changed some config defaults.

v0.2.12
- fix: incorrect config defaults for FuelMeter, SmelterFuel should be off because it's redundant with the icon on.

v0.2.11
- cleanup config options for fuel meter and fuel icon.  fixed up icons on windmill.

v0.2.10
- cleanup hover icon UI, it was drawing with a very faint gray background rect. It's been removed.

v0.2.9
- update readme to fix images not loading.

v0.2.8
- improved fuel icon info and made the config on by default.
- Add fuel meter and hover icon updates for more things.

v0.2.7
- add a fuel meter to fireplaces.
- add compatibility with Seasons for displaying correct fireplace burn time when computing days of fuel remaining if Seasons has fireplaceDrainMultiplier burn rates defined per season.

v0.2.6
- add option to automatically adjust the burn rate of fireplaces to display easily recognizable max days when full.  Eliminates the need to adjust the day length via ZenWorldSettings to get accurate metrics (although you can still do that if you want)

v0.2.5
- update for Zen.ModLib v1.1.0

v0.2.4
- fixed for compatibility with jewelcrafting and epic loot graphics.

v0.2.3
- recompile for compatibility with internal changes to Zen.ModLib

v0.2.2
- fixed config sync

v0.2.1
- removed BepInEx from dependency, Zen.ModLib handles it.

v0.2.0
- use Zen.ModLib

v0.1.14
- improved error message when handling missing items from mods that were removed. Explain to the user why there is an error. (run world_clean to purge old items from removed mods)

v0.1.13
- update logging and configs subsystem

v0.1.12
- Add hovertext for beehives to display their status: happy, sleeping, etc.

v0.1.11
- UPDATE FOR VALHEIM v0.220.3

v0.1.10
- set container max icons to 0 if all icons are disabled. fixes the display text to be correct when no icons are shown.

v0.1.9
- add config option to set the number of icons on containers.

v0.1.8
- no code changes.
- update readme with instructions for mod devs to display hover icons for their custom objects.

v0.1.7
- minor fix: turn off an error log that was left on by accident in the last build.

v0.1.6
- add config option to add item description to hovertext for items on the ground or on stands. (on by default)
- tweak container hovertext to show the delta of extra items in the containers beyond the 5 on the hover icons.  Example: Instead of "7 Items" it would now say "+2 More items..." since the hover icons show the first 5.
- no longer can be used in peer to peer games, connect to a vanilla dedicated server if you want mixed clients to be able to use it.

v0.1.5
- <s>relaxed server checks so that it can be run as host in peer to peer games without a dedicated server.</s>

v0.1.4 
- fixed typo.
 
v0.1.3 
- Update README, no code changes.

v0.1.2 
- initial release
