# Chillara — Daily Expense Tracker

A fast, single-page expense tracker: tap in an amount on the keypad, pick a
category and payment method, hit **Add**. It keeps a running monthly total,
a category/payment breakdown, and lets you export any month (or everything)
as CSV.

This is a plain static web app — `index.html`, no build step, no server,
no account required. It works standalone in any browser, saving your
entries to that browser's local storage on this device.

## Run it locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy with GitHub Pages (recommended)

1. In this repository, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to "Deploy from a branch".
3. Pick the branch you want published (e.g. `main`) and folder `/ (root)`.
4. Save — GitHub gives you a URL like
   `https://<your-username>.github.io/Expence_Tracker/`.

Open that URL on your phone and use **"Add to Home Screen"** (Safari) or
**"Install app"** (Chrome/Edge) — the manifest and icons are already set up
so it launches full-screen like a native app.

## Data & backups

Entries are saved in your browser's local storage under keys prefixed
`chillara:`, grouped by month. That means:

- Data stays on the device/browser you used to add it — it does not sync
  between devices on its own.
- Clearing site data/cookies for this page will erase your entries, so use
  **Export everything** (in the monthly breakdown view) every so often to
  save a CSV backup.

## Files

- `index.html` — the entire app (markup, styles, and logic).
- `manifest.json` — web app manifest for "Add to Home Screen".
- `icon.svg` — app icon used by the manifest.
