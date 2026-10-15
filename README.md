# Susu

Free group contribution (rotating savings) tracker for Ghana. Works offline as an iPhone home-screen app.

## Features

- Create susu groups: contribution amount, currency (default GHS), frequency (daily / weekly / monthly), start date, members, payout order
- Auto-built round schedule — each round shows who collects the pot
- Tick who has paid per round; unpaid members highlighted; mark payout done
- Dashboard: current round, next payout, collected total, debts, progress
- Member history and WhatsApp reminders (`wa.me` with Ghana `0…` → `233…`)
- Share group status via system share sheet or WhatsApp
- Multiple groups · Export / import JSON backup
- No account, no paid services — data stays in `localStorage`

## Install (iPhone)

1. Open the site in Safari  
2. Tap Share → **Add to Home Screen**  
3. Open **Susu** from your home screen  

## Files

| File | Role |
|------|------|
| `index.html` | App (HTML + CSS + JS) |
| `manifest.json` | PWA manifest |
| `icon.png` | 512×512 icon |
| `sw.js` | Service worker (cache-first shell, network-first HTML) |

## Run locally

Serve the folder over HTTP (needed for the service worker):

```bash
python3 -m http.server 8765 --directory /workspace/susu
```

Then open `http://localhost:8765/`.

## Privacy

Everything is stored on the device. Export a JSON backup from Settings before clearing browser data.
