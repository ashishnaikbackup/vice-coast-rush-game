# Vice Coast Rush

A fast, single-file 3D arcade stunt-driving game for the browser. Blast a hypercar across an endless chain of sea-stunt decks, hit ramps, grab Vice Orbs, chain boost pads and nitro, and see how far you can get.

## Play

**https://ashishnaikbackup.github.io/vice-coast-rush-game/** (once GitHub Pages is enabled for the repo)

Or download `index.html` and open it in a modern browser (internet needed once for the Three.js CDN).

## Controls

| Action | Keys | Touch |
| --- | --- | --- |
| Gas | `W` / `↑` | GAS (right thumb) |
| Brake / reverse | `S` / `↓` | BRAKE (right thumb) |
| Steer / air pitch | `A` `D` / `←` `→` | ◀ ▶ (left thumb) |
| Drift | `Space` | BRAKE |
| Nitro | `Shift` / `E` | NITRO |
| Respawn | `R` | ↺ CP |
| Pause | `P` / `Esc` | II button |

## Features

- Endless procedurally chained decks: stunt straights, container bridges, sky pipes, neon platforms
- Launch ramps, turbo chevron boost pads, collectible Vice Orbs, checkpoints
- Drift and air-time stunt scoring, hyper-nitro, supersonic speed lines
- Rival hypercar, 5 paint finishes, 3 sky themes, Low/Med/Auto/High graphics
- Original synthwave soundtrack generated in the browser (no audio files), intensity follows your speed; music and SFX toggles
- Touch layout: steering pad under the left thumb, pedals under the right thumb, haptic feedback on supported phones
- Orb combos (up to x5) and distance milestone bonuses every 500 m
- Best score saved in your browser

## Changelog

### Update 3: smoother scenery

- Islands, yachts and ocean waves now sit in the world and stream past you (they used to travel with the car, which looked like the background was buffering)
- Auto quality no longer toggles shadows mid-run (that froze the game while shaders recompiled); it only lowers resolution after sustained low FPS
- Shaders are pre-compiled at launch; lighter ocean material

### Update 2: speed, touch, music

- About 40% slower top speed (210 km/h cruise, 290 km/h nitro) with retuned acceleration, ramps and rival
- Thumb-reach touch pads, pause button, correct keyboard legend
- Procedural synthwave soundtrack
- Orb combos, milestone bonuses, how-to line

### Update 1: playability pass

- **Fixed a crash:** `THREE.Object3D.DEFAULT_UP` does not exist in Three.js r128, so the car update threw every frame after launch.
- **Fixed frozen steering:** reversing direction left a tiny non-zero steering value that blocked the opposite input.
- **Retuned jumps:** ramps launched ~250 m against 22-34 m gaps, so cars overshot decks and dropped into the sea. One ramp now clears one gap.
- **Fairer layout:** smaller side-to-side offset between decks.
- **Self-centering car:** it straightens out when you release steering.
- **Soft guard-rails:** slide along deck edges instead of dropping off.
- **Smarter respawn:** back on the road where you last had ground, with speed to clear the next jump (old checkpoints could already be deleted, causing endless respawn loops).
- Memory leak fixed (deck geometry is now disposed), pause, saved best score, stuck-key protection.

## Tech

HTML, CSS and JavaScript in one file, Three.js r128 (CDN), procedural Web Audio. No build step.

## License

All rights reserved by the repository owner unless a license file is added. Three.js remains under its own license.
