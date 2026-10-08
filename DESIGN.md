# Paw ResQ: Visual Design System & Tokens (Phase 5)

## 1. Brand Identity & Aesthetic Philosophy
**Paw ResQ** balances **emergency urgency** with **warm human empathy**. Unlike cold clinical medical apps or harsh red-alert security tools, Paw ResQ utilizes a soft, organic, and welcoming color palette designed to calm a panicked bystander while maintaining high legibility under pressure.

* **Core Aesthetic Keywords:** *Compassionate Warmth, Calm Resilience, High Visibility, Human Connection.*

---

## 2. Color Palette & UI Design Tokens

### Color Tokens

| Token Name | Hex Code | Color Preview | Purpose / UI Application |
| :--- | :--- | :--- | :--- |
| `color-primary-amber` | `#E06D53` | 🟠 Warm Terracotta | Primary Hero Buttons, Brand Headers, Main Navigation Icons |
| `color-emergency-coral` | `#D94E34` | 🔴 Emergency Coral | High-priority SOS Button, Bleeding/Critical Severity Badges |
| `color-healing-sage` | `#5E9B7E` | 🟢 Sage Green | Verified Badges, Open 24/7 Status, Helper Accepted Banner |
| `color-bg-cream` | `#FAF7F2` | 🐚 Soothing Cream | Global App Background (Soft, low glare, comforting) |
| `color-surface-white` | `#FFFFFF` | ⚪ Warm White | Card Containers, Modals, Input Fields |
| `color-text-primary` | `#2B2B2B` | ⬛ Deep Charcoal | Primary Headings, Title Text (High Contrast Legibility) |
| `color-text-secondary` | `#6E6A66` | 🩶 Muted Taupe | Subtitles, Metadata, Distance & Timestamp Labels |
| `color-border-subtle` | `#E6E0D8` | 🔲 Soft Border | Card Outlines, Divider Lines |

---

## 3. Typography Hierarchy & Font Tokens

* **Primary Font Family:** `Plus Jakarta Sans` or `Inter` (Humanist, highly accessible sans-serif font designed for screen legibility).

| Style Level | Font Weight | Size | Line Height | Application |
| :--- | :--- | :--- | :--- | :--- |
| **Heading 1 (H1)** | Bold (700) | 26px / 1.6 rem | 32px | Screen Titles, Main SOS Alert Banners |
| **Heading 2 (H2)** | SemiBold (600) | 20px / 1.25 rem | 26px | Card Section Headers, Provider Names |
| **Heading 3 (H3)** | Medium (500) | 16px / 1.0 rem | 22px | Subheaders, Input Labels, Tab Titles |
| **Body Regular** | Regular (400) | 14px / 0.875 rem | 20px | Chat Messages, Description Text, First-Aid Tips |
| **Microcopy / Badges** | Medium (500) | 12px / 0.75 rem | 16px | Status Pill Badges, Distances, Timestamps |

---

## 4. Microcopy & Tone of Voice Guidelines

| UI Context | Cold / Technical Copy (Avoid) | Paw ResQ Reassuring Microcopy (Use) |
| :--- | :--- | :--- |
| **SOS Confirmation** | "Incident #3409 Submitted to Database." | "Help is on the way! Alerting 8 nearby rescuers..." |
| **Location Detection** | "GPS Position Locked." | "📍 Located near Hitech City. We're pinpointing your help zone." |
| **Helper Acceptance** | "User #92 Accepted Assignment." | " Rahul M. (Verified Volunteer) is en route! ETA ~ 4 mins." |
| **First-Aid Guidance** | "Caution: Risk of rabies infection." | "💡 Keep a safe distance & stay calm. Help is arriving shortly." |

---

## 5. UI Component States & Styling Rules

### 1. Emergency Hero SOS Button (`Hero Button Component`)
* **Shape:** Large 16px Rounded Rectangle with subtle inner padding.
* **Background:** `color-emergency-coral` (`#D94E34`) with soft pulse animation.
* **Text:** Bold White 18px + Microphone icon for Voice Dictation.

### 2. Status & Hazard Badges (`Pill Component`)
* **Shape:** Fully rounded 20px capsule pills.
* **Variants:**
  * `Verified Helper ✓`: Green background (`#5E9B7E`) + White bold text.
  * `Bleeding / Critical`: Red Tint background (`#FCEAE6`) + Dark Red text (`#D94E34`).
  * `Biting Risk ⚠️`: Amber Tint background (`#FFF4E5`) + Dark Amber text (`#B86E00`).

### 3. Card Containers (`Surface Component`)
* **Shape:** 16px Rounded Corners with subtle `1px solid #E6E0D8` border.
* **Shadow:** Soft 4px blur, 2% opacity elevation shadow for depth.
