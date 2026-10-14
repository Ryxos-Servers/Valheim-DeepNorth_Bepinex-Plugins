v1.14.21
- recompile for Valheim v1.0.17

v1.14.20
- recompile with embedded shaders for windows, osx, and linux to fix a bug where the yellow outline of highlighted pieces was not displaying correctly on mac.

v1.14.19
- recompile quick outline shader for macOS.

v1.14.18
- add a config to disable ZenMods from updating KeyHints for compatibility with other mods that want to change the key hints structure or do other things which cause conflicts.

v1.14.17
- fix vanilla: Show the AltDodge key in the key hint when the key is defined in settings.

v1.14.16
- update for Valheim v1.0.16

v1.14.15
- added a config option to prevent AltDodge from firing if the UI is open or no movement is applied.
- changed the dependency to BepInEx 5.4.2351

v1.14.14
- fix vanilla: Prevent AltDodge from firing if the UI is open.  This way you can use that keybind for other things with the UI is open.  Such as the Alt key doing stuff in the inventory or construction screen, etc.

v1.14.13
- add config: only admin can see the build piece author info.
- hide steamID from the player list if the viewer is not admin.
- add compatibility for AzuAntiCheat when using admin-relay commands.

v1.14.12
- fix: config option to disable the console on the server was not working with DeepNorth update.

v1.14.11
- BROKEN! Use v1.14.12 instead.

v1.14.10
- add a config variable to NOT display items as "cheated" and NOT disable achievements.  This works the same as the vanilla console command "yesiuseddevcommandsbutiwantmyachievementsanyway", but it's synced to all players on the server to make life easier for admin.
- add a vanilla fix to swap the trophy and achievements icons in the info panel because they are backwards in vanilla.  there is a config to turn it back to the backwards state if you want to keep seeing it wrong.

v1.14.9
- changed InventoryGui.Update transpiler of JoyButtonY tap detection for better compatibility with other mods, now just consumes the result of GetButtonDown("JoyButtonY") instead of replacing the function, also raised the priority slightly from normal to high.

v1.14.8
- added helper functions
- fix vanilla: prevent nullref on title screen when inv has an item with a worldlevel > 0

v1.14.7
- relaxed valheim version check to be non-fatal.
- recompile for Valheim v1.0.15

v1.14.6
- add config: "Admin / Unencumbered Gods" if you are in god mode, you will never be encumbered.  Default: true

v1.14.5
- fix vanilla: when opening containers with scroll bars the alignment of the grid was not reset when switching to containers without scrollbars.  this resulted in the grid being shifted up and looking weird. 

v1.14.4
- updated for support Valheim version v1.0.14
- removed config to map the Radial Menu key since vanilla now has the option.

v1.14.3
- fix: InteractAlt (Q) was not registering correctly, the translation string was not loading.

v1.14.2
- fix: pressing the Y button on gamepad when inside the build menu to select repair was automatically opening the inventory. 

v1.14.1
- add config "Inputs / Keyboard Radial Menu" for setting the radial menu key.  Vanilla does not currently have a way to change it from the default: G
- fix: gamepad layout2 was incorrectly mapping the crouch button when triggers were swapped.
- fix: version check accepts both v1.0.12 (steam) and v1.0.11 (microsoft)

v1.14.0
- update for Valheim (Deep North)
- require BepInEx to v5.4.2350
- require JVL to v2.30.0
- add support for tracking player history (login/logout)
- add internal mechanisms for syncing server realtime clock to clients.
- add method to create mod specific data files in BepInEx/configs/ZenDragon.Data dir.
- add StringList.FromDictionary() method.

v1.13.7
- fix: attack animation exploit prevention could get stuck if rapidly swapping between attack and equip/unequip animations within the same frame.

v1.13.6
- compatibility: can now set Alternative Interact Key to None under the Input settings to revert to vanilla behavior for Shift + E.

v1.13.5
- fix: apply the same fix from 1.13.4 to all gamepad controller configurations, not just classic.

v1.13.4
- fix: gamepad in classic controller configuration was causing dismount when pressing LB.

v1.13.3
- fix: gamepad in classic controller configuration was applying the Interact (Use) behavior when pressing LB.

v1.13.2
- fix: changing keyboard layout support fixed for InteractAlt (Q) when used in other languages.

v1.13.1
- bugfix: gamepad "sit" was not working reliably when controls were extended with gamepad remap and Attack Animation Exploit prevention is active.
- changed the config option for forcing gamepad remap under Input configs, if you changed the default revisit this setting.
- cleaned up some old code.

v1.13.0
- updated VirtualInventory subsystem to be more robust and support ZenRecycle burning trash in bonfires.
- be sure to update ZenRecycle, ZenItemStand, and ZenBeehive after updating this.
- NOTE: version number is wrong in the binary for this version: It's v1.13  instead of v1.13.0 - typo error

v1.12.18
- simplify configs: unify attack anim exploit prevention into a single checkbox.

v1.12.17
- bugfix: introduced a bug in v1.12.16 that caused the bow draw ring animation to stutter when firing.

v1.12.16
- improved exploit detection: added prevention for bow attack animation cancelling and new config to toggle it on/off.

v1.12.15
- improved exploit detection: Prevent attack animation cancelling

v1.12.14
- enhance vanilla fast attack exploit detection.
- added internal event hooks for InventoryGrid element updates so that other ZenMods can centralize the Transpilers and avoid duplicate code.

v1.12.13
- fix vanilla exploit: prevent emote fast attack.
- bumped JVL requirement to v2.29.2

v1.12.12
- use v1.12.13 instead.

v1.12.11
- removed feature: mouse3 / mouse4 button swap option.  This sort of thing is best handled by the os or drivers, it's lower-level and faster if handled there vs patching the keybind methods inside the game app.

v1.12.10
- fix: the console was not parsing arguments with quotes in them in some edge cases.

v1.12.9
- fix for wolf foods to be compatible with ZenRaids v1.0.1 item despawn protection

v1.12.8
- fix config default for "Network - RPC NoSpam Everyone - Nearby Only" does not need "Step" in the list since it's covered by ZNetView anyhow.
 
v1.12.7
- rename network rpc optimization configs to be easier to unerstand and to also provide an option to disable the functionality only on the client but not on the server so that mods like EWP can still work. The config names were all changed for this section. if you changed the defaults, you should revisit the config and read the descriptions again.

v1.12.6
- changed the network optimization configs to be more fine-grained, check your configs if you changed the defaults.  There is a new Optimizations section.  
- Added a bypass for RPC_TeleportTo so that the "tp" command should work.

v1.12.5
- added a vanilla fix option: Fix Network - ZDOMan.SendZDOToPeer2, this will send ZDO updates to all peers every frame instead of spreading it out over multiple frames. Read the config description before enabling this feature.
- renamed the config "Fix Network - Spam Everyone RPC", if you changed your defaults, change them again.

v1.12.4
- simpler rpc range calculation. square instead of circle.

v1.12.3
- UI consistency: ensure reformatted HoverText always positions InteractSecondary action after InteractPrimary action.  This handles edge cases where external mods may append [Shift + E] SecondaryAction at the end of the HoverText instead of inserting it after [E] PrimaryAction.

v1.12.2
- extend the network optimization config beyond just Footstep and RPC_DamageText messages, also apply range filter to all ZNetView broadcast messages.  Only send to players within range. Does a tree really need to braodcast to the whole server when it grows? No, it does not.
- fix: listkeys command was not showing player keys.

v1.12.1
- use v1.12.2 instead.

v1.12.0
- add config: Network optimization to disable spam of Footsteps and DamageText messages.  Only send messages to players in the same zone (or nearby zone) instead of the whole server.
- bugfix: admin remote commands run on the dedicated server were not printing results to console was not working.

v1.11.14
- fix: when connecting to vanilla servers ConfigSync was not called which would cause some ZenMods to fail to initialize properly. This update calls ConfigSync at least once on startup even if connecting to a vanilla server.

v1.11.13
- add VirtualInventory class for ZenMods to be able to open certain pieces as Containers without having to attach a Container component which have caused issues with some other mods.

v1.11.12
- fix: when destroying "piece_chest_treasure" after outline was applied it would leave purple shaders behind.

v1.11.11
- fix: removed logging warnings accidentally left over from debug build.

v1.11.10
- Add config option to parse console commands that have spaces in them by checking for surrounding quotes.  such as "Player Name" with spaces.
- update JVL dependency to v2.29.1

v1.11.9
- fix edge case: ensure cheat mode is explicitly disabled by default before enabling /devcommands to prevent commands being out of sync with context.

v1.11.8
- add config admin auto-enable /devcommands on login

v1.11.7 
- fix: auto login admin modes working in single player games.

v1.11.6
- improve admin tools and additional indicators for accessing warded areas as admin.
- bugfixes & security improvements.

v1.11.5
- fix: config options for auto login admin mode settings were not being set on login.

v1.11.4
- add config: Admin Login NoCost for admins to automatically set nocost mode on login.
- add config: Admin Display Status Indicators: show status indicators on bottom left corner for various admin modes: devcommands, god, ghost, nocost.
- add config: Admin Run Slash Commands From Chat: admin can execute console commands via chat with /
- add admin console command zen_repairall to repair all pieces within a given radius, default 20

v1.11.3
- minor fix: zen_playerlist console command was not showing total number of players online.

v1.11.2
- relax permission of configs for admins to start in god/ghost mode to be per-profile instead of server wide. That way individual profiles can define the desired login behavior.

v1.11.1
- add admin console commands for basic server maintenance:
  - zen_playerlist
  - zen_broadcast <message>

v1.11.0
- add configs to enable running admin console commands when connected to dedicated server.
- if the mod ServerDevCommands is installed, then this feature has no effect and delegates to ServerDevCommands instead.

v1.10.13
- fix: Highlight/outline materials could become invalid when destroying a piece that was previously highlighted.  Purple shaders would display on the wreckage.

v1.10.12
- added VirtualContainer system for other ZenMods to use.
- added InterpolatedStringHandlers for logging for lazy evaluation of log entries.
- config option "Alternative Interact Use Shift+E" changed to admin only and default changed to false.

v1.10.11
- more optimizations

v1.10.10
- bugfixes & optimizations

v1.10.9
- add data type "KeyboardShortcut" to Compendium help info.

v1.10.8
- improve version checking.
- formatting improvements on compendium.

v1.10.7
- fix vanilla gamepad: prevent TriggerL + X from dropping items from your inventory.  It should not.
- misc bugfixes.

v1.10.6
- compatibility: other mods were causing config sync to fire before all prefabs were registered. verify that prefabs have been registered before performing config sync.
- small edge case fix.

v1.10.5
- use v1.10.6 instead.

v1.10.4
- added an option to suppress the "Too Hard" message when using Stagbreaker to find Silver.
- rename the Chair exploit config option, check your configs if you disabled it.

v1.10.3
- add Valheim version check to ensure that the mod is compatible with the installed version of Valheim.

v1.10.2
- add some additional config options for the Compendium Help Infos to control insertion point and label prefix.
- config option name changed General / Show Help Info is now "Compendium / Enable Help Info"

v1.10.1
- cleanup the Compendium help info to show the correct mouse button number since valheim offsets by 1.

v1.10.0
- added help info to the Compendium (Raven menu) to include the basic info about any ZenMods installed.

v1.9.5
- added error handling when parsing configs for better reporting of syntax errors.
- added a secondary prefab lookup cache for when the JVL cache is unable to find modded content.
- marked some internal Prefab lookup methods as obsolete.

v1.9.4
- same as v1.9.5 but has slightly less optimized logging for prefab cache lookups when not debugging.

v1.9.3
- prevent unpatching during game shutdown so that the vanilla fix to prevent ShieldGenerators from throwing a nullref on game shutdown does not get unpatched before the game quits.

v1.9.2
- add config sync locking to prevent reentrant race conditions when other mods force a config resync in the middle of dictionary indexing.
- vanilla fix to prevent ShieldGenerators from throwing a nullref error on game shutdown.

v1.9.1
- add interop relay for fetching portal rune symbols from other mods.

v1.9.0
- add admin config to toggle allowing the console when connected to a server. disabled by default (except for admin)
- add admin config to toggle allowing client side ZenMod debug logs when running the server.
- improved KeyHint subroutines to handle temporary label changes.

v1.8.7
- fix typo in lib param name, update ZenTargeting to match.

v1.8.6
- add Zone-to-CantorID functions.
- add Biome localization functions.
- improve: admin command 'relay' for admin-only commands

v1.8.5
- added null-safe function to check if the player is in god mode.

v1.8.4
- small bugfix for future compatibility, no major changes from v1.8.3, just handles null in an edge case more gracefully.

v1.8.3
- added a few extra helper functions.

v1.8.2
- added new internal functions
- added prefab caching syntax shortcuts
- removed WrapNet21.dll
- update JVL to v2.28.0

v1.8.1
- update time functions to use double precision for future compatibility.

v1.8.0
- moved configs "Hide Modded Text" and "Hide Logout Menu" to ZenLogin v1.3.0 because those options make more sense there.
- no other changes.

v1.7.5
- fix vanilla: prevent vanilla null ref exception that happens when standing near a shield generator and quitting the game.

v1.7.4
- fix: UI meters were not calculated correctly in some edge cases.
- fix: internal versioning mismatch error.  Mod's public Version number was not updated in v1.7.2 to match thunderstore's version number. it still presented itself on thunderstore as v1.7.2, but internally presented itself as v1.7.1.  This version corrects the issue by making sure everything is v1.7.3. you should use v1.7.3 instead of 1.7.2 or v1.7.1
- no code changes.

v1.7.2
- fix vanilla: unify the smelter resource loss bugfix from v1.7.1 to also apply to fireplaces.

v1.7.1
- fix vanilla: Prevent loss of resources when the Smelter ZDO owner leaves the area while another player is adding items to the smelter. Automatically claim ownership of the smelter ZDO since the resource has already been removed from the player's inventory.
- interface change for Interop message passing.

v1.7.0
- add a centralized Interop message passing system to allow mods to communicate with each other without binary compilation or reflection. See Thunderstore wiki entry for more details.

v1.6.10
- internal code cleanup: no major changes.

v1.6.9
- add config for gamepad emote wheel button press duration.

v1.6.8
- compatibility: ProtectiveWards / Waystones / etc., hover text for Interact Alt button now works with all mods that use the Standard Vanilla Patterns in their hover text for Shift + E:
```
[<color=yellow><b>$KEY_AltKeys + $KEY_Use</b></color>]
[<color=yellow><b>$KEY_AltPlace + $KEY_Use</b></color>]
```

v1.6.7
- fix vanilla: wolves will eat bear and serpent meat, config to adjust for other meats.

v1.6.6
- improved code for preventing the chair exploit.  
  - No longer prevents sitting in an invalid chair, instead checks that the chair is in a valid position and it doesn't overlap anything before you can build it.

v1.6.5
- identical to v1.6.6, but not optimized.  use v1.6.6 instead.

v1.6.4
- add config: fix chair exploit, enabled by default.

v1.6.3
- fix: removed code no longer needed due to fixes in Valheim v0.221.12.

v1.6.2
- fix: gamepad crouch was not working after latest valheim update.
- fix: when using ZenUI with disabled inventory slide animation and gamepad classic control scheme pressing alt+Y to activate guardian power would display the inventory momentarily, fixed.
- change: gamepad Sit was moved from alt+X to alt+Select since Sit isn't worthy of a face button.
- added config option for disabling gamepad emote wheel.

v1.6.1
- added an extension method for checking input mappings.

v1.6.0
- fix for compatibility with Valheim v0.221.10
- prevent null ref error when using ZenTargeting and the latest version of Valheim

v1.5.9
- add config options for toggling some fixes for vanilla bugs:
  - verify if the fire is lit under the cauldron (for compatibility with Valheim RAFT)
  - fix excessive attack stamina drain when running.
  
v1.5.8
- add a few extra safety checks on top of v1.5.7

v1.5.7
- fix: the vanilla fix to set player keys when bosses die was not being assigned to all players in the area when a boss dies.

v1.5.6
- fix, v1.5.5 was an invalid patch. typo caused the index to be incorrect.

v1.5.5
- add a fallback lookup for finding the item prefab when mods do not register cloned items correctly.  Creates an index of item display name mapped to the item prefab during data sanitization so that mods that do not register cloned items a valid m_dropPrefab or sharedData index can still locate their prefab.

v1.5.4
- edge case minor cleanup: adjust timings so that After Sync sanitization, if enabled, is guaranteed to run on World Start but before any other ZenMod.

v1.5.3
- added a config option "Sanitize Data After Sync" which will enable a second pass of SanitizeData. The second pass runs after mods have synchronized their items and recipes and registered them to ObjectDB. The option is disabled by default.  Enable it if you see errors in your logs regarding: "Exception: Missing dropPrefab and sharedData index" that means that a mod did not register an item correctly in the ObjectDB and SanitizeData will attempt to correct it.

v1.5.2
- add null checks to InventoryGrid.DisableElement

v1.5.1
- add fix to vanilla to apply per-player keys when a boss is killed. Vanilla simply doesn't set the key, it queues it, but if you don't die or teleport the key is never set.

v1.5.0
- change UIColor from struct to class for internal memory optimization. 
- This update requires updating all ZenMods. After you update this, you MUST update any other ZenMods you are using.  Use a mod manager like R2 or Gale.  They will handle version dependencies automatically. ALl ZenMods are designed to be used with mod managers to ensure version dependency chains are correct.  If you are already using a mod manager, this process will be automatic.
 
v1.4.7
- add LitPanel to materials lib

v1.4.6
- add additional UI colors and itemData helper methods.

v1.4.5
- add helper method for detecting tower shields.
- add helper methods for transpilers

v1.4.4
- add vanilla fix for ship chairs to make sure they always report as being on a ship.
- added some helper methods for detecting attached doodads.

v1.4.3
- small fix for ZenWorldSettings v1.1.2

v1.4.2
- relay command now works over any distance.

v1.4.1
- added some helper functions

v1.4.0
- add a Console section to the configs:
  - Relay Command option to help server admins issue commands as players.  Useful for modifying player keys or other maintenance tasks.  Disabled by default.
  - Admin Only commands, a list of commands that are only executable by admins. Defaults to seed-related commands
- To avoid code overlap, update ZenWorldSettings when you update this. It had shared functionality moved here.

v1.3.11
- fix: edge-case data sanitization issue where an item was sanitized repeatedly due to not taking a snapshot of the list first before iterating and modifying it.

v1.3.10
- added a config option to disable Shift+E, This can be handy when trying to run and press E at the same time. See configs for more info.

v1.3.9
- use v1.3.10 instead, mislabeled configs in this version.

v1.3.8
- fix: transpiler compatibility issue with AdventureBackpacks and InventoryGui.Update / Hide

v1.3.7
- add an option to hide the Logout menu

v1.3.6
- add vanilla fix to prevent closing inventory when a text box is open.
- change the path to UI transparency material.

v1.3.5
- fix: Init of InteractAlt now uses const string instead of dynamically generated string so that it can be used inside a Transpiler during Unity debug sessions.

v1.3.4
- same as v1.3.5 but there was a typo in this version.

v1.3.3
- fix: move call to GUIManager out of OnDestroy because it can cause nullref error in JVL on shutdown in some edge cases when the GUIManager static constructor is invoked for the first time during shutdown.

v1.3.2
- fix vanilla: Player.AutoPickup was doing a SphereOverlap every frame of FixedUpdate.  Not a good use of memory.  Changed it to SphereOverlapNonAlloc so that a memory buffer is only allocated once.
- create WrapNet21.dll to handle calls to ImageConversion.LoadImage via wrapped Netstandard2.1 calls.

v1.3.1
- fix config option: show/hide modded text on the title screen was not working after reboot.

v1.3.0
- update for Valheim v0.221.4, Call to Arms

v1.2.15
- cleanup item data sanitization code, add an extra check.
- fix vanilla: when moving items between container and player inventory via ctrl-click: refresh the crafting panel.
- fix: remove the warning from the logs when using Configuration Manager.

v1.2.14
- recompiled to fix the version mismatch error.
- added some helper functions

v1.2.13
- build version mismatch error: skip

v1.2.12
- build version mismatch error: skip

v1.2.11
- vanilla bugfix: prevent excess stamina drain when transitioning from running to attacking.  In vanilla, you will drain stamina as if you are running, even though you are no longer running until you release the movement input.

v1.2.10
- bugfix: Startup warning fixed. Translations were not being filtered against "Remove Rich Text From Translations" config option due to nullref. Cause: incorrect field definition order.

v1.2.9
- Config moved from ZenUI: Remove rich text from translations.
- Config moved from ZenUI: Hide modded text on the title screen.
- vanilla bugfix: take a screenshot of your face while holding tool when the HUD is disabled (ctrl+F3). Now you can rotate the camera all the way around to see your face while holding a hammer.

v1.2.8
- gamepad fix: change the Interact-Alt button from LeftBumper/Trigger to LeftStickButton for compatibility with all scenarios. (Was not working correctly when interacting with objects that require the player to move, such as the bed)

v1.2.7
- add ZenDebug for internal use
- add HarmonyExt helper methods for simplifying syntax of common patches.

v1.2.6
- updated compression lib Microsoft.Powershell.Archive to v1.2.5 which should fix the path separator issue when compressing .zip archives to use forward slashes instead of backslashes.
- No code changes, just repackaged for path separator compatibility in the zip archive.

v1.2.5
- centralized logic for searching the area for build pieces.
- moved highlight outline color configuration here instead of being in various mods.
- misc code cleanup.

v1.2.4
- internal refactoring creates per assembly KeyHints to fix a bug in the developer workflow. No change for end-users.

v1.2.3
- fix vanilla: suppress Unity.Debug "PlatformUserID failed to parse" messages unless logging is enabled.

v1.2.2
- add IsUsing() extension method to Humanoid for item usage checks.

v1.2.1
- fix: gamepad remap compatibility conflict. Dpad-down "Show/Hide Weapon" with Plant Easily usage of LB+Dpad-down to resize the planting grid.

v1.2.0
- refactor for code cleanup and optimizations.
- change the default of mouse3/mouse4 button swap to false.
- improved logging system efficiency
- update to BepInEx v5.4.2332
- update to JVL v2.26.0
- NOTE: You must update all ZenMods after updating Zen.ModLib. if you do not, then they will not function. It is strongly recommended that you use a mod manager like Gale or R2 as the version dependency chain is handled automatically when using a mod manager.

v1.1.26
- modify KeyHint handling to accommodate multiple hints with the same name in different categories.
- hide the "Close" KeyHint on the Inventory screen as it does not follow the behavior of hints anywhere else in the game and wastes limited space that could be used for more important things.

v1.1.25
- fix: edge cases that could cause nullref when highlighting pieces.
- fix: keyhints nullref in edge cases

v1.1.24
- fix: translation loading error that was causing some translations to not load correctly.

v1.1.23
- add a config option to swap Mouse3 and Mouse4 buttons because Valheim maps them inverted.

v1.1.22
- Move Piece highlighting code from ZenSign into this shared lib so that other ZenMods can use it, like ZenDistributor.

v1.1.21
- add InventoryGrid.GetHoveredItem

v1.1.20
- add TryAddItem function to InventoryExt that returns the added item if successful.
- add capability to KeyHint management to alter key hint label
- fix: in string handling with ProperCase() where it would error on empty string.
- fix: gamepad map button returned to the default behavior.
- add: vanilla fix for handling TextInput when the inventory is open.
- add: universal TextPrompt input wrapper around TextInput
- rework gamepad remap to make room for ZenMap's portable maps and return of the dedicated map button.  If you use gamepad, check the button map after this update.  A few minor changes have been applied if you use ZenMods which require gamepad remap.
- add function for applying custom texture to item prefabs.

v1.1.19
- refactor some internal functions and added additional utilities relating to inventory item lookup.

v1.1.18
- add UI.CleanImageTransparency for quick access to shader for cleanup of icon transparencies.

v1.1.17
- removed write operations to avoid Thunderstore automated checks from triggering false-positives.

v1.1.16
- added utility functions for sprite handling.

v1.1.15
- extra checks for data validation. some mods really mangle items and forget to add basic things like ItemDrop components.

v1.1.14
- added an option for automatic sanitization of item and recipe data on game start. this handles cases where mods do not properly index their items into all ObjectDB indexes.
- config option to disable sanitization if desired.

v1.1.13
- improved internal logging mechanism.

v1.1.12
- fixed a null ref warning preventing some configs from loading when checking if ConfigManager is installed.

v1.1.11
- fix vanilla: when in DebugFly mode give the player a nicer animation state than the default which is to make them look like they are standing on solid ground, which is goofy looking.
- fix vanilla: correct for missing space at the end of the translation string: `$msg_turretotherammo`
- moved general purpose UI meter creation code out of `ZenHoverItem` into this lib so that other ZenMods can use it.

v1.1.10
- added helper time conversion functions: RealToGameTime and RealToGameTimeFuel

v1.1.9
- internal changes for making console command prefixes public so that other ZenMods can read them.  Nothing major.

v1.1.8
- added a config option to control the threshold before warnings get logged about potential performance impacts from mods like ConfigWatcher which can cause excessive IO thrashing from constantly reloading your config files.

v1.1.7
- replaced calls to GUIManager.IsHeadless() with internal implementation ModLib.IsHeadless because JVL and Jewelcrafting were fighting when GUIManager's static constructor would cause PrefabManager to initialize assets and that triggered the softref system which would somehow cause errors whenever Jewelcrafting was installed.

v1.1.6
- added check if ConfigurationManager is installed. Pause detecting config file IO thrashing if the ConfigurationManager window is open, resume detection once it closes.

v1.1.5
- added a fix for a bug in vanilla where CraftingStations and CookingStations were not correctly checking if the fire was actually lit under them.

v1.1.4
- added Localize() extension that takes params.
- require version matching at Patch level instead of Minor.  Everyone must run the same exact version. Too complicated to debug otherwise.

v1.1.3
- add compatibility for Seasons mod in fireplace fuel burn rate calculations.

v1.1.2
- Changed remap of gamepad sit from Select to X + Alt Function to free up room for ZenConstruction to use Select as the dedicated Hammer button.

v1.1.1
- Add method: UI.InsertInteractAlt

v1.1.0
- improved config sync handling for prefabs and fallback for single player mode.
- refactored internal code
- add a default constructor to StringList
- code cleanup: remove some public methods, breaks backwards compatibility with some ZenMods, update all ZenMods.

v1.0.5
- add capability to automatically sync config changes for custom crafting items.

v1.0.4
- internal code cleanup

v1.0.3
- relocated input refresh method to base class, no major changes.

v1.0.2
- fix minor logging issue.

v1.0.1
- add config option to force gamepad remap if desired.

v1.0.0
- initial release