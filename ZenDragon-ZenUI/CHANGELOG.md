v1.8.0
- update for Valheim (Deep North)
- recompile for Zen.ModLib v1.14.0

v1.7.3
- added a slight dim to the "!" indicator when it's on an item that can't be crafted and isn't selected because it was clashingly too bright before against a dark bkg.

v1.7.2
- aesthetics:
- changed the uncrafted item indicator dot into an "!" and positioned it in the top left.
- changed the default color of the indicator to be a bit easier to see instead of beige (reset your color config to default if you want to see it)
- search text box: automatically resets if you change crafting stations.
- search text box: sound effects removed due to non-standard behavior to have sounds on keypress.

v1.7.1
- moved the dot to the bottom right corner instead of top right because it was overlapping the food icon.

v1.7.0
- add feature: configs for the crafting panel to show a dot in the corner of the items which have never been crafted or held.
- recompile for Zen.ModLib v1.13.7

v1.6.11
- cosmetic fix: flush the tooltip Iconic or Abstract view cache to show recomputed weights when splitting or combining stacks.
- recompile for Zen.ModLib v1.13.5

v1.6.10
- fix: null exception when using VNEI + Gamepad
- recompile for Zen.ModLib v1.13.2

v1.6.9
- fix: issue where the crafting panel would overlay the grid on top of the vanilla UI elements when logging in and selecting an element after logout.
- state was not being initialized correctly after logout.

v1.6.8
- incomplete fix, use v1.6.9 instead.

v1.6.7
- add config to hide the inventory item amount max stack size. options are either vanilla style, hide it when full, or always hide it.
- optionally toggle showing the max stack size by holding down the Tooltip Details Key.  Default: LeftAlt / Gamepad: Y
- recompile for Zen.ModLib v1.13.1

v1.6.5
- fix conflict when using ZenPortal + ExtraSlots
- recompile for Zen.ModLib v1.12.14

v1.6.4
- fix: item level stars were not displaying in the inventory.
- recompile for Zen.ModLib v1.12.12

v1.6.3
- optimization of the HotkeyBar ammo icon code.

v1.6.2
- minor cosmetic fix for tooltips.  they were not resetting the cached value when equipping an item.

v1.6.1
- add config: food fork icon colors use a simplified formula of simple majority value: health, stamina, or eitr instead of vanilla's "greater than half" computation. This helps avoid confusion when the values are close together, such as the case with some modded food items.

v1.6.0
- add a system clock local time display to the system menu so you can keep track of the real world obligations easier. by default, it displays when you open the system menu (press esc / gamepad: start button).  You can configure it to always display or never display in the configs.
- recompile for Zen.ModLib v1.12.11

v1.5.10
- a small bugfix for compatibility with ZenDistributor due to the new stacking rules introduced in v1.5.9

v1.5.9
- add config to ignore equipable items when stacking.
- rename configs related to inventory stacking
- recompile for Zen.ModLib v1.10.12

v1.5.8
- add config to suppress piece repair notifications from the top left corner. they are redundant and just clutter up the UI.
- reorg config sections: Notifications have their own section now. Biome Notice configs were moved, update your configs as needed if you changed the values for that option.

v1.5.7
- optimizations

v1.5.6
- add option to hide the ship sail indicator.
- recompile for Zen.ModLib v1.10.11

v1.5.5
- fix camera clipping through walls in first-person mode.
- fix div by zero error that could happen when first person mode was "Always"
- recompile for Zen.ModLib v1.10.7

v1.5.4
- adjust the config option for tooltip delay's default to vanilla instead of custom value of 3 from prev versions.
- slight optimization for crafting panel group icon initialization
- recompile for Zen.ModLib v1.9.5

v1.5.3
- fix: sometimes when using the first-person camera, the player's body could clip into the view causing a weird effect.  guarantee the body never renders if in first-person view.

v1.5.2
- Piece health bar displays as a colored gradient: moved this feature from ZenConstruction because it is UI related, not construction related. If you are also using ZenConstruction you should update that mod as well to avoid duplicate functionality.

v1.5.1
- added additional first person mode options: Can be locked always on by server admin if desired.
- added option to determine when the ship controls are repositioned.

v1.5.0
- added feature: first person mode. Zoom all the way in to view the first-person camera. Enabled by default under Camera config settings.
- recompiled with Zen.ModLib v1.8.6

v1.4.6
- proper fix: the fix of 1.4.5 did not work as expected, use this instead.

v1.4.5
- fix: some tooltip item names had the letters squished together too tight and they would overlap a bit. This increases the character spacing slightly so that the letters don't overlap.
- recompile for Zen.ModLib v1.8.1

v1.4.4
- change config: Colored Food Bars is no longer admin-only config.  This change is to allow colorblind players to disable this setting if desired when playing on a multiplayer server.

v1.4.3
- added a small lookup cache for optimization.

v1.4.2
- fix: ship hp bar had Y offset issue.

v1.4.1
- add feature: show ship HP bar next to the Captain's wheel.

v1.4.0
- skip this version.

v1.3.2
- fix: add explicit compatibility for KG's "Marketplace And Server NPCs Revamped." Changed the Terminal.AddString chat capitalization transpiler to run before Marketplace's transpiler to avoid conflicts due to Marketplace's Nops overwriting the opcode but not the operand therefor causing invalid matches when ZenUI's transpiler was running after.

v1.3.1
- fix: lower the priority of the "disable autocapitalization transpiler" so that it runs last and doesn't cause errors with other mods.

v1.3.0
- add feature: disable auto capitalization of shouts in the chat.

v1.2.4
- change config default: Inventory equip Assigned Gear Slots master switch is no longer admin-only. 
- change config default: Torch auto-assigned gear slot is now disabled by default, it used to auto-assign to hotbar slot 8.

v1.2.3
- fix: after Valheim update v0.221.10 the crafting panel scrolling was too slow.
- add config: Scroll Sensitivity for the Crafting Panel.

v1.2.2
- add config option to disable colored durability bars.
- add a small sound click when changing crafting groups to match the rest of the inventory UI soundscape.
- improved FPS when opening inventory:
  - add a Canvas for the crafting grid to optimize for faster drawing on slow computers when the crafting grid has many items in it.

v1.2.1
- optimizations improved FPS in inventory.

v1.2.0
- add tooltip icons for armor sets
- add tooltip info for weapons with special abilities.
- update for Zen.ModLib v1.5.0

v1.1.6
- fix: config tooltip style: detailed was not working in all cases.

v1.1.5
- tooltip aesthetics and formatting

v1.1.4
- bugfix

v1.1.3
- fix: broke the tooltips in VNEI

v1.1.2
- bugfixes and optimizations

v1.1.1
- fix: tooltip not updated correctly in some edge cases.

v1.1.0
- new feature: Tooltip summary icons show at-a-glance details for attack, defense, magic, food, status effects, and more. Quick summary of total stack weight, movement speed penalties, and description in an easy-to-read format. Press and hold the hotkey for full details at any time.
- changed config, added a new section for Tooltips.

![Example Tooltip](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenUI/tooltip_summary3.jpg?raw=true)

v1.0.1
- cleanup DamageModifiers tooltip and remove the redundant phrase "Damage modifier" so that it doesn't overflow with items like the new bear set armors and others.  It's pretty clear that it's a damage modifier.  It doesn't need a label. It's causing overflow formatting problems for long modifiers.

v1.0.0
- New Feature: Tooltip summary/detail toggle. show the description and total weight of an item in your inventory in a clean and easy to read format.  Hold the hotkey to see full details.
- New Config: Tooltip delay adjustment.  Reduce or increase the duration of time before the tooltip appears on mouse hover.

v0.9.2
- fix: scrolling issue in the crafting panel. it would sometimes be in the wrong position.
- fix: inventory equipment assigned slots auto positioning was blocking you from swapping icons around under certain edge-cases.

v0.9.1 
- do not use this version, scrolling is broken.

v0.9.0
- new behavior: when you close the crafting panel, it will remember the last item you had selected. this helps you track the material requirements for a given item without having to scroll to find it again the next time you open the window. when used with `ZenSign` you can then middle-click on the material's icon, it will direct you to the nearest container with that item.

v0.8.5
- preventative: saw an obscure error log posted on discord with some null refs in `CraftingPanel.IsNoCraftCost` so I added extra checks just in case.  Have not been able to reproduce it, and I have no idea how that person got nulls there, but maybe it will help just in case.

v0.8.4
- fix: filtered status effects are now shown on the raven menu Active Effects. They are only hidden from the Hud icons.

v0.8.3
- add config to hide status effect icons from the UI. By default, it hides the Wind Run, Belt Strength, and Wisp Light icons as I feel they are redundant and take up too much space telling you something you already know.

v0.8.2
- functionally identical to v0.8.3. I just forgot to update the README.

v0.8.1
- add config: LOD Bias - view objects farther away. This is a vanilla feature, but by default it's not set to a very far draw distance.  This just automatically sets the value to a higher value when the game starts so that you can see stuff farther away.  If you have a potato PC, set this to 0 to disable it and revert to vanilla.

v0.8.0
- add feature: Assigned gear slot positions. The 6 armor positions: head, chest, shoulder, legs, utility, and trinket can now have an assigned slot position in the inventory.  For example, when a helmet is equipped it will automatically be moved to the configured grid position in your inventory.  Position is applied when you equip an item.

v0.7.28
- fix: flicker of container contents and repair button that can happen when sliding animation is disabled by redrawing the elements once on the same frame that the container or station opens. no change if slide animation is enabled.

v0.7.27
- fix possible null ref in GetIncompleteSourceStacks

v0.7.26
- add an option: search text box position
- changed some names of config options, check your configs.

v0.7.25
- fixed typo

v0.7.24
- fixed typo

v0.7.23
- add Portuguese (Brazilian) translation

v0.7.22
- fix compatibility with Jewelcrafting:  
  - display socket success chance
  - correct the recipe list redraw issue

v0.7.21
- fix nullref error when opening a container for the first time in a game session.

v0.7.20
- Add an option "Discovery" to ShowBiomeNotice that allows admin to disable the notification for biome discovery. NOTE: Check your existing configs.
- Elevate configs: ShowBiomeNotice and ColoredFoodBars, to admin-only settings for better configuration control.

v0.7.19
- skip this, use v0.7.20 instead.

v0.7.18
- bugfix: config to disable the search box was not working.
- cleanup uncraftable items code and config settings.

v0.7.17
- Prevent the skills panel from opening automatically when accessing a crafting station or opening a container.
- Change color options for uncraftable items:
  - control item icon brightness; or use black and white.
  - control the position and color of the X, if used.
  
v0.7.16
- improved search filter logic for finding partial words

v0.7.15
- add config: disable hover tooltip on crafting grid items
- add translation: Korean

v0.7.14
- fix: flicker of "Take All" button label when it switches states.

v0.7.13
- fix: stack weight limit was not always calculating correctly.
- update readme

v0.7.12
- typo in changelog, same as 0.7.13

v0.7.11
- Moved the following configs from ZenPlayer to ZenUI as a new "Inventory" section in the configs:
  - RemoveItemFromSmallestStack
  - CombineExistingStacks
  - ExcludeHotbarWhenStacking
  - DiscardStyle

v0.7.10
- New Config: "Enable Take Stacks" 
- When enabled, the Take All button changes behavior to three states instead of one. The state changes based on the condition of the inventory:
  - Take stacks: Unfilled stacks in the player's inventory are filled (example: refill ammo). (ignores weight).
  - Take weight: If there are no stacks that can be filled, the button will take items up to max weight.
  - Take all: Press again, items are moved to inventory via vanilla behavior (ignores weight).

v0.7.9
- add Polish translation
- add Russian translation

v0.7.8
- add hover in color, when hovering over an item that is not currently craftable, it changes from black and white to color while the mouse cursor is over the item.  this aids in visibility and recognition.

v0.7.7
- add German translation

v0.7.6
- apply full-stack coloring to hotbar, not just normal inventory.
- reorganize config options to group all color-related settings together. NOTE: if you have set custom colors, you will need to set them again.  Your old values are still in your config file.

v0.7.5
- fix: ammo was not sorting correctly.

v0.7.4
- add support for explicit removal of an item from a crafting group in the "Crafting Group Assignment" section via the syntax: -prefabName

v0.7.3
- added a config option to adjust the selected crafting item info position.

v0.7.2
- update to use Zen.ModLib v1.3.0

v0.7.1
- fix armor sort order: weapon sorting by repair station level was not restricted to only weapons, so it was spilling over onto armor comparisons as well.

v0.7.0
- Update for Valheim v0.221.4, Call To Arms
- Organize the Trinket item type into the Magic category.

v0.6.16
- search can now search by armor set names (configurable, active by default)
- removed the config option to sort armor sets together.
- refined search code.

v0.6.15
- same as v0.6.16 (minor internal code changes)

v0.6.14
- fix: crafting sort order, organize weapons by damage (physical, nonphysical) then by block power.  prior versions applied block power before damage when sorting.
- add the ButcherKnife to the tools section. (you will need to update any existing configs to apply the new defaults in the Crafting Group Assignment Tools section to see the butcher knife listed in the Tools section)

v0.6.13
- show amount totals when the multicraft button is held down.
- calculate the amounts dynamically based on RequireOnlyOneIngredient. For example, Raw Fish will display different amounts to be crafted based on the type of fish you have in your inventory.

v0.6.12
- sort bucklers together at the top of the group of shields instead of after medium shields.  now small > medium > large ordering.  instead of medium > small > large ordering. within each size order by defense rating in ascending order.

v0.6.11
- improve sorting rules for other mods.
- add a config option to sort armor sets together at the top.

v0.6.10
- improved sorting rules. add compatibility fixes to handle cases introduced by other mods which do not categorize ammo correctly for their skill type.

v0.6.9
- same as v0.6.10, this is just a less elegant implementation of the same logic.

v0.6.8
- compatibility fix: some mods with custom recipes were causing the crafting UI to not show the number of items that will be crafted.

v0.6.7
- small changes to improve compatibility when loading data from some other mods in edge cases.

v0.6.6
- fix: compatibility with jewelcrafting.
- fix: selecting an item variant would not toggle the item.

v0.6.5
- add detailed info that persists after moving the cursor off of an item in the crafting grid. that way you can see the details of what you are crafting before you press the craft button. similar info behavior as gamepad users, now on keyboard and mouse.
- add soundFX when clicking on a crafting grid item (mouse only because it's not consistent with the behavior in other grids for gamepad to have sound effects when scrolling)

v0.6.4
- fix: add compatibility for wackyDB and other mods that add recipes late in the load cycle.

v0.6.3
- fix: adjusted the Repair button positioning to be compatible with other mods.
- caching and other optimizations for performance improvements when opening / closing inventory with many items.
- config option Enable Slide Animation changed to false by default because the animation can cause choppy animations in some cases. (you can turn it on if you like the slide animations)
- updated for Zen.ModLib v1.2.14


v0.6.2
- add config: Item Stack Color Full
- add config: Item Stack Color Partial
- moved config to Zen.ModLib: Remove Rich Text From Translations
- moved config to Zen.ModLib: Hide Modded Text on Title Screen

v0.6.1
- New config: hide variants when the item can not be crafted. Reduces clutter
- New config: Show uncraftable items in black and white or color with red X. 
- New config: show any known items from any known station so that you can view the item's resources from anywhere.  this helps you locate which items you need to gather.

v0.6.0
- removed admin-only requirement from color configs so that they can be set when connected to a vanilla server.
- updated for Zen.ModLib v1.2.0
- recompile for BepInEx v5.4.2332
- recompile for JVL v2.26.0

v0.5.10
- add full tooltip details to the item's crafting requirements.

v0.5.9
- reduce red X intensity at night. It was too bright.
- minor code cleanup.

v0.5.8
- fix for compatibility with Azumatt ItemCompare.

v0.5.7
- add config option: show craftable items together at the top of the list (on by default)

v0.5.6
- improve visual distinction when item can not be crafted: made the red X larger and centered it over the item's icon.

v0.5.5
- remove admin requirement for biome notification config option.

v0.5.4
- add a stronger visual distinction for items that you do not have resources to craft yet on the crafting panel: Red X and darker tint to uncraftable items.

v0.5.3
- cleanup references to food panels on logout. 

v0.5.2
- fix: was not displaying the socket tab correctly in Jewelcrafting's Gemcutter table.

v0.5.1
- fix: when applying search filter to item recipe requirements: exclude resources with zero amount requirement from the results.

v0.5.0
- added search filter to crafting UI
- changed config names related to crafting, check your configs.

v0.4.10
- fix: handle other mods adding their own custom tabs.

v0.4.9
- fix: sorting order was incorrect when dealing with multiple items of the same name but different amounts.  before: amount/name, now: name/amount.
- fix: add notice to the item's tooltip for items which only require one ingredient.

v0.4.8
- fix: case where a modded item with a non-vanilla ItemType could not be explicitly assigned to a different group via the configs.

v0.4.7
- handle case where mods add multiple recipes to craft the same item.

v0.4.6
- epic loot compatibility fix.

v0.4.5
- bugfix: error would occur when the config for crafting group item assignment was changed from default to blank.
- no longer requires game restart for changes to crafting groups to take effect.

v0.4.4
- added a "magic" crafting group category. 
- added config options for explicitly mapping items to groups allowing mod authors and end users to override the default groupings on a per item basis.

v0.4.3
- revert changes that were trying to fix epic loot.  better they are handled within epic loot itself. I have, reached out to the devs and will coordinate a fix.

v0.4.2
- change config option: Enable Crafting Panel no longer requires admin.  Does not need to be installed on server to change the value.
- Fix for epic loot compatibility.  The UI in epic loot was not displaying some text on certain dialogs.

v0.4.1
- added a new crafting menu which lists items by icon instead of name.

v0.3.2
- add feature: colored food bars. food icons tint to the color of the food type you ate. Health, Stamina, Eitr.

v0.3.1
- set default config option panel slide animations: enabled (same as vanilla)

v0.3.0
- add option to auto open skills panel
- add option to enable/disable the panel slide animation

v0.2.8
- added a finer grain of control to Biome notifications config options.

v0.2.7
- minor bugfix to biome notifications displaying twice under rare edge cases.

v0.2.6
- update readme, no code changes.

v0.2.5
- add biome notifications when changing biome via teleport or resurrection or first login.

v0.2.4
- update for Zen.ModLib v1.1.0

v0.2.3
- fixed config sync

v0.2.2
- fix fishing bait not displaying correctly in the hotbar.

v0.2.1
- removed BepInEx from dependency, Zen.ModLib handles it.

v0.2.0
- use Zen.ModLib

v0.1.6
- add a config option for the rotation mentioned in v0.1.5

v0.1.5
- tone down the durability bar color brightness and added config options.
- The durability bar was turning gray at 25% remaining.  Now stays red until broken at 0%.
- rotated item quality symbols 90 degrees and added support for modded items up to level 8 soft cap with dots & stars. Then beyond level 8 there is no limit as you can add extra symbols via config.

v0.1.4
- update logging and config subsystem.

v0.1.3
- UPDATE FOR VALHEIM v0.220.3
- Removed the patch for hiding the ship hud when Ctrl+F3 pressed because the bug was fixed in vanilla.

v0.1.2 
- Added option to hide ship controls wheel when main HUD is hidden.