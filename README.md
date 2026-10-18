# Programmed Color-Coded Row Operation Simulator

An offline, installable app for practising **Gauss-Jordan elimination** (Grade 11 Finite Mathematics), built from *Annex 6: Programmed Color-Coded Row Operation Simulator (Student User Guide)*.

You compute every new row. The simulator checks it, **finds why a wrong answer is wrong, solves the step correctly and explains it using the Annex 6 error-check prompts**.

## Features
- Color **and** symbol key for rows (R1 red ●, R2 blue ■, R3 green ▲, R4 orange ◆), so it works for learners with color-vision difficulty
- Operation panel in R-notation (swap, multiply, add) that rejects invalid moves
- Instant step checker that names the error type: Setup (fact), Valid operation (concept), Arithmetic and sign (operation), Copying (carelessness), Conclusion
- Worked-out correct solution, side-by-side matrices, and the failed Annex 6 prompt
- Pivot Path hint ("Which move next?") with a teacher on/off switch
- Automatic error log (Part 7) with CSV download
- "Spot the error" practice (Part 5)
- Interactive guided tutorial
- Exact fraction arithmetic; 2 to 4 equations; your own systems
- Works fully offline, no accounts, no data leaves the device

## Use it
- **Online:** open the GitHub Pages link of this repository, then use *Install app* (or the browser's "Add to Home screen" / "Install") to keep it on a phone, tablet or computer.
- **No internet at all:** download `index.html` and double-click it. It is a single self-contained file.
- **Locally with install support:** `python3 -m http.server 8000` in this folder, then open http://localhost:8000

## Publish on GitHub Pages
1. Create a repository and push this folder to the `main` branch.
2. In the repository: **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. The included workflow (`.github/workflows/pages.yml`) deploys on every push. Your site will be at `https://<username>.github.io/<repository>/`.

## Updating
Edit `index.html`, then change `VERSION` in `sw.js` (for example `row-ops-v2`) so installed copies pick up the update.

## Files
| File | Purpose |
|---|---|
| `index.html` | The whole simulator (HTML, CSS, JavaScript) |
| `manifest.webmanifest` | Makes it installable |
| `sw.js` | Offline cache |
| `icons/` | App icons |
| `.github/workflows/pages.yml` | Automatic GitHub Pages deployment |
