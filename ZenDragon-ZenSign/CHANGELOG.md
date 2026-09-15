v1.9.0
- update for Valheim (Deep North)
- recompile for Zen.ModLib v1.14.0

v1.8.1
- fix: when swapping items on ItemStands in multiplayer the signs totals were not synchronized for all players for that item.
- added pet rock's hat to the sign counts.

v1.8.0
- integrated scanning beehives and itemstands for contents. (still working on ArmorStands)
- fix: when searching for fuel in containers, the wards were not being checked correctly so some containers could be highlighted when they shouldn't have been.
- recompile for Zen.ModLib v1.11.13

v1.7.1
- fix the text in the Compendium explaining how to search from inventory.

v1.7.0
- add help info to Compendium
- recompile for Zen.ModLib v1.10.0

v1.6.0
- add feature: track static resource pieces such as wood stacks, stone piles, and coin piles. For example, Now when you add a sign to track coins it will also include the nearby piles of coins in the displayed total.
- add config: Ignored Pieces, list any pieces that will not be used for tracking.

v1.5.1
- fix: certain edge cases when searching for fuel for a fireplace was unable to find the fuel in nearby containers.

v1.5.0
- add configs for setting the crafting station and crafting materials for building signs.  Default is vanilla values.

v1.4.1
- removed the CraftyCarts incompatibility flag as CraftyCarts v3.1.11 fixed the incompatible code.

v1.4.0
- update for Zen.ModLib v1.5.0

v1.3.9
- add Portuguese_Brazilian translation

v1.3.8
- add translation for:
  - Polish
  - Russian
  
v1.3.7
- cosmetics:
- added an outline to the sign text and changed the default text color to off-white.
- reset your text color config to see the off-white color instead of bright white.

v1.3.6
- add German translations

v1.3.5
- update for Valheim v0.221.4, Call to Arms
- relaxed the config option Item Display Style to be end-user configurable, not admin only.

v1.3.4
- moved highlight color config to Zen.ModLib
- update to Zen.ModLib v1.2.5

v1.3.3
- improved responsiveness when middle-clicking a recipe ingredient for search.

v1.3.2
- refinement of the prev update. Can now also search from the build piece selection menu.

v1.3.1
- add feature: search for build item ingredients from actively selected build peace.  Open inventory while a build piece is on your cursor and middle-click a recipe ingredient from build HUD ingredients.

v1.3.0
- bugfixes
- updated for Zen.ModLib v1.2.0
- recompile for BepInEx v5.4.2332
- recompile for JVL v2.26.0

v1.2.14
- Add KeyHint for container search in SignUI

v1.2.13
- bugfix: nullref error when search results are destroyed while highlighted.

v1.2.12
- update readme, no code changes.

v1.2.11
- Cleaned up configs: removed unsupported gamepad button customization.  No features were removed, just configs that were no longer needed/supported.
- update to Zen.ModLib v1.1.24

v1.2.10
- move the piece highlighting code into Zen.ModLib so that other ZenMods can use it like ZenDistribute.

v1.2.9
- fix: ensure the mouse cursor is inside the correct area before doing a middle-click search.

v1.2.8
- add feature: search for crafting requirements by middle-clicking them.  nearby chests will highlight.

v1.2.7
- compatibility fix for "Missing Pieces - Wooden Drawer"

v1.2.6
- code cleanup, minor optimizations, no major functional changes.
- flagged as incompatible with CraftyCarts because the carts mod alters the load timing of containers in such a way that it creates a race condition. This results in indeterministic calculations between containers and signs when moving through an area.  This results in signs not always showing the correct totals. 

v1.2.5
- update for compatibility with ZenRaids v0.3.6, ignore alt interaction press on fireplaces when searching for fuel.

v1.2.4
- update for Zen.ModLib v1.1.0

v1.2.3
- recompile for compatibility with internal changes to Zen.ModLib

v1.2.2
- fixed config sync

v1.2.1
- removed BepInEx from dependency, Zen.ModLib handles it.

v1.2.0
- Refactor to use Zen.ModLib
- Config option for outline color
- Config option to set the default mode of the camera focus toggle key.

v1.1.1
- add outline to sign icons. looks nicer.

v1.1.0
- improved sign rendering to properly handle fog and mist. no more glow in the dark sign icons that don't blend correctly with the atmosphere.

v1.0.15
- add config option to bypass search camera autofocus when key is held down, default LeftShift

v1.0.14
- update readme and description, no code changes.

v1.0.13
- update logging and configs subsystem

v1.0.12
- UPDATE FOR VALHEIM v0.220.3

v1.0.11
- fix nullref when closing build cursor

v1.0.10
- <s>fix nullref when closing build cursor</s>
- ERROR IN UPDATE: signs do not init, use v1.0.11 instead.

v1.0.9
- Fixed: when vanilla and modded players were in the same area it would sometimes cause signs to become unresponsive to new item assignment.

v1.0.8
- Bugfixes
  - Sometimes smashing a chest would not update signs.
  - Can play with friends who don't have the mod installed, like xbox clients.
  - Misc optimizations

v1.0.7
- Relax the config permissions if connecting to vanilla server.

v1.0.6
- Fix shaders for Vulkan support.

v1.0.5
- Update README, no code change.

v1.0.4
- Removed compatibility restrictions.

v1.0.3
- Optimize outline rendering to compute once on startup instead of every time they are enabled. (No performance impact on gameplay, I just don't like to waste CPU cycles)

v1.0.2
- fixed compatibility issue with ZenMap.

v1.0.1
- minor tweaks

v1.0.0
- version number correction for release

v0.3.25
- initial release

