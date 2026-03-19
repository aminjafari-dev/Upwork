# Senior Flutter Developer - Offline-first Golf Instrument

## Job snapshot
- Project: MyProgrix (minimalist, offline-first golf instrument)
- Goal: Build a tiny, high-reliability product that feels like an instrument, not an app
- Budget: $3,500 fixed price
- Type: Fixed scope, fixed price, pay-per-gate
- Tech: Flutter, Dart, iOS, Android, In-App Purchases

----

## Locked scope and non-negotiables
- Max 4 screens, max 2 onboarding screens, Reset screen, and 1-tap check-in ("Felt the shift?")
- No scope creep: no dashboards, coaching, gamification, push, accounts, or cloud sync
- Dependency cap: fewer than 50 packages
- Offline-first: reset must work fully offline
- Store-ready subscriptions + restore + legal links
- Top-layer wording audit: no "8 seconds", no breathing/counting framing, no coaching/therapy/performance claims
- Blind-operable use: haptics primary, visuals secondary
- Consumer flow must exit cleanly after cue
- Client-owned GitHub repo, all work through PRs with regular pushes

----

## Core function (locked)
- One-tap start
- About 8-second internal loop (no countdown UI)
- 0.5-second cue around t=4s
- Instant cancel on lock/app-switch/background (Kill Gate)
- Usage moments: tee shot, after mistake, or focus drift

----

## Milestones / gates (pay-per-gate)
### M1 - Kill Gate (Priority 1)
- Requirement: Any interrupt stops instantly and returns to Ready
- Proof: 50-cycle stress test + videos + 1-page log on 2 Android + 1 iPhone

### M2 - Feel Gate
- Requirement: stable timing, cue around 4s, no drift, consistent haptic feel
- Proof: device videos + 0-10 feel note + 1-page log on 2 Android + 1 iPhone
- Extra: client does 3-5 tester naive feel check
- If fail: one tuning iteration only, no new screens
- Rule: native phones only (no web/PWA feel proxy)

### M3 - Store-ready
- Requirement: 7-day trial subscription, store-managed eligibility, restore, manage subscription links, legal links, paywall disclosure accuracy, wording audit pass
- Proof: iOS + Android restore flow videos, paywall screenshots, legal checks, dependency cap proof

----

## Required proposal response
- Share 1-2 shipped Flutter apps (App Store/Play links)
- Reply "YES" confirming locked terms (fixed scope/price, pay-per-gate, dependency cap, client GitHub, proof videos)
- Answer technical questions:
  - Kill Gate lifecycle targets + instant stop guarantee + 50-cycle proof method
  - Top subscription rejection reason + prevention plan
  - Blind-operable flow + clean exit after cue
- Quote must include:
  - Total fixed EUR price
  - Split by M1/M2/M3
  - Estimated weeks
  - Exact proof devices (model + OS)
- Add 1-2 sentence motivation for this minimalist offline-first haptic product
