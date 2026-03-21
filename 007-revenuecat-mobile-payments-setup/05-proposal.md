# Proposal: RevenueCat + Google Play + App Store Setup

yeah!

----

## Main risk and solution

The usual failure is **not** the RevenueCat SDK—it is **mismatched product IDs** (Play base plans, App Store subscription SKUs, and RevenueCat products/offerings) or **incomplete Apple agreements**. I fix that by **mapping every ID** before linking accounts, then verifying **purchase + restore** on Internal Testing and TestFlight.

----

## Quick project questions

1) What are your **Android package name** and **iOS bundle ID** as they exist in the stores today?  
2) Can you paste the **exact subscription product IDs** (or a screenshot) from the app and/or current RevenueCat dashboard?  
3) Is **Apple Paid Applications** + **banking/tax** already complete for this app?  
4) Do you use **one entitlement** (e.g. `pro`) for all tiers, or several?

----

## Why I fit

- **IAP + RevenueCat:** I connect Play (service account JSON, subscriptions, testers) and App Store Connect (subscriptions, sandbox, TestFlight path) to RevenueCat **entitlements, products, and offerings** so they match your paywall.  
- **React Native / Expo:** Your app is SDK-ready; I deliver the **public** `goog_...` and `appl_...` keys for `.env` / EAS build—no secret keys in the client.

----

## Plan

**Milestone 1:** Play Console—subscriptions, license testers, Internal Testing; service account JSON; linked in RevenueCat.  
**Milestone 2:** App Store Connect—subscription group + products; agreements checked; sandbox + TestFlight path; RevenueCat linked.  
**Milestone 3:** RevenueCat—apps, entitlements, products, offerings aligned with both stores.  
**Milestone 4:** Hand you **public API keys**, env variable names, and a short **verification checklist**; confirm purchases on both platforms; **remove my access**.

----

## Direct answers

**Timeline:** About **3–5 business days** depending on Apple agreement status and how fast testers are ready (often same week if IDs are clear).  
**Budget:** **$120** fixed matches your post; if scope grows (many products, regions, or extra environments), we align before work.  
**Native Express / coding:** Not required for this task. I have **React Native + Expo** context; happy to help if you add code later.  
**Weekly hours:** N/A for a one-time setup; **as needed** for invites and a short verification call.  
**Start:** Within **1–2 days** of accepted contract and access.

----

## Next step

Send **admin invites** to the email you want on file + your **product ID list** and **bundle/package names**—I will reply with anything missing before I change production settings.
