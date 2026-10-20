---
title: Privacy by Design
permalink: /privacy-by-design/
---

# Privacy by Design — FMP Tracker

How FMP Tracker's design maps to the seven foundational principles of
Privacy by Design (Ann Cavoukian, Information and Privacy Commissioner of
Ontario) and to the privacy-by-default requirement in Quebec's Law 25.

*Last updated: October 20, 2026, for version 1.0.0. A design record, not legal
advice or a certification.* FMP Tracker is not affiliated with or endorsed by the Information and Privacy Commissioner of Ontario, Ann Cavoukian, or the Commission d’accès à l’information du Québec.

## Summary

FMP Tracker processes everything on the user's iPhone. It has no server, no
account, no analytics, no advertising, no crash reporting, and no third-party
software that transmits data. The developer receives nothing, which is why the
App Store privacy label reads **"Data Not Collected."** Every optional data
flow (Apple Health, Apple Watch data, workout reminders) is **off until the
user turns it on**.

## The seven principles

| # | Principle | How FMP Tracker meets it |
|---|---|---|
| 1 | **Proactive not reactive; preventative not remedial** | Privacy was a design constraint before any feature was built: no server, accounts, analytics, crash reporting or third-party purchase services. |
| 2 | **Privacy as the default setting** | Apple Health sync, Apple Watch data and workout reminders are all off on install. Nothing leaves the device unless the user starts it, such as exporting a CSV file or tapping a video link. |
| 3 | **Privacy embedded into design** | All data is stored on the device. Reminders are local notifications; no push token is ever requested. The food database and graphics are bundled with the app, so nothing is downloaded at runtime, and the app contains no network code. |
| 4 | **Full functionality: positive-sum, not zero-sum** | Every feature works offline, with Apple Health off, and without an Apple Watch. Privacy doesn't cost the user features. |
| 5 | **End-to-end security: full lifecycle protection** | Data sits in iOS app storage, protected by the device's encryption and passcode. Exported files are deleted after sharing. **Delete All My Data** removes everything in one step, as does deleting the app. |
| 6 | **Visibility and transparency: keep it open** | A public [privacy policy](../privacy/), the same text inside the app, a "Data Not Collected" App Store label, and Apple Health permission prompts that state exactly what is read and written. Links that open other services are disclosed. |
| 7 | **Respect for user privacy: keep it user-centric** | The user controls everything: export to CSV, delete single entries, delete all data, revoke Apple Health access in iOS Settings. Apple Health access is limited to what features use: read weight, height, heart rate, active energy and workouts; write workouts and weight. |

## Quebec Law 25

### Privacy by default
Law 25 requires that an enterprise offering a technological product to the
public with privacy settings ensure those settings provide **the highest level
of confidentiality by default, without any intervention by the person
concerned**.

Every FMP Tracker setting that would read or share data outside the app's own
storage starts in its most private state:

| Setting | Default | Effect while off |
|---|---|---|
| Apple Health sync | Off | Nothing read from or written to Apple Health |
| Apple Watch data | Off | No heart rate, energy or workout data read |
| Workout reminders | Off | No notification permission requested |
| Apple Watch app | Only if the user installs it on their watch | The workout and logged sets pass directly between the user's iPhone and watch, never through a server |
| CSV export | Never automatic | Created only when the user exports, then deleted |
| Clinician report | Never automatic | A PDF made only when the user asks, shared where they choose, then deleted |

### Other obligations
Most of Law 25's other duties attach to an enterprise that collects personal
information. FMP Tracker collects none, so they largely don't arise:

| Obligation | Status |
|---|---|
| Person in charge of the protection of personal information | No collection; privacy contact published: fmp-tracker-support@protonmail.com |
| Privacy policy in clear, simple terms | [Published](../privacy/) and in the app |
| Privacy impact assessment | Not triggered by the current design; required before adding any feature that collects data |
| Confidentiality incident register and reporting | No data is held, so there is nothing to breach |
| Consent for collection, use and communication | No collection; Apple Health access uses Apple's own per-type consent prompts |
| Automated decisions or profiling | None. Program suggestions are made on the device from the user's own answers and never leave it |

## Keeping it this way

Before any new feature that touches data, it is checked against these
questions: Does data leave the device? Is the default anything but the most
private option? Does it request a new Apple Health type? Does it create files
that aren't deleted after use? Does it add software that transmits data? A
"yes" means updating the privacy policy, the App Store privacy label and this
page first.

## Sources
- Ann Cavoukian, *Privacy by Design: The 7 Foundational Principles*,
  Information and Privacy Commissioner of Ontario.
- *Act respecting the protection of personal information in the private
  sector* (CQLR c P-39.1), as amended by Quebec's Law 25.
- Apple, [App privacy details on the App Store](https://developer.apple.com/app-store/app-privacy-details/).
