# ZenHoverItem

Show item icons on the cursor because the human brain recognizes images much faster than it recognizes words.  Quickly identify things via the inventory item icon.

NOTE: Fireplaces and torches show remaining fuel as the number of days left instead of hours, minutes, and seconds because the game uses days as a unit of time, not clocks.

- Containers
- Smelters
- Dropped Items & Pickables
- Armor and Item Stands
- Beehives
- Fermenters
- Sap Collectors
- Ovens
- Cooking Stations
- Fireplaces
- Etc.

### Attention Mod Devs

If you would like to display icons from your own mod please visit the [wiki](https://thunderstore.io/c/valheim/p/ZenDragon/ZenHoverItem/wiki/) for instructions on how to display your own custom icon data as hover icons. Easy to integrate: no hard dependency, no API, no reflection required.

### Containers (With Item Counts)
![Screenshot Containers](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/container.jpg)

### Fuel Remaining In Days
![Screenshot Fuel Remaining](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/fuelremaining.jpg)

### Smelters Queue
![Screenshot Smelters](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/smelter.jpg)

### Dropped Items (and Pickables)
![Screenshot Item Drop](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/itemdrop.jpg)

### Beehive Honey
![Screenshot Beehive](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/beehive.jpg)

### Armor Stands
![Screenshot Armor Stand](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/armorstand.jpg)

### Item Stands
![Screenshot Item Stand](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/itemstand.jpg)

### Fermenters
![Screenshot Fermenter](https://raw.githubusercontent.com/ZenDragonX/ZenMods_Valheim/refs/heads/main/screenshots/ZenHoverItem/fermenter.jpg)


### ModDevs: Invoking Icons

If you are a mod dev you can show your own icons from your own mods:

Inside your GetHoverText patch or Update loop use Unity's SendMessage function with a list of prefab names or icon sprites that you want to display as HoverIcons.  This is not a hard dependency, it will not error if ZenHoverItem is not installed.  It simply sends a message and ZenHoverItem listens for it if it's installed, otherwise nothing happens.

```
// yourData[] can be an array of:
// - Icons: Sprite[]
// - ItemPrefabNames: string[]
// - Tuples Style 1: (Sprite Icon, string Label)[]
// - Tuples Style 2: (string ItemPrefabName, string Label)[]
// NOTE: you can put null in an array Icon or ItemPrefabName to skip a position. 
// You can not put null for the entire tuple.
// Anything beyond 5 elements will be ignored, it will not error if you go beyond the limit.

SendMessage("ZenDragon.ZenHoverItem::UpdateIcons", yourData[], SendMessageOptions.DontRequireReceiver);
```

NOTE: It will only display 5 icons max.  Anymore than that and horizontal width is ugly.  4 is the ideal soft max. Best if you keep it 4 or under.  However, 5 is there just in case.  Generally a good idea to not clutter the UI.

## Client / Server Requirements

NOTE: Technically it is *not required* on the server. However, if it is installed on the server then it will force all clients to have it installed as well. This is to enable two modes of usage:
1. Dedicated server admins can put the mod on the server to enforce all clients to have the mod installed and sync admin configs.
2. Trusted friends can agree to run the same mods and connect through a vanilla dedicated server with no enforcement but with locked admin configs.

## Client Only

This mod operates entirely client side. That means you can connect to any vanilla server with this mod installed.  Other players do not need to have the mod installed.

NOTE:  If you host a game session with this mod installed then it will be considered to be installed on the server since your session is the server. Therefor, all clients will be required to have it.  If you don't want to require all players to have this mod then you will need to host your game in a dedicated server.  You can easily download and run the Valheim Dedicated Server from Steam or host one in the cloud.

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
## Settings file was created by plugin ZenHoverItem v1.2.0
## Plugin GUID: ZenDragon.ZenHoverItem

[Armor Stand]

## [Admin] Display the hover icons for armor stands
# Setting type: Boolean
# Default value: false
Show Hover Icons = false

## [Admin] Display the hover text for armor stands
# Setting type: Boolean
# Default value: true
Show Hover Text = true

[Containers]

## [Admin] How many icons to display on containers?
# Setting type: Int32
# Default value: 4
# Acceptable value range: From 0 to 5
Max Icons = 4

## [Admin] Show the summary text for containers
# Setting type: Boolean
# Default value: true
Show Summary Text = true

## [Admin] Show the phrase "Hold to stack" on the tooltip for containers (vanilla: true)
# Setting type: Boolean
# Default value: true
Show Hold To Stack = true

## [Admin] Show a hint on non-player made containers but don't reveal their contents until you open it.
## Once you open it the contents will display on the hover icons until you leave the area.
# Setting type: Boolean
# Default value: true
Show Uncrafted As Mystery = true

[Fuel]

## [Admin] Show the hover icon for fuelable things such as fireplaces, torches, and smelters
# Setting type: FuelPieceType
# Default value: Fireplace, SmelterFuel, SmelterOre
# Acceptable values: None, Fireplace, SmelterFuel, SmelterOre
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Show Icon = Fireplace, SmelterFuel, SmelterOre

## [Admin] Show the capacity x/max for fuelable things such as fireplaces, torches, and smelters
# Setting type: FuelPieceType
# Default value: Fireplace, SmelterFuel
# Acceptable values: None, Fireplace, SmelterFuel, SmelterOre
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Show Capacity = Fireplace, SmelterFuel

## [Admin] Show the meter
# Setting type: FuelPieceType
# Default value: SmelterOre
# Acceptable values: None, Fireplace, SmelterFuel, SmelterOre
# Multiple values can be set at the same time by separating them with , (e.g. Debug, Warning)
Show Meter = SmelterOre

## [Admin] Show the queue on smelters
# Setting type: Boolean
# Default value: true
Show Smelter Queue = true

## [Admin] Show the number of game days of fuel remaining on Fireplaces. (Vanilla: false)
## This helps you understand the different dynamics of the various light sources and realize they are not just cosmetic.
## The game itself does not provide a clock. Vikings had no clocks. The only unit of time they had was days.
## Install ZenCompass to see the passage of time.
## NOTE: This is very important when using ZenRaids as you need to know how long before the fire burns out and monsters spawn.
## Also, in a mod like Seasons you need to know if you have enough fuel to last the winter.
# Setting type: Boolean
# Default value: true
Display Fuel Days = true

## [Admin] This will adjust the fuel burn rate on fireplaces so the amount of days remaining when full are easily recognizable numbers. (Vanilla: false)
## Vanilla day lengths and fuel burn times are not evenly divisible resulting in awkward max fuel days.
## This adjusts the burn rate per unit of fuel so they divide evenly with the day length.
## The result is that max fuel days will be easily recognizable days 20, 25, 50, 60 instead of 22, 28, 56, 67.
## [logout required for changes to take effect]
# Setting type: Boolean
# Default value: true
Adjust Fuel Burn Rate = true

[General]

## [Admin] Display hover icons on the crosshair for important pieces, such as containers (Global)
# Setting type: Boolean
# Default value: true
Show Hover Icons = true

## [Admin] Display the resources of static stacks, piles, and the treasure chest.
# Setting type: Boolean
# Default value: true
Show Stacks And Piles = true

## Hold down this key to display the total for all valuables.
## If set to None then the total is always displayed without needing to hold a key.
# Setting type: KeyCode
# Default value: LeftAlt
# Acceptable values: None, Backspace, Tab, Clear, Return, Pause, Escape, Space, Exclaim, DoubleQuote, Hash, Dollar, Percent, Ampersand, Quote, LeftParen, RightParen, Asterisk, Plus, Comma, Minus, Period, Slash, Alpha0, Alpha1, Alpha2, Alpha3, Alpha4, Alpha5, Alpha6, Alpha7, Alpha8, Alpha9, Colon, Semicolon, Less, Equals, Greater, Question, At, LeftBracket, Backslash, RightBracket, Caret, Underscore, BackQuote, A, B, C, D, E, F, G, H, I, J, K, L, M, N, O, P, Q, R, S, T, U, V, W, X, Y, Z, LeftCurlyBracket, Pipe, RightCurlyBracket, Tilde, Delete, Keypad0, Keypad1, Keypad2, Keypad3, Keypad4, Keypad5, Keypad6, Keypad7, Keypad8, Keypad9, KeypadPeriod, KeypadDivide, KeypadMultiply, KeypadMinus, KeypadPlus, KeypadEnter, KeypadEquals, UpArrow, DownArrow, RightArrow, LeftArrow, Insert, Home, End, PageUp, PageDown, F1, F2, F3, F4, F5, F6, F7, F8, F9, F10, F11, F12, F13, F14, F15, Numlock, CapsLock, ScrollLock, RightShift, LeftShift, RightControl, LeftControl, RightAlt, LeftAlt, RightCommand, RightMeta, RightApple, LeftCommand, LeftMeta, LeftApple, LeftWindows, RightWindows, AltGr, Help, Print, SysReq, Break, Menu, WheelUp, WheelDown, Mouse0, Mouse1, Mouse2, Mouse3, Mouse4, Mouse5, Mouse6, JoystickButton0, JoystickButton1, JoystickButton2, JoystickButton3, JoystickButton4, JoystickButton5, JoystickButton6, JoystickButton7, JoystickButton8, JoystickButton9, JoystickButton10, JoystickButton11, JoystickButton12, JoystickButton13, JoystickButton14, JoystickButton15, JoystickButton16, JoystickButton17, JoystickButton18, JoystickButton19, Joystick1Button0, Joystick1Button1, Joystick1Button2, Joystick1Button3, Joystick1Button4, Joystick1Button5, Joystick1Button6, Joystick1Button7, Joystick1Button8, Joystick1Button9, Joystick1Button10, Joystick1Button11, Joystick1Button12, Joystick1Button13, Joystick1Button14, Joystick1Button15, Joystick1Button16, Joystick1Button17, Joystick1Button18, Joystick1Button19, Joystick2Button0, Joystick2Button1, Joystick2Button2, Joystick2Button3, Joystick2Button4, Joystick2Button5, Joystick2Button6, Joystick2Button7, Joystick2Button8, Joystick2Button9, Joystick2Button10, Joystick2Button11, Joystick2Button12, Joystick2Button13, Joystick2Button14, Joystick2Button15, Joystick2Button16, Joystick2Button17, Joystick2Button18, Joystick2Button19, Joystick3Button0, Joystick3Button1, Joystick3Button2, Joystick3Button3, Joystick3Button4, Joystick3Button5, Joystick3Button6, Joystick3Button7, Joystick3Button8, Joystick3Button9, Joystick3Button10, Joystick3Button11, Joystick3Button12, Joystick3Button13, Joystick3Button14, Joystick3Button15, Joystick3Button16, Joystick3Button17, Joystick3Button18, Joystick3Button19, Joystick4Button0, Joystick4Button1, Joystick4Button2, Joystick4Button3, Joystick4Button4, Joystick4Button5, Joystick4Button6, Joystick4Button7, Joystick4Button8, Joystick4Button9, Joystick4Button10, Joystick4Button11, Joystick4Button12, Joystick4Button13, Joystick4Button14, Joystick4Button15, Joystick4Button16, Joystick4Button17, Joystick4Button18, Joystick4Button19, Joystick5Button0, Joystick5Button1, Joystick5Button2, Joystick5Button3, Joystick5Button4, Joystick5Button5, Joystick5Button6, Joystick5Button7, Joystick5Button8, Joystick5Button9, Joystick5Button10, Joystick5Button11, Joystick5Button12, Joystick5Button13, Joystick5Button14, Joystick5Button15, Joystick5Button16, Joystick5Button17, Joystick5Button18, Joystick5Button19, Joystick6Button0, Joystick6Button1, Joystick6Button2, Joystick6Button3, Joystick6Button4, Joystick6Button5, Joystick6Button6, Joystick6Button7, Joystick6Button8, Joystick6Button9, Joystick6Button10, Joystick6Button11, Joystick6Button12, Joystick6Button13, Joystick6Button14, Joystick6Button15, Joystick6Button16, Joystick6Button17, Joystick6Button18, Joystick6Button19, Joystick7Button0, Joystick7Button1, Joystick7Button2, Joystick7Button3, Joystick7Button4, Joystick7Button5, Joystick7Button6, Joystick7Button7, Joystick7Button8, Joystick7Button9, Joystick7Button10, Joystick7Button11, Joystick7Button12, Joystick7Button13, Joystick7Button14, Joystick7Button15, Joystick7Button16, Joystick7Button17, Joystick7Button18, Joystick7Button19, Joystick8Button0, Joystick8Button1, Joystick8Button2, Joystick8Button3, Joystick8Button4, Joystick8Button5, Joystick8Button6, Joystick8Button7, Joystick8Button8, Joystick8Button9, Joystick8Button10, Joystick8Button11, Joystick8Button12, Joystick8Button13, Joystick8Button14, Joystick8Button15, Joystick8Button16, Joystick8Button17, Joystick8Button18, Joystick8Button19, F16, F17, F18, F19, F20, F21, F22, F23, F24
Show Valuables Total = LeftAlt

[Items]

## [Admin] Display the item description when hovering over items on the ground or on stands
# Setting type: Boolean
# Default value: true
Show Item Description = true

[Plants / Crops]

## [Admin] Reformat the hover text for crops to make it look nicer (vanilla: false)
# Setting type: Boolean
# Default value: true
Reformat HoverText = true

[Shield Generator]

## [Admin] Display the power of the shield as a meter when looking at the generator
# Setting type: Boolean
# Default value: true
Show Shield Meter = true

```

---
#### Like My Mods? Donations Welcome

`Bitcoin`

<img alt="Donation QR" src="https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/BTC_QR.png?raw=true" width=180>
