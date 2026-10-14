# ⚒️ Balrond TwinStones

Balrond TwinStones adds a buildable **Teleport Obelisk** to Valheim, allowing you to create paired short-distance teleport connections between locations.

Use TwinStones to connect nearby bases, outposts, mining camps, workshops, docks, farms, or other places where a full portal network would be unnecessary.

---

## ✨ Features

- Buildable **Teleport Obelisk**
- Pair two obelisks together for two-way travel
- Configurable maximum linking distance
- Configurable construction cost
- Rename individual obelisks
- Visual states for unlinked, pending, and connected stones
- Connection effects between linked obelisks
- Multiplayer support
- Server-synchronized gameplay configuration
- External JSON translation support

---

## 🧱 Building the Teleport Obelisk

The **Teleport Obelisk** is built with a **Stonecutter** and appears in the build menu.

### Default Build Cost

| Material | Amount |
|---|---:|
| Stone | 10 |
| Thunderstone | 2 |
| Greydwarf Eye | 4 |
| Iron | 2 |

The construction cost can be changed in the mod configuration.

---

## 🔗 How to Link TwinStones

1. Build two **Teleport Obelisks**.
2. Hold **Shift** and press **Use** on the first obelisk.
3. Go to the second obelisk.
4. Hold **Shift** and press **Use** again.
5. If both stones are within the allowed linking distance, they become paired.
6. Press **Use** on either linked obelisk to teleport to the other one.

By default, TwinStones can be linked up to **50 meters** apart.

---

## 🎮 Controls

| Input | Action |
|---|---|
| **Use (E)** | Teleport through a linked TwinStone |
| **Shift + Use** | Start or complete a link; use again on the same pending stone to cancel |
| **Ctrl + Use** | Cancel a pending link or disconnect an existing pair |
| **Alt + Use** | Rename the obelisk |

Obelisk names can contain up to **32 characters**.

---

## 🚪 Teleporting

Once two TwinStones are linked, simply press **Use** on either one to travel to its paired stone.

Teleporting will not work when:

- the obelisk is not linked,
- the linked TwinStone no longer exists or is currently unavailable,
- the short teleport cooldown is still active.

Destroying a linked TwinStone will attempt to clear the connection on its paired stone as well.

Pending links are automatically cleared when the player dies or disconnects.

---

## ⚙️ Configuration

The configuration file is created after the game is launched with the mod installed.

Default location:

```text
BepInEx/config/balrond.astafaraios.BalrondTwinStones.cfg
```

You can edit the file manually while the game is closed, or use a compatible BepInEx configuration manager.

### Available Settings

| Section | Setting | Default | Description |
|---|---|---:|---|
| `Server` | `LockConfiguration` | `true` | Locks synchronized gameplay settings to the host/server values. |
| `Portal` | `MaxLinkDistance` | `50` | Maximum distance in meters between two TwinStones when linking them. |
| `Portal` | `BuildRecipe` | `Stone:10,Thunderstone:2,GreydwarfEye:4,Iron:2` | Construction cost of the Teleport Obelisk. |
| `Diagnostics` | `AudioDebugLogging` | `false` | Enables additional audio diagnostic logging. This setting is local and is not synchronized. |

### Changing the Build Recipe

`BuildRecipe` uses Valheim prefab names in this format:

```text
PrefabName:Amount,PrefabName:Amount
```

Default:

```text
Stone:10,Thunderstone:2,GreydwarfEye:4,Iron:2
```

For example:

```text
Stone:20,GreydwarfEye:10,Iron:5
```

Use valid item prefab names rather than translated display names.

---

## 🌐 Multiplayer & Server Configuration

TwinStones automatically synchronizes its gameplay configuration in multiplayer.

The **host/server configuration is authoritative** for synchronized settings such as:

- `MaxLinkDistance`
- `BuildRecipe`

When `LockConfiguration = true`, connected clients use the host/server values and cannot override those synchronized settings with different local values.

For a dedicated server, configure TwinStones in the server's own BepInEx configuration folder. Players connecting to that server will receive the synchronized gameplay settings automatically.

`AudioDebugLogging` is intentionally local and can be enabled independently by each player for troubleshooting.

---

## 🌍 Translations

TwinStones supports external JSON translation files.

Translation files are loaded from:

```text
BepInEx/config/BalrondTwinStones-translation/
```

The folder is created automatically when the mod runs.

Create one `.json` file for each language you want to provide. The filename should match the Valheim language name, for example:

```text
English.json
German.json
Polish.json
```

Translation files use a simple key/value JSON format:

```json
{
  "tag_linked": "Linked",
  "tag_not_linked": "Not linked",
  "tag_link_started": "Link started",
  "tag_disconnected": "Disconnected"
}
```

If a translation for the currently selected language is not available, TwinStones falls back to **English** when an English translation file is available.

This makes it possible to add or update translations without modifying the mod itself.

---

## 🔧 Installation

1. Install **BepInEx** for Valheim.
2. Place Balrond TwinStones in your `BepInEx/plugins` folder.
3. Start Valheim.
4. Build two **Teleport Obelisks** and link them together.

For multiplayer, install the mod on the server/host and on connecting clients.

---

## 🤝 Compatibility

Balrond TwinStones is designed for multiplayer and uses Valheim's normal network synchronization for its placed objects.

Potential conflicts may occur with mods that directly modify the same Teleport Obelisk prefab, replace build-piece registration, or heavily alter player teleport behavior.

---

## 💬 Community & Support

Discord: https://discord.gg/Jfp8T5N7Pv  
Ko-fi: https://ko-fi.com/balrond1020

---

⚒️ **Build your TwinStones, link them together, and create convenient short-distance travel routes across Valheim.**
