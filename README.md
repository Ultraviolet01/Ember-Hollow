# Ember Hollow

An original 2D cave arcade game. Grab the gems on the cave floor, stash them in the bank on the cave wall, and dodge the rocks falling from the ceiling.

## Slapjam #2

Made for [Slapjam #2](https://itch.io/jam/slapjam-ai-2).

### How Ember Hollow fits the theme: Speed
- Every wave speeds up both the caveman and the falling rocks.
- Each rock gives a split-second warning, so every gem run is a narrow escape.
- You are always choosing between grabbing a gem fast and staying alive.

### Jam rules (from the jam page)
- Theme: Speed.
- Build window: 48 hours, October 29 15:00 UTC to October 31 15:00 UTC (2026).
- Format: mobile portrait browser game, aiming for 720x1280.
- Must work with touch controls and be playable in the browser on itch.io.
- Submit through the jam page before the deadline. Zip-only submissions and externally hosted playable builds are not allowed.
- Builds cannot be updated after the deadline, not even to fix a game-breaking bug.
- AI tools must be used as part of making the game. Code, art, music, voices and 3D are all allowed.
- Tick every tool you actually used in the optional tools checklist. A blank answer counts as unreported.
- Every entry needs a valid email in the private prize-contact field. Never post email or payment details publicly.
- Solo, teams and multiple entries are allowed. English descriptions are recommended.
- Judging: Fun, Visual Appeal and Theme Following, weighted equally. Judged by hosts and approved judges until November 7, 2026, 15:00 UTC.
- Prizes: $500 / $200 / $100 / $100 / $100, plus a $100 Best Game Hosted on Rosebud award (the game must also be published and playable on Rosebud).

### How this build meets them
- Portrait 720x1280 game world, scaled to fit any phone screen.
- One-touch control: tap anywhere to turn around.
- Plain HTML5, no build step. Upload `index.html` and `assets/` as an HTML zip on itch.io and set it to "playable in the browser".
- AI tools used: Higgsfield (Z Image for the hero, gem, rock and cave art, plus background removal) and Claude (game code).

## How to play
- Your caveman runs on his own.
- Tap, click or press Space to turn around. Arrow keys also set direction.
- One gem appears on the cave floor at a time. Run over it to pick it up. The next one only appears after you bank it.
- Carry one gem at a time back to the stone bank in the left cave wall. It flies into the bank and stacks up there.
- Rocks break off the ceiling at random spots. Each rock first appears hanging from the ceiling, shaking, with grit falling and a shadow growing on the floor, then it drops.
- One rock on the head and the run is over instantly.

## Scoring
- Each banked gem is worth 10 points, plus more the further from the bank you grabbed it.
- Banking in a row adds a streak bonus of +2 per streak level.

## Saved on this device
- Best wave reached (saved the moment you reach a new wave, so it survives closing the tab).
- Best haul (score), banked gems and shop upgrades.
- Everything is stored in the browser's local storage on this device only.

## Waves
- A new wave starts every 24 seconds.
- Rocks hang for about 0.75 seconds (down to 0.4 in later waves), then hit the floor in under half a second.
- Each wave makes the caveman run 7% faster (up to wave 11) and the rocks fall faster, more often and with less warning.
- From wave 2, two rocks can drop at once.

## Trader (shop)
- Banked gems from every run are saved and can be spent between runs.
- Keen Ears: rock warnings start 15% sooner per level (2 levels).
- Quick Feet: +8% run speed (3 levels).
- Long Arms: bigger grab range (3 levels).

## Files
- `index.html`: the whole game (HTML5 canvas, synthesised sound, saves in the browser). No build step.
- `assets/`: art generated with Higgsfield (hero, gem, falling rock, portrait and landscape cave backgrounds).

## Run locally
- Serve the folder with any static server, for example `python3 -m http.server`, and open `index.html`.
