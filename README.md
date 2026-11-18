# Vice Coast Rush

A fast, single-file 3D arcade stunt-driving game for the browser. Blast a hypercar across an endless chain of sea-stunt decks, hit ramps, grab Vice Orbs, chain boost pads and nitro, and see how far you can get.

## Play

**https://ashishnaikbackup.github.io/vice-coast-rush/** (once GitHub Pages is enabled for the repo)

Or download `index.html` and open it in a modern browser (internet needed once for the Three.js CDN).

## Controls

| Action | Keys | Touch |
| --- | --- | --- |
| Steer / air pitch | `A` `D` / arrows | on-screen arrows |
| Gas / brake | `W` `S` | GAS / BRAKE |
| Drift | `Space` | BRAKE |
| Nitro | `Shift` / `E` | NITRO |
| Respawn | `R` | ↺ CP |
| Pause | `P` / `Esc` | — |

## Features

- Endless procedurally chained decks: stunt straights, container bridges, sky pipes, neon platforms
- Launch ramps, turbo chevron boost pads, collectible Vice Orbs, checkpoints
- Drift and air-time stunt scoring, hyper-nitro, supersonic speed lines
- Rival hypercar, 5 paint finishes, 3 sky themes, Low/Med/Auto/High graphics
- Best score saved in your browser

## Changelog (playability pass)

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
