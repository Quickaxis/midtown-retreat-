# Refinement Plan: Bold Typography & Transparent Glass

Enhancing the Apple-inspired redesign with bolder typography and high-transparency glass effects for the hero section.

## Design Refinements

### Typography (Bulkier & Elegant)
- **Headings (Playfair Display)**:
  - Hero: 100px, font-weight 800, italic, line-height 1.0, tight letter-spacing (-0.02em).
  - Global Sections: Playfair Display, font-weight 700.
- **Hero Subtext**: DM Sans 700 (Bold), 18px, white, 0.9 opacity.

### Glass Effects (Transparent & Sharp)
- **Transparent Navbar**:
  - `background: rgba(255,255,255,0.08)`
  - `backdrop-filter: blur(20px)`
  - White link text and transparent logo background.
- **Hero Floating Card**:
  - `background: rgba(255,255,255,0.12)`
  - `backdrop-filter: blur(16px)`
  - White text.

## Proposed Changes
- [MODIFY] `index.html`: Update Google Fonts import, CSS variables for fonts, and styles for navbar/hero/headings.

## Verification Plan
- [ ] Verify legibility of white text on transparent glass over the hero image.
- [ ] Check "Playfair Display" rendering at large sizes (100px).
- [ ] Audit all section headings for weight consistency.

## Room Pricing Overhaul
| Room | Original | Disc. Price | Badge |
|---|---|---|---|
| Sage | ₹2,500 | ₹1,600 | 36% OFF |
| Teal | ₹3,000 | ₹1,800 | 40% OFF |
| Gold | ₹3,500 | ₹2,000 | 43% OFF |

## Verification Plan
- [ ] Check glassmorphism consistency across browsers.
- [ ] Verify typography scaling and tight tracking.
- [ ] Test mobile responsiveness of the floating pill navbar.
