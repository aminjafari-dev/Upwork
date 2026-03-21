# Business Ideas: Store + RevenueCat Setup Project

**Clarifying questions (if scope is unclear before work)**

1) Are subscription **product IDs** already fixed in the app/RevenueCat, or can we rename them to match store rules?  
2) Is the app **same bundle ID** on iOS and package name on Android as in the stores already?  
3) Do you need **only subscriptions**, or also consumables/non-renewing IAP?  
4) Which **RevenueCat project** is canonical (staging vs production)?  
5) Who owns **tax, pricing, and base country** decisions in App Store Connect and Play Console?

----

## Business summary

This is a **one-time operational delivery** job: connect an existing React Native/Expo app’s paywall (RevenueCat) to real products in Google Play and App Store Connect, with correct API keys and test paths (Internal Testing + TestFlight). Success means **test users can buy and restore** without code changes. Money for the client comes from **subscription revenue after launch**; this task removes the **blocker** between “integrated SDK” and “live test purchases.”

----

## Competitors

**Direct “competitors” (same problem, different solution):**

- **Doing it without RevenueCat** (native StoreKit + Play Billing only): more custom glue, harder to maintain cross-platform.  
- **Other subscription backends** (e.g. custom server + receipt validation): higher build cost; not what this job uses.

**Indirect substitutes:**

- **Hiring an agency** for full app + payments: overkill for this scope.  
- **Freelancers who only code** but don’t touch consoles: leaves the client stuck on credentials and product mapping.

*Assumption:* Client stays on RevenueCat; this job is about **correct store + RC configuration**, not switching stacks.

----

## Similar business examples

- **SaaS-style mobile apps** (fitness, learning): subscription in Play/App Store + RevenueCat for entitlements and experiments.  
- **Newsletter or creator apps**: same pattern—products defined in stores, **single source of truth** in RevenueCat Offerings.  
What works: **one entitlement** (e.g. `pro`), **products** attached per store, **one current offering** for the paywall.

----

## Personalized ideas for this project

### Quick wins (apply now)

| Idea | Why it helps | Effort | Impact |
|------|----------------|--------|--------|
| Document **product ID map** (Play ↔ App Store ↔ RevenueCat) in one sheet | Stops mismatches that break purchases | Low | High |
| Use **Internal Testing** + **TestFlight** with a **checklist** (license testers, sandbox Apple ID) | Faster verification; fewer “it works on my device” loops | Low | High |
| Confirm **Expo public env** only has **public** RC keys; no secret keys in app | Security and review safety | Low | High |

### Mid-term improvements

| Idea | Why it helps | Effort | Impact |
|------|----------------|--------|--------|
| Add **RevenueCat dashboard** notes + screenshots for the client handoff | They can onboard the next dev without re-doing discovery | Medium | Medium |
| Plan **staging vs production** offerings (if they use both) | Avoids shipping test products by mistake | Medium | Medium |

### Growth ideas (scale / differentiation)

| Idea | Why it helps | Effort | Impact |
|------|----------------|--------|--------|
| Use RevenueCat **experiments** on paywall copy after launch | Improves conversion without app releases | Medium | High |
| Align **web** or **other platforms** later under same entitlements | One entitlement story across products | High | Medium |

----

## Next best action

1. Accept scope: **stores + RevenueCat only**, verification on Internal Testing + TestFlight, deliver **public keys** and a short handoff doc.  
2. Before invites: align on **bundle ID, package name, and product IDs** already in the app.  
3. After access: **Play service account → RC**, **App Store shared secret / App Store Connect API key → RC**, then **mirror products and offerings** and run one purchase on each platform.
