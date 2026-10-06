# Amazza Purchase Tracker

A single-file web app for tracking purchases, computing weighted-average cost per item, and calculating sell rates. Works offline, installs to your phone's home screen, and stores everything on your own device.

## What's new in this version

- **One simple "New item" form.** Tap **+ New item** on Entry, Sell Rates or the Items screen. Type the name, pick a category (or create one right there), and optionally the purchase rate, selling price and rack. The item code is made automatically, continuing the category's own series (NV-018 becomes NV-019).
- **No duplicates by accident.** While you type a name, matching catalogue items appear; tap one to use it instead.
- **Can't find an item while searching?** A button offers to add exactly what you typed as a new item.
- **Sell Rates fills itself.** Every catalogue item is listed automatically, including new ones the moment you add them. No more adding items by hand. Cost fills in from your average purchase cost. Filters: All, Not priced, Priced, Purchased.
- **Old custom items are now real items.** Items you added earlier "outside the catalogue" are moved into the catalogue under their original codes, so you can pick them again.
- **Your data is untouched.** Same storage as before. On first open, the app also keeps a copy of your old data on the device (Backup menu: **Download pre-upgrade copy**).

## Screens

- **Entry**: browse the catalogue and log a purchase (vendor, bill no., date, line items).
- **Report**: weighted-average cost per item, searchable and sortable, with Excel export.
- **Sell Rates**: cost + extra expense = net rate; type a **markup %** or a **selling price** and the other fills in. Sort, search, filter, export to Excel.
- **Profit**: monthly quantity sold and average selling price per item, with net profit.
- **History**: every purchase, folded by month, with PDF and ZIP export.
- **Items** (the "Edit items" button): search, edit, move or remove items; rename or delete categories.
- **Backup** (the ⋯ button): export/import everything as one JSON file.

## Updating the live site (no command line needed)

1. Before updating, open the current app and use **⋯ → Export backup** once, just to be safe.
2. In your GitHub repo `PURCHASE_CALCULATOR`, click **Add file → Upload files**.
3. Drag in **`index.html`** and **`README.md`** (and `.nojekyll` if it isn't there already). Click **Commit changes**.
4. Wait a minute or two, then open the app and refresh. On a phone, close and reopen the app if it still shows the old screens.

Keep the same repo and URL. Your data is stored per web address, so a new repo or a different URL would open empty.

## Installing on your phone

Open the live URL in your phone's browser, then use **Add to Home Screen** (Share menu on iPhone, the ⋮ menu on Android). It launches like a normal app.

## Where your data lives: important

All purchases, catalogue edits, and sell-rate rows are saved in the browser's local storage **on the specific device and browser you're using**. Nothing is sent anywhere. That means:

- Clearing the browser's site data, or uninstalling, **erases everything**.
- Data does **not** sync between your phone and your computer automatically.

So use **Backup → Export** regularly and keep the JSON file somewhere safe (Drive, email to yourself, etc.). To move data to another device, open the app there and use **Backup → Import**. Older backup files import fine.

## Files in this folder

| File | Purpose |
|------|---------|
| `index.html` | The entire app. Open it directly in any browser, or host it. |
| `.nojekyll` | Tells GitHub Pages to serve the files as-is (leave it empty). |
| `README.md` | This file. |
