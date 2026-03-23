# Zenzo Ads — Project risks (client view) and mitigations

This document is written for **you as the client** and your **product/engineering** partners. Each risk is **what can go wrong**, then **what to do about it** in practical terms.

----

## 1) Scope creep: trying to match Meta/TikTok in v1

**Risk:** The product list (OTP, social login, image + **video**, targeting, analytics, payments, web + mobile) **sounds** like one release. In reality, each layer hides **weeks** of integration work. Teams that chase parity **ship late** or ship **broken dashboards**.

**Mitigation:** Publish a **written MVP** with **one primary advertiser outcome** (for example: “traffic to a URL”). Rank features as **MVP / phase 2 / later**. **Video**, **advanced segments**, and **full web** are common **phase 2** items unless you have extra budget and a backend already in place.

----

## 2) Weak trust: metrics or spend feel wrong

**Risk:** Diaspora advertisers compare Zenzo to tools they already use. If **views** and **clicks** don’t match intuition, or **spend** is hard to reconcile, **churn** happens quietly—before you get product feedback.

**Mitigation:** Define **one glossary** for v1: what counts as an **impression**, a **click**, and **billable spend**. Implement **server-side** rules where possible (don’t trust the client only). Add **daily** spend caps and **receipts** early. Run **3–5 real campaigns** with small budgets before public launch.

----

## 3) “Community” targeting is vague in data

**Risk:** “Community” is your **differentiator**, but if it is **undefined** (no taxonomy, no source, no review), targeting becomes **guesswork** or **offensive** (wrong assumptions).

**Mitigation:** Ship **v0** as a **curated list** (languages, regions, interest tags you approve). Document **how** a community gets on the list. Plan **moderation** for sensitive categories (politics, money, charities) before you scale spend.

----

## 4) Payments and reconciliation errors

**Risk:** Ad spend touches **real money**. Failed cards, **double charges**, currency confusion, or **webhook** bugs create support load and **legal** exposure.

**Mitigation:** Choose **one PSP** and **one** money model for MVP (for example **prepaid wallet** or **card per campaign**). Make **webhooks** **idempotent**. Keep a **ledger** on the server; never put **secret keys** in mobile apps. Write a **one-page refund** policy for platform errors.

----

## 5) Fraud, bots, and click inflation (even at small scale)

**Risk:** Any public ad surface attracts **bots** and **accidental** double counts. You cannot stop **all** fraud in MVP, but **obvious** abuse destroys trust.

**Mitigation:** **Rate limits**, basic **server checks**, **anomaly alerts** (CTR spikes, impossible geo jumps). Log **enough** to investigate without storing unnecessary PII. Plan **phase 2** for stronger signals with **legal** review.

----

## 6) Backend and mobile out of sync

**Risk:** If APIs change weekly without versioning, **iOS, Android, and web** drift. Bugs cluster around **edge cases** (paused campaigns, midnight boundaries, timezone).

**Mitigation:** **Version** APIs (`/v1/...`). Freeze **contracts** per milestone. Use **one** source of truth for **campaign state** and **timezone** (usually **UTC** server-side, local display only).

----

## 7) Content and policy: scams, hate, misleading ads

**Risk:** Diaspora communities are **high-trust** networks when healthy—and **high-damage** when bad actors appear. One viral scam ad can **hurt the brand**.

**Mitigation:** **Simple** review rules for v1: categories that require **manual approval**, **report ad** flow, **ban** repeat offenders. Align **terms** with your lawyer for **your** markets.

----

## 8) Design and UX debt

**Risk:** “Clean, modern UI” is easy to promise. Without **components**, **states**, and **empty/error** patterns, the app feels **unfinished** even if APIs work.

**Mitigation:** Use **Figma** (or equivalent) for **core** screens. Build a **small design system** (spacing, type, buttons, cards). **Mobile-first** layouts; don’t block MVP on **perfect** animation.

----

## 9) Dependency risk: inventory (where ads actually show)

**Risk:** A self-serve **builder** without **inventory** is a **demo**. If “where ads appear” is unclear, **delivery** and **reporting** stay hypothetical.

**Mitigation:** Name **one** inventory story for MVP: **your** app/website only, **one** partner, or **sponsored slots** in a feed you control. **Fake** delivery in staging is fine only if everyone agrees it is **staging**.

----

## 10) Team and continuity: knowledge loss between contractors

**Risk:** If only one person knows **how** events are defined or **how** webhooks are wired, **handoffs** are painful. Contract-to-hire helps only if **docs** exist.

**Mitigation:** Require **README**, **env list**, **architecture sketch**, and **runbooks** for payments and releases. **Short weekly** demos with **written** milestone acceptance.

----

## Summary table

| Risk | If ignored | Primary mitigation |
|------|------------|-------------------|
| Scope creep | Late or broken MVP | Written MVP + phases |
| Bad metrics/spend | Silent churn | Glossary + server rules + pilot |
| Vague “community” | Weak targeting / harm | Curated taxonomy + moderation path |
| Payment bugs | Support + legal pain | One PSP model + ledger + policy |
| Fraud | Trust collapse | Limits + alerts + phase 2 plan |
| API drift | Cross-platform bugs | Versioned APIs + stable contracts |
| Bad ads | Brand damage | Policy + review + reporting |
| Weak UX | “Feels cheap” | Design system + states |
| No real inventory | Fake product | Define placement v1 |
| No docs | Handoff failure | Docs + weekly demos |

----

## Next step (for the client)

Pick **one** MVP story and **one** inventory answer, then ask your developer for a **milestone plan** that matches **budget** and **calendar**—with **acceptance criteria** per milestone.
