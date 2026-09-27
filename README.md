# Gulabi Nagar

A walkable, cel-shaded, Jaipur-inspired railway neighbourhood. Explore a fictional station, bazaar and promenade in your browser. This adaptation builds on [Kenton-GMI's Sakuragaoka Station](https://github.com/Kenton-GMI/sakuragaoka-station), licensed under MIT; see [LICENSE](./LICENSE).

## Explore

```sh
npm install
npm run dev
```

Open [http://127.0.0.1:5180](http://127.0.0.1:5180). The browser loads Three.js and the Devanagari font from local files, so the game needs no external assets at runtime.

WASD or arrow keys walk, the mouse looks around, Shift runs, Space jumps, and F toggles flight. Keys 1–5 jump to the bazaar, chowk, station platform, crossing and promenade. H hides the interface, M toggles sound, and Esc releases the pointer. On touch devices, drag the left side to walk and the right side to look. The graphics selector at the top right switches quality.

The town has pink plaster façades, arched windows, rooftop chhatris, a neighbourhood mandir, a chai cart, auto-rickshaws, Indian shop signs, Hindi railway announcements, and gulmohar-coloured trees and drifting petals. The original walking, shop interiors, train timetable, crossing, synthesized sound and graphics settings remain functional. The town and railway are fictional. The scene is inspired by Jaipur, not a precise reconstruction of a real station or its rail network.

## Verify

```sh
npm run check
node tools/playtest.mjs
```

The browser playtest expects Chrome at `/Applications/Google Chrome.app/Contents/MacOS/Google Chrome` and a running server on port 5180. It checks scene loading, controls, movement, simulation updates, desktop and mobile layouts, and saves screenshots under `art/verification/`.

The source is plain Three.js ES modules. `src/world/layout.js` defines coordinates and names; `src/world/jaipur.js` adds the adapted geometry; `src/world/` contains procedural scene modules. The Devanagari font in `assets/` is licensed separately under the SIL Open Font License; see `assets/FONT-LICENSE.txt`.
