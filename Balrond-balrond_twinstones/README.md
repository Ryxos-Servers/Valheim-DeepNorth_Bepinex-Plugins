# ⚒️ Balrond TwinStones

---

## Overview

This mod adds a new buildable **Teleport Obelisk** to Valheim.

Teleport Obelisks can be linked together in pairs. Once two obelisks are connected, a player can use one obelisk to teleport to the other one. The system is meant for **short-distance travel**, outposts, bases, mining camps and local travel networks.

Each obelisk stores its own persistent ID and linked target through ZDO data, so the connection can stay synchronized in multiplayer.

---

## 🧭 How It Works

1. Build a **Teleport Obelisk**.
2. Use **Shift + Use** on the first obelisk to start linking.
3. Go to the second obelisk and press **Shift + Use** again.
4. If the second obelisk is close enough, both obelisks become linked.
5. Press **Use** on a linked obelisk to teleport to its paired obelisk.

The default maximum link distance in the script is **50 meters**.

The default teleport cooldown is **1.5 seconds** per player.

---

## ⚙️ Features

- New buildable **Teleport Obelisk**
- Pair-based teleport system
- Two-way teleport connection
- Short-distance link limit
- Per-player pending link state
- Renameable obelisks
- Visual states for:
  - unconnected obelisk
  - pending link obelisk
  - connected obelisk
- Temporary connection effect between linked obelisks
- Multiplayer synchronization through ZDO
- Pending links are cleared on player death or disconnect

---

## 🧱 Building

- **Teleport Obelisk**


### Build Piece

The Teleport Obelisk is built using the **Stonecutter** crafting station.

Based on the build piece setup in code (piece_obeliskPortal_bal), the exact construction cost is:

**🧱 Build Cost**
Stone x10
Thunderstone x2
Greydwarf Eye x4
Iron x2

---

## 🎮 Controls

### Normal Interaction

- **Use (E)** — teleport to the linked obelisk
- **Shift + Use** — start linking, finish linking, relink, or cancel if used again on the same pending obelisk
- **Ctrl + Use** — cancel pending link or disconnect an existing link
- **Alt + Use** — rename the obelisk

---

## 🔗 Linking Instructions

### Start a Link

Press **Shift + Use** on an obelisk.

That obelisk becomes the pending source for your player.

### Complete a Link

Go to another obelisk and press **Shift + Use**.

If the obelisks are within the allowed range, they are linked together.

### Cancel a Pending Link

You can cancel a pending link by:

- pressing **Shift + Use** again on the same obelisk, or
- pressing **Ctrl + Use** while you have a pending link.

### Disconnect Linked Obelisks

Press **Ctrl + Use** on a linked obelisk.

Both sides of the connection are cleared.

### Rename an Obelisk

Press **Alt + Use** to open the name input.

The name limit is **32 characters**.

---

## 🚪 Teleporting

Once two obelisks are linked, press **Use (E)** on either obelisk to teleport to the other one.

The destination position uses the target obelisk exit point if one exists. Otherwise, it places the player slightly in front of the target obelisk using the script exit offset.

Default exit offset:

- Y: `0.5`
- Z: `1.5`

---

## 🚫 Exceptions & Limitations

Teleporting will not work if:

- the obelisk is not linked
- the linked target is missing, destroyed, unloaded, or invalid
- the teleport cooldown is still active

Linking will not work if:

- the second obelisk is farther than the maximum link distance
- the first pending obelisk is missing or invalid
- another player currently has that obelisk in pending link state

When a linked obelisk is destroyed, the script attempts to clear the connection on the other obelisk.

When a player dies or disconnects, their pending link state is cleared automatically.

---

## 🧪 Technical Notes

The obelisk stores these values in ZDO:

- portal ID
- linked portal ID
- portal name
- pending player ID

The plugin registers assets and build pieces through the standard Valheim / BepInEx / Harmony initialization flow.

Plugin info:
- GUID: `balrond.astafaraios.BalrondTwinStones`
- Name: `BalrondTwinStones`

---

## 🔧 Installation

1. Install **BepInEx** for Valheim.
2. Place the mod DLL into:

   `BepInEx/plugins`

3. Start the game.
4. Build a **Teleport Obelisk** and link it with another one.

---

## 🤝 Compatibility

- Multiplayer-friendly
- Uses Valheim ZDO synchronization
- Uses Harmony patches
- Compatible with most mods that do not replace the same build piece or interfere with the same teleport object behavior

Potential conflicts may happen with mods that modify:

- the same obelisk prefab
- build piece registration
- player teleport behavior
- ZNetView / ZDO ownership handling on the same objects

---

## 💬 Community & Support

Discord: https://discord.gg/Jfp8T5N7Pv  
Ko-fi: https://ko-fi.com/balrond1020

---

⚒️ Build your TwinStones and create short-distance teleport paths across Valheim!
