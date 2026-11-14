# Symptom Log

A simple offline web app for logging digestive symptoms with one-tap buttons and sliders. Every entry is timestamped automatically. All data stays **on the phone** (browser storage). Nothing is sent anywhere.

## What it tracks

- **Nausea, dizziness, stomach (upper abdomen):** intensity from 0 to 10, plus detail chips (after meal, food helped…)
- **Stool:** consistency, plus greasy / pale / floating / foul / urgent
- **Meal:** size, plus fatty / dairy / gluten / coffee / alcohol / sweeteners
- **Medication:** editable list of names, dose count, with meal yes/no
- **Woke up:** one tap at night (with undo and optional details)
- **End of day:** overall day 1–5, hours of sleep, stress, period
- **Weight:** weekly, in kg
- **Blood pressure:** upper/lower (mmHg) and pulse

Detail chips are sorted by how often they're used. Add your own with **+ new** in any form, and remove unused ones in Settings. Night-time is worked out from the logged time (default 22:00–7:00, adjustable).

The **Entries** tab shows entries day by day, or all of them with a filter by type. Tap any entry to edit or delete it.

The **Overview** tab has two views, each for a single day (with an hour-by-hour chart and that day's entries), 7 days, 30 days, all data, or a custom from–to range. **Charts** shows trends over 7, 14, 30, 60 days or everything, with period days shaded. **Diagnostic** uses everything that's logged, in collapsible sections:
- **Key facts:** days logged, how often nausea happens and how much of it is at night, greasy stools, sleep, weight trend in kg/week, and how many meals were covered by medication
- **Combined chart** and **When it happens** (day × hour map)
- **All parameters** grid by day or week. Symptoms are coloured green to red. Food types, medication and notes are shown in blue as counts.
- **After meals:** for each food type (including your own), meal size, late meals, and meals with or without medication, the % of meals followed by nausea, stomach pain, dizziness, a stool or a greasy stool within 4 hours
- **Medication:** how many meals were covered, plus averages from up to 30 logged days before the first dose and up to 30 after
- **Symptom details:** how often each detail was ticked, nausea timing relative to the last meal, typical wake-up time, and blood pressure sitting vs standing
- **Time of day**, plus **menstrual cycle** phases (1–5 days before, during the period, other days)
- **Correlation analysis** across symptoms, sleep, stress, food types, late meals, medication, blood pressure, period and notes, including next-day effects (e.g. dairy yesterday and nausea today)
- **Comparisons** (period, short sleep, stress, each food type, late meals, notes, and so on)

**Summary for the doctor:** choose 1 day, 7 days, a calendar month, all data, or a custom date range. It includes everything above. **Summary for the doctor** produces a printable page: key figures, charts, a day-by-day table and optionally every single entry. Save it as a PDF from the browser's print/share menu.

**Backup:** Settings → *Back up now* opens the phone's share menu. Choose **Drive** (and a folder) or **Save to Files**. You get a JSON backup (for restoring) and a CSV (for Excel). The Log screen reminds you if no backup was made for 7 days. *Restore backup* can pick the file straight from Drive.

**Display:** dark mode turns on automatically from 18:00 to 7:00. You can switch to follow the phone, or always light or always dark, in Settings.

## Publish on GitHub Pages

1. Create a new repository on GitHub, e.g. `symptom-log` (public is fine because the data never leaves the phone).
2. Upload all files from this folder: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`, `README.md`.
3. Go to **Settings → Pages → Build and deployment**, set Source to *Deploy from a branch* and Branch to `main` / `(root)`, then save.
4. After about a minute the app is live at `https://<your-username>.github.io/symptom-log/`.

## Install on the phone

- **Android (Chrome):** open the link, then use the ⋮ menu → *Add to Home screen* / *Install app*.
- **iPhone (Safari):** open the link, then use Share → *Add to Home Screen*.

After the first visit it also works offline.

## Notes

- The data belongs to the browser on that phone. Clearing the browser data deletes it, so back up to Drive now and then.
- On iPhone, data from an installed home-screen app is kept separately from Safari. Always use the same icon.
- This is not a medical device. Warning signs need a doctor.
