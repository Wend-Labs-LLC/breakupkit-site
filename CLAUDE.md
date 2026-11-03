# Break-Up Kit Site

## What it is
The public support page and privacy policy for the Break-Up Kit app
(see ../breakup-kit). These are the URLs App Store Connect links to.
Published by Wend Labs LLC.

- Repo: github.com/Wend-Labs-LLC/breakupkit-site (branch: `main`)
- Hosted on GitHub Pages from `main`, so **pushing to main publishes live**

## Stack
- Plain static HTML + one CSS file. No build step, no JS, no dependencies.
- `.nojekyll` turns off Jekyll processing on GitHub Pages.

## Key files
- `index.html`: Support page with crisis lines (988, Crisis Text Line, 911),
  contact email, and FAQ (data storage, restore purchases, pricing, reminders,
  SendEx shelf, deleting data, "is this therapy?")
- `privacy.html`: Privacy policy, effective November 1, 2026
- `style.css`: Shared styles. Colors match the app's palette, with
  automatic dark mode.

## Run and build
- Nothing to build. Open `index.html` in a browser, or run a static server
  (for example `npx serve .`).
- Deploys automatically when `main` is pushed (ask first; see rules).

## Keep in sync with the app
This copy makes promises about the app. If the app changes, these pages
need to change too:
- Pricing: free tools, 7-day trial, one-time $4.99 unlock, no subscription
- Data: no accounts, servers, analytics, or ads; everything stays on device
- Permissions: microphone, camera, notifications. No photo library
  permission; SendEx attaches photos through the phone's own picker.
- SendEx: messages fade after 24 hours unless kept
If you change `privacy.html`, update the effective date.

## Current status (as of 2026-11-02)
- Privacy policy reworded 2026-11-02: no photo library permission; photos
  come through the system picker. Effective date November 2, 2026.
- Pricing copy stays. The 7-day trial (a free product) and the $4.99 unlock
  are set up in App Store Connect; the app's purchase code isn't built yet.
- Purchases are described as "handled by Apple." When the Android app ships,
  that section needs to mention Google Play too.

## Rules
- Any build uploaded to App Store Connect must be a production build, never
  development.
- Never push to main, delete files, or submit builds without asking me.
- Never run ship.ps1, eas build, or eas submit without my explicit yes in the
  current session, including when working unattended.
- When working unattended, if something is ambiguous, choose the safest
  option, log it in PROGRESS.md, and move on.
- At the end of every session, update PROGRESS.md with what you did, what's
  left, decisions made, and questions for me.
