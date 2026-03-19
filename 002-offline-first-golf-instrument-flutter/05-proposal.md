# Main risk: missed interrupt handling can break trust instantly
If kill behavior is not truly immediate on lock/app-switch/background, users feel "zombie haptics" and the product fails fast. I prevent this by building M1 first with one hard stop path wired to all critical lifecycle interrupts and proving it with your 50-cycle gate evidence.

----

Quick project questions
1) Please confirm your exact 2 Android test devices (flagship + mid/low) and iPhone model.
2) Do you already have final privacy/terms/support URLs for M3, or should I prepare temporary production-safe pages?
3) For subscription, do you want monthly only, or monthly + yearly from day one?

----

Why I fit
I build small, reliability-first Flutter products where lifecycle safety and timing behavior matter more than feature count. I also work in strict PR-based delivery with binary proof gates, which matches your pass/fail model.

----

Plan
Milestone 1: Kill Gate implementation + 50-cycle stress proof pack.  
Milestone 2: Feel Gate timing/haptics validation + one tuning iteration if needed.  
Milestone 3: Store-ready subscriptions, restore, legal links, wording audit, dependency cap proof.

----

Direct answers
Shipped Flutter apps: please insert your 1-2 App Store/Play links here before sending.

YES - fixed scope, fixed price, pay-per-gate, locked scope, <50 dependencies, client-owned GitHub, proof videos.

Kill Gate: I target `resumed/inactive/paused/detached` + app lifecycle/background transitions, route all exits through one synchronous `stopNow()` that cancels timers/haptics/state, then verify with 50 scripted interrupt cycles per device and timestamped logs + videos.

Store/IAP: #1 rejection risk is paywall/trial disclosure mismatch vs store config. I prevent it by deriving paywall copy directly from active product metadata and testing purchase/restore states on both platforms.

Instrument feel: no countdown UI, haptics-first cue, minimal visual dependency, and immediate clean exit to Ready right after cue.

Quote: EUR 3,400 total fixed (M1: 1,350 | M2: 1,050 | M3: 1,000).  
Estimated time: 3-4 weeks.  
Proof devices: Samsung Galaxy S24 (Android 14), Xiaomi Redmi Note 13 (Android 14), iPhone 13 (iOS 18).

This kind of product appeals to me because it is pure execution quality: tiny scope, high reliability, and real-world usage pressure where details truly matter.

----

Next step
If this aligns, I can start with M1 immediately and share the exact 50-cycle test matrix in the first PR.
