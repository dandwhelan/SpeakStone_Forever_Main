# SpeakStone Forever - Main

SpeakStone's base add-on for **WoW Forever** (Classic+, interface `16001`). Quests, greetings and books are read
aloud with voices similar to the in-game characters, not a generic narrator.

Unofficial; not affiliated with Blizzard Entertainment.

Website: https://speakstone.beanw.co.uk

## What it does

SpeakStone reads World of Warcraft out loud. Open a quest, talk to an NPC or read a book, and you hear it in a voice
similar to the in-game character who says it, not one generic narrator. The same NPC keeps the same voice in their
quests, their greetings and their books.

![Welcome tutorial](docs/screenshots/01_welcome_tutorial.png)

- **Quests, greetings and books, voiced.** Quest text (description, progress, completion), NPC greetings and book pages.
- **Choose how it reads.** Full narration, story only, or manual (press Play).
  Show a compact speech bar, subtitles or nothing at all, with a portrait or a moving 3D head of the speaker.
- **Walk away and keep listening.** The speech bar carries on after you leave the NPC. Talk to someone else and their
  line waits its turn instead of cutting the first one off.
- **Read-along.** The words being spoken are highlighted as the voice reads them.
- **Pause and Resume** pick up from where you stopped.
- **Controller and TV support.** Xbox and PlayStation button prompts, big text for playing from the sofa, a rumble when
  a quest is queued, and a tutorial you can finish without a mouse.
- **Dialogue UI support.** Its play button plays SpeakStone, its text follows the voice, and quests queue or wait in combat.
- **Dyslexia-friendly fonts** (Atkinson Hyperlegible, Lexend, Andika, OpenDyslexic and more) and Parchment, Stone and
  Midnight themes.
- **The SpeakStone Guide.** Browse and play every voiced quest, greeting and book in game.
- **Help fill the gaps.** Lines with no voice yet are noted as you play, so they can be added.

| | |
|---|---|
| ![Controller and TV](docs/screenshots/02_controller_and_tv.png) | ![Choose how it reads](docs/screenshots/03_choose_how_it_reads.png) |
| Controller and TV support | Choose how it reads |
| ![Dialogue UI](docs/screenshots/04_dialogue_ui.png) | ![Walk away, keep listening](docs/screenshots/06_walk_away_keep_listening.png) |
| Dialogue UI support | Walk away, keep listening |
| ![Read-along](docs/screenshots/07_read_along.png) | ![The Guide](docs/screenshots/08_guide.png) |
| Read-along highlighting | The SpeakStone Guide |
| ![Fonts](docs/screenshots/09_reading_fonts.png) | ![Help fill the gaps](docs/screenshots/05_help_fill_the_gaps.png) |
| Dyslexia-friendly fonts and themes | Help fill the gaps |

## How it works

1. **This add-on is the player.** It holds the code, the settings, the Guide and the quest and book text, but no audio.
2. **The voice packs hold the audio.** Each pack is its own add-on (Audio Packs 1 to 3, plus Chatter for greetings) and registers its lines with this
   add-on when the game loads. Install the packs for the content you play; a line whose pack is missing is simply silent.
3. **When a quest, greeting or book opens**, SpeakStone looks the line up by quest ID and part (description, progress,
   completion), by NPC and greeting, or by book and page, and plays it if a pack has it. Long lines are stored in parts
   of about 10 to 15 seconds, cut in natural pauses, so Pause and Resume can carry on from where you stopped.
4. **Lines with no voice yet are saved as you play** (quest text, greetings and book pages, and who said them). Export
   them from the minimap button (right-click) and paste them on the [website](https://speakstone.beanw.co.uk), or let
   the free SpeakStone Worker app send them for you. New lines are usually voiced by the next day and arrive in the
   packs with their next update.

![Minimap button](docs/screenshots/10_minimap_button.png) ![/ss](docs/screenshots/11_slash_ss.png)

### Commands

| Command | What it does |
|---|---|
| `/ss` | Settings and the Guide |
| `/ss tutorial` | Run the setup tutorial again |
| `/ssauto on` or `off` | Autoplay on or off |
| `/ssmissing` | Text captured for quests with no voice, ready to paste on the website |
| `/ssharvest export` | Export everything captured (also: right-click the minimap button) |
| `/qrlibrary` | The Guide |

Minimap button: left-click opens Settings, right-click exports captured text, middle-click toggles chat messages.

## The website and the Worker

[speakstone.beanw.co.uk](https://speakstone.beanw.co.uk): paste the text you captured so it gets a voice, hear samples,
and get the Worker.

The **SpeakStone Worker** (optional, Windows and Linux) keeps your SpeakStone add-ons up to date, sends the text you
capture, and can lend your graphics card to make new lines while the PC is idle. It steps aside whenever another
program needs the card. You can also **lend your voice**: record a couple of minutes on the website and it can be used
for characters in SpeakStone. Free, a person listens to every take, and you can withdraw at any time.

| | |
|---|---|
| ![Website](docs/screenshots/12_website.png) | ![Worker setup](docs/screenshots/13_worker_setup.png) |
| The SpeakStone website | SpeakStone Worker setup |
| ![Worker board](docs/screenshots/14_worker_board.png) | ![Lend your voice](docs/screenshots/15_lend_your_voice.png) |
| The Worker at work | Lend your voice |

## Install

1. **SpeakStone Forever - Main** (this addon: code only, no audio)
2. **SpeakStone Forever Audio Pack 1** ([SpeakStone_Forever_Audio_Pack1](https://github.com/dandwhelan/SpeakStone_Forever_Audio_Pack1))
3. **SpeakStone Forever Audio Pack 2** ([SpeakStone_Forever_Audio_Pack2](https://github.com/dandwhelan/SpeakStone_Forever_Audio_Pack2))
4. **SpeakStone Forever Audio Pack 3** ([SpeakStone_Forever_Audio_Pack3](https://github.com/dandwhelan/SpeakStone_Forever_Audio_Pack3)): books
5. **SpeakStone Narration - Forever Chatter** ([SpeakStone_Forever_Chatter](https://github.com/dandwhelan/SpeakStone_Forever_Chatter)): NPC greetings and some quests

Install all five. Every audio pack requires this add-on. Without Chatter, nearly every NPC greeting is
silent, as are some quests; without Audio Pack 3, books are silent.

## Credits

Quest and dialogue text for WoW Forever is matched from community data by Efficient Games (EG Link), licensed under CC BY 4.0: https://github.com/JIVESCORP/eg-link-output-wowf

Unofficial; not affiliated with Blizzard Entertainment.

## Built from SpeakStone_Main

Everything here is produced by `tools/build_forever_main.py` from the retail
[SpeakStone_Main](https://github.com/dandwhelan/SpeakStone_Main) payload.
Exactly three things differ from retail:

1. `## Interface: 16001`
2. `## Title: SpeakStone Forever - Main`
3. SavedVariables renamed to `SpeakStone_ForeverMainDB` (in the `.toc` and every Lua reference)

Captures made on this client are reported to the site as `flavour: "forever"`
by `Harvester.lua`, from the interface number. Quest IDs are only unique within
one game, so this is what keeps Forever quest text from merging into retail's.

Fixes belong in SpeakStone_Main; rebuild this rather than editing it.

Player site: https://speakstone.beanw.co.uk
