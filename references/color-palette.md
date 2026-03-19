# Color Palette & Brand Style

**This is the single source of truth for all colors and brand-specific styles.** To customize diagrams for your own brand, edit this file — everything else in the skill is universal.

**Theme: Light with pastel shades.** All fills should be soft, washed-out pastels. Strokes should be medium-toned (never dark). Never use the darkest shades (no `#1e3a5f`, `#1e293b`, `#1e40af` or equivalently dark values). Everything should feel airy and easy on the eye against a white canvas.

---

## Shape Colors (Semantic)

Colors encode meaning, not decoration. Each semantic purpose has a fill/stroke pair.

| Semantic Purpose | Fill | Stroke |
|------------------|------|--------|
| Primary/Neutral | `#dbeafe` | `#93c5fd` |
| Secondary | `#eff6ff` | `#bfdbfe` |
| Tertiary | `#e0f2fe` | `#7dd3fc` |
| Start/Trigger | `#ffedd5` | `#fdba74` |
| End/Success | `#d1fae5` | `#6ee7b7` |
| Warning/Reset | `#fee2e2` | `#fca5a5` |
| Decision | `#fef9c3` | `#fde047` |
| AI/LLM | `#ede9fe` | `#c4b5fd` |
| Inactive/Disabled | `#f8fafc` | `#cbd5e1` (use dashed stroke) |
| Error | `#ffe4e6` | `#fda4af` |

**Rule**: Always pair a soft pastel fill with a slightly more saturated (but still light) stroke. Never use strokes darker than the stroke values listed above.

---

## Text Colors (Hierarchy)

Use color on free-floating text to create visual hierarchy without containers.

| Level | Color | Use For |
|-------|-------|---------|
| Title | `#3b82f6` | Section headings, major labels |
| Subtitle | `#60a5fa` | Subheadings, secondary labels |
| Body/Detail | `#94a3b8` | Descriptions, annotations, metadata |
| On light fills | `#374151` | Text inside light-colored shapes |

---

## Evidence Artifact Colors

Used for code snippets, data examples, and other concrete evidence inside technical diagrams.

| Artifact | Background | Text Color |
|----------|-----------|------------|
| Code snippet | `#f1f5f9` | `#475569` |
| JSON/data example | `#f0fdf4` | `#4ade80` |

---

## Default Stroke & Line Colors

| Element | Color |
|---------|-------|
| Arrows | Use the stroke color of the source element's semantic purpose |
| Structural lines (dividers, trees, timelines) | `#cbd5e1` (light slate) |
| Marker dots (fill + stroke) | `#93c5fd` |

---

## Background

| Property | Value |
|----------|-------|
| Canvas background | `#ffffff` |
