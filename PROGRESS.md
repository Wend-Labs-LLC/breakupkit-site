# Progress — Break-Up Kit Site

## Session 2026-11-03 (later): pages match the app as it ships
### Done (branch `ship-pricing-permissions`, local, off `main`; not pushed)
- Checked the app code first (`../breakup-kit`, branch with the purchase
  code). The tool pages are base64 HTML inside `src/kit.html`; decoded and
  searched them.
  - Trial **is implemented**: `7daytrial` is a free App Store product; the
    app opens SendEx, Funny Bone and Light Mode for 7 days from its
    purchase date, then locks them unless `breakupunlock` ($4.99) is owned.
    So only the trial version of the copy was written.
  - Permissions it actually requests: microphone (`getUserMedia({audio})`
    when recording a SendEx call), camera (iOS `NSCameraUsageDescription`;
    the attach button's system menu offers Take Photo or Video),
    notifications (when the daily reminder is turned on). Nothing else.
    No photo library permission is declared or requested.
  - SendEx attachments are object URLs only, never stored; the shelf keeps
    words only.
  - The app loads Google Fonts when online (kit and all five tool pages).
- `index.html`: new "What's free, and what does it cost?" and "How does
  the 7-Day free trial work?" cards; restore card renamed to Full Unlock
  and uses the app's button label "Restore purchases"; data card links to
  the policy for what the app sends.
- `privacy.html`: removed the Photos permission bullet and the photo
  picker / photo library sentences. Permissions now say each is asked on
  first use and there are no others. Purchases names the free tier, the
  7-Day free trial and the $4.99 Full Unlock. Added a **Fonts** section
  (Google Fonts gets IP and device details when online). Effective date
  stays November 3, 2026 (today).
- Checked: no "photo library"/"picker" wording left; tags balance in both
  pages. Not viewed in a browser (other sessions may have been using it).

### Decisions (unattended, safest option)
- Kept "Anything you attach to a SendEx text or email is shown on screen
  only and never saved." It's about storage, not photo access, and the
  code confirms it.
- Added the Google Fonts disclosure without asking: the old policy said
  only the purchase record leaves the phone, which isn't true when online.

### Questions for you
- Publish when? I'd merge and push this when the purchase build goes live.
  The live site already describes the trial and $4.99 price, so pushing
  sooner is also fine. If it goes live after Nov 3, change the effective
  date to that day.
- Google Fonts: keep the disclosure, or bundle the fonts into the app so
  nothing goes to Google? Bundling is cleaner for privacy and the App
  Store label. If you do, drop the Fonts section.
- App Store Connect privacy label may need to reflect the Google Fonts
  request (IP address). Not checked (browser skipped).
- `main` is 2 local commits ahead of `origin/main` (PROGRESS only), from
  the last session.

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
