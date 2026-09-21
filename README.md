# SpeakStone Forever - Main

SpeakStone's base addon for **WoW Forever** (Classic+, interface `16001`).
Plays AI-generated voiceovers for quests, books and gossip, each in the
NPC's own voice.

This is code only. Audio ships in separate pack addons
(`SpeakStone_Pack_Forever_*`), which require this one.

## Generated, not hand-maintained

Everything here is produced by `tools/build_forever_main.py` from the retail
[SpeakStone_Main](https://github.com/dandwhelan/SpeakStone_Main) payload.
Exactly three things differ from retail:

1. `## Interface: 16001`
2. `## Title: SpeakStone Forever - Main`
3. SavedVariables renamed to `SpeakStone_ForeverMainDB` (in the `.toc` and every Lua reference)

Captures made on this client are reported to the site as `flavour: "forever"`
by `Harvester.lua`, from the interface number. Quest IDs are only unique within
one game, so this is what keeps Forever quest text from merging into retail's.

Fixes belong in SpeakStone_Main; regenerate this rather than editing it.
