# Answers AI — Color System

## Primary Palette

| Token | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Background (Dark Navy) | `#080C15` | `rgb(8, 12, 21)` | Page background, base layer |
| Primary Text (White) | `#FFFFFF` | `rgb(255, 255, 255)` | Headlines, H1-H3, hero text |
| Accent Orange | `#FF6600` | `rgb(255, 102, 0)` | CTAs, badges, primary buttons, price emphasis, checkmarks |
| Accent Blue | `#29A8FF` | `rgb(41, 168, 255)` | Link hover, secondary accent, "invisible" highlights |

## Secondary & Neutral Shades

| Token | Hex | RGB | Usage |
|-------|-----|-----|-------|
| Body Paragraph Text | `#8D9BAE` | `rgb(141, 155, 174)` | Paragraphs, descriptions, subtitles |
| Sub-labels (Dimmed) | `#5E6D82` | `rgb(94, 109, 130)` | Fine print, notes, timestamps, meta |
| Card Fill | `#0D1422` | `rgb(13, 20, 34)` | Feature cards, pricing cards, demo phone bg |
| Card Border | `#1D2636` | `rgb(29, 38, 54)` | Card borders, dividers, input borders |

## CSS Variables (:root)

```css
:root {
    --bg: #080C15;
    --bg-card: #0D1422;
    --bg-elevated: #111827;
    --text-primary: #FFFFFF;
    --text-body: #8D9BAE;
    --text-dim: #5E6D82;
    --accent-orange: #FF6600;
    --accent-blue: #29A8FF;
    --border: #1D2636;
}
```

## Applied Rules

- **Hero background**: `radial-gradient(ellipse at center top, #0D1422 0%, #080C15 60%)`
- **CTA section background**: `radial-gradient(ellipse at center, #0D1422 0%, #080C15 70%)`
- **Feature icon bg**: `linear-gradient(135deg, rgba(255,102,0,0.2), rgba(255,102,0,0.05))` with `border: 1px solid rgba(255,102,0,0.25)`
- **Buttons**: orange fill `#FF6600`, white text, orange shadow
- **Secondary buttons**: transparent bg, `#1D2636` border, hover → blue border/text
- **Cards**: `#0D1422` fill, `#1D2636` border, hover → orange-tinted border
- **Language toggle**: transparent bg, orange border, orange text → hover fills orange

## Contrast Ratios

| Combo | Ratio | WCAG |
|-------|-------|------|
| White on `#080C15` | 18.8:1 | AAA |
| `#8D9BAE` on `#080C15` | 5.2:1 | AA |
| `#5E6D82` on `#080C15` | 3.1:1 | AA (large text only) |
| `#FF6600` on `#080C15` | 5.8:1 | AA |
| `#29A8FF` on `#080C15` | 7.4:1 | AA |
