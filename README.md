# Focus App (PWA)

A mobile-first Progressive Web App for focus sessions with a Pomodoro timer, distraction block list, local analytics, streaks, and offline support.

## Features

- Focus timer
  - Pomodoro defaults: 25 min focus, 5 min break
  - Custom focus and break minutes
  - Start, pause, and reset
- Website block list
  - Add/remove distracting domains (for example: `youtube.com`, `reddit.com`)
  - During active focus sessions, blocked domains trigger a warning in the built-in site checker
- Focus dashboard
  - Today focus time
  - Sessions completed today
  - Weekly focus hours (last 7 days)
- Streak system
  - Daily focus streak (consecutive active days)
- Notifications
  - Session start and completion notifications
- Local-first storage
  - Uses `localStorage` only
- PWA capabilities
  - Installable on Android and iPhone home screen
  - Offline app shell via service worker cache

## Project Files

- `index.html`
- `styles.css`
- `app.js`
- `manifest.json`
- `service-worker.js`
- `icons/`
  - `icon-192.png`
  - `icon-512.png`
  - `icon-maskable-512.png`

## Run Locally

1. Serve the folder with a local web server (recommended for service worker behavior).
2. Open the app in a modern browser.

Quick option with Python:

```bash
python -m http.server 8080
```

Then visit `http://localhost:8080`.

## Install on Phone

- Android (Chrome): open app URL, then choose **Install app** / **Add to Home screen**.
- iPhone (Safari): tap **Share** -> **Add to Home Screen**.

## Notes on Blocking Behavior

Because web PWAs cannot globally intercept other apps or browser tabs across all domains, this app enforces blocking in its built-in site checker during active focus mode.