# Pipe Merge

A mobile-first merge game with low-poly smoking gear. Slide an item up the 3D table, it sticks where it lands, and two matching items merge into the next tier.

**Tiers:** Papers → One-hitter → Spoon pipe → Bowl → Bubbler → Bong → Hookah → Dab rig

## How to play
- Drag left or right at the bottom to aim, release to launch.
- Two matching items touching (or nearly touching) merge into the next tier.
- Each level has a goal item and a shot limit. Clear it to bank your score plus a bonus into your stash.
- **Collect** banks your current score without ending the level. If the table fills or you run out of shots, unbanked score is lost.
- Spend your stash in the **Shop** on backdrops, table tops, item skins and launch trails.

## Run it
It's a single static page with no build step and no dependencies.

```bash
# open index.html directly, or serve the folder:
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy with GitHub Pages
1. Push this folder to a GitHub repo.
2. In the repo, go to **Settings → Pages**.
3. Set the source to your main branch, root folder, and save.
4. Your game will be live at `https://<your-username>.github.io/<repo-name>/`.

Open that link on your phone and use **Add to Home Screen** to install it. The icon and offline support come from `manifest.webmanifest` and `sw.js`.

## Files
| File | Purpose |
| --- | --- |
| `index.html` | The whole game (canvas, physics, shop, rendering) |
| `manifest.webmanifest` | Install metadata for Add to Home Screen |
| `sw.js` | Offline caching. Bump `CACHE` when you change files |
| `icon-*.png`, `apple-touch-icon.png`, `favicon.png` | App icons |

## Saves
Progress (level, stash, shop purchases) is stored in your browser's `localStorage`, so it stays on the device you play on.
