# Foglands

**Foglands** replaces the oppressive purple particle mist in Valheim's Mistlands with a more pleasant, atmospheric fog
system. The thick, motion-sickness-inducing mist is replaced with a lighter gray fog during the day, while a Time-Based Fog system brings back denser fog at night - keeping your Demisters relevant and the biome challenging.

I made this mod because it's one that I want for my next playthrough.

Installing the mod on the server requires all clients to have it installed. It will kick them if they don't. It will also sync the configurations down to clients. Can be used client only.

## Why Foglands?

The vanilla Mistlands mist has been widely criticized for:

- Causing motion sickness and eye strain
- Being too visually oppressive (can't see anything)
- Making the Wisplight feel mandatory just to navigate
- Performance issues from the heavy particle system

Foglands attempts to address all of these while preserving the atmosphere that makes Mistlands unique.

## Comparison

### Without the mod
![Without Mod](https://i.imgur.com/zpG6fW8.png)

### With the mod
![](https://i.imgur.com/jBcAt75.png)

## Features

### Pleasant Daytime Fog

- Replaces the purple/blue mist with a neutral gray fog
- Significantly reduced particle density for better visibility
- Smaller, more transparent particles that feel like natural fog
- Better performance in Mistlands due to reduced particle count

### Time-Based Fog System

The fog intensity changes throughout the Valheim day cycle, synced with vanilla's day/night timing:

| Time of Day   | Real Time* | Fog State | Description                                          |
|---------------|------------|-----------|------------------------------------------------------|
| 04:30 - 07:30 | ~3.75 min  | **Dawn**  | Fog gradually clears as morning arrives              |
| 07:30 - 16:30 | ~11.25 min | **Day**   | Light fog - comfortable exploration, good visibility |
| 16:30 - 19:30 | ~3.75 min  | **Dusk**  | Fog gradually thickens as evening approaches         |
| 19:30 - 04:30 | ~11.25 min | **Night** | Heavy fog - reduced visibility, denser particles     |

*Based on vanilla's 30-minute day cycle and 1.5 hour transition setting

### Weather Integration

Bad weather makes the fog thicker, just like other biomes have weather-based challenges:

| Weather      | Fog Effect                        |
|--------------|-----------------------------------|
| Clear/Normal | Standard fog based on time of day |
| Rain         | 1.25x fog thickness               |
| Thunderstorm | 1.5x fog thickness                |
| Snow         | Slight fog increase               |

Weather effects stack with time-of-day effects. Avoid it if you can!

### Demister Relevance

With Foglands, your Demisters shift from "mandatory to see anything" to "the tool that beats the dangerous night fog":

- **During the day**: Demisters are optional - the fog is light enough to explore without them
- **At night**: Time-based fog brings back dense fog, and Demisters push it back just like vanilla
- **Gameplay detection**: During daytime, enemies don't get the "mist" detection bonus; at night they do (unless you're
  near a Demister)

This means you can:

- Explore freely during the day without feeling forced to carry a Wisplight
- Plan dangerous activities for daytime
- Use Demisters strategically for nighttime operations, base lighting, or aesthetics instead of need

## Configuration

All settings are server-synced and can be found in `BepInEx/config/Azumatt.Foglands.cfg`.

### Fog Settings (Section 2)

| Setting               | Default        | Description                                                                                         |
|-----------------------|----------------|-----------------------------------------------------------------------------------------------------|
| Disable Particle Mist | Off            | Set to On to completely remove all fog (not recommended). Does not work if MistBeGone is installed. |
| Fog Color (R/G/B)     | 0.45/0.45/0.50 | Fog particle color - default is neutral gray with slight blue tint                                  |

### Fog System Settings (Section 3)

| Setting                   | Default | Description                                                    |
|---------------------------|---------|----------------------------------------------------------------|
| Enable Time-Based Veil    | On      | Toggle the day/night fog cycle                                 |
| Transition Duration Hours | 1.5     | How long dawn/dusk transitions take (synced to vanilla timing) |
| Night Fog Multiplier      | 2.5     | How much thicker night fog is (1.0 = same as day)              |
| Night Fog Alpha           | 0.5     | Fog opacity at night (higher = more opaque)                    |
| Day Fog Alpha             | 0.25    | Fog opacity during the day                                     |

### Weather Settings (Section 4)

| Setting                    | Default | Description                                   |
|----------------------------|---------|-----------------------------------------------|
| Enable Weather Integration | On      | Toggle weather affecting fog thickness        |
| Storm Fog Multiplier       | 1.5     | Fog thickness multiplier during thunderstorms |
| Rain Fog Multiplier        | 1.25    | Fog thickness multiplier during rain          |

### Customization Examples

**"I want even clearer daytime fog"**

- Lower `Day Fog Alpha` to 0.15-0.20

**"I want more challenging nights"**

- Increase `Night Fog Multiplier` to 3.0-4.0
- Increase `Night Fog Alpha` to 0.6-0.7

**"I want quick transitions (short dusk/dawn)"**

- Set `Transition Duration Hours` to 0.5

**"I want gradual transitions (long dusk/dawn)"**

- Set `Transition Duration Hours` to 3.0-4.0

**"I just want vanilla fog with gray color"**

- Set `Night Fog Multiplier` to 1.0
- Set `Night Fog Alpha` and `Day Fog Alpha` to the same value

**"I don't want weather to affect fog"**

- Set `Enable Weather Integration` to Off

**"I want storms to be terrifying"**

- Increase `Storm Fog Multiplier` to 2.0-2.5

**"I want a different fog color"**

- Adjust `Fog Color Red/Green/Blue` values (0-1 range)
- Example: Greenish fog = R:0.4, G:0.5, B:0.4

## Performance

Foglands is designed to be **more performant than vanilla**:

- **Daytime**: ~40% of vanilla particle emission = significantly better performance
- **Night**: Up to ~100% of vanilla emission = similar performance
- **Max particles**: Reduced from 4000 to 2000
- **Particle lifetime**: Reduced from 5s to 4s

The performance savings come from the particle system changes.

## Compatibility

- **MistBeGone**: Since this changes how the mist looks, and a little how it works, it should be fine to use with MistBeGone. The "Disable Particle Mist" configuration option in this mod is ignored if MistBeGone is installed at the same time. This ensures the mist hiding is controlled by MistBeGone.
- **Wisplight Range Mods**: Yes, works fine with them. The mist doesn't change function.
- **Mods that change the mist**: Mods that directly change the mist or particle system might conflict. I have not tested with any, but it's possible.

## Technical Details


## Installation

1. Install [BepInEx](https://valheim.thunderstore.io/package/denikson/BepInExPack_Valheim/)
2. Place `Foglands.dll` in your `BepInEx/plugins` folder
3. Launch the game - config file will be generated on first run
4. Adjust settings to your preference


**Need Help?**

- Discord servers (see below, click images)
- Include `BepInEx/LogOutput.log` from BepInEx folder when reporting bugs in the #mod-bug-reports forum.


### Author: Azumatt

**Discord**: Azumatt#2625

**Steam**: https://steamcommunity.com/id/azumatt/

[![Odin Plus Discord](https://i.imgur.com/XXP6HCU.png)](https://discord.gg/Pb6bVMnFb2)
[![Azumatt's Discord](https://i.imgur.com/Xlcbmm9.png)](https://discord.gg/pdHgy6Bsng)