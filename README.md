# Wortkiste

Vocabulary, verb and grammar trainer for *Spektrum Deutsch B1+*, as an installable offline web app.

This repository contains **only the app**. The book's word list (`wortkiste-buchliste.json`) is copyrighted and is **not** part of this repository or the website. You load it once on your phone, and it stays on the device.

## Files

| File | Purpose |
|---|---|
| `index.html` | The whole app |
| `sw.js` | Offline cache |
| `manifest.webmanifest` | Name and icons for "Add to Home Screen" |
| `icons/` | App icons |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |
| `.gitignore` | Keeps the word list file out of git |

## 1. Put it on GitHub Pages

```
cd C:\Projects\Wortkiste\Repositories
git clone https://github.com/<your-user>/wortkiste.git
cd wortkiste
REM copy the files from this folder in here (not wortkiste-buchliste.json)
git add .
git commit -m "Wortkiste app"
git push
```

Or create the repository on github.com and upload the files with **Add file → Upload files**.

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save**.

After a minute the app is live at `https://<your-user>.github.io/wortkiste/`.

The site is public, but it contains nothing from the book. `noindex` keeps search engines from listing it.

## 2. Install it on your phone

- **iPhone (Safari):** open the URL → Share → **Zum Home-Bildschirm**.
- **Android (Chrome):** open the URL → ⋮ menu → **App installieren** (or *Zum Startbildschirm hinzufügen*).

## 3. Load the word list (once)

1. Copy `wortkiste-buchliste.json` to your phone (AirDrop / iCloud Drive / Files on iPhone; Google Drive or Downloads on Android).
2. Open Wortkiste **from the home-screen icon** (on iPhone the installed app has its own storage, separate from Safari).
3. Tap **Buchliste laden → Datei auswählen** and pick the file.

The app restarts with all 12 chapters. From then on it works offline.

## Move your progress from the Claude version

In the old version: **Meine Wörter → Backup anzeigen → Kopieren**.
In the installed app: paste into the same box → **Backup einlesen**.

## Updating the app

Replace `index.html`, change `VERSION` in `sw.js` (e.g. `wortkiste-v2`), commit and push. The phone picks up the new version the next time you open the app with internet. Your word list, own words and progress stay on the phone.
