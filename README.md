# Color Sort - HTML5 game

## Run it
Open `index.html` in a browser (Chrome/Safari/Edge). It is one self-contained file: all art is embedded, so no server is needed.
For phones, host the file on any static host (Netlify, GitHub Pages, itch.io) and open the link.

## What's inside
- Gameplay: 100 levels in 13 themed worlds, realistic pouring (level surface, stream, splash), undo/hint/shuffle, stars, coins.
- Bottle Shop: 6 bottle shapes bought with coins. Daily reward with 7-day streak. Music, sound and haptics toggles.
- Water pouring uses your recording (`assets/pour_original.m4a`), trimmed into an intro, a seamless loop and an outro tail (`assets/pour_trimmed.wav`). Pitch rises slightly as the bottle fills. If the recording can't load, a synthesized pour sound plays instead.
- `assets/` holds the extracted sprites (bottle glass, corks, masks, ribbons, buttons, HUD) if you want to reuse them.

## Before publishing
1. Rewarded ads: the "Watch ad" flow is a placeholder. In `index.html`, replace the body of `window.showRewardedAd(onReward)` with your ad SDK and call `onReward()` when the ad completes.
2. Leaderboard: it uses Claude artifact shared storage and only works there. Outside it, the trophy shows a local score. For a public release, connect your own backend (e.g. Firebase) in `lbSubmit()` and `openLB()`.
3. Daily streak and purchases are stored in localStorage on the device, so they can be edited by players. Use a server to protect them.
4. Font: the title font loads from Google Fonts (needs internet). Bundle "Lilita One" locally for offline play.
5. App stores: wrap the page with Capacitor or Cordova to make an Android/iOS app (also adds real haptics on iOS and native ad SDKs).
