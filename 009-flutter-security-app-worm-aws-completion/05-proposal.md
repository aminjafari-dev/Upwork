# Upwork Proposal — Senior Flutter (Security, WORM, AWS, Twilio)

**Title:** Finish the prototype without breaking background evidence + uploads

----

**Main risk and solution**

The biggest project risk is a **background capture + continuous upload** path that fails on **low-RAM Android**, **network drops**, or **OS limits** — then alerts and SOS look fine while **evidence gaps** break trust. I prevent that with a **checkpointed upload queue**, **multipart + retry**, **encrypted local spool**, and **S3 Object Lock / IAM** aligned to your retention model, tested on a **2GB-class device** early.

----

**Quick project questions**

1) **Regions & compliance** — Which countries and app stores matter first, and do you already have **legal sign-off** on how recording and notifications must behave there?  
2) **AWS shape** — Single bucket with Object Lock, **KMS** expectations, and approximate **max session length / file size** per user?  
3) **WhatsApp** — Do you already have a **Meta Business** asset and **approved use case**, or should I include **Twilio + Meta** setup time in the estimate?  
4) **Companion vs FCM-only** — Is the “trusted contacts” side **one Flutter app** plus backend, or **FCM to existing phones** only for MVP?

----

**Why I fit**

- **Flutter production delivery** — Provider-based apps, platform channels where native foreground services and camera/audio stacks need tight control, release builds with **obfuscation** and secrets out of source.  
- **Cloud + messaging** — **S3** immutable patterns, presigned flows, and **Twilio** error/retry design; lightweight **Firebase Functions** or similar for FCM triggers when needed.

----

**Plan**

- **Milestone 1:** Audit repo under NDA; profile current capture/upload/sensors on a low-RAM device; fix the **queue + resume** path first.  
- **Milestone 2:** Android **foreground service** + background sensor policy; geofencing/stop rules with tuning knobs.  
- **Milestone 3:** **Twilio WhatsApp** production cutover, idempotent retries, monitoring hooks.  
- **Milestone 4:** Security pass (root detection, SOS hardening, key management), **FCM/trusted push** path, docs, signed **APK** (+ **IPA** if we scope iOS).

----

**Direct answers**

- **Timeline:** **6–10 weeks** part-time for core production hardening, depending on NDA access and WhatsApp/Meta readiness; **1–3 months** matches scope if we add iOS and companion backend depth.  
- **Budget / rate:** Your **$40–70/hr** range works; I’ll give a **hour range per milestone** after a short technical review under NDA.  
- **State management:** Stay on **Provider** unless profiling shows a clear bottleneck — then we isolate **notifiers** or move hot paths to **smaller granular models** before a full rewrite.  
- **Start date:** Within **3–5 business days** of signed contract + NDA/repo access.  
- **Weekly hours:** **15–25 hrs/week** typical for me on hourly safety-critical work; can flex toward **under 30** as you prefer.

----

**Next step**

Send the **NDA** and (if possible) a **5-minute Loom** of the current build on Android — I’ll reply with a **milestone quote in hours** and the **top 5 technical risks** from the recording.
