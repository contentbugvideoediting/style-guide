# Apple Liquid Glass Design System Reference

Apple's current Liquid Glass design system (introduced in mid-2025) utilizes a sophisticated evolution of its proprietary typography and materials for iOS widgets. The system focuses on a "fluid glass" aesthetic with dynamic, high-fidelity font rendering.

## Typography & Typefaces

The primary font remains San Francisco (SF), but with unique modifications for the Liquid Glass interface:

- **System Font:** SF Pro is the universal typeface for iOS widgets.
- **Liquid Glass Scaling:** The San Francisco typeface in Liquid Glass is uniquely crafted to dynamically scale its weight, width, and height to "nestle into the scene" based on the background and available space.
- **Secondary Option:** New York (NY), a serif companion, is also available for a more traditional or graphic display.

## Widget Styles & "Liquid Glass" Visuals

The Liquid Glass material is a dynamic layer that combines transparency with fluid optical properties:

- **Material Layers:** Widgets are crafted from multiple layers of Liquid Glass, featuring specular highlights and allowing for high personalization while maintaining familiarity.
- **Glass Controls:** Background elements for widgets and playback controls interact with animations to create an immersive, premium feel.
- **Transparency Options:** Users can adjust the "look" of Liquid Glass in Settings:
  - **Clear:** Maximum transparency for a true glass look.
  - **Tinted:** Increased opacity and contrast.

## Standard Sizing & Hierarchy

Apple's Human Interface Guidelines define specific size ranges to ensure legibility on high-resolution Retina displays:

- **Minimum Size:** 11 pt is the absolute minimum for legibility.
- **Default Body:** 17 pt is the standard for body text.
- **Title/Heading:** Usually 20 pt or larger, often using the SF Pro Display variant for better optical scaling at large sizes.
- **Variants:**
  - Use SF Pro Text for sizes 19 pt or smaller.
  - Use SF Pro Display for sizes 20 pt or larger.

## Retina Rendering & Quality

- **Subpixel Rendering:** Apple has largely moved toward grayscale anti-aliasing for modern Retina displays to ensure text appears super-crisp without the color-fringing sometimes seen in older subpixel methods.
- **Dynamic Type:** Widgets support Dynamic Type, allowing fonts to scale automatically from Small to AX5 (Accessibility) based on user preference.

## Apple Font Family — Full Reference (from developer.apple.com/fonts)

### SF Pro
- Neutral, flexible, sans-serif — system font for all Apple platforms
- 9 weights with italics, 4 widths, rounded variant
- Variable optical sizes for optimal legibility
- Supports 150+ languages (Latin, Greek, Cyrillic)
- Advanced features: small caps, fractions, inferior/superior numerals, arrows
- Context-aware: colon switches to vertically centered form in time displays
- Size-specific outlines + dynamic tracking at any point size

### SF Compact
- Compact, space-efficient design optimized for small sizes and narrow columns
- System font for watchOS
- Rounded variant included

### SF Mono
- Monospaced variant for coding environments (Xcode)
- 6 weights, enables row/column alignment

### New York
- Serif companion typeface based on historical type styles
- 6 weights, variable optical sizes
- Reading face at small sizes, display face at larger sizes

### SF Script Extensions
All designed to work with SF Pro for multilingual typesetting (9 weights, rounded variants, variable optical sizes):
- **SF Arabic** — Contemporary Naskh style
- **SF Armenian** — Adjusted proportions for multilingual balance
- **SF Georgian** — Modern Georgian, Mkhedruli, Mtavruli uppercase
- **SF Hebrew** — Full Niqqud diacritical marks

### SF Symbols
- Library of thousands of symbols designed to integrate with San Francisco

### Key Technical Notes
- **SF Pro Text**: Use for sizes 19 pt or smaller
- **SF Pro Display**: Use for sizes 20 pt or larger
- Proportional number widths by default
- OS applies size-specific font features automatically

### Web CSS Font Stack (what we use)
```css
font-family: 'SF Pro Display', 'SF Pro Text', -apple-system, BlinkMacSystemFont, system-ui, 'Helvetica Neue', Arial, sans-serif;
```

## Sources

1. https://developer.apple.com/fonts/
2. https://developer.apple.com
3. https://www.apple.com
4. https://en.wikipedia.org
5. https://www.figma.com
6. https://www.smashingmagazine.com
7. https://support.apple.com
8. https://medium.com
