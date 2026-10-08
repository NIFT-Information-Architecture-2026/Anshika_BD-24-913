# Paw ResQ: Low-Fidelity Wireframes & User Flows (Phase 4)

## 1. Overview
This document specifies the structural wireframes, layout logic, and user flows for **Paw ResQ**, incorporating the mandatory location-first architecture, dual user perspectives (Bystander vs. Helper), Guest SOS emergency flow, clean bottom navigation bar, voice-command transcription engine, and detailed step-by-step page designs.

---

## 2. Non-Skippable Location & Guest SOS Flow
```mermaid
flowchart TD
    AppLaunch["App Opened (Guest or Logged In)"] --> GPS["Auto-Detect GPS Location"]
    GPS --> LocationConfirm{"Location Detected?"}
    
    LocationConfirm -- Yes --> LockPin["Lock Location Pin in Top Header"]
    LocationConfirm -- No --> ManualPin["Mandatory Location Selection Modal"]
    
    LockPin --> Home["Home Screen"]
    ManualPin --> Home
    
    Home --> SOSClick["Tap: Found an Animal (SOS)"]
    SOSClick --> FastReport["Guest Emergency SOS Form (Supports Voice SOS Dictation)"]
    FastReport --> PhoneOTP["Quick 1-Tap Phone OTP Verification"]
    PhoneOTP --> Dispatch["Dispatch Multi-Broadcast Alert"]
```

---

## 3. Clean Bottom Navigation Bar Schema

```
+-----------------------------------------------------------------------+
|  [ 🏠 Home ]    [ 🔍 Search ]    [ 🚨 Quick SOS ]    [ 💬 Chat ]    [ 👤 Profile ]  |
+-----------------------------------------------------------------------+
```

---

## 4. Home Screen Interface: Dual Perspective Layouts

### Perspective A: The Reporter / Bystander (Finding an Animal)

```
+-------------------------------------------------------------+
| [Profile / Sign In]   📍 Hitech City, Hyd   [🔔]  [🗺️ Map]  |
+-------------------------------------------------------------+
|                                                             |
|   +-----------------------------------------------------+   |
|   | 🚨 FOUND AN INJURED ANIMAL (HERO SOS CARD)          |   |
|   |    Tap for Immediate Location-Based Help            |   |
|   |    🎙️ [Hold to Speak Voice SOS]                     |   |
|   +-----------------------------------------------------+   |
|                                                             |
|   +--------------------------+  +-----------------------+   |
|   | 🛟 ACTIVE RESCUES        |  | 🩺 NEARBY VETS        |   |
|   |    Track ongoing cases   |  |    Emergency clinics  |   |
|   +--------------------------+  +-----------------------+   |
|                                                             |
|   +-----------------------------------------------------+   |
|   | 💡 First-Aid Card: Keep animal warm & quiet          |   |
|   +-----------------------------------------------------+   |
|                                                             |
+-------------------------------------------------------------+
| [🏠 Home]   [🔍 Search]   [🚨 SOS]   [💬 Chat]   [👤 Profile]|
+-------------------------------------------------------------+
```

---

## 5. Page 2: Emergency SOS Flow (With Voice Dictation Engine)

### Bystander Creation Flow
1. **Step 2.1: LOCATION (MANDATORY):** Auto GPS pin lock + Landmark note. Cannot be skipped.
2. **Step 2.2: CONDITION & HAZARD TAGS (MANDATORY):** Select tags OR **Hold Mic Button to Dictate** (e.g., *"Injured dog bleeding near banyan tree"* ➔ AI auto-selects `Dog` + `Bleeding` tags + transcribes text).
3. **Step 2.3: RECIPIENT SELECTOR (MANDATORY):** Multi-select (Volunteers, NGOs, Vets, Transport). Cannot be skipped.
4. **Step 2.4: PHOTO UPLOAD (OPTIONAL):** Upload photo or tap `[ SKIP & DISPATCH INSTANTLY ]`.

---

## 6. Page 3: Search & Directory Screen (`[ 🔍 Search ]` Tab)

```
+-------------------------------------------------------------+
| 🔍 [ Search Vets, NGOs, Rescuers...       ]   [⚙️ Filter]   |
+-------------------------------------------------------------+
| ( [All]  [🟢 Open 24/7]  [🩺 Vets]  [🏢 NGOs]  [🏠 Shelters] )|
+-------------------------------------------------------------+
| 📍 Results within 5 km of Hitech City        [🗺️ Map View] |
+-------------------------------------------------------------+
|                                                             |
|  +-------------------------------------------------------+  |
|  | 🩺 Dr. Sharma Emergency Pet Clinic   🟢 Open 24/7     |  |
|  |    Verified Vet ✓ | ★ 4.9 (140 reviews) | 1.2 km away |  |
|  |    [📞 Call Now]    [💬 Chat]    [⭐️ Write Review]     |  |
|  +-------------------------------------------------------+  |
|                                                             |
+-------------------------------------------------------------+
| [🏠 Home]   [🔍 Search]   [🚨 SOS]   [💬 Chat]   [👤 Profile]|
+-------------------------------------------------------------+
```

---

## 7. Page 4: In-App Chat & Communication Console (With Voice & Transcription)

```
+-------------------------------------------------------------+
| [←]  Rahul M. (Volunteer) 🟢 En Route (4 mins)  [📞 Call]   |
+-------------------------------------------------------------+
| 🤖 [System]: SOS Alert accepted by Rahul M.                 |
|                                                             |
| [Bystander - Voice Message]:                                |
| 🔊 ▶ [•••••••••••••••••] 0:12 sec                          |
| 📄 Transcribed Text: "He is moving towards the tea stall   |
|    near pillar 14, please hurry."                           |
|                                                             |
| [Helper]: "Got it, I am turning into the street now."       |
|                                                             |
| +---------------------------------------------------------+ |
| | Quick Actions: [📸 Add Photo] [📍 Re-send Pin] [🤝 Arrived]| |
| +---------------------------------------------------------+ |
| | Type a message...                        | 🎙️ | [▶]     | |
+-------------------------------------------------------------+
| [🏠 Home]   [🔍 Search]   [🚨 SOS]   [💬 Chat]   [👤 Profile]|
+-------------------------------------------------------------+
```

---

## 8. Page 5: Profile & Impact History Screen (`[ 👤 Profile ]` Tab)

### Overview
Page 5 handles user identity, rescue impact metrics, credential verification for helpers, and historical tracking of all past animals helped.

```
+-------------------------------------------------------------+
| [⚙️ Settings]                MY PROFILE         [🔔 Notifications]|
+-------------------------------------------------------------+
|                                                             |
|    ( 👤 Avatar )   Priyanka Sharma                          |
|                    📍 Hitech City, Hyderabad                |
|                    🎖️ Life Saver Level 2 (3 Animals Saved)  |
|                                                             |
| +---------------------------------------------------------+ |
| | 🏅 COMMUNITY BADGES: [🐾 First Responder] [❤️ Caretaker]| |
| +---------------------------------------------------------+ |
|                                                             |
|  --- 📜 PAST ANIMALS HELPED (RESCUE LOGS) ---              |
|                                                             |
|  +-------------------------------------------------------+  |
|  | 🐶 "Tommy" (Brown Street Dog)       🟢 Recovered & Adopted|  |
|  |    Reported: Sep 24, 2026 | Rescuer: Rahul M.         |  |
|  |    🖼️ [View Recovery Photos & Health Updates]        |  |
|  +-------------------------------------------------------+  |
|                                                             |
|  +-------------------------------------------------------+  |
|  | 🐱 Injured Kitten                   🟡 Under Treatment   |  |
|  |    Reported: Oct 02, 2026 | Clinic: Dr. Sharma Pet    |  |
|  |    🖼️ [View Clinic Case Progress]                      |  |
|  +-------------------------------------------------------+  |
|                                                             |
|  --- 🛡️ HELPER VERIFICATION PORTAL ---                      |
|  +-------------------------------------------------------+  |
|  | Want to respond to rescues as a Volunteer, NGO, or Vet?|  |
|  | [ 📄 Submit Govt ID / Medical License for Verification ]|  |
|  +-------------------------------------------------------+  |
|                                                             |
+-------------------------------------------------------------+
| [🏠 Home]   [🔍 Search]   [🚨 SOS]   [💬 Chat]   [👤 Profile]|
+-------------------------------------------------------------+
```

### Key Components of Page 5:
1. **User Identity & Impact Dashboard:** Displays user name, location, impact level (e.g. *Life Saver Level 2 — 3 Animals Saved*), and community badges.
2. **Past Animals Helped Timeline (Case Logs):** Detailed history cards for every rescue initiated by the user, featuring real-time recovery status (`🟢 Recovered & Adopted`, `🟡 Under Treatment`, `🔵 Sheltered`) and recovery photos uploaded by shelters/vets.
3. **Helper Verification Portal:** Allows volunteers, NGOs, and vets to upload Aadhaar/Govt ID, NGO registration certificates, or medical licenses to earn the **Verified Helper Badge ✓**.
4. **App Settings & Preferences:** Location radius settings, notification preferences, and emergency hotlines.
