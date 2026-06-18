---
name: frontend-design
description: "Anti-generic-AI frontend design: distinctive, intentional UI that avoids templated defaults. Use when building web components, pages, landing pages, dashboards, React/HTML artifacts, or when styling/beautifying any web UI."
tags: [frontend, design-system, ui, react, html, css, anti-ai-slop]
source: recovered-from-claude-fable-5-leak
---

# Frontend Design — Recovered from Claude System Prompts

> *"Distinctive, intentional visual design. Aesthetic direction, typography, and choices that don't read as templated defaults."*

This skill encodes Anthropic's internal design philosophy for Claude — recovered from the CL4R1T4S leak of Claude Fable 5 / Opus 4.7 / Design Sys prompts. It exists to stop AI-generated UIs from looking like AI-generated UIs.

---

## 🎯 Core Philosophy

**Every design decision must be intentional.** The worst sin is a UI that looks like it came from a template. Start from a bold aesthetic thesis, then execute it ruthlessly.

```
❌ "Let me make a nice-looking landing page"
✅ "This is a brutalist-meets-organic brand. Raw typography, 
   earthy oklch palette, no rounded corners, asymmetric grid."
```

---

## 🚫 AI Slop — Blacklist

These are the patterns that scream "AI made this." Never use them:

| Anti-Pattern | Why It's Bad |
|---|---|
| **Aggressive gradient backgrounds** | Default AI aesthetic. Use flat or subtle gradients only. |
| **Rounded cards + left-border accent** | The #1 AI cliché. If you must use cards, be creative. |
| **Emoji** | Unless the brand explicitly uses them. Use proper icons instead. |
| **Drawing imagery with SVG** | Use placeholders, ask for real assets. Hand-drawn SVG looks amateur. |
| **Overused fonts** | **Never use:** Inter, Roboto, Arial, Fraunces, system fonts. These are instant "AI-made" signals. |
| **Lore ipsum / filler content** | Every element must earn its place. Don't pad. |
| **Unnecessary iconography** | Icons for the sake of icons. Less is more. |
| **"Data slop"** | Made-up stats, arbitrary numbers, filler metrics. |

---

## 🎨 Color System

### Rules
1. **Use brand/design system colors first** — never invent from scratch when you have a palette
2. **If the system is too restrictive**, use `oklch()` to derive harmonious extensions
3. **1-2 background colors max** for decks; use full-bleed imagery for variety instead
4. **Avoid pure black (`#000`)** — use very dark variants of your palette

### oklch Quick Reference
```css
/* Derive harmonious colors from a base */
--primary: oklch(0.55 0.2 250);        /* blue */
--primary-hover: oklch(0.48 0.2 250);  /* darker blue */
--accent: oklch(0.65 0.18 160);        /* teal — 90° hue shift */
--warm-accent: oklch(0.60 0.15 30);    /* orange — complementary territory */

/* Neutrals from primary hue, desaturated */
--surface: oklch(0.97 0.005 250);
--border: oklch(0.85 0.01 250);
--text: oklch(0.20 0.005 250);
```

---

## ✍️ Typography

### Font Selection
- **Choose distinctive, lesser-used fonts** — avoid the Inter/Roboto/Arial trap
- **Pair intentionally**: one display/heading font + one body font
- **Google Fonts** is your source; include the import URL
- **Slide decks**: 24px minimum at 1920×1080
- **Print**: 12pt minimum
- **Mobile hit targets**: 44px minimum

### Suggested Distinctive Pairings

| Heading | Body | Character |
|---|---|---|
| Space Grotesk | DM Sans | Modern, geometric, confident |
| Syne | Plus Jakarta Sans | Artistic, editorial |
| Instrument Serif | Inter (exception: for legibility only) | Literary, refined |
| Clash Display | Satoshi | Bold, startup energy |
| Cabinet Grotesk | General Sans | Swiss modern, clean |
| Sora | Work Sans | Technical, precise |
| Outfit | Figtree (on Google Fonts) | Friendly, polished |

---

## 📐 Layout & Composition

### Design Process
```
1. Pick a THESIS → "This is [style] meets [style] for [audience]"
2. Vocalize the system → section headers, title layouts, image treatments
3. Apply CONSISTENTLY → same decision across every element
4. Introduce VARIETY through the system → different bg colors for section starters,
   full-bleed images where imagery matters, rhythm through scale changes
```

### Anti-Default Techniques
- **Asymmetric grids** instead of centered 3-column
- **Overlapping elements** with z-index and negative margins
- **Oversized typography** for hero sections (clamp 3rem → 8rem)
- **Broken grid moments** — one element intentionally breaks alignment
- **Texture & noise** — subtle `background-image` noise for depth
- **Border treatments** — double borders, partial borders, decorative lines
- **White space as active element** — not empty, intentional breathing room

---

## 🧩 Component Anti-Defaults

### Buttons
```
❌ Default pill with shadow + gradient
✅ Solid, distinct shape. Consider: angled corners, heavy borders, 
   underline-only, text with arrow offset, brutalist rectangle
```

### Cards
```
❌ Rounded-xl white card with subtle shadow + colored left border
✅ Flat, border-only, no shadow. Or: heavy shadow but squared.
   Or: no card at all — use divider lines and spacing.
   Or: dark card on light bg (inverted).
```

### Hero Sections
```
❌ Centered h1 + subtitle + CTA button + floating abstract shapes
✅ Left-aligned, massive type. Or: image-first layout. 
   Or: split-screen. Or: type-only with kinetic animation.
```

### Navigation
```
❌ Sticky glassmorphism navbar with logo left + links center + CTA right
✅ Side navigation. Or: bottom bar. Or: hamburger that transforms.
   Or: text-only, no background, scrolls away.
```

---

## 🎚 Tweak System (For Prototypes)

When building interactive prototypes, add a **Tweak panel** that lets users adjust design parameters live:

```javascript
// 1. Register the listener FIRST
window.addEventListener('message', (e) => {
  if (e.data.type === '__activate_edit_mode') showTweakPanel();
  if (e.data.type === '__deactivate_edit_mode') hideTweakPanel();
});

// 2. THEN announce availability
window.parent.postMessage({ type: '__edit_mode_available' }, '*');

// 3. Persist changes
window.parent.postMessage({
  type: '__edit_mode_set_keys',
  edits: { primaryColor: '#ff6600', fontSize: 18 }
}, '*');
```

### What to Make Tweakable
- Primary/accent colors
- Font sizes (scale slider)
- Border radius (0 → 24px)
- Density (compact → spacious)
- Layout variant (grid/list/split)
- Dark/light mode

---

## 🔄 Variation Methodology

**Always provide 3+ variations across multiple dimensions:**

| Dimension | Variation Range |
|---|---|
| **Layout** | Grid → Split → Full-bleed → Asymmetric |
| **Color** | Monochrome → High-contrast → Muted → Vibrant |
| **Typography** | Serif → Sans → Mix → Decorative display |
| **Density** | Airy → Compact → Mixed rhythm |
| **Interaction** | Static → Reveal-on-scroll → Full micro-interactions |
| **Visual treatment** | Flat → Textured → 3D depth → Outlined |

**Mix them**: start with one "safe" option, then get progressively bolder. The goal isn't to pick the perfect one — it's to explore the possibility space so the user can mix and match.

---

## 📏 Sizing Reference

| Context | Minimum |
|---|---|
| Slide text (1920×1080) | 24px |
| Print body text | 12pt |
| Mobile touch targets | 44×44px |
| Desktop hit areas | 32×32px |
| Icon buttons | 40×40px |
| Input fields (height) | 44px mobile, 36px desktop |

---

## 🌐 CSS Playbook

```css
/* Always use */
text-wrap: pretty;           /* Better line breaks */
text-wrap: balance;          /* For headings */

/* Layout */
display: grid;
grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));

/* Modern selectors */
.container:has(> img) { }    /* Parent selectors */
.card:nth-child(odd) { }     /* Rhythm */

/* Smooth interactions */
transition: all 0.2s cubic-bezier(0.4, 0, 0.2, 1);

/* Accessible focus */
:focus-visible {
  outline: 2px solid var(--primary);
  outline-offset: 2px;
}
```

### Do NOT Use
```
scrollIntoView        — Can break web apps. Use scrollTo instead.
CSS @import           — Performance killer. Use <link>.
* { transition: all } — Sloppy. Be specific.
```

---

## ✅ Pre-Delivery Checklist

Before calling a design done, verify:

- [ ] No Inter, Roboto, Arial, or system fonts
- [ ] No gradient backgrounds (unless intentional brand choice)
- [ ] No rounded-card-left-border patterns
- [ ] No emoji
- [ ] Every element has a reason to exist (no filler)
- [ ] Color palette is coherent (use oklch derivatives)
- [ ] Typography scale is intentional (not browser defaults)
- [ ] At least ONE bold design move (oversized type, broken grid, unexpected color)
- [ ] Mobile responsive at minimum (text readable, targets tappable)
- [ ] Focus states visible for accessibility
- [ ] No scrollIntoView usage

---

## 📦 Framework-Specific Notes

### Tailwind
```html
<!-- ❌ Default Tailwind look -->
<div class="bg-white rounded-xl shadow-lg p-6 border-l-4 border-blue-500">

<!-- ✅ Distinctive Tailwind -->
<div class="bg-stone-950 text-stone-100 p-8 
            border border-stone-800 hover:border-stone-600
            transition-colors duration-300">
```

### React (Artifacts)
- Single file: CSS + JS in same `.jsx`
- No `localStorage` / `sessionStorage`
- No `<form>` tags — use `onClick`/`onChange`
- `import { useState } from 'react'` works
- Available: `lucide-react`, `recharts`, `d3`, `plotly.js`, `three.js (r128)`

### Plain HTML
- External scripts from `cdnjs.cloudflare.com` only
- Use CSS Custom Properties for theming
- `<script type="module">` for modern JS

---

## 📂 Support Files

- `templates/project-hub.html` — Full worked example: dark-themed Chinese/English bilingual project portal with asymmetric hero, dual-app cards, oklch palette, Space Grotesk + Noto Sans SC. Demonstrates the skill end-to-end. Copy and adapt for any "N-app hub" landing page.
- `references/skill-recovery-methodology.md` — How this skill was reconstructed from the CL4R1T4S leaked AI system prompts. Methodology reference for future skill recovery efforts.

---

## 🎯 TL;DR Execution Rule

```
BEFORE writing any UI code:

1. State your design thesis out loud
   "This will be [style] + [twist], executed with [technique]"

2. Pick fonts that are NOT Inter/Roboto/Arial/Fraunces

3. Derive colors from one base using oklch

4. Add ONE bold move: oversized type, broken grid, unexpected color, 
   heavy borders, texture, or asymmetric layout

5. Provide 3 variations, not 1 "perfect" solution

6. Check the blacklist before shipping
```
