# Ember Hollow

An original 2D cave arcade game. Grab the gems on the cave floor, stash them in the bank on the cave wall, and dodge the rocks falling from the ceiling.

## How to play
- Your caveman runs on his own.
- Tap, click or press Space to turn around. Arrow keys also set direction.
- One gem appears on the cave floor at a time. Run over it to pick it up. The next one only appears after you bank it.
- Carry one gem at a time back to the stone bank in the left cave wall. It flies into the bank and stacks up there.
- Rocks break off the ceiling at random spots. Each rock first appears hanging from the ceiling, shaking, with grit falling and a shadow growing on the floor, then it drops.
- One rock on the head and the run is over instantly.

## Scoring
- Each banked gem is worth 10 points, plus more the further from the bank you grabbed it.
- Banking in a row without getting hit adds a streak bonus of +2 per streak level.

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
- `assets/`: art generated with Higgsfield (hero, gem, falling rock, cave background).

## Run locally
- Serve the folder with any static server, for example `python3 -m http.server`, and open `index.html`.
