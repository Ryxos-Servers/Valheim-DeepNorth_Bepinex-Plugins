# ZenSign

Stay organized! Signs can display the quantity of an item in nearby chests.  Locate the item by interacting with the sign. Works in multiplayer. Full gamepad support.

### Features

- Easy to use intuitive interface. Apply any item to a sign to count all instances of it in nearby containers.
- Adjust sign text color.
- Real-time instant update of totals.
- Search the area and instantly find anything in your hoard by tapping the sign. The chests containing that item will highlight. The camera will focus on the closest chest.
  - ... Or you can search the area for an item in your inventory by middle-clicking it.
  - ... Or the crafting menu recipe ingredients.
  - ... Or the build HUD recipe ingredients. 
- Locate fuel by interacting with a fireplace, and the camera will focus on the nearest container with the required fuel.
- High performance. Can deal with thousands of items with no loss of framerate.
- Backwards compatible - add/remove the mod and your existing signs won't break.
- Multiplayer support.
- Full gamepad support.

### Organize Your Hoard

Example: Icon Mode
![Example - Icon Mode](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenSign/example.jpg?raw=true)

### Helpful Auto Updating Signs

Example: Text Mode
![Example - No Icon Mode](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenSign/example_no_icon.jpg?raw=true)

### Highlight Search Results

![Highlight Chests](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenSign/highlight.jpg?raw=true)

### Why use this?

Vanilla container sizes and manual item movement were well-thought-out intentional features created by the developers. However, there are a few shortcomings to this approach because by default it quickly runs into the problem of *finding* anything.  In multiplayer the problem is compounded since a new player has no idea where their friends stashed the item they are looking for. Each player has their own logical organization that makes sense to them but may not make sense to anyone else.  

Vanilla signs offer some help for improving organization via textual hints, but they quickly fall apart when looking for a very specific item in a hoard of hundreds of containers that someone else organized.  Furthermore, if someone moved the item to a different container, then the signs would need to be manually updated to reflect the new supply status.  As such, there is no automated way to quickly get a *Warehouse Overview* of your total supplies available in a specific location.

The common solutions to this problem have been to automate the process by using mods to teleport items into your hands via crafting directly from containers. However, this can shorten the gameplay loop since it bypasses the logistical needs of well-planned organization and warehouse construction.  This is like having the dots in the Pac-Man maze automatically come to you. Easier, but less interactive.

Manually managing the hoard logistics is a key part of what makes Valheim great. When we bypass that mechanism by crafting directly from containers, we are speeding up the gameplay loop. Hoard size should be a function of logistical space.  I.e., if you have a giant stash of gear, you should need to build a giant room to contain it. That's part of the progression.  

### The Solution

Vanilla signs have been augmented to enable the player to assign an item to them.  The item's icon and quantity available in all the containers in the area is displayed on the sign.  The totals are updated in realtime.  A player can glance at the wall to see how many bars of iron their friends have put into the hoard while they were away. They can tap the sign to highlight which chests contain the iron bars. The camera will swiftly pan towards the nearest chest, and all the chests in the area that contain iron will be highlighted for easy access.

Stay close to vanilla mechanics while also providing an immersive and enjoyable way for individuals to have an easy overview of all items in their hoard. Simultaneously emphasizing a collaborative multiplayer experience so that players can more easily work together.

### How To Use

Point at a sign and use the 1-8 hotkey to assign an item to a sign. (NOTE: pair with `ZenUseItem` to make assigning items even easier)

The total will be displayed next to the item icon on that sign.  Interact with a sign that has an item assigned to it to highlight all containers nearby that have that item in them. 

Switch the sign to track a different item by assigning a new item to it.

If you want to reset a sign back to text mode, then assign any item to it twice.  The sign will reset to a vanilla text sign.

### Search Area

Tap any sign with an item on it to instantly locate that item in nearby containers.

### Inventory Search

 If you don't have a sign setup for an item in your inventory, you can also search directly from your inventory. This makes it easier to find containers to stash existing items in case there is no sign nearby. Press the hotkey while pointing at the item in your inventory.  The hotkey is defined in the config file. The default is the middle mouse button.  This functionality can also be disabled in the config file if you don't want it.

### Fuel Search

When fueling a light source, if you do not have the fuel in your inventory, it will highlight the nearest container to show you where the fuel is.  This is to simply make it easier to find fuel in the dark.

Carts and ships are not included in the totals.  Unload cargo into your warehouse to see the totals reflected on the signs.  Use `ZenDistributor` to quickly unload your carts.

### Summary

Since crafting from containers can speed up the game loop this provides a way to approach the issue of hoard management that remains true to the vanilla gameplay mechanics. Coupled with enhanced organizational tools and an intuitive interface, this mod gives all players more information and eases management tasks without full automation and maintains immersion.

## Client / Server Requirements

NOTE: Technically, it is *not required* on the server. However, if it is installed on the server then it will force all clients to have it installed as well. This is to enable two modes of usage:
1. Dedicated server admins can put the mod on the server to enforce all clients to have the mod installed and sync admin configs.
2. Trusted friends can agree to run the same mods and connect through a vanilla dedicated server with no enforcement but with locked admin configs.

## Client Only

This mod operates entirely client side. That means you can connect to any vanilla server with this mod installed.  Other players do not need to have the mod installed.

NOTE: If you host a game session with this mod installed, then it will be considered to be installed on the server since your session is the server. Therefore, all clients will be required to have it.  If you don't want to require all players to have this mod, then you will need to host your game in a dedicated server.  You can download and run the Valheim Dedicated Server from Steam or host one in the cloud.

## Extend Functionality with Additional ZenMods

- `ZenUseItem`: Apply items to objects directly from inventory without needing to use the 1-8 hot bar.
- `ZenDistributor`: Easily unload all the cargo from your cart into nearby chests.
- `ZenRedecorate`: Move chests and other things around without destroying them.
- `ZenHoverItem`: Show hover icons for everything.
- `ZenItemStand`: Armor Stands and Item Stands open like containers.  Quick swap gear.
- `ZenBeehive`: Beehives open like containers. Include their totals in the sign's count.
- `ZenRecycle`: Obliterators return a randomly selected ingredient of the item.
- `ZenTargeting`: Target lock is awesome!
- `ZenUI`: Replace the crafting panel with a visual one making items easier to find.

## Improve Your Experience

### [CORE MODS](https://thunderstore.io/c/valheim/p/ZenDragon/ZenModpack_CORE/)

The full collection of all Zen MODS:

- Radically improved QoL
- Incredible performance
- Pre-configured
- 100% Gamepad support
- Spectacularly immersive

Enjoy!

## Sample Config File

```
## Settings file was created by plugin ZenSign v1.8.0
## Plugin GUID: ZenDragon.ZenSign

[Crafting]

## [Admin] Crafting station required to construct a sign. (Vanilla: None)
## [restart required for changes to take effect]
# Setting type: String
# Default value: None
# Acceptable values: None, Workbench, Forge, Stonecutter, Cauldron, ArtisanTable, BlackForge, GaldrTable, MeadKetill, FoodPreparationTable
Crafting Station = None

## [Admin] Crafting material requirements for building a sign.
## [restart required for changes to take effect]
# Setting type: StringList
# Default value: Wood:2, Coal:1
Crafting Requirements = Wood:2, Coal:1

[Fuel]

## [Admin] Range to search when sourcing fuel from containers for lights.
# Setting type: Single
# Default value: 25
# Acceptable value range: From 0 to 50
Fuel Search Range = 25

[General]

## [Admin] Radius of the sign to search for containers.
# Setting type: Single
# Default value: 20
# Acceptable value range: From 1 to 25
Sign Search Radius = 20

## [Admin] The color of sign text. (Vanilla: Black)
# Setting type: Color
# Default value: E0E7DAFF
Sign Text Color = E0E7DAFF

## [Admin] Comma separated list of item prefab names that are not assignable to signs.
# Setting type: StringList
# Default value: 
Ignored Items = 

## [Admin] Pieces which will be excluded from container tracking
## NOTE: Private chests are automatically ignored.
# Setting type: StringList
# Default value: 
Ignored Pieces = 

## [Admin] Number of seconds that highlighted objects will persist.  Set to 0 to disable highlighting.
# Setting type: Single
# Default value: 10
# Acceptable value range: From 0 to 60
Highlight Duration = 10

## [Admin] Only allow stackable items to be assigned to Signs. Otherwise any item can be assigned.
# Setting type: Boolean
# Default value: false
Stackable Items Only = false

## Show the item on the sign as an icon or text only?
# Setting type: ItemDisplayMode
# Default value: Icons
# Acceptable values: Icons, Text
Item Display Style = Icons

## [Admin] List of pieces that signs should track because they hold resources but are not Containers.
## Uses the build cost resource list of the piece itself for resource tracking.
## Useful for things like stacks of wood, piles of rock, or treasure chests.
## For example: Your sign totals for coins will include your gold piles.
## Can restrict the resource list of a piece to only include a subset of its resource list. 
## For example: See piece_treasure_chest.
# Setting type: StringList
# Default value: wood_stack, wood_fine_stack, wood_core_stack, wood_yggdrasil_stack, blackwood_stack, bone_stack, treasure_stack, stone_pile, coal_pile, blackmarble_pile, grausten_pile, skull_pile, treasure_pile, piece_chest_treasure:Coins:Ruby:SilverNecklace
Static Resource Pieces = wood_stack, wood_fine_stack, wood_core_stack, wood_yggdrasil_stack, blackwood_stack, bone_stack, treasure_stack, stone_pile, coal_pile, blackmarble_pile, grausten_pile, skull_pile, treasure_pile, piece_chest_treasure:Coins:Ruby:SilverNecklace

[Input]

## [Admin] Remove Rich Text formatting tags from sign text.
## This prevents <color> tag changes, but also prevents abuse of <size> tags on multiplayer servers.
# Setting type: Boolean
# Default value: true
No Rich Text Tags = true

## [Admin] Search directly from inventory via hotkeys enabled / disable.
## Note: Admin in God mode can always search from inventory
# Setting type: Boolean
# Default value: true
Inventory Search = true

## Keyboard or mouse button to press to search for an item from the inventory UI.
## Gamepad is the "Select" button. KeyHints at the bottom of the screen show the correct button.
# Setting type: KeyCode
# Default value: Mouse2
# Acceptable values: None, Backspace, Tab, Clear, Return, Pause, Escape, Space, Exclaim, DoubleQuote, Hash, Dollar, Percent, Ampersand, Quote, LeftParen, RightParen, Asterisk, Plus, Comma, Minus, Period, Slash, Alpha0, Alpha1, Alpha2, Alpha3, Alpha4, Alpha5, Alpha6, Alpha7, Alpha8, Alpha9, Colon, Semicolon, Less, Equals, Greater, Question, At, LeftBracket, Backslash, RightBracket, Caret, Underscore, BackQuote, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z, LeftCurlyBracket, Pipe, RightCurlyBracket, Tilde, Delete, Keypad0, Keypad1, Keypad2, Keypad3, Keypad4, Keypad5, Keypad6, Keypad7, Keypad8, Keypad9, KeypadPeriod, KeypadDivide, KeypadMultiply, KeypadMinus, KeypadPlus, KeypadEnter, KeypadEquals, UpArrow, DownArrow, RightArrow, LeftArrow, Insert, Home, End, PageUp, PageDown, F1, F2, F3, F4, F5, F6, F7, F8, F9, F10, F11, F12, F13, F14, F15, Numlock, CapsLock, ScrollLock, RightShift, LeftShift, RightControl, LeftControl, RightAlt, LeftAlt, RightCommand, RightMeta, RightApple, LeftCommand, LeftMeta, LeftApple, LeftWindows, RightWindows, AltGr, Help, Print, SysReq, Break, Menu, WheelUp, WheelDown, Mouse0, Mouse1, Mouse2, Mouse3, Mouse4, Mouse5, Mouse6, JoystickButton0, JoystickButton1, JoystickButton2, JoystickButton3, JoystickButton4, JoystickButton5, JoystickButton6, JoystickButton7, JoystickButton8, JoystickButton9, JoystickButton10, JoystickButton11, JoystickButton12, JoystickButton13, JoystickButton14, JoystickButton15, JoystickButton16, JoystickButton17, JoystickButton18, JoystickButton19, Joystick1Button0, Joystick1Button1, Joystick1Button2, Joystick1Button3, Joystick1Button4, Joystick1Button5, Joystick1Button6, Joystick1Button7, Joystick1Button8, Joystick1Button9, Joystick1Button10, Joystick1Button11, Joystick1Button12, Joystick1Button13, Joystick1Button14, Joystick1Button15, Joystick1Button16, Joystick1Button17, Joystick1Button18, Joystick1Button19, Joystick2Button0, Joystick2Button1, Joystick2Button2, Joystick2Button3, Joystick2Button4, Joystick2Button5, Joystick2Button6, Joystick2Button7, Joystick2Button8, Joystick2Button9, Joystick2Button10, Joystick2Button11, Joystick2Button12, Joystick2Button13, Joystick2Button14, Joystick2Button15, Joystick2Button16, Joystick2Button17, Joystick2Button18, Joystick2Button19, Joystick3Button0, Joystick3Button1, Joystick3Button2, Joystick3Button3, Joystick3Button4, Joystick3Button5, Joystick3Button6, Joystick3Button7, Joystick3Button8, Joystick3Button9, Joystick3Button10, Joystick3Button11, Joystick3Button12, Joystick3Button13, Joystick3Button14, Joystick3Button15, Joystick3Button16, Joystick3Button17, Joystick3Button18, Joystick3Button19, Joystick4Button0, Joystick4Button1, Joystick4Button2, Joystick4Button3, Joystick4Button4, Joystick4Button5, Joystick4Button6, Joystick4Button7, Joystick4Button8, Joystick4Button9, Joystick4Button10, Joystick4Button11, Joystick4Button12, Joystick4Button13, Joystick4Button14, Joystick4Button15, Joystick4Button16, Joystick4Button17, Joystick4Button18, Joystick4Button19, Joystick5Button0, Joystick5Button1, Joystick5Button2, Joystick5Button3, Joystick5Button4, Joystick5Button5, Joystick5Button6, Joystick5Button7, Joystick5Button8, Joystick5Button9, Joystick5Button10, Joystick5Button11, Joystick5Button12, Joystick5Button13, Joystick5Button14, Joystick5Button15, Joystick5Button16, Joystick5Button17, Joystick5Button18, Joystick5Button19, Joystick6Button0, Joystick6Button1, Joystick6Button2, Joystick6Button3, Joystick6Button4, Joystick6Button5, Joystick6Button6, Joystick6Button7, Joystick6Button8, Joystick6Button9, Joystick6Button10, Joystick6Button11, Joystick6Button12, Joystick6Button13, Joystick6Button14, Joystick6Button15, Joystick6Button16, Joystick6Button17, Joystick6Button18, Joystick6Button19, Joystick7Button0, Joystick7Button1, Joystick7Button2, Joystick7Button3, Joystick7Button4, Joystick7Button5, Joystick7Button6, Joystick7Button7, Joystick7Button8, Joystick7Button9, Joystick7Button10, Joystick7Button11, Joystick7Button12, Joystick7Button13, Joystick7Button14, Joystick7Button15, Joystick7Button16, Joystick7Button17, Joystick7Button18, Joystick7Button19, Joystick8Button0, Joystick8Button1, Joystick8Button2, Joystick8Button3, Joystick8Button4, Joystick8Button5, Joystick8Button6, Joystick8Button7, Joystick8Button8, Joystick8Button9, Joystick8Button10, Joystick8Button11, Joystick8Button12, Joystick8Button13, Joystick8Button14, Joystick8Button15, Joystick8Button16, Joystick8Button17, Joystick8Button18, Joystick8Button19, F16, F17, F18, F19, F20, F21, F22, F23, F24
Inventory Search - Keyboard/Mouse = Mouse2

## Hold this key down when performing a search to invert the default behavior of focusing the camera on the nearest search result.
## Note: Gamepad uses the standard alt-function button as defined in on the in game controls screen and can not be changed.
# Setting type: KeyCode
# Default value: LeftShift
# Acceptable values: None, Backspace, Tab, Clear, Return, Pause, Escape, Space, Exclaim, DoubleQuote, Hash, Dollar, Percent, Ampersand, Quote, LeftParen, RightParen, Asterisk, Plus, Comma, Minus, Period, Slash, Alpha0, Alpha1, Alpha2, Alpha3, Alpha4, Alpha5, Alpha6, Alpha7, Alpha8, Alpha9, Colon, Semicolon, Less, Equals, Greater, Question, At, LeftBracket, Backslash, RightBracket, Caret, Underscore, BackQuote, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z, LeftCurlyBracket, Pipe, RightCurlyBracket, Tilde, Delete, Keypad0, Keypad1, Keypad2, Keypad3, Keypad4, Keypad5, Keypad6, Keypad7, Keypad8, Keypad9, KeypadPeriod, KeypadDivide, KeypadMultiply, KeypadMinus, KeypadPlus, KeypadEnter, KeypadEquals, UpArrow, DownArrow, RightArrow, LeftArrow, Insert, Home, End, PageUp, PageDown, F1, F2, F3, F4, F5, F6, F7, F8, F9, F10, F11, F12, F13, F14, F15, Numlock, CapsLock, ScrollLock, RightShift, LeftShift, RightControl, LeftControl, RightAlt, LeftAlt, RightCommand, RightMeta, RightApple, LeftCommand, LeftMeta, LeftApple, LeftWindows, RightWindows, AltGr, Help, Print, SysReq, Break, Menu, WheelUp, WheelDown, Mouse0, Mouse1, Mouse2, Mouse3, Mouse4, Mouse5, Mouse6, JoystickButton0, JoystickButton1, JoystickButton2, JoystickButton3, JoystickButton4, JoystickButton5, JoystickButton6, JoystickButton7, JoystickButton8, JoystickButton9, JoystickButton10, JoystickButton11, JoystickButton12, JoystickButton13, JoystickButton14, JoystickButton15, JoystickButton16, JoystickButton17, JoystickButton18, JoystickButton19, Joystick1Button0, Joystick1Button1, Joystick1Button2, Joystick1Button3, Joystick1Button4, Joystick1Button5, Joystick1Button6, Joystick1Button7, Joystick1Button8, Joystick1Button9, Joystick1Button10, Joystick1Button11, Joystick1Button12, Joystick1Button13, Joystick1Button14, Joystick1Button15, Joystick1Button16, Joystick1Button17, Joystick1Button18, Joystick1Button19, Joystick2Button0, Joystick2Button1, Joystick2Button2, Joystick2Button3, Joystick2Button4, Joystick2Button5, Joystick2Button6, Joystick2Button7, Joystick2Button8, Joystick2Button9, Joystick2Button10, Joystick2Button11, Joystick2Button12, Joystick2Button13, Joystick2Button14, Joystick2Button15, Joystick2Button16, Joystick2Button17, Joystick2Button18, Joystick2Button19, Joystick3Button0, Joystick3Button1, Joystick3Button2, Joystick3Button3, Joystick3Button4, Joystick3Button5, Joystick3Button6, Joystick3Button7, Joystick3Button8, Joystick3Button9, Joystick3Button10, Joystick3Button11, Joystick3Button12, Joystick3Button13, Joystick3Button14, Joystick3Button15, Joystick3Button16, Joystick3Button17, Joystick3Button18, Joystick3Button19, Joystick4Button0, Joystick4Button1, Joystick4Button2, Joystick4Button3, Joystick4Button4, Joystick4Button5, Joystick4Button6, Joystick4Button7, Joystick4Button8, Joystick4Button9, Joystick4Button10, Joystick4Button11, Joystick4Button12, Joystick4Button13, Joystick4Button14, Joystick4Button15, Joystick4Button16, Joystick4Button17, Joystick4Button18, Joystick4Button19, Joystick5Button0, Joystick5Button1, Joystick5Button2, Joystick5Button3, Joystick5Button4, Joystick5Button5, Joystick5Button6, Joystick5Button7, Joystick5Button8, Joystick5Button9, Joystick5Button10, Joystick5Button11, Joystick5Button12, Joystick5Button13, Joystick5Button14, Joystick5Button15, Joystick5Button16, Joystick5Button17, Joystick5Button18, Joystick5Button19, Joystick6Button0, Joystick6Button1, Joystick6Button2, Joystick6Button3, Joystick6Button4, Joystick6Button5, Joystick6Button6, Joystick6Button7, Joystick6Button8, Joystick6Button9, Joystick6Button10, Joystick6Button11, Joystick6Button12, Joystick6Button13, Joystick6Button14, Joystick6Button15, Joystick6Button16, Joystick6Button17, Joystick6Button18, Joystick6Button19, Joystick7Button0, Joystick7Button1, Joystick7Button2, Joystick7Button3, Joystick7Button4, Joystick7Button5, Joystick7Button6, Joystick7Button7, Joystick7Button8, Joystick7Button9, Joystick7Button10, Joystick7Button11, Joystick7Button12, Joystick7Button13, Joystick7Button14, Joystick7Button15, Joystick7Button16, Joystick7Button17, Joystick7Button18, Joystick7Button19, Joystick8Button0, Joystick8Button1, Joystick8Button2, Joystick8Button3, Joystick8Button4, Joystick8Button5, Joystick8Button6, Joystick8Button7, Joystick8Button8, Joystick8Button9, Joystick8Button10, Joystick8Button11, Joystick8Button12, Joystick8Button13, Joystick8Button14, Joystick8Button15, Joystick8Button16, Joystick8Button17, Joystick8Button18, Joystick8Button19, F16, F17, F18, F19, F20, F21, F22, F23, F24
Search Result - Focus Camera Toggle = LeftShift

## After searching for an item the camera will be focused on the nearest search result.
## If this is false it will not move the camera.
## Whatever this setting is Search Result - Focus Camera Toggle will invoke the opposite behavior when pressed.
# Setting type: Boolean
# Default value: true
Search Result - Focus Camera Default = true

```

---
### Like My Mods? Donations Welcome

`Bitcoin`

<img alt="Donation QR" src="https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/BTC_QR.png?raw=true" width=180>
