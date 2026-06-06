# Life Tracker

A personal 24-hour time tracker built as a single HTML file. No server, no login, no app store needed. Works fully offline and installs on your phone home screen like a native app.

**Live:** https://thrishulant1.github.io/life-tracker

---

## What it does

Track every 15 minutes of your day, see where your time actually goes, and get a daily productivity score — all stored privately on your device.

---

## Features

### Day View
- 24-hour grid — every 15-minute slot of your day laid out visually
- Tap a slot to assign a category (Office, Coding, Sleeping, etc.)
- Hold and drag across multiple slots to assign them all at once
- Long-press a filled slot to edit or clear it
- Action bar appears when slots are selected — assign or clear in bulk
- Tap the live clock bar to instantly log what you're doing right now
- Copy yesterday's schedule to today with one tap
- Smart fill — fills remaining empty slots based on your typical daily routine
- Live clock showing current time, current activity (with blinking dot), and slot progress bar
- Swipe left/right to navigate between days

### Timer Mode
- Built-in 15-minute countdown timer (Pomodoro-style)
- When it finishes, prompts you to log what you worked on

### Week View
- Weekly summary card — score, productive hours, wasted hours, top activities
- See your full week at a glance — one card per day
- Per-category time bars showing how you spent each day
- 30-day productivity heatmap (darker = more productive)
- Click any heatmap cell to jump to that day
- Navigate to previous weeks

### Insights
- 7-day and 30-day bar charts per category
- Total hours, daily average, and peak day for each category
- Tap any bar to see the full breakdown for that day
- Navigate to previous months

### Scoring System
- Daily score = Productive time / (Productive + Wasted) × 100
- Weekly score = average of last 7 days, shown on the Day page
- Streak counter — consecutive days you've logged anything
- Comparison to last week (up/down arrow)

### Settings
- Dark / light mode toggle
- Sleep warning — excess sleep over 8h counts as wasted time
- Daily goal — set a target productive % and see a live progress bar on the day view
- Custom categories — add your own with name, color, and type
- Edit any existing category
- Year progress grid — 365 boxes, today highlighted in orange
- Export all data as CSV (open in Google Sheets for charts)
- Import CSV to restore from a backup
- Backup as JSON — full safe export, includes all slots and notes
- Restore from JSON backup — merges without overwriting existing data
- Clear all data

---

## Scoring Rules

| Category   | Type       | Rule |
|------------|------------|------|
| Office     | Productive | Always counts positively |
| Coding     | Productive | Always counts positively |
| Learning   | Productive | Always counts positively |
| Emails/msg | Productive | Always counts positively |
| Sleeping   | Sleep      | 0–8h = productive, over 8h = wasted |
| Breakfast  | Meal       | Combined meals up to 1h/day = productive, over = wasted |
| Dinner     | Meal       | Combined meals up to 1h/day = productive, over = wasted |
| Break      | Break      | Up to 1h/day = productive, over = wasted |
| Personal   | Personal   | Up to 1h/day = productive, over = wasted |
| Home help  | Neutral    | Not counted in score at all |
| Scrolling  | Wasted     | Always pulls score down |

---

## How to install on your phone

**iPhone:**
1. Open https://thrishulant1.github.io/life-tracker in Safari
2. Tap the Share button → "Add to Home Screen"
3. Opens like a native app, works fully offline

**Android:**
1. Open the link in Chrome
2. Tap the three-dot menu → "Add to Home Screen"
3. Same result — works offline

---

## Roadmap

**Fixes**
- [ ] Live clock flicker on first load
- [ ] Smoother drag-select on touch screens

**Upcoming features**
- [ ] Monthly calendar view (proper calendar layout)
- [ ] Reminder notification — "log your last 15 minutes"
- [ ] Convert to iOS app using Capacitor
- [ ] Convert to Android app using Capacitor
- [ ] Google Drive / iCloud sync

---

## Tech Stack

| What | How |
|---|---|
| Language | Pure HTML + CSS + JavaScript |
| Frameworks | None — zero dependencies |
| Data storage | `localStorage` on the device |
| Hosting | GitHub Pages (free) |
| File count | 1 (`index.html`) |

---

## File Structure

```
life-tracker/
├── index.html     ← entire app (HTML + CSS + JS in one file)
├── README.md      ← this file
└── CONTEXT.md     ← project context for AI assistants
```

---

## Converting to a Native App (future plan)

The app is designed to eventually be wrapped into a real iOS/Android app using [Capacitor](https://capacitorjs.com):

```bash
npm install @capacitor/core @capacitor/cli
npx cap init
npx cap add ios
npx cap add android
```

Copy `index.html` into the `www/` folder and build. The localStorage data model will carry over directly.

---

## License

MIT — free to use, modify, and build on.

---

*Built by Thrishula N T — learning to build apps one feature at a time.*
