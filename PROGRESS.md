# Progress — Break-Up Kit Site

## Session 2026-11-02
### Done
- Added CLAUDE.md. Pushed to main.
- Reworded `privacy.html` (you approved): split "Camera and photos" into
  Camera and Photos. The app has no photo library permission; SendEx's
  attach buttons use the phone's own picker, which shares only the chosen
  items. Effective date changed to November 2, 2026.

### Decisions
- Kept the pricing copy: the trial and unlock exist in App Store Connect and
  the app's purchase code is planned.

## Session 2026-11-03
### Done
- `privacy.html` now covers (merged and pushed to main Nov 3, live):
  RevenueCat (anonymous app user ID, App Store purchase records, request
  details; used only to unlock and restore; deletion by email). Wording
  matches Gem State's policy. FAQ: "no servers" became "no servers of its
  own". Effective date November 3, 2026.

### Decisions
- You chose to publish it now, before the app uses RevenueCat.

## What's left (code)
- [ ] **Medium (when Android ships):** The Purchases section and pricing
      FAQ only mention Apple. Add Google Play.
- [ ] **Watch:** If the app's purchase plan changes, update the pricing FAQ
      in `index.html`.
