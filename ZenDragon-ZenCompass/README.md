# ZenCompass

Radial compass that *replaces* your minimap in the corner of your screen. 

Map icons display on the radar when you get close to them.

Designed in conjunction with the `ZenMap` mod, try them together for a truly immersive experience!

- Craftable compass item.
- Craftable sunstone item. (sun position and wind direction)
- Integrated daylight tracking ring.  The sun rises in the east and sets in the west.
- Integrated wind direction ring.
- Integrated with the ship navigation HUD.
- Disabled in dungeons, getting lost is fun!
- Designed to malfunction in the Mistlands and Snowstorms for a more immersive experience. 
- Highly optimized, no performance impact.
- Automatic removal of death pins when looting tombstone.

### Important!

The early game provides the Sunstone.  This is a primitive but useful tool you can use to figure out the wind direction and sun position.  Using the knowledge that the sun sets in the West and rises in the East, you can deduce your approximate orientation.

By default, it is configured to give the early game a sense of mystery and challenge. The player will have progression of first crafting a basic Sunstone for basic navigation using time-of-day and wind direction.  

Later the player can craft a Compass. The mod is pre-configured to require an iron nail and a level 5 workbench before you can craft the compass.  This means you will have to get to go through the swamps to get at least a little bit of iron scrap and then head into the mountains to find some obsidian to craft the level 5 workbench. However, you don't have to kill bonemass. When you finally get the compass, it will feel like a very nice reward for your progress.

If you want to receive the compass earlier, you can adjust the configs to remove the IronNails and set the workbench level requirement lower.  Additionally, you can remove the requirements for the Sunstone if you do not want to use it in the early game.  Or you can turn off all crafting requirements and make the compass permanently available depending on the level of challenge that you prefer.

NOTE: If you want a minimap in the corner of your screen, then this is not the mod for you.

### On Foot
![Screenshot Land](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenCompass/land.jpg?raw=true)

### On Ship
![Screenshot Ship](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenCompass/ship.jpg?raw=true)

### Compass Item
![Item Compass](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenCompass/item_compass.jpg?raw=true)

### Sunstone Item
![Item Sunstone](https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/screenshots/ZenCompass/item_sunstone.jpg?raw=true)

## Client / Server Requirements

NOTE: Technically it is *not required* on the server. However, if it is installed on the server then it will force all clients to have it installed as well. This is to enable two modes of usage:
1. Dedicated server admins can put the mod on the server to enforce all clients to have the mod installed and sync admin configs.
2. Trusted friends can agree to run the same mods and connect through a vanilla dedicated server with no enforcement but with locked admin configs.

## Client Only

This mod operates entirely client side. That means you can connect to any vanilla server with this mod installed.  Other players do not need to have the mod installed.

NOTE:  If you host a game session with this mod installed then it will be considered to be installed on the server since your session is the server. Therefor, all clients will be required to have it.  If you don't want to require all players to have this mod then you will need to host your game in a dedicated server.  You can easily download and run the Valheim Dedicated Server from Steam or host one in the cloud.


## Improve Your Experience

### [CORE Complete](https://thunderstore.io/c/valheim/p/ZenDragon/ZenModpack_CORE/)

The full collection of all Zen MODS:

- Radically improved QoL
- Incredible performance
- Pre-configured
- 100% Gamepad support
- Spectacularly immersive

Enjoy!

## Sample Config File

```
## Settings file was created by plugin ZenCompass v1.7.1
## Plugin GUID: ZenDragon.ZenCompass

[Appearance]

## Adjust the display scale of the compass. It has two display modes: Small and Large.
## It will be small while there are no pins on the radar and large when there are pins.
## Set your scale preference with both scenarios in mind.
## Also this compounds with the vanilla GUI scaling options found in the Settings.
# Setting type: Single
# Default value: 1
# Acceptable value range: From 0.5 to 2
Display Scale = 1

## [Admin] Show the player's facing direction (gear-arrow).
# Setting type: NavTool
# Default value: Compass
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Show Heading = Compass

## [Admin] Show the north/south arrow on the compass.
# Setting type: Boolean
# Default value: true
Show North Arrow = true

## [Admin] Show the camera's looking direction.
# Setting type: NavTool
# Default value: Compass, Sunstone
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Show Camera Direction = Compass, Sunstone

## [Admin] Track the sun with an indicator icon along the outer ring.
## The sun moves from east to west through the southern sky.
# Setting type: NavTool
# Default value: Compass, Sunstone
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Track Sun = Compass, Sunstone

## [Admin] Track the wind direction with an indicator on the outer ring.
# Setting type: NavTool
# Default value: Compass, Sunstone
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Track Wind = Compass, Sunstone

## [Admin] Oriented such that up is always the direction you are looking.
## [Disabling this on the sunstone makes the sunstone behave like a compass since it's locked to the north/south orientaiton.
## This option is only here for completeness, it is not recommended to disable it for sunstone]
# Setting type: NavTool
# Default value: Sunstone
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Rotating = Sunstone

## [Admin] The sun ring moves idependently along the outer ring, ignoring axis rotation. Right is sunrise, left is sunset.
## [This option has no effect if Rotating is disabled]
# Setting type: NavTool
# Default value: Compass
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Rotating - Sun Ring Is Time = Compass

[Behavior]

## Auto shrink the radar when there are no pins nearby.
# Setting type: Boolean
# Default value: true
Shrink When Empty = true

## [Admin] How far to scan for pins, as percentage.  Set to 0 to disable the radar function.
# Setting type: Int32
# Default value: 100
# Acceptable value range: From 0 to 300
Radar Range Percent = 100

## [Admin] Can be used inside dungeons.
# Setting type: Boolean
# Default value: false
Allow In Dungeon = false

## [Admin] List of Biome:Weather conditions that cause the compass to malfunction.
## Leave blank to disable the malfunction conditions.
## Use the keyword 'All' to apply to all biomes or weathers.
## Only one biome per entry, but a given biome can have multiple weathers.
## Use | to separate multiple weathers, example:
## Biome:Weather1|Weather2|Weather3|...
## Possible biomes: [Meadows, Swamp, Mountain, BlackForest, Plains, AshLands, DeepNorth, Ocean, Mistlands, All]
## Possible weather: https://valheim.fandom.com/wiki/Environment#Weather
# Setting type: StringList
# Default value: All:SnowStorm, Mistlands:All, Ocean:ThunderStorm|nofogts
Malfunction Conditions = All:SnowStorm, Mistlands:All, Ocean:ThunderStorm|nofogts

## [Admin] How many seconds to wait before transitioning to/from malfunction state once a condition is met.
## Set to 0 to for instant change.
## When entering a biome or a weather condition it can be helpful to wait a few seconds before malfunctioning
## That way the environment can fully transition before the compass gives out. 
## Also it helps when on a biome line so it doesn't keep switching between malfunction and normal states.
# Setting type: Single
# Default value: 15
# Acceptable value range: From 0 to 60
Malfunction Transition Delay = 15

## [Admin] Malfunctions can happen in certain environmental conditions.
## [Changing this config value will not update instantly. Malfunction Transition Delay time must expire first]
# Setting type: NavTool
# Default value: Compass, Sunstone
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Malfunction = Compass, Sunstone

## [Admin] Sun position is tracked in dark environments such as poor weather or foggy atmosphere. 
# Setting type: NavTool
# Default value: Compass, Sunstone
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Track Sun In Dark Env = Compass, Sunstone

## [Admin] The sun position is tracked at night.
## [This overrides Track Sun In Dark Env: Even if you can track the sun in poor weather, you can't track it at night.]
# Setting type: NavTool
# Default value: Compass
# Acceptable values: None, Compass, Sunstone
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Track Sun At Night = Compass

[Compatibility]

## [Admin] Reposition the Status Effect icons to make room for the compass.
## Disable this for compatibility with other mods which reposition the Status Effects.
# Setting type: Boolean
# Default value: true
Resposition Status Effects = true

## [Admin] Reposition ship power indicator HUD element (sails / rudder power)
## This mod will by default position it just to the right of the wheel for easy viewing
## Disable this for compatibility with other mods which reposition the ship power HUD element
# Setting type: Boolean
# Default value: true
Reposition Ship Power Indicator = true

[Crafting]

## [Admin] The item must be in your inventory before it can be used.
## [Disable to make the compass always available; no crafting required]
# Setting type: Boolean
# Default value: true
Craft To Use = true

## [Admin] The item must be equipped before it can be used.
## [Craft To Use must be true for this to have any effect]
## [logout required for changes to take effect]
# Setting type: Boolean
# Default value: true
Equip To Use = true

## [Admin] The compass provides cardinal directions in the day or night. 
## Additionally it can be used to tell the time of day and track wind direction.
## [restart required for changes to take effect]
# Setting type: Boolean
# Default value: true
Item Compass - Enabled = true

## [Admin] The station required to craft the compass.
## NOTE: For an easier game you can change this to a level 5 Workbench
## Thereby requiring Obsidian from the mountains, but no need to kill the Dragon or Bonemass.
## The idea is to pair this mod with ZenMap and experience the first portion of the game with no compass.
## [restart required for changes to take effect]
# Setting type: String
# Default value: ArtisanTable
# Acceptable values: None, Workbench, Forge, Stonecutter, Cauldron, ArtisanTable, BlackForge, GaldrTable, MeadKetill, FoodPreparationTable
Item Compass - Station = ArtisanTable

## [Admin] The station level required to craft the compass.
## Note: The Sunstone is available at an earlier stage of progression.
## [restart required for changes to take effect]
# Setting type: Int32
# Default value: 1
# Acceptable value range: From 1 to 5
Item Compass - Station Level = 1

## [Admin] The materials required to craft the compass, an advanced navigation aid.
## The idea is to pair this mod with ZenMap and experience the first portion of the game with no compass.
## For an easier game: 
## - Adjust the crafting station requirements.
## - Change the Iron Nail requirement to a Bronze Nail.
## - Remove the Crystal requirement and change it to BoneFragments:4
## [restart required for changes to take effect]
# Setting type: StringList
# Default value: ZenSunstone:1, FineWood:4, Crystal:2, IronNails:1
Item Compass - Materials = ZenSunstone:1, FineWood:4, Crystal:2, IronNails:1

## [Admin] A basic navigation aid. The Sunstone allows you to track the sun's position.
## [restart required for changes to take effect]
# Setting type: Boolean
# Default value: true
Item Sunstone - Enabled = true

## [Admin] The station required to craft the sunstone.
## [restart required for changes to take effect]
# Setting type: String
# Default value: Stonecutter
# Acceptable values: None, Workbench, Forge, Stonecutter, Cauldron, ArtisanTable, BlackForge, GaldrTable, MeadKetill, FoodPreparationTable
Item Sunstone - Station = Stonecutter

## [Admin] The station level required to craft the sunstone.
## [restart required for changes to take effect]
# Setting type: Int32
# Default value: 1
# Acceptable value range: From 1 to 5
Item Sunstone - Station Level = 1

## [Admin] The materials required to craft the sunstone.
## [restart required for changes to take effect]
# Setting type: StringList
# Default value: Ruby:1
Item Sunstone - Materials = Ruby:1

## [Admin] What happens to the crafted item when the player dies?
# Setting type: DeathRule
# Default value: Tombstone
# Acceptable values: Tombstone, Keep, Destroy
Player Death = Tombstone

[Death Pins]

## [Admin] Death pins will be automatically removed from the map & compass after looting the tombstone
# Setting type: Boolean
# Default value: true
Auto Remove Death Pin = true

## Normally you don't need this key. However, if you were away and someone looted your tombstone
## while your character was not there then it is possible that your Death Pin would persist even
## though the tombstone was gone. In that scenario you can stand near your pin and press this key
## to manually cleanup your map & compass.
## NOTE: The ZenMap mod automatically tracks and removes death pins reliably 100% of the time
## even if you are far away or offline and someone else loots your tombstone it will still work.
# Setting type: KeyCode
# Default value: Delete
# Acceptable values: None, Backspace, Tab, Clear, Return, Pause, Escape, Space, Exclaim, DoubleQuote, Hash, Dollar, Percent, Ampersand, Quote, LeftParen, RightParen, Asterisk, Plus, Comma, Minus, Period, Slash, Alpha0, Alpha1, Alpha2, Alpha3, Alpha4, Alpha5, Alpha6, Alpha7, Alpha8, Alpha9, Colon, Semicolon, Less, Equals, Greater, Question, At, LeftBracket, Backslash, RightBracket, Caret, Underscore, BackQuote, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z, LeftCurlyBracket, Pipe, RightCurlyBracket, Tilde, Delete, Keypad0, Keypad1, Keypad2, Keypad3, Keypad4, Keypad5, Keypad6, Keypad7, Keypad8, Keypad9, KeypadPeriod, KeypadDivide, KeypadMultiply, KeypadMinus, KeypadPlus, KeypadEnter, KeypadEquals, UpArrow, DownArrow, RightArrow, LeftArrow, Insert, Home, End, PageUp, PageDown, F1, F2, F3, F4, F5, F6, F7, F8, F9, F10, F11, F12, F13, F14, F15, Numlock, CapsLock, ScrollLock, RightShift, LeftShift, RightControl, LeftControl, RightAlt, LeftAlt, RightCommand, RightMeta, RightApple, LeftCommand, LeftMeta, LeftApple, LeftWindows, RightWindows, AltGr, Help, Print, SysReq, Break, Menu, WheelUp, WheelDown, Mouse0, Mouse1, Mouse2, Mouse3, Mouse4, Mouse5, Mouse6, JoystickButton0, JoystickButton1, JoystickButton2, JoystickButton3, JoystickButton4, JoystickButton5, JoystickButton6, JoystickButton7, JoystickButton8, JoystickButton9, JoystickButton10, JoystickButton11, JoystickButton12, JoystickButton13, JoystickButton14, JoystickButton15, JoystickButton16, JoystickButton17, JoystickButton18, JoystickButton19, Joystick1Button0, Joystick1Button1, Joystick1Button2, Joystick1Button3, Joystick1Button4, Joystick1Button5, Joystick1Button6, Joystick1Button7, Joystick1Button8, Joystick1Button9, Joystick1Button10, Joystick1Button11, Joystick1Button12, Joystick1Button13, Joystick1Button14, Joystick1Button15, Joystick1Button16, Joystick1Button17, Joystick1Button18, Joystick1Button19, Joystick2Button0, Joystick2Button1, Joystick2Button2, Joystick2Button3, Joystick2Button4, Joystick2Button5, Joystick2Button6, Joystick2Button7, Joystick2Button8, Joystick2Button9, Joystick2Button10, Joystick2Button11, Joystick2Button12, Joystick2Button13, Joystick2Button14, Joystick2Button15, Joystick2Button16, Joystick2Button17, Joystick2Button18, Joystick2Button19, Joystick3Button0, Joystick3Button1, Joystick3Button2, Joystick3Button3, Joystick3Button4, Joystick3Button5, Joystick3Button6, Joystick3Button7, Joystick3Button8, Joystick3Button9, Joystick3Button10, Joystick3Button11, Joystick3Button12, Joystick3Button13, Joystick3Button14, Joystick3Button15, Joystick3Button16, Joystick3Button17, Joystick3Button18, Joystick3Button19, Joystick4Button0, Joystick4Button1, Joystick4Button2, Joystick4Button3, Joystick4Button4, Joystick4Button5, Joystick4Button6, Joystick4Button7, Joystick4Button8, Joystick4Button9, Joystick4Button10, Joystick4Button11, Joystick4Button12, Joystick4Button13, Joystick4Button14, Joystick4Button15, Joystick4Button16, Joystick4Button17, Joystick4Button18, Joystick4Button19, Joystick5Button0, Joystick5Button1, Joystick5Button2, Joystick5Button3, Joystick5Button4, Joystick5Button5, Joystick5Button6, Joystick5Button7, Joystick5Button8, Joystick5Button9, Joystick5Button10, Joystick5Button11, Joystick5Button12, Joystick5Button13, Joystick5Button14, Joystick5Button15, Joystick5Button16, Joystick5Button17, Joystick5Button18, Joystick5Button19, Joystick6Button0, Joystick6Button1, Joystick6Button2, Joystick6Button3, Joystick6Button4, Joystick6Button5, Joystick6Button6, Joystick6Button7, Joystick6Button8, Joystick6Button9, Joystick6Button10, Joystick6Button11, Joystick6Button12, Joystick6Button13, Joystick6Button14, Joystick6Button15, Joystick6Button16, Joystick6Button17, Joystick6Button18, Joystick6Button19, Joystick7Button0, Joystick7Button1, Joystick7Button2, Joystick7Button3, Joystick7Button4, Joystick7Button5, Joystick7Button6, Joystick7Button7, Joystick7Button8, Joystick7Button9, Joystick7Button10, Joystick7Button11, Joystick7Button12, Joystick7Button13, Joystick7Button14, Joystick7Button15, Joystick7Button16, Joystick7Button17, Joystick7Button18, Joystick7Button19, Joystick8Button0, Joystick8Button1, Joystick8Button2, Joystick8Button3, Joystick8Button4, Joystick8Button5, Joystick8Button6, Joystick8Button7, Joystick8Button8, Joystick8Button9, Joystick8Button10, Joystick8Button11, Joystick8Button12, Joystick8Button13, Joystick8Button14, Joystick8Button15, Joystick8Button16, Joystick8Button17, Joystick8Button18, Joystick8Button19, F16, F17, F18, F19, F20, F21, F22, F23, F24
Key - Force Remove Death Pin = Delete

```

---
### Like My Mods? Donations Welcome

`Bitcoin`

<img alt="Donation QR" src="https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/BTC_QR.png?raw=true" width=180>
