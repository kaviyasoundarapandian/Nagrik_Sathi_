# Nagrik Sathi: Test Cases

**Environment:** Chrome (Android and desktop), served over http://localhost or https. Test with a real phone for GPS, SMS and voice.

| ID | Feature | Steps | Expected result | Status |
|---|---|---|---|---|
| TC01 | App load | Open app URL | Home screen loads, no console errors | |
| TC02 | Install PWA | Use "Install app" in browser menu | App installs and opens full screen | |
| TC03 | Offline | Load once, enable airplane mode, reopen | App shell opens; safety steps and helplines visible | |
| TC04 | Guest access | Choose "Continue as guest" | Home opens without login | |
| TC05 | Profile password | Create profile, set password, reload, sign in | Correct password signs in; wrong password is rejected | |
| TC06 | SOS | Add contact from sample data, tap SOS, allow location | SMS app opens with message and location link | |
| TC07 | Call 112 | Tap the 112 button | Dialer opens with 112 | |
| TC08 | Disaster alert | Allow location, open alerts | 3-day forecast with risk level and safety steps | |
| TC09 | Alert offline | Open alerts with no network | Cached or offline safety steps shown; no crash | |
| TC10 | Report problem | Fill report, attach photo, save | Report appears in saved list; stays after reload | |
| TC11 | Photo privacy | Attach photo with GPS EXIF, save | Saved photo has no location metadata | |
| TC12 | Language switch | Select Hindi, then Tamil | Interface text changes | |
| TC13 | Unsupported language | Select Bodo | Hindi fallback and Bhashini link shown | |
| TC14 | Voice assistant | Say "Hi Bharat" and ask for helplines | Assistant responds in speech and text | |
| TC15 | Official links | Open 10 random service links | All open official `.gov.in` or approved sites | |
| TC16 | Helplines | Check 112, 1091, 181, 1098, 14567 | Numbers match official sources | |
| TC17 | Accessibility | Enable large text and high contrast | Layout stays readable, no overlap | |
| TC18 | Permission denied | Deny location, tap SOS | Clear message; app does not crash | |
| TC19 | Low-end device | Run on 2 GB RAM phone with 3G speed | Loads and responds smoothly | |
| TC20 | Dark mode | Switch device to dark theme | Colours switch correctly | |

Record Pass/Fail in the Status column and note the device and browser version.
