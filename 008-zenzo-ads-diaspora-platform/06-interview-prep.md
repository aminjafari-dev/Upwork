# Zenzo Ads — Job Interview Prep (Q&A)

## How to use this file

- Keep answers **natural** (20–45 seconds each unless they ask for depth).
- **Edit the profile block below** so every “I” answer matches your real numbers, links, and stack.
- I drafted answers in **your direction** (mobile + APIs + Flutter/Riverpod and React Native/Expo from your other Upwork drafts). Replace anything that does not match you.

----

## Your profile (edit this — facts only)

| Field | Your value |
|--------|------------|
| **Name / how you want to be addressed** | *[Edit]* |
| **Location / timezone** | *[Edit — note: client prefers Europe]* |
| **Years in mobile development** | *[Edit]* |
| **Primary stack** | *[e.g. Flutter + Riverpod; React Native + Expo]* |
| **Backend comfort** | *[e.g. REST/GraphQL, webhooks, Firebase, Supabase, Node]* |
| **Relevant proof (1–2)** | *[App store links, GitHub, case study, Upwork history — edit]* |
| **Payments / subscriptions (if true)** | *[e.g. Stripe, in-app purchases, RevenueCat — edit]* |
| **Analytics (if true)** | *[e.g. custom events, Firebase Analytics, Amplitude — edit]* |

----

## A) Warm-up & fit

### 1) Tell us about yourself and your mobile experience.

**Answer:**  
I’m a mobile developer focused on **production apps that lean on backends**—auth, uploads, dashboards, and payments—not just static screens. I work mainly in **[your stack: Flutter / React Native / native]**, and I care about **clear architecture** so the same APIs can serve **iOS, Android, and later web** without duplicating logic. Outside code, I’m used to **short async updates** and **weekly demos** so product direction stays aligned.

*(Edit the bracketed stack line to your truth.)*

----

### 2) Why are you interested in Zenzo Ads specifically?

**Answer:**  
It sits at the intersection of **product design, data, and trust**. Diaspora audiences are sensitive to **spam and scams**, so the platform has to earn trust through **clean UX and honest metrics**—that is a harder, more interesting problem than a generic content app. I also like that you are aiming for **long-term depth**, not a one-off brochure app.

----

### 3) Our role may grow into contract-to-hire. Is that something you want?

**Answer:**  
I’m open to it **if the product roadmap and working style are a good match**. I would treat the first phase as a **paid trial on both sides**: delivery quality, communication, and whether I enjoy the domain. If we both want to go deeper after a strong MVP, we can discuss **role, timezone overlap, and compensation** openly.

----

## B) Technical — platform & architecture

### 4) Native iOS/Android or cross-platform — what would you use for Zenzo and why?

**Answer:**  
For speed to MVP with **one team**, I’d lean **cross-platform**—**Flutter** or **React Native**—because you need **mobile-first** now and likely **web** soon after. Both can share business logic and API clients. I pick the stack based on **your existing code, your team skills, and performance needs** (especially for **video creatives**). If you already have strong native codebases, I align with that instead of forcing a rewrite.

*(Name your real preference here: Flutter vs RN vs native.)*

----

### 5) How would you structure the MVP so we ship on time without fake “Meta parity”?

**Answer:**  
I’d lock **one advertiser journey**: sign up → add payment → create **text + image** campaign → set **schedule + basic targeting** → launch → see **impressions, clicks, spend** in a dashboard. I’d defer **full video pipeline polish** and **advanced segments** until **tracking and billing** are solid. That reduces the classic failure mode: pretty UI with **untrusted numbers**.

----

### 6) Walk us through how you’d integrate OTP and social login.

**Answer:**  
I’d use a **proven auth provider** you’re comfortable with—**Firebase Auth**, **Supabase Auth**, **Auth0**, or **Cognito**—so OTP delivery, token refresh, and social OAuth are handled safely. Mobile keeps **short-lived tokens**, uses **secure storage** for refresh material, and never logs secrets. Social login would cover **the providers your users actually use**—often Google and Apple on mobile—plus email/phone OTP as a fallback.

*(Name the provider you have real experience with.)*

----

### 7) How do you approach backend/API integration on a project like this?

**Answer:**  
I start from **contracts**: OpenAPI or written endpoints for **campaigns, creatives, targeting, delivery events, billing**. On the client I use **typed models**, **central API layer**, and **consistent error handling** so retries and empty states do not fragment across screens. For heavy work—**billing webhooks, reconciliation**—I prefer clear **server-side** ownership so the app stays thin and auditable.

----

### 8) Ad creatives include image and video. How would you handle uploads and playback?

**Answer:**  
**Images:** compression, size caps, MIME checks, progress UI, retry on failure—usually to **object storage** with **signed URLs**. **Video:** validate duration, size, and format; upload in chunks if needed; generate a **poster frame** for cards in the feed; use **platform players** (Expo AV, video_player, or native) with **adaptive streaming** if you move to HLS later. I would not block MVP on a perfect transcoding pipeline unless you require it—scope that as **phase 2**.

----

## C) Ads domain — analytics, targeting, money

### 9) What experience do you have with ads, analytics, or social-style feeds?

**Answer:**  
I’ve worked on apps where **events and funnels** matter—**custom analytics**, dashboards, and user actions tied to business outcomes. I may not have built a full **Meta-scale ad network**, but I know how to implement **event schemas**, **deduplication basics**, and **honest reporting** so stakeholders trust the dashboard. For Zenzo, I’d partner with you on **definitions** so “view” and “click” mean one thing everywhere.

*(Add one real example: analytics-heavy app, marketplace, content app, etc.)*

----

### 10) How would you define and track impressions, clicks, and engagement?

**Answer:**  
**Impression:** ad becomes eligible and **renders in viewport** for a minimum time (you pick the rule—e.g. 1 second visible). **Click:** verified tap with **navigation to the destination URL** or in-app browser. **Engagement:** could include **video quartiles**, **saves**, or **shares**—but I’d keep MVP to **impressions + clicks + CTR + spend** so advertisers can compare to tools they know. Everything gets a **stable event name** and **server timestamp** so mobile and web do not disagree.

----

### 11) How should we handle payments for ad spend?

**Answer:**  
For MVP, I like a **prepaid wallet or card hold** with **daily spend caps** and **clear receipts**. Technically that is usually **Stripe** (or regional PSP) with **customer + payment method**, then **server-side** ledger for **authorized vs captured** amounts. I keep **webhooks** idempotent and log failures so finance can reconcile. I avoid putting **secret keys** in the mobile app.

*(Say Stripe/other only if you have real experience.)*

----

### 12) Audience targeting: location, community, interests — how do you implement that responsibly?

**Answer:**  
**Location:** coarse geo from **user-consented** signals—**country/region** first; city-level only if privacy policy and consent support it. **Community and interests:** start with a **controlled taxonomy** you maintain (tags, languages, regions) so targeting is explainable and not a black box. I’d avoid **sensitive inference** early and add **review** for categories that could harm trust in diaspora markets.

----

### 13) What about fraud, bots, or click inflation?

**Answer:**  
MVP cannot solve all fraud, but we can reduce obvious issues: **rate limits**, **basic bot filtering** on the server, **anomaly alerts** (CTR spikes, impossible geo jumps), and **refund policy** when delivery breaks. Longer term you’d add **device signals** and stronger validation—without turning the app into spyware; that needs **legal guidance**.

----

## D) Product, UX, and collaboration

### 14) How do you deliver a clean, modern UI without full design from us?

**Answer:**  
I’d propose a **tight design system**: spacing, typography, components, and states (loading/empty/error). If you have **Figma**, I match it. If not, I build **simple, consistent** screens and leave room for a designer to refine later—no random one-off styles. Mobile-first means **thumb reach**, **short forms**, and **obvious primary actions** (“Create campaign,” “Add funds”).

----

### 15) How do you collaborate on product vision when requirements shift?

**Answer:**  
I treat the roadmap as **negotiated**. If scope grows, I return with **impact on time, risk, and cost** before coding. I document **MVP vs phase 2** in writing so everyone sees the same cut line. That protects both sides—especially on a **fixed-price** start.

----

### 16) What is the biggest risk you see in Zenzo Ads?

**Answer:**  
**Trust in metrics and money.** If spend feels wrong or analytics look flaky, advertisers leave—even if the UI looks good. I’d de-risk **event pipeline + billing correctness** early, before chasing feature parity with giant ad platforms.

----

## E) Process, timeline, and commercial

### 17) What timeline do you see for an MVP?

**Answer:**  
Roughly **8–12 weeks** for a credible slice, depending on whether **web** is day-one, how mature the **backend** is, and how far **video** goes in v1. I’d confirm with a **2-week sprint 0** for discovery, API review, and UI skeleton.

*(Adjust weeks to your honest estimate.)*

----

### 18) Our posted budget is $3,500 fixed. What can we realistically get?

**Answer:**  
**$3,500** is enough for a **focused MVP slice** if we keep scope tight—**auth, payments path, campaign creation for text/image, scheduling, basic targeting, core analytics, and hardening**. Broader parity (full video pipeline, advanced segments, web dashboard depth) fits better as **phase 2** with a clear follow-on budget or hourly continuation.

----

### 19) How will you communicate day to day?

**Answer:**  
I prefer **one async channel** (Slack/Discord/Upwork) for daily questions, plus a **short weekly summary**: shipped, blockers, next week. For decisions, I ask **yes/no or A/B** questions so you can answer fast. If you want **live demos**, I’m happy to schedule **predictable** slots.

*(Match your real preference: daily standup vs async.)*

----

### 20) How do you test before release?

**Answer:**  
**Unit tests** for core logic where it pays off, plus **integration tests** on critical flows: auth, pay, create campaign, view dashboard. **Manual QA** on real devices for **iOS and Android**, including poor network and payment failure paths. Before launch, a **release checklist**: store listings, env configs, analytics sanity check.

----

## F) Closing — your questions for them

Use 2–4 of these in the interview (pick what you still do not know).

1. **MVP:** Is **web** required at launch, or can we ship **mobile-first**?  
2. **Inventory:** Where do ads actually **render** in v1—your own app only, partner sites, or both?  
3. **Data:** Who owns **community targeting** lists at launch—manual, partner feed, or user-generated tags?  
4. **Payments:** **Stripe**, local PSP, or **in-app** vs web-only billing?  
5. **Team:** Who is on **backend**, **design**, and **product** on your side?  
6. **Success metric:** What single KPI proves the MVP worked—signups, spend, or repeat campaigns?

----

## Quick crib sheet (30-second “why hire me”)

**Answer:**  
Zenzo wins if **advertisers trust the numbers and the spend**. I focus on **solid API integration, clear MVP scope, and mobile UX** that does not fight the user. I communicate in **small, frequent updates** so we adjust early instead of discovering problems late. **[Close with one sentence tied to your real proof—edit this.]**
