# ZenPath

Run on paths using less stamina.

- Dirt paths drain half stamina
- Paved paths drain no stamina.
- Does not change run speed on paths.
- Reduce movement speed on snow.
- Very optimized.

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


### Sample Config File

```
## Settings file was created by plugin ZenPath v0.4.1
## Plugin GUID: ZenDragon.ZenPath

[General]

## [Admin] Stamina drain percent when running on dirt, wood, or metal (Vanilla: 1)
# Setting type: Single
# Default value: 0.5
# Acceptable value range: From 0 to 1
Stamina Usage Path = 0.5

## [Admin] Stamina drain percent when running on a paved surface or stone. (Vanilla: 1)
# Setting type: Single
# Default value: 0
# Acceptable value range: From 0 to 1
Stamina Usage Paved = 0

## [Admin] Movement speed when on snow as a percentage. (Vanilla: 1)
# Setting type: Single
# Default value: 0.75
# Acceptable value range: From 0.1 to 1
Move Speed Snow = 0.75

## [Admin] The ground is treated as snow if any of these keys are present.
## Comma separated list of global keys or per-player keys.
## NOTE: Seasons does not enable the global keys by default. Turn them on in the Seasons configs.
# Setting type: StringList
# Default value: season_winter
Ground Is Snow = season_winter

## [Admin] Display the status effect icon when running on paths
# Setting type: Boolean
# Default value: true
Show Status Icon = true

```

---
#### Like My Mods? Donations Welcome

`Bitcoin`

<img alt="Donation QR" src="https://github.com/ZenDragonX/ZenMods_Valheim/blob/main/BTC_QR.png?raw=true" width=180>
