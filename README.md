# Color Sort — Fantasy Bottles

Polished offline-first mobile puzzle prototype inspired by the supplied reference concept.

## Included
- 20-level world map with locked/unlocked progression
- Solvable level generation by scrambling a solved state through legal pours
- Glossy glass bottles and animated liquid movement
- Custom CSS/SVG game icons (no emoji UI icons)
- Undo, hint and shuffle boosters
- Coins, three-star completion feedback and confetti
- Local progress persistence
- Responsive portrait mobile UI
- No external runtime dependencies

## Run
Open `index.html` in a modern mobile/desktop browser. For best PWA behavior, serve the folder from a local HTTPS/HTTP server rather than `file://`.

## Android packaging
The web game is structured for wrapping in a WebView/Capacitor-style Android shell. Native Android build/signing and physical-device QA should be done in an Android build environment before Play Store release.
