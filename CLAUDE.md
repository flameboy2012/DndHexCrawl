# D&D Hexcrawl Campaign — Agent Guide

This repository is an **Obsidian vault** of DM notes for a D&D 5e sandbox hexcrawl campaign. There is no code; the work is writing and organising campaign notes. Players never see this vault, so spoilers are fine.

## Lore Summary

**Beha** was a yuan-ti wizard king who ruled the whole map over 2,000 years ago, when it was all sandy oasis. His sigil is a serpent devouring its own tail. He tried to become a god by slaying **Queen Nellye**, the Sidhe Queen (Fey queen and nature god), and stealing her power. **Baram, Keeper of Dragons**, came down with his dragon flight, laid waste to the kingdom and struck Beha down. Beha was buried and forgotten.

Beha's two artifacts were conduits for his power:
- **Rod of Beha** — 2ft black obsidian rod, works as a Staff of Power. It holds a **fragment of Beha** that gives helpful advice while it waits for a chance to **possess** its attuned bearer. The rod and tome are drawn to each other, like the One Ring. Only the rod can unpick the seals on Beha's corpse. **The party has it.**
- **Tome of Beha** — his spellbook: high-level spells (including _wish_) and the ascension ritual. **Lady Dice has it.**

Rumours have twisted the rod into a "staff"; only Drongo the bush wizard knows the truth.

**Lady Dice** is the main antagonist: a human divination wizard who became a lich ~200 years ago when a ritual to bind fate and protect her lover went wrong. Her soul was split; part is in a die (her phylactery). She wants Beha's power to **undo her lichdom** before her remaining humanity runs out (three strikes rule). She doesn't know about the fragment in the rod. If she gets both artifacts, Beha will possess her. Her apprentice Callus fled from the party at the Tomb of Beha.

**Other factions** (see `NPCS/Factions.md`): Captain Szolsassih's yuan-ti pirates (descendants of Beha's followers), Queen Nellye, Lady Hallowstride (vampire lord), Drongo, Baram, and Jiaolong the river dragon.

**Campaign shape:** sandbox, endgame is a battle with Lady Dice over the tome, and the ending depends on who the party sides with. Region order pushed by quest hooks: Grassland → Forest → Oasis/Swamp → Bushland → Tundra.

For full details, read `NPCS/Beha.md`, `NPCS/Lady Dice.md`, `NPCS/Factions.md`, and the `Items/` notes before writing new lore.

## Directory Structure

| Path | Contents |
| ---- | -------- |
| `Locations Key.md` | Master index: hex map image, and a table per region linking every hex note with NPC / dungeon / wilderness flags. Update it when adding a hex note. |
| `Locations/<Region>/` | One note per hex. Regions: `Forrest`, `Grassland`, `Oasis`, `Swamp`, `Mountain` (Mountain = Tundra). Images for a region sit alongside its notes. |
| `NPCS/` | NPC and faction notes. `Factions.md` is the faction overview. Images in `NPCS/Images/`. |
| `Items/` | Artifacts and notable magic items. |
| `Questions/` | Worldbuilding question files the DM answers (see Workflow). |
| `Random Encounters/` | d12 encounter table per region. Oasis uses `Oasis Random Encounters.md`. |
| `Rules/` | House rules: `Travel.md`, `Weather.md`, `Random Encounters.md`, `Exploration XP.md`. |
| `Exploration Tracker.md` / `.html` | Printable checklist of hexes explored per region. The HTML is a print version of the same tracker. |
| `TODO.md` | DM's to-do list of regions and content still to build. |
| `Hex Map.png` | The world map. |

Bushland and Jungle have no notes yet.

## Conventions

- **Hex IDs** are column letter + row number (`A9`, `F8`, `I2`). File names are `<Hex> – <Title>.md`. Most use an **en dash** (`–`), but some Swamp and Mountain notes use a hyphen (`F8 - Tomb of Beha.md`, `I2 - Castle Dice.md`). Match the existing file name exactly when linking.
- **Links** are Obsidian wikilinks: `[[Note Name]]`, `[[Note|alias]]`, `[[Note#Heading]]`. Images are embedded with `![[image.png]]`.
- **Hex note format** (Grassland/Forest style): an italic type line (`_Major Location / Dragon Lair_`), descriptive prose, then a footer like `**NPC:** … **Dungeon:** ✓ **Links:** …` or `**Tags:** …`.
- **Read-aloud text** (Oasis onward): put what the DM reads to players on first arrival in a `> [!quote] Read Aloud` callout right after the type line. Write it in second person, covering only what the party can see, hear and smell, with no secrets. Put everything else under `## DM Notes`.
- **Stat blocks** are linked to 5e.tools rather than copied (e.g. `https://5e.tools/bestiary.html#lich_mm`). Use the hash format: `bestiary.html#` + the exact 5e.tools name in lower case, with spaces as `%20` and hyphens and brackets kept, then `_` + the source (e.g. `https://5e.tools/bestiary.html#yuan-ti%20malison%20(type%201)_mm`). Items work the same way (`https://5e.tools/items.html#staff%20of%20power_dmg`). Don't use the `bestiary/<slug>.html` pages: they hang on loading. 5e.tools blocks curl behind Cloudflare, so check new links in the browser.
- **Exploration XP** is awarded per hex by tier (Early 50 / Mid 250 / Late 500, ×2 for notable sites). See `Rules/Exploration XP.md`.
- Mark ideas the DM hasn't confirmed as `_Idea (unconfirmed):_` rather than writing them as canon.

## Workflow

- **Lore questions.** To develop lore, write a question file in `Questions/` grouped by topic, with a blank `> ` answer line under each question and a suggested priority. The DM answers in the file. Then review the answers, flag contradictions with existing notes, and write the agreed lore into the relevant notes.
- **Check for conflicts.** Before writing lore, search the vault for existing mentions (e.g. `grep -ri "beha"`). Raise conflicts with the DM instead of overwriting their notes.
- **Git.** Remote is `origin` (GitHub, `main` branch). Commit and push only when the DM asks. LF→CRLF warnings on Windows are harmless.
- The `.obsidian/` folder is git-ignored; don't edit it.
