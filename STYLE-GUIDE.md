# Content Bug Website — Style Guide

Based on Apple's Liquid Glass Design System (mid-2025).

## Typography

### Font Files (self-hosted woff2)
All fonts live in `website/style-guide/fonts/`:

| File | Family | Weight | Use |
|------|--------|--------|-----|
| `sf-pro-display_regular.woff2` | SF Pro Display | 400 | Display body (20px+) |
| `sf-pro-display_medium.woff2` | SF Pro Display | 500 | Subtitles, nav |
| `sf-pro-display_semibold.woff2` | SF Pro Display | 600 | Headings, titles, buttons |
| `sf-pro-display_bold.woff2` | SF Pro Display | 700 | Hero title, stat values |
| `sf-pro-text_regular.woff2` | SF Pro Text | 400 | Body text (<20px) |
| `sf-pro-text_semibold.woff2` | SF Pro Text | 600 | Labels, small bold text |

### Apple Typography Rules
- **SF Pro Display**: Use for text **20px and larger** (titles, headings, hero)
- **SF Pro Text**: Use for text **under 20px** (body, captions, labels, cards)
- Minimum legible size: **11px**
- Default body: **16px** (SF Pro Text)
- Grayscale anti-aliasing: `-webkit-font-smoothing: antialiased`
- Optimized rendering: `text-rendering: optimizeLegibility`

### CSS Variables
```css
--font-display: 'SF Pro Display', -apple-system, BlinkMacSystemFont, system-ui, 'Helvetica Neue', Arial, sans-serif;
--font-text: 'SF Pro Text', -apple-system, BlinkMacSystemFont, system-ui, 'Helvetica Neue', Arial, sans-serif;
--font: var(--font-text); /* default body */
```

### Type Scale (current site values)
| Element | Size | Weight | Font | Letter-spacing |
|---------|------|--------|------|----------------|
| Hero Title | clamp(30px, 4.5vw, 56px) | 600 | Display | -0.04em |
| Section Title | clamp(24px, 3.5vw, 40px) | 600 | Display | -0.035em |
| Section Sub | clamp(16px, 2vw, 22px) | 500 | Display | — |
| Section Label | 14px | 700 | Text | 2px (uppercase) |
| Body | 16px | 400 | Text | — |
| Button | 16px | 600 | Text | -0.01em |
| Card text | 12-13px | 400-500 | Text | — |
| Stat value | 17px | 700 | Text | — |
| Caption/small | 9-10px | 600 | Text | 0.06-0.1em |

## Colors

### Core Palette
| Token | Value | Use |
|-------|-------|-----|
| `--white` / `--t1` | `#1d1d1f` | Primary text (Apple dark) |
| `--t2` | `#6e6e73` | Secondary text |
| `--t3` | `#86868b` | Tertiary text |
| `--blue` | `#0071e3` | Primary accent (Apple Blue) |
| `--blue2` | `#0077ed` | Hover state |
| `--blue3` | `#2997ff` | Dark-section accent |
| `--gold` | `#f5a623` | Stars/ratings |

### Section Backgrounds
| Section | Background |
|---------|-----------|
| Odd (1,3,5,7) | `#ffffff` (pure white) |
| Even (2,4,6) | `#0c1627` (dark navy solid) |

### Glass & Cards
| Token | Value |
|-------|-------|
| `--glass-bg` | `#ffffff` |
| `--glass-bg-alt` | `#f5f5f7` |
| `--glass-border` | `#d2d2d7` |
| `--card-border` | `#d2d2d7` |

## Spacing (8px base rhythm)
| Token | Value |
|-------|-------|
| `--s1` | 8px |
| `--s2` | 16px |
| `--s3` | 24px |
| `--s4` | 32px |
| `--s6` | 48px |
| `--s8` | 64px |
| `--s10` | 80px |

## Border Radius
| Token | Value | Use |
|-------|-------|-----|
| `--radius` | 18px | Cards, panels |
| `--radius-sm` | 14px | Buttons, badges |
| `--radius-pill` | 100px | Pills, tags |

## Shadows
| Token | Value |
|-------|-------|
| `--shadow-card` | `0 2px 8px rgba(0,0,0,.04), 0 4px 16px rgba(0,0,0,.06)` |
| `--shadow-hover` | `0 4px 12px rgba(0,0,0,.06), 0 12px 32px rgba(0,0,0,.08)` |
| `--shadow-btn` | `0 2px 8px rgba(0,113,227,.2), 0 6px 20px rgba(0,113,227,.15)` |

## Liquid Glass Effects
- Glass bubbles: `::before` pseudo-elements with radial gradients (pure CSS, no blur)
- Dark section bubbles: `rgba(41,151,255,.02-.03)` opacity
- Light section bubbles: `rgba(0,113,227,.04-.05)` opacity
- Box-shadow inset orbs on dark sections for ambient glow
- Zero `backdrop-filter`, zero `blur()` — GPU-composited only

## Motion
```css
--ease: cubic-bezier(.22, 1, .36, 1);
```
Transitions: 0.3-0.4s for UI, 0.5s for sections

## Source
See `APPLE-LIQUID-GLASS-REFERENCE.md` for the full Apple design system documentation.
