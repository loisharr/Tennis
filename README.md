# Deuce Court

A singles tennis game built for your phone. It's one web page, with no build step and no dependencies, and it works offline once installed.

## How to play

- **Move:** drag anywhere on the screen. Your player swings by itself when the ball is in reach.
- **Aim:** the middle of your hitting zone (the ring around your feet) sends the ball straight. The edges angle it wide, and the very edge can land out.
- **Serve:** tap to toss, then tap again as the ball peaks. Tap left or right of centre to aim. Better timing means a faster, safer serve.
- On a computer, use the arrow keys or WASD to move, Space to serve, and Esc to pause.

Choose an opponent (Club, County, Tour), a match length (a 7-point tiebreak, a short set to 4 games, or a full set to 6 games) and a surface (hard, clay or grass, each with its own bounce). Scoring follows real tennis: deuce, advantage, second serves, tiebreaks, break points and match points.

## Put it on your phone

1. Host the folder anywhere static. The simplest option is GitHub Pages: go to **Settings → Pages**, choose **Deploy from a branch**, and pick this branch and `/ (root)`.
2. Open the Pages URL on your phone.
3. Add it to your home screen:
   - **iPhone (Safari):** Share → *Add to Home Screen*
   - **Android (Chrome):** ⋮ menu → *Install app* or *Add to Home screen*

It then opens full screen like a native app and keeps working without a connection.

## Files

| File | Purpose |
| --- | --- |
| `index.html` | The whole game: rendering, physics, opponent AI, scoring, menus |
| `manifest.webmanifest` | App name, icons and full-screen display for home-screen install |
| `sw.js` | Service worker that caches the game for offline play |
| `icon.svg`, `icon-192.png`, `icon-512.png` | App icons |

To run it locally, serve the folder (for example `python3 -m http.server`) and open `http://localhost:8000`.
