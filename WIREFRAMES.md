# Paw ResQ: Low-Fidelity Wireframes & User Flows (Phase 4)

## 1. Overview
This document specifies the structural wireframes, layout logic, and user flows for **Paw ResQ**, incorporating the mandatory location-first architecture, dual user perspectives (Bystander vs. Helper), and top/bottom navigation layouts.

---

## 2. Non-Skippable Location Mandate Architecture
```
[ App Launch ]
      │
      ▼
[ Auto-Detect GPS Location ] ─── (Success) ───► [ Lock Geolocation Pin in Top Header ]
      │
   (Fails / Permission Disabled)
      │
      ▼
[ Full-Screen Mandatory Location Modal: "Paw ResQ requires location to connect you with nearby help" ]
```

---

## 3. Home Screen Interface: Dual Perspective Analysis

### Perspective A: The Reporter / Bystander (Finding an Animal)
* **Primary Need:** Maximum speed, zero friction, obvious primary emergency call-to-action.
* **Header:** Profile indicator (left), Notification bell + Map pin locator (right). Current detected address displayed in top banner.
* **Body Action Cards:**
  1. 🚨 **Found an Animal** *(Primary Highlighted Card - Triggers Emergency Form)*
  2. 🛟 **Active Rescues** *(Tracks status of previously reported rescues)*
  3. 🩺 **Nearby Vets** *(Quick map/list view of emergency clinics)*
* **Bottom Bar:** Search bar in center, In-app chat box icon in corner.

---

### Perspective B: The Helper / Responder (Volunteer, NGO, Vet)
* **Primary Need:** Immediate awareness of incoming emergency pings in their area, status toggles (Available / Offline).
* **Header:** Helper Profile with Verified Badge (left), Active Rescue Alerts counter + Map View of open cases (right).
* **Body Action Cards:**
  1. ⚡ **Incoming Emergency Alerts** *(List of nearby open animal reports needing help)*
  2. 🩺 **Vet / Shelter Status** *(Update clinic availability or transport capacity)*
  3. 📋 **Assigned Cases** *(Current active rescues being handled)*
* **Bottom Bar:** Search bar in center, Direct Chat with Bystanders in corner.

---

## 4. Textual Low-Fidelity Layout: Home Screen (Bystander View)

```
+-------------------------------------------------------------+
| [Avatar / Sign Up]   📍 Hitech City, Hyd    [🔔]  [🗺️ Map]  |
+-------------------------------------------------------------+
|                                                             |
|   +-----------------------------------------------------+   |
|   | 🚨 FOUND AN INJURED ANIMAL                          |   |
|   |    Tap for Immediate Location-Based Help            |   |
|   +-----------------------------------------------------+   |
|                                                             |
|   +--------------------------+  +-----------------------+   |
|   | 🛟 ACTIVE RESCUES        |  | 🩺 NEARBY VETS        |   |
|   |    Track ongoing cases   |  |    Emergency clinics  |   |
|   +--------------------------+  +-----------------------+   |
|                                                             |
|   +-----------------------------------------------------+   |
|   | 💡 Quick First-Aid Tip: Do not move animal if bleeding|  |
|   +-----------------------------------------------------+   |
|                                                             |
+-------------------------------------------------------------+
| [ 🔍 Search nearby Vets, NGOs... ]              [ 💬 Chat ] |
+-------------------------------------------------------------+
```

---

## 5. Textual Low-Fidelity Layout: Home Screen (Helper View)

```
+-------------------------------------------------------------+
| [Verified Helper ID]  🟢 Status: Active    [🔔 (3)] [🗺️ Map]  |
+-------------------------------------------------------------+
|                                                             |
|   +-----------------------------------------------------+   |
|   | ⚡ 3 OPEN RESCUE PINGS WITHIN 3 KM                   |   |
|   |    Tap to view details and accept emergency         |   |
|   +-----------------------------------------------------+   |
|                                                             |
|   +--------------------------+  +-----------------------+   |
|   | 📋 MY ASSIGNED CASES     |  | 🚑 TRANSPORT STATUS   |   |
|   |    2 Active Handoffs     |  |    Ambulance Ready    |   |
|   +--------------------------+  +-----------------------+   |
|                                                             |
+-------------------------------------------------------------+
| [ 🔍 Search Rescues, Cases... ]                 [ 💬 Chat ] |
+-------------------------------------------------------------+
```
