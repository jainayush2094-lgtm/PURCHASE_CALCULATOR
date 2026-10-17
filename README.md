# Amazza Purchase Tracker

A single-file web app for tracking purchases, computing weighted-average cost per item, and calculating sell rates. Works offline, installs to your phone's home screen, and stores everything on your own device.

## What's inside

- **Entry** — browse the catalogue and log a purchase (vendor, bill no., date, line items).
- **Report** — weighted-average cost per item code, searchable and sortable, with Excel export.
- **Sales** — the Sell Rate Calculator. Pull any item from the catalogue, add an extra-expense amount to get a net rate, then set either a **markup %** or a **selling price** and the other fills in automatically. Sort by markup %, selling price, net rate, cost, or profit; search the worksheet; export to Excel.
- **History** — every purchase, auto-folded into collapsible month groups (newest month open by default) so there's far less scrolling. Expand all / Collapse all controls included.
- **Catalogue Manager** — add or remove items and whole categories. Shared across Entry and Sales.
- **Backup** — export/import all data (purchases, catalogue, and the sell-rate worksheet) as a single JSON file.

## Hosting it on GitHub Pages (no command line needed)

1. Sign in to GitHub and click **New repository**. Give it any name (for example `amazza-tracker`), keep it **Public**, and create it.
2. On the new repo page, click **Add file → Upload files**.
3. Drag in all three files from this folder: **`index.html`**, **`README.md`**, and **`.nojekyll`**. Click **Commit changes**.
4. Go to the repo's **Settings → Pages**.
5. Under **Build and deployment**, set **Source** to *Deploy from a branch*, choose the **`main`** branch and the **`/ (root)`** folder, and click **Save**.
6. Wait about a minute, then refresh. GitHub shows the live URL — it'll look like `https://<your-username>.github.io/amazza-tracker/`. Open it and the app loads.

To update later, repeat **Add file → Upload files** and re-upload `index.html` (committing the change replaces the old one). The live site refreshes within a minute or two.

## Installing on your phone

Open the live URL in your phone's browser, then use **Add to Home Screen** (Share menu on iPhone, the ⋮ menu on Android). It launches like a normal app.

## Where your data lives — important

All purchases, catalogue edits, and sell-rate rows are saved in the browser's local storage **on the specific device and browser you're using**. Nothing is sent anywhere. That means:

- Clearing the browser's site data, or uninstalling, **erases everything**.
- Data does **not** sync between your phone and your computer automatically.

So use **Backup → Export** regularly and keep the JSON file somewhere safe (Drive, email to yourself, etc.). To move data to another device, open the app there and use **Backup → Import**.

## Files in this folder

| File | Purpose |
|------|---------|
| `index.html` | The entire app — open it directly in any browser, or host it. |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is (leave it empty). |
| `README.md` | This file. |
