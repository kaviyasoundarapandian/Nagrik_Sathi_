# Nagrik Sathi

One multilingual, offline-ready citizen app for safety, disaster alerts and government services.

- **Team:** Nagrik Sathi (HSC|TN|00977), Tamil Nadu
- **Theme:** Governance & Civic Technology
- **Type:** Installable Progressive Web App (single file, no backend)

## Problem
Emergency help, complaints, schemes, exams and documents are scattered across many portals and helplines. Rural, elderly, disabled and low-literacy citizens face language and internet gaps, and fake sites target people searching for services.

## Features
- **One-tap SOS:** prefilled SMS with live location to trusted contacts, plus direct call to 112
- **Disaster alerts:** 3-day forecast-based alerts (Open-Meteo) and offline safety steps for flood, cyclone, earthquake, fire and heat
- **Report a problem:** anonymous civic reports with photo and GPS; photo location metadata is stripped
- **Official-service gateway:** schemes, exams, pension, documents, bills and helplines linking to official `.gov.in` sites
- **22 Indian languages** and a hands-free **"Hi Bharat"** voice assistant
- **Inclusive design:** sign-language help, live captions, large text, high contrast
- **Privacy first:** no server; data stays on the device; optional local profile protected with a password (PBKDF2)

## Quick start
No installation or build is needed.

1. Clone: `git clone https://github.com/kaviyasoundarapandian/Nagriksathi.git`
2. Serve the folder (a service worker needs http/https, not `file://`):
   ```bash
   cd Nagriksathi
   python3 -m http.server 8000
   ```
3. Open `http://localhost:8000` in Chrome or Edge on desktop or Android.
4. Optional: use the browser's "Install app" / "Add to Home screen".

The same `index.html` is also packaged inside the Android APK (`assets/index.html`) using an Android Studio WebView wrapper.

## Environment variables
None. The app needs no API keys or secrets. The only external data call is the free Open-Meteo forecast API, which needs no key.

## Browser permissions used
Location (SOS, alerts, places), microphone (voice assistant), motion sensor (shake detection), storage (reports and profile). Every permission is requested only when the feature is used.

## Project structure
```
index.html          Complete app (HTML, CSS, JavaScript)
docs/DESIGN.md      Technical design and architecture diagrams
tests/TEST_CASES.md Manual test cases
tests/sample_data.json  Sample data for testing
LICENSE             MIT License
```

## Testing
See [tests/TEST_CASES.md](tests/TEST_CASES.md) and [tests/sample_data.json](tests/sample_data.json).

## Limitations
- A web app cannot send SMS silently or run while closed; SOS opens a prefilled SMS and the 112 call for the user to confirm.
- Forecast alerts are indicative and are **not** official warnings. Always check IMD, Sachet and NDMA.
- Helpline numbers and portal links can change; confirm on the official site.
- Some languages (for example Bodo) fall back to Hindi, with a Bhashini link.

## Roadmap
Native wrapper with push alerts, CAP alert feed, optional district dashboard, community-reviewed translations.

## Data sources and references
Open-Meteo, IMD, NDMA Sachet, myScheme, UMANG, DigiLocker, CPGRAMS, Bhashini, UN SDGs.

## License
MIT. See [LICENSE](LICENSE).
