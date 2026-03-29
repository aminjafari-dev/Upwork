# Business ideas — Health triage app (demo sprint)

## Business summary

They are building a **clinical health triage** product: users go through **questions and symptom inputs**, and the app follows **predefined logic** to route them (e.g. urgency level, next step, or care pathway). The **business goal right now** is a **credible stakeholder demo on Monday (CET)**, not a full clinical launch. Money model later may be B2B (providers, insurers, employers) or B2C; the immediate need is **trust + flow clarity** in the room.

---

## Competitors

**Direct (same job-to-be-done: “help me decide what to do when I feel unwell”)**  

- **NHS 111 / regional triage lines and apps** — trusted public triage patterns users already know.  
- **Babylon / similar digital triage assistants** — structured questionnaires + routing (brand and regulation heavy).  
- **Symptom checker features inside insurer or telehealth apps** — same core loop: questions → outcome.

**Indirect (substitutes)**  

- **Search (“Google my symptoms”)** — fast but noisy; your product wins on **structured, consistent** paths.  
- **Booking a GP / urgent care without triage** — your product wins if it **reduces wrong-channel visits** in the story they tell investors.

*Assumptions:* Exact market and regulatory class are unknown; ideas below focus on **demo readiness** and **delivery risk**, not claims about diagnosis.

---

## Similar business examples

- **Public health symptom checkers** — succeed when the **path feels calm**, **steps are short**, and **outcomes are plain language**.  
- **Onboarding-heavy fintech or insurance apps** — same skill: **branching forms**, **state**, **back button behavior**, **no dead ends**.  
- **Clinical decision support (CDS) demos** — stakeholders react to **traceability**: “if user answers X, we show Y because…”

---

## Personalized ideas for this project

### Quick wins (can apply now)

1. **Frozen “demo script” build** — Lock one golden path (and 1–2 edge paths) as the only scenarios shown Monday; hide unfinished branches behind a dev flag.
  - **Why:** Maximizes polish where eyes will go. **Effort:** low. **Impact:** high.
2. **Single source of truth for triage rules** — Move branching data to one config/module so symptom logic and UI stay in sync.
  - **Why:** Stops “fixed in UI, broken in logic” bugs under time pressure. **Effort:** medium. **Impact:** high.
3. **Questionnaire state checklist** — Persist step index + answers; define behavior for back, kill app, and rotate.
  - **Why:** Demo-killer bugs are usually **navigation/state**, not missing pixels. **Effort:** low–medium. **Impact:** high.

### Mid-term improvements

1. **Outcome screen template** — One consistent layout for all endpoints (what it means, what to do next, disclaimers).
  - **Why:** Looks product-ready; easier for stakeholders to compare severities. **Effort:** medium. **Impact:** medium.
2. **Lightweight “decision trace” for demo mode** — Optional panel or log: last N answers + rule id / branch name (no PHI).
  - **Why:** Clinical audiences trust **auditability** more than animations. **Effort:** medium. **Impact:** medium.

### Growth ideas (scale and differentiation)

1. **Localization-ready copy layer** — Even if only English Monday, externalize strings for EU/Sweden story later.
  - **Why:** Matches Göteborg/EU positioning without redoing UI. **Effort:** medium. **Impact:** medium (longer term).
2. **Analytics hooks on nodes** — Event per question + outcome (privacy-safe).
  - **Why:** After demo, they can see **drop-off** and tune flows. **Effort:** medium. **Impact:** medium.

---

## Next best action (for them / for your collaboration)

1. **After NDA:** Get repo access, 15-minute Loom or call: “these 3 screens must work Monday.”
2. **Write a one-page demo scope:** in-scope paths, out-of-scope branches, definition of “done.”
3. **Daily (or twice daily) async demo video** from now through Monday CET — reduces mismatch and last-hour panic.

