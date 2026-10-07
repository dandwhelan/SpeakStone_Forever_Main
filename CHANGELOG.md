# Changelog

## 3.1.2 (October 2026)

### Books

- **Book text stays on screen:** when a book is being read aloud and you walk away (or close it), the speech bar now
  keeps showing the text of the page being read instead of "No text for this line".

### Behind the scenes

- The addon now also notes which character model an NPC uses when you talk to them, so a new NPC's voice can be
  matched to the right race and sex without guessing. Nothing about you is recorded.

## 3.1.1 (October 2026)

### Speech bar

- **Quest queue fixes:** anything else that cuts the current quest off (a book, a gossip line, the library) now clears
  the queue too, so stale quests never start later out of nowhere, and a quest whose clip fails to play moves on to
  the next. A talking head only pauses the queue: the rest carries on once the NPC has finished speaking.
- Turning "Show all the text" on or off from `/ss` or the Options page now resizes the bar straight away.

### Settings window

- **Tidier layout:** Queue quests and Auto-accept moved to Playback. Auto-scroll and Grow sit under "Show the speech
  frame" and grey out while it's off. Capture moved to Interface, and debug messages became a small Advanced line at
  the bottom. The three link cards are now one Links card with a button per address, Export and Clear moved onto the
  Capture card, and the bottom row is just the Library buttons and Profiles. The window is shorter, and the captures
  card only lists what you've actually captured.

### Tutorial

- **Speech bar page:** shows the sample bar so you can drag it into place, pick a size and set its options. The
  tutorial moves itself off the bar while you do. The "Where things are" page now covers the bar's buttons and
  keybinds.
- **What's new:** players who already went through the tutorial get a short run (what's new, the speech bar page)
  instead of the whole thing, with a button for the full tutorial.
- **Profiles** now set the speech bar options too (Story Only queues quests; Manual turns the bar off), and there's a
  new **Subtitles** profile: extra large bar, the whole passage shown, quests queued.

### Fixes

- **Audio Library quest titles:** the built-in title list (for quests your character has never seen) was loaded but
  never read, because of a leftover name from the rename. Far fewer quests now show as "Unknown quest".
- Leftover QuestReader names inside the addon renamed to SpeakStone. The old `/qr...` commands still work.
- **Lighter on busy cities:** NPC chat lines are no longer hashed when narration isn't set to wait for NPC voices, and
  a line is checked once rather than twice when harvesting is on.

## 3.1.0 (October 2026)

### New for WoW Forever

- **The speech bar comes to WoW Forever.** Close the quest window mid-line and a bar keeps showing who is speaking and the full text, with Pause, Stop and Replay, three sizes plus Extra large, and auto-accept quests (off by default). New keybind: Pause / resume narration.

### Speech bar

- **Auto-scroll:** the text in the speech bar now scrolls along with the voice, so the line being spoken stays in
  view. Scroll with the mouse wheel to look around and it waits a few seconds before carrying on. Can be turned off
  ("Auto-scroll the speech frame text").
- **Show all the text:** a new option makes the bar grow taller to fit the whole passage instead of scrolling (very
  long text still scrolls). Off by default.
- **Extra large size** added to the bar's Size menu (gear or right-click).
- **Quest queue** (off by default, "Queue quests instead of interrupting"): talk to another quest giver while a quest
  is still being read and the new quest waits its turn instead of cutting the first one off. The bar shows where you
  are (1/2, 2/2...) and a **Next** button skips ahead. Stop clears the queue. While quests are queued, NPC greetings
  don't interrupt them and closing a gossip window doesn't stop them.
- The NPC name and quest title now sit on their own line, so the buttons no longer cover the quest name.
- All the new options are in `/ss` under "Speech frame", in the game's Options › AddOns page, and on the bar's gear
  menu.

## 3.0.0 — the big voice update (October 2026)

**Almost the whole SpeakStone library has been re-voiced.** Characters speak with far more emphasis and personality, exclamations sound natural, and sound quality is better everywhere. Voices have been checked so every NPC fits their race and sex.

### WoW Forever

- **Thousands of Forever lines refreshed** with the new, more expressive voices.
- **Quests Blizzard later rewrote now match the WoW Forever wording**, so what you hear matches what you read.
- **New WoW Forever quests voiced**, plus quests sent in by players.
- **Voice fixes:** NPCs that had a voice of the wrong sex now have the right one, and many NPCs that were silent now speak.
- Creatures and objects that speak are now narrated, and clips that started with a long silence or played much quieter than the rest have been fixed.
- Gossip now picks the right line for far more NPCs, and the Audio Library shows names for many more quests and NPCs.

### Also in 3.0.0 (folded in from the unreleased 2.0.7)

- Lots more in-game gossip and books found and voiced, a new book view for reading and listening to in-game books, a new narrator voice, and quality-of-life improvements across the add-on.

**Update all Forever packs (Audio Pack 1, Audio Pack 2 and Chatter) to 3.0.0 together** — new lines now live in the Chatter pack.

### Thank you

A huge thanks to everyone who shared their game data: AuthenticSenpai, silvy, Pappnase, illset, Benny McBackstab and Vanadan, plus everyone who contributed anonymously.
