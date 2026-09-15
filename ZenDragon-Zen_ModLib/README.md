# Zen.ModLib

This is a core dependency, shared library for all `ZenMods`

It encapsulates common reusable functions and behaviors that are shared across all `ZenMods`

It should be included automatically by any `ZenMod` you install if you are using a package manager like R2 or Gale. If you are not using a package manager, you need to install this manually.

Generally this would be run with other `ZenMods`. However, even by itself, it applies the following: 
- Validates all the items and recipes added to the ObjectDB from any mods to make sure they are formed correctly. 
- Puts your avatar into a floating animation when you are in debug fly mode.  So that's nice.
- Configure console commands to be admin-only default to seed-related commands.
- Relay console commands through another player for server admin maintenance.

Fixes a few small vanilla bugs:
- Remove blank PlayerKeys
- Changes Player.AutoPickup's Physics.SphereOverlap to SphereOverlapNonAlloc
- Hide the ExitMenu KeyHint
- Allow TextInput while in Inventory
- Make sure the fire is actually lit under Cauldrons
- Gamepad fixes
- Config option to disable gamepad emote wheel.
- Prevent logging "Parse Error Platform User ID"
- Prevent excess stamina drain when running and transitioning into an attack.
- Allow the camera to rotate 360 while using tools with the HUD hidden.
- Fix the text on turrets: wordsClumpsTogether
- Fix ship chairs so that they correctly register as being on a ship.  Some are not correct in vanilla, such as the Raft mast or Longship bow.
- Fix wolves eat additional meats. The default adds bear and serpent meats, add others via configs.
- Fix exploit: chair wall bypass.
- Fix exploit: suppress "Too Hard" message when using Stagbreaker to find Silver.
- Fix exploit: attack animation cancelling.

Optimizations:
  - Network messages can be filtered to only send to nearby players instead of everyone on the server.
  - Dedicated servers can send to all players at once instead of spreading it out over multiple frame updates.

But you should really use this in conjunction with another `ZenMod`, because that's its intended purpose.

Learn more via the links below...

## Improve Your Experience

### [ALL ZenMods](https://thunderstore.io/c/valheim/p/ZenDragon/ZenModpack_CORE/)

The full collection of all Zen MODS:

- Radically improved QoL
- Incredible performance
- Pre-configured
- 100% Gamepad support
- Spectacularly immersive

Enjoy!
