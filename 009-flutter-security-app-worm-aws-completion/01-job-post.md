# Job Post — Flutter Security App (WORM, AWS, Completion)

**Source:** Upwork (posted ~11 hours ago, worldwide)  
**Client:** Daniele Menichetti — Founder (app name confidential)  
**Engagement:** Hourly **$40–$70**, **under 30 hrs/week**, **1–3 months**, expert, contract-to-hire possible  
**Proposals:** fewer than 5 at time of capture  

---

## Summary (as posted)

Cross-platform **Flutter** app (Android/iOS). **~85% complete prototype**. Seeking **senior Flutter developer** for **completion and optimization**.

---

## Tech stack

- **Framework:** Flutter / Dart  
- **State:** Provider  
- **Local storage:** SharedPreferences  
- **Maps:** flutter_map + OpenStreetMap + OpenRouteService  
- **Notifications:** flutter_local_notifications  
- **Sensors:** sensors_plus (accelerometer, gyroscope)  
- **Geolocation:** geolocator  
- **Audio:** `record`  
- **Camera:** `camera`  
- **Speech-to-text:** speech_to_text  
- **Email:** EmailJS REST API  
- **Messaging:** Twilio API + CallMeBot fallback  
- **Wakelock:** wakelock_plus  
- **Permissions:** permission_handler  

---

## Work required (critical points)

1. **Simultaneous audio + video recording**  
   Combined recording; background; **no visual notification, no sound** (per post). Uses `camera` + `record`.

2. **Real-time cloud upload (WORM)**  
   Continuous streaming to **AWS S3 Object Lock** or **Azure Immutable Storage**. Immutable (write-once). Upload must survive **device power-off during transmission** (continuous buffer / resume).

3. **Background sensor detection**  
   Accelerometer + gyroscope active when app is backgrounded or screen off. **Android Foreground Service** required (currently foreground-only).

4. **Dynamic geofencing**  
   Monitor deviation from preset route; alert if **anomalous stop ~30s** in area not on planned route. Suggested: Google Maps Geofencing API or custom stream with geolocator.

5. **Twilio WhatsApp — production**  
   Move from **Sandbox** to **Meta-approved WhatsApp Business** number; sending without recipient opt-in (per post). Error handling + automatic retry.

6. **Performance**  
   Smooth on **~2GB RAM**, entry-level CPU; fewer unnecessary rebuilds; optimize sensor sampling.

7. **Security and obfuscation**  
   No hardcoded API keys in production; release **code obfuscation**; protect active SOS screen (back, screenshots, screen recording); **root detection**.

8. **Push to trusted contacts**  
   Real-time push via **companion app or FCM**; lightweight backend (**Firebase Functions** or equivalent).

---

## Deliverables

- Complete, documented Flutter source  
- Signed, optimized release **APK**  
- **IPA** if iOS experience available  
- API integrations documentation  
- Correct `.gitignore` and secrets protection  

---

## Notes

- Source shared **after NDA**  
- **All rights** to client  
- **Post-launch** availability for updates/maintenance  

---

## Application ask

Portfolio with **similar apps**, documented Flutter experience, **detailed quote**.

---

## Skills tagged

Application Security, AWS Application (and related Flutter/mobile stack from post).
