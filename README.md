# Personal Mission Control — version 0.1

A simple, installable, offline-first Progressive Web App (PWA) for Android and desktop.

## What works now
- Today: select up to three priority tasks.
- Inbox: quickly capture ideas, then move them to Today when ready.
- Projects: view tasks grouped by Pack 179, Engineering, Home, Personal, and Other.
- Focus mode: one task, one next step, and a 10-minute timer.
- Edit or complete tasks. Data is stored locally in the browser.
- Export task backups as JSON, or import a previous backup.
- Works offline after loading once on an HTTPS site.

The initial four tasks are **examples**, not actual imported tasks. Nothing syncs to Gmail, Google Calendar, Google Drive, or ChatGPT. There is no account or backend. Clearing browser storage or switching devices can remove tasks unless they are exported.

## Test it on a computer
From this folder, run:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000/`. Localhost supports PWA service workers.

## Put it on your Android home screen via GitHub Pages
1. Create a GitHub repository, e.g. `mission-control`.
2. Upload the **contents** of this folder to the repository root (not the zip itself).
3. In the repository, choose **Settings → Pages → Build and deployment → Deploy from a branch**, select `main` and `/ (root)`, then save.
4. Open the HTTPS GitHub Pages URL on Android in Chrome.
5. Chrome's menu should offer **Install app** or **Add to Home screen** after the site is eligible. The wording may vary.

**Important privacy note:** GitHub Pages publicly hosts these app files (including the four example task titles embedded in code), but it does *not* upload your newly entered tasks. Those remain in the browser's local storage. Do not put real private tasks directly into the source code of a public repository.

## Future phases
- Phase 2: calendar reading, secure sign-in, notifications, and reliable multi-device sync.
- Phase 3: AI task triage and suggested next actions, subject to review.
- Phase 4: optional Pack 179, engineering, and home modules.

To connect Gmail, Google Calendar, or AI APIs, create a secure backend with OAuth and protected credentials. **Never** put API keys or account passwords directly in this client-side code.
