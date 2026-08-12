# Hu.Be — Design rules for Lovable

Paste this alongside the wireframe. The wireframe shows *layout*; this defines the *system* so every new
section stays on-brand. Rule of thumb: **navy dominates, orange is rare, Nunito does everything.**

---

## 1. Colour — five colours only

| Role | Hex | Use |
|------|-----|-----|
| Navy (primary) | `#0f233d` | Default page & section background. Should cover **50–60%** of every screen. |
| Blue (secondary) | `#005588` | Supporting depth only. Sparingly. |
| Orange (accent) | `#fc8747` | **CTAs and key figures ONLY.** Never body text, never large fills. |
| Yellow (rare) | `#fed23d` | Tiny data highlights only. Almost never. |
| White | `#ffffff` | Text on navy, breathing space. |

**Navy surface steps** (for cards stacked on navy — built from navy, never grey):
- `#0a182b` deepest (vignettes) · `#142d4d` card on navy · `#1c3a63` card hover · `#26486f` divider on navy

**Text tints:**
- On navy: white at 100 / 80 / 60 / 40 / 12% opacity (primary → hairline)
- On white: navy `#0f233d` at 100 / 70 / 50 / 12% opacity
- Rare light section background: `#fbf9f4` (warm off-white, NOT pure white)

**Hard rules:** No greys. No pastels. No gradients other than the navy radial-vignette pattern already in the
wireframe. Orange never exceeds ~5% of a screen. Text selection = orange bg on navy text.

---

## 2. Typography — Nunito only, hierarchy from weight

**One font: Nunito** (self-hosted, weights 200–900). Hierarchy comes from **weight**, not from mixing families.

Weights: ExtraLight 200 · Light 300 · Regular 400 · Medium 500 · SemiBold 600 · Bold 700 · ExtraBold 800 · Black 900.

**Web type scale** (base 16px body):
- Hero/display: clamp ~40→80px, weight **900**, line-height 1.0, letter-spacing −0.01em
- H2 section head: clamp ~36→64px, weight 900
- H3: 24–32px, weight 800
- Body: 16px, line-height 1.5–1.6, colour = 80% tint (never full white/navy for paragraphs)
- Lead paragraph: 19–20px
- Label/eyebrow: 11–13px, SemiBold/Bold, letter-spacing 0.14em, UPPERCASE — **only on 2–3 word labels**
- Key figure: 96–220px, weight 900, orange (the one place orange dominates)

**Type rules:**
- Body text never below 14px.
- Headlines are large and confident; never centre body copy.
- Quotes are **never italic** — use lighter weight (300) for emphasis, orange left-border.
- Emphasis inside a headline = wrap word in orange (`em` styled non-italic, colour orange).
- Emphasis inside body = brighter/heavier same colour (white or navy), never orange.

---

## 3. Shape, spacing, elevation

- **Radii:** 6 / 10 / 16 (default card) / 24 (large surface) / 32 / 999px (pills). CTAs & chips are always full pills.
- **Spacing:** 4px base scale — 4/8/12/16/20/24/32/40/48/64/80/96. Sections breathe (~112px vertical padding).
- **Max content width:** ~1280px, 48px side gutters.
- **Shadows:** used sparingly — soft navy shadow, or the orange "glow" (`0 0 0 1px rgba(252,135,71,.3), 0 12px 40px rgba(252,135,71,.18)`) for accent moments only.
- **Motion:** ease-out `cubic-bezier(0.22,0.61,0.36,1)`; durations 120/200/360ms. Signature slow ambient
  animations: the lantern "breathes" on a 4s loop, halos pulse, orbits rotate slowly. Keep motion calm, never snappy/bouncy.

---

## 4. Component patterns (match the wireframe)

- **Primary CTA:** orange pill, navy text, weight 800. **Secondary CTA:** transparent pill, white text, 1px white-40% border.
- **Eyebrow:** small pill, orange text on orange-tint bg (`rgba(252,135,71,.14)`) with orange-40% border, uppercase tracked.
- **Cards:** navy-700 fill, 1px white-12% border, radius 16–24px. Hover lifts to navy-600.
- **Nav:** navy bar, white-80% links, orange pill CTA on the right, 1px white-12% bottom border.
- **Footer:** deepest navy `#0a182b`, tracked uppercase column heads at white-60%, links at white-80%.
- **Key figure block:** giant orange number, caption at white-80% with white(bold) inline highlights, tiny tracked uppercase source line.

---

## 5. Voice / content notes for generated copy

- British English. No em-dashes. No blame framing (culture problems are never a person's fault).
- Avoid HR-tech clichés and buzzwords. Plain, warm, matter-of-fact.
- Brand is **Hu.Be by Wise Humanity** — the "." in Hu.Be is orange.

---

## 6. What to hand Lovable

1. This file + the wireframe.
2. The token stylesheet `colors_and_type.css` (has every CSS variable + `@font-face` for Nunito). Ask Lovable to
   import it and drive everything from the `var(--…)` tokens rather than hard-coded hexes.
3. The Nunito font files (or let it load Nunito from Google Fonts as a fallback).

If Lovable can only take one instruction: **"Use colors_and_type.css as the single source of truth for colour,
type and spacing. Navy dominates, orange is reserved for CTAs and key numbers, Nunito is the only typeface."**
