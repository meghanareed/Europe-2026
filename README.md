# Grand Tour 2026 — Travel Companion

A self-contained mobile web app of your private travel guide: **Belgium · Luxembourg · Alsace · Switzerland, July 10–21, 2026.** Built for your five travelers to use on their phones during the trip.

It's a single `index.html` file — no build step, no dependencies, no server. Once a phone has opened it, it works **fully offline** (perfect for walking around with roaming off).

## What's inside

- **Today** — a live "departure board" that auto-detects the date and opens to the right day during the trip (and counts down before it). Shows the day's plan, weather, and any heads-up notes.
- **Days** — all 12 days. Each opens to an hour-by-hour timetable, the self-guided walking tour (every stop is a one-tap Google Maps link), where to eat, local dishes to try, "good to know" tips, and a private notes box.
- **Places** — your four hotels (tap to navigate or call), plus every city's sights, restaurants, and local specialties, all tappable to Maps.
- **Pack** — the five checklists with checkboxes that save on the device. The hotel-checkout list is handy at every stop.
- **Info** — emergency numbers (tap to call 112/police), hospitals & US embassy contacts, money/power/VAT notes, full private-driver details, transport tables, and the route at a glance.

The accent color shifts by country as the trip moves (Belgium gold → Luxembourg blue → Alsace red → Switzerland green), so travelers can tell which leg they're on at a glance.

> Notes and checkmarks save in each person's own browser (per device). They aren't shared between travelers, and they persist as long as the same browser is used.

---

## Option A — GitHub Pages (free, recommended)

1. Create a new repository on GitHub (e.g. `grand-tour-2026`). Public is fine.
2. Upload `index.html` to the repo (drag-and-drop in the GitHub web UI works).
3. Go to **Settings → Pages**. Under "Build and deployment," set **Source: Deploy from a branch**, **Branch: `main` / `/ (root)`**, and Save.
4. Wait ~1 minute. Your link will be:
   `https://<your-username>.github.io/grand-tour-2026/`
5. Open that link, then send it to the group.

## Option B — Netlify Drop (free, no account login needed to try)

Go to **app.netlify.com/drop** and drag `index.html` (or the whole folder) onto the page. You'll get an instant public link to share.

## Option C — Just send the file

Email or AirDrop `index.html` to each traveler. On a phone, opening it from Files/Mail loads the app. (A hosted link from A or B is smoother to share via a single QR code.)

---

## Get it onto travelers' home screens (offline + app-like)

After opening the link on a phone:

- **iPhone (Safari):** Share button → **Add to Home Screen**.
- **Android (Chrome):** ⋮ menu → **Add to Home screen** / **Install app**.

This caches it for offline use and gives it an app icon. Tell everyone to do this **before** leaving on Wi-Fi, and to also download the **Google Maps offline area** for each city.

### Tip: one QR code for the whole group
Once you have a link (Option A or B), make a free QR code for it (e.g. search "QR code generator") and drop it into your group chat or the printed guide — everyone scans once and they're in.

---

## Editing later

- Day-to-day content lives in a single JavaScript object named `DATA` near the top of the `<script>` in `index.html`. You can adjust any text, time, or map link there directly.
- The country accent colors are in the `LEGS` object just below `DATA`.
- It also still renders fine opened straight from your computer (double-click `index.html`).
