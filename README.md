# LabStock — Hospital Laboratory Inventory

A simple, downloadable web app (PWA) for a hospital laboratory store.

## Problem it solves
The lab takes test strips / kits / inventory from the hospital's central store (daily or monthly).
Tracking who took what, and how much was used each day, was messy. LabStock makes it simple:

1. **Stock In** — when the lab takes stock from the store, enter item + quantity once (e.g. Glucose Strips × 500). Stock increases automatically.
2. **Daily Usage (manual)** — at the end of the day, enter how many tests were done per item. Stock decreases automatically.
3. **Daily Usage (PDF)** — or upload the day's test-report PDF. The app reads the PDF, matches tests by each item's *PDF Keywords*, shows a preview, and deducts on confirmation.
4. **Low-stock alerts** — items at/below their minimum level are flagged on the dashboard.
5. **History / Ledger** — every in/out entry with date, person and source. Deleting a wrong entry auto-reverses the stock.
6. **Reports** — any period: received, used, current balance per item. CSV export + print/PDF.

## App install (downloadable)
It's a PWA — open the site, tap **Install App** (or browser menu → Add to Home screen). It then works like a normal app, even offline.

## Data
All data is stored locally in the browser on that device (`localStorage`). Use **Settings → Backup** regularly; restore from the backup file on a new device. No server or login needed.

## Items & PDF matching
Test/inventory names are fully editable in **Inventory**. For PDF matching, set each item's **PDF Keywords** to the exact names used in the lab's PDF reports (comma-separated aliases, e.g. `glucose, rbs, fbs, sugar`).

## Tech
Single static site (HTML/CSS/JS + PDF.js via CDN), PWA with service worker. Deploys to Vercel with no build step.

Developed by **Syed Abdul Aleem** · WhatsApp 03295566111
