# PM Team Selection — Retro Arcade Character Select

A single-page, retro 8-bit arcade character-select screen for the Project Management team, built with vanilla HTML/CSS/JS (no build step, no dependencies). Fully self-contained for **GitHub Pages**.

## How this repo is structured

```
index.html                 ← the whole app (CSS + JS inline)
assets/
  photos/                  ← put each person's headshot here
  video/                   ← put Lena's video clip here
```

The page already contains **all 20 team members' data** (role, location, languages, hobbies, fun facts, etc.) pulled from `pm team.xlsx`. The only thing missing is the actual image/video files, since those currently live in a private, authenticated SharePoint folder that only works for people signed into the EquipNet tenant — which won't work for a public GitHub Pages site.

## 1. Add the photos (required for real headshots)

Download each photo from the `PMteam` SharePoint folder and save it into `assets/photos/` using **these exact lowercase filenames**:

| Person | Filename |
|---|---|
| Aaron D'Souza | `aaron.jpg` |
| Bailey Richardson | `bailey.jpg` |
| Bill Condon | `bill.jpg` |
| Crystal Carpenter | `crystal.jpg` |
| David Palacio | `david.jpg` |
| Elba Boria | `elba.jpg` |
| Joanna Kozoswist | `joanna.jpg` |
| Juliana Gutierrez Martinez | `juliana.jpeg` |
| Kevin Roman | `kevin.jpg` |
| Khyati K. | `khyati.jpg` |
| Lauren Underdown | `lauren.jpg` |
| Laurie Wilson | `laurie.jpg` |
| Lena Morano | `lena.jpg` |
| Mike Hudson | `mike.jpg` |
| Quincy Monsorate | `quincy.png` |
| Ryan Hynes | `ryan.jpg` |
| Sal Olivo | `sal.jpg` |
| Simon Smith | `simon.jpg` |
| Willie Strong | `willie.jpg` |
| Symau Tamwo | *(no photo on file — will auto-generate a retro avatar)* |

**You don't have to add every photo.** Anyone missing a file automatically gets a generated retro pixel-avatar with their initials instead of a broken image — the page never breaks.

## 2. Add Lena's video clip (optional)

Download `Lena_vid.mp4` from the SharePoint folder and save it as:
```
assets/video/lena_vid.mp4
```
If this file is missing, the page automatically falls back to Lena's static photo (or avatar) — no errors, no broken video icon.

## 3. Push to GitHub and enable Pages

1. Create a new **public** GitHub repository.
2. Upload this entire folder (`index.html` + `assets/` with your added files) to the repo root.
3. Go to **Settings → Pages**, set Source to **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
4. Your site goes live at:
   ```
   https://<your-username>.github.io/<repo-name>/
   ```

No SharePoint login, no external hosting, no server — just static files served by GitHub.

## Features recap

- CRT scanlines, neon cyan/pink/yellow glow, pixel fonts (Press Start 2P + Teko)
- Web Audio API beeps on hover/select (no audio files needed)
- Pulsing glowing SVG world map as the default background; fades to a city skyline per person's location when selected
- Left panel: compact character portrait (now sized to stay proportional on any screen, including large desktop monitors) with name, role badge, and stage location
- Right panel: full dossier — responsibilities, expertise, languages, hobby, food, fun fact, dream destination, and a 10-year tenure power gauge
- Bottom roster strip with ← → arrow-key navigation
- **Volume toggle button** appears on Lena's video clip so you can turn her sound on/off (video starts muted to satisfy browser autoplay rules — click the 🔇/🔊 button to unmute)
