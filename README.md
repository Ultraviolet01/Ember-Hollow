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
- Touch control: hold the left or right half of the screen to run that way. Arrows in the bottom corners show which side is held.
- Plain HTML5, no build step. Upload `index.html` and `assets/` as an HTML zip on itch.io and set it to "playable in the browser".
- AI tools used: Higgsfield (Z Image for the hero, gem, rock and cave art, plus background removal) and Claude (game code).

## How to play
- Hold the left half of the screen to run left, the right half to run right. Let go and he stops.
- On a keyboard, hold the Left/Right arrow keys or A/D.
- One gem appears on the cave floor at a time. Run over it to pick it up. The next one only appears after you bank it.
- Carry one gem at a time back to the stone bank in the left cave wall. It flies into the bank and stacks up there.
- Rocks fall straight down from the top of the screen at random spots. A shadow on the floor and a trickle of grit show where one is about to come down.
- One rock on the head and the run is over instantly.

## Scoring
- Each banked gem is worth 10 points, plus more the further from the bank you grabbed it.
- Banking in a row adds a streak bonus of +2 per streak level.

## Sound
- All sound is made in code with the Web Audio API. There are no audio files.
- Background music plays the whole time: a calm cave tune on the title, shop and game over screens, and a drum-driven version during a run.
- The run music speeds up with every wave (116 bpm at wave 1, up to 176 bpm), so you hear the Speed theme as well as see it.
- Sound effects: gem pickup chime, gem clinking into the wall bank (the reward run gets higher with each streak), a crack when a rock breaks loose, a rock smash, the bonk when a rock hits the caveman, a wave fanfare, the 3-2-1 resume countdown, and a sad game over tune.
- Music and Sound have separate on/off buttons on the title screen. Both choices are saved on this device.
- Audio starts after the first tap or key press, because browsers block sound until then.

## Saved on this device
- Best wave reached (saved the moment you reach a new wave, so it survives closing the tab).
- Best haul (score), banked gems, shop upgrades and the Music and Sound settings.
- Everything is stored in the browser's local storage on this device only.

## Waves
- A new wave starts every 24 seconds.
- The floor shadow appears about 0.45 seconds before a rock comes into view (down to 0.2 in later waves), then the rock takes under a second to reach the floor.
- Each wave makes the caveman's run speed 7% faster (up to wave 11) and the rocks fall faster, more often and with less warning.
- From wave 2, two rocks can drop at once.

## Trader (shop)
- Banked gems from every run are saved and can be spent between runs.
- Keen Ears: the floor shadow warning appears 15% sooner per level (2 levels).
- Quick Feet: +8% run speed (3 levels).
- Long Arms: bigger grab range (3 levels).

## Files
- `index.html`: the whole game (HTML5 canvas, Web Audio music and sound effects, saves in the browser). No build step.
- `assets/`: art generated with Higgsfield (hero, gem, falling rock, portrait and landscape cave backgrounds).

## Run locally
- Serve the folder with any static server, for example `python3 -m http.server`, and open `index.html`.
