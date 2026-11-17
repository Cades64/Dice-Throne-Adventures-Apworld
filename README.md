# Dice Throne Adventures — Archipelago Manual APWorld

Manual randomizer integration for **Dice Throne Adventures** for use with [Archipelago](https://archipelago.gg/).

**Creator:** Cades64  
**Game name in multiworld:** `Manual_DiceThroneAdventures_Cades64`  
**File:** `manual_dicethroneadventures_cades64.apworld`

---

## What this is

This is a **Manual** world: Archipelago randomizes items and locations, and you track progress in the **Manual client**. You decide when checks are done and which unlocked abilities the table actually uses. It does not mod or automate the physical game.

Works for solo or multiplayer Adventures at the same table (or remote, if everyone’s on the same multiworld).

---

## Requirements

- [Archipelago](https://archipelago.gg/) (recent stable recommended)
- This `.apworld` installed
- The **Manual client** (from the Archipelago launcher / Manual project) for your player slot
- Dice Throne Adventures (and any expansions you enable in the options)

---

## Install

1. Download `manual_dicethroneadventures_cades64.apworld`.
2. Place it in Archipelago’s **custom worlds** folder  
   (e.g. Windows: `C:\ProgramData\Archipelago\custom_worlds\` — exact path depends on your install).
3. Restart the Archipelago launcher / generator if it was already open.
4. Generate a seed as usual. Your game should appear as **Manual_DiceThroneAdventures_Cades64**.
5. Connect with the **Manual client** for that slot.

**After every apworld update, generate a new seed.** Old rooms may not match the new package.

---

## Goals (End Objective)

| Goal | Notes |
|------|--------|
| Campaign | Main campaign clear |
| Campaign (Stupid Edition) | Harder campaign variant |
| One Shot Map | One-shot map clear |
| One Shot Map (Stupid Edition) | Harder one-shot |
| Minion Rush | Minion rush clear |
| Minion Rush (Stupid Edition) | Harder minion rush |

Pick one in the YAML / player options under the end objective / goal setting.

---

## Important options

### Character abilities

| Option | Default | What it does |
|--------|---------|----------------|
| **Randomize Character Abilities** | On | Puts abilities into the randomizer |
| **Abilities in Pool** | 9 (range 0–18) | How many abilities each player gets. **0** = no ability randomization and no starting ability |
| **Enforce Unique Board Positions** | On | At most one ability per board **slot**, so two cards don’t fight for the same position (e.g. Pick Axe vs Tithe). Turn **off** to allow any mix |
| **Preferred Starting Board** | Any | If set to a character, your **starting** ability is from that board (forced in if needed). **Any** = random among your selected abilities |

Each player gets their own set of abilities in the pool and **one starting ability** so the game is playable immediately. Who uses which unlocked ability at the table is up to the group.

### Character boards & mythics

Toggles for each hero board and mythic card (order matches the Adventures line, e.g. Barbarian → … → Sun Elf). Disable boards you don’t own or don’t want in the pool.

### Expansions (off by default)

| Option | Default | Content |
|--------|---------|---------|
| **Include Unchained Expansion** | Off | Unchained enemies, boss cards, Scenario ?, etc. |
| **Include Legacy Content** | Off | Legacy minions, tiles (e.g. Colosseum, Poison sprout), etc. |

Turn these on only if everyone has that content.

### Other

- **Death Link** — optional; follow your group’s preference  
- **Trap percentage / randomize traps** — replaces some filler with traps (see list below)  
- Category toggles (tiles, minion defeats, boss loot, scenarios, etc.) — include or exclude whole check types  

---

## Traps

When a trap is received, resolve it on the table:

| Trap | Effect |
|------|--------|
| Level I–IV Minion Trap | Spawn that level minion on the **active** player (wait until the current battle ends if needed) |
| Entangle Trap | All players get Entangle |
| Bleed Trap | All players get 2 Bleed tokens |
| Poison Trap | All players get a Poison token |
| Whither Trap | All players get 2 Whither |
| Weakness Trap | One player gets Entangle, Hex, Silence, and 1 Whither |
| Stun Trap | The next time a minion would attack, it also inflicts Stun |
| Burn Trap | Two players (if able) get Burn |

---

## Multiplayer notes

- Each Archipelago slot playing this world gets its **own** ability pool and starting ability.
- Ability **names** are shared (not “Player 1 only” items). The table decides who equips what when something is unlocked.
- Expansions and boards should match what the group actually owns.

---

## Updating

1. Replace the old `.apworld` with the new one in `custom_worlds`.
2. Restart launcher/generator if needed.
3. **Generate a new seed** — do not reuse old rooms after an update.

---

## Known limits

- This is **Manual**: no automatic detection of in-game state; you mark checks and honor item unlocks.
- More product lines (Santa vs Krampus, Marvel, promos, Santa’s Workshop, Nexus, future content, etc.) are **not** fully modeled yet; expect more toggles in later versions.
- Some expansion names were normalized for spelling (e.g. double bound, Black wurm, Poison sprout, Colosseum).

---

## Credits

- **Archipelago** — multiworld randomizer framework  
- **Manual for Archipelago** — Manual apworld template and client  
- **Dice Throne Adventures** — © its respective owners; this is a fan project for use with Archipelago, not an official product  

---

## Feedback / bugs

Report issues with: Archipelago version, whether Unchained/Legacy were on, ability options used, and single vs multiplayer.
