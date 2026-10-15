# Paw ResQ: Visual Design System & Tokens (Phase 5)

## 1. Brand Identity & Aesthetic Philosophy
**Paw ResQ** embodies an **editorial, empathetic, and organic** design language developed under the creative direction of NIFT Fashion Communication. It intentionally rejects cold clinical tech aesthetics and alarming sirens in favor of tactile warmth, high-legibility modernism, and visual calm under pressure.

* **Core Aesthetic Keywords:** *Linen Warmth, Organic Geometry, High-Visibility Coral, Soft-Line Minimalism.*

---

## 2. Color Palette & The 60-30-10 Harmony Rule

To balance the gentle comfort of **Linen** with the welcoming spirit of **Warm Amber** and the urgency of **High-Visibility Coral**, our palette applies the editorial 60-30-10 distribution:

```
┌──────────────────────────────────────┬──────────────────────┬───────────┐
│           60% Base Canvas            │     30% Structure    │10% Accent │
│      Soothing Organic Linen          │  Warm Amber / Earth  │ Hi-Vis    │
│            (#F6F3EE)                 │      (#D87440)       │ Coral     │
│                                      │                      │ (#E04832) │
└──────────────────────────────────────┴──────────────────────┴───────────┘
```

### Color Tokens

| Token Name | Hex Code | Swatch Name | UI Role & Purpose |
| :--- | :--- | :--- | :--- |
| `color-base-linen` | `#F6F3EE` | 🐚 Organic Linen | **60% Primary Canvas:** Screen backgrounds, soft page canvas, glare-free outdoor legibility. |
| `color-surface-card` | `#FFFFFF` | ⚪ Warm White | Card containers, bottom sheets, form input fields. |
| `color-brand-amber` | `#D87440` | 🟠 Warm Amber | **30% Structure:** Secondary buttons, active navigation states, community highlight cards. |
| `color-accent-coral` | `#E04832` | 🔴 High-Vis Coral | **10% Emergency Accent:** Hero SOS button, critical alert badges, live action calls. |
| `color-healing-sage` | `#4F8B71` | 🟢 Healing Sage | Verified responder badges, open 24/7 indicators, safe status tags. |
| `color-text-charcoal`| `#23211F` | ⬛ Deep Earth Charcoal | High-contrast readable typography for headings & body copy. |
| `color-text-muted`   | `#726B64` | 🩶 Soft Clay Taupe | Secondary subtitles, timestamps, distance counters. |
| `color-border-soft`  | `#E8E2D9` | 🔲 Muted Linen Border | Subtle 1px dividers and organic card outlines. |

---

## 3. Typographic System: 2-Typeface Hierarchy

To keep the interface clean, modern, and uncluttered, only **two typefaces** are used across the entire product:

1. **Display & Headings:** `Plus Jakarta Sans` (Bold, contemporary geometric grotesque with humanized curves. Zero calligraphy; 100% bold editorial clarity).
2. **Body & UI Elements:** `Inter` (The world standard for mobile legibility, neutral x-height, rapid scanability under stress).

### Typographic Scale

| Level | Typeface | Weight | Size | Line Height | Usage |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Display H1** | Plus Jakarta Sans | Bold (700) | 26px / 1.6rem | 32px | Screen titles, Emergency Hero Card heading |
| **Card H2** | Plus Jakarta Sans | SemiBold (600)| 20px / 1.25rem| 26px | Provider names, SOS alert titles |
| **Subhead H3** | Plus Jakarta Sans | SemiBold (600)| 16px / 1.0rem | 22px | Section labels, modal headers |
| **Body Regular** | Inter | Regular (400) | 14px / 0.875rem | 20px | Chat messages, first-aid text, explanations |
| **Body Small** | Inter | Medium (500) | 12px / 0.75rem | 16px | Status labels, timestamps, distance badges |

---

## 4. Microcopy & Tone of Voice: Softer Sentence Case

All headings, buttons, and status indicators strictly employ **softer sentence case** rather than harsh, shouting uppercase tokens:

| UI Context | Harsh / Robotic (Avoid) | Paw ResQ Softer Sentence Case (Approved) |
| :--- | :--- | :--- |
| **Emergency Button** | `EMERGENCY SOS NOW` | 🚨 Found an animal |
| **Helper Found** | `RESCUER ASSIGNED` | Helper found: Rahul M. is on the way |
| **Verification** | `VERIFIED NGO` | Verified NGO ✓ |
| **Chat Notice** | `LIVE LOCATION LOCKED` | Live location shared with helper |
| **Empty State** | `NO RESCUES FOUND` | No emergencies in your area right now |

---

## 5. Tactile UI Geometry & Soft-Line Iconography

### 1. Organic Card Geometry
* **Corner Radius:** Generous `20px` to `24px` smooth border-radius for an organic, friendly, welcoming feel.
* **Surface Styling:** Pure white (`#FFFFFF`) elevated over linen background (`#F6F3EE`) with a subtle `1px solid #E8E2D9` outline and a soft ambient shadow (`box-shadow: 0 4px 16px rgba(35, 33, 31, 0.04)`).
* **Pill Badges:** Complete rounded capsule pills (`border-radius: 9999px`) with gentle padding (`4px 12px`).

### 2. Soft-Line Minimalist Iconography
To prevent visual clutter alongside warm amber and coral colors:
* **Stroke Weight:** 1.75px uniform thin lines with rounded terminal caps.
* **Style:** Outline minimalist (e.g., Lucide / Feather icon style). No heavy fills or cartoonish motifs.
* **Icon Color:** Inherits `color-text-charcoal` (`#23211F`) or `color-brand-amber` (`#D87440`).

### 3. Hero SOS Button Spec
* **Background:** `color-accent-coral` (`#E04832`) with a gentle, non-aggressive pulse animation.
* **Typography:** Plus Jakarta Sans Bold, 17px, White (`#FFFFFF`).
* **Geometry:** `20px` rounded corner rectangle with generous `18px 24px` touch target.
