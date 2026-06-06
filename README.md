# Life Tracker

A personal 24-hour time tracker built as a single HTML file. No server, no login, no app store. Works offline and installs on your phone home screen.

## What it does

- 24-hour grid — every 15-minute slot of your day laid out visually
- Tap a slot to log what you were doing
- Hold and drag to select many slots at once (e.g. 8 hours of sleep in one move)
- Timer mode — classic 15-minute countdown with log prompt
- Week view — see your full week at a glance
- Insights — 7-day and 30-day bar charts per category
- Sleep warning — if you sleep more than 8 hours, excess counts as wasted time
- All data saved locally on your device (no internet needed after first load)

## Categories

| Category   | Type       |
|------------|------------|
| Office     | Productive |
| Coding     | Productive |
| Learning   | Productive |
| Emails/msg | Productive |
| Scrolling  | Wasted     |
| Sleeping   | Sleep      |
| Break/food | Neutral    |
| Personal   | Neutral    |

## How to use on your phone

1. Open the GitHub Pages link in Safari (iPhone) or Chrome (Android)
2. Tap Share → "Add to Home Screen"
3. Opens like a native app, works fully offline

## Roadmap

- [ ] Swipe left/right to change day
- [ ] Monthly heatmap (like GitHub contribution graph)
- [ ] Custom categories
- [ ] Weekly productivity score
- [ ] CSV export
- [ ] Convert to iOS/Android app via Capacitor
- [ ] Streak counter

## Tech

Pure HTML + CSS + JavaScript. Zero dependencies. Zero frameworks. Single file.
Data stored in `localStorage` on the device.

## Converting to a native app

This can be wrapped into a real iOS/Android app using [Capacitor](https://capacitorjs.com):

```bash
npm install @capacitor/core @capacitor/cli
npx cap init
npx cap add ios
npx cap add android
```

Then copy `index.html` into the `www/` folder and build.

## License

MIT — free to use, modify, and build on.
