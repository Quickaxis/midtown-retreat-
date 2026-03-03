# Implementation Plan: UI & UX Refinements (Mar 2026)

This plan covers the second phase of refinements for the Midtown Retreat website, focusing on mobile navigation, room card design, and a unified lightbox system.

## User Review Required

> [!IMPORTANT]
> - Mobile Navigation: The hamburger menu will be replaced by a horizontal scrollable pill at the top. This is a significant change in UX for mobile users.
> - Lightbox: Every image on the site will now trigger the lightbox. This includes descriptive cards and decor images.

## Proposed Changes

### 1. Global Navigation (index, rooms, explore)
- **CSS**: Remove `.menu-toggle` and hidden `.nav-links`.
- **Nav Pill**: Width 100% on mobile (within container), `overflow-x: auto`, `white-space: nowrap`.
- **Layout**: Flex container: Logo (left) | Nav Links (center, scrollable) | Book Button (right).
- **Styles**: 12px font, DM Sans, fixed position, transparent/white glass effect.

### 2. Room Cards (rooms.html)
- **Dimensions**: Min-height 680px (desktop), Image height 380px (desktop) / 280px (mobile).
- **Positioning**: `object-position: center 30%` for room images.
- **Borders**: Image border-radius 0, Card border-radius 24px.
- **Mobile**: Stack cards vertically, full width.

### 3. Unified Lightbox (Global)
- **HTML**: Standardized lightbox overlay on all pages.
- **JS**: Logic to identify all `img` tags (excluding logo/icons) and trigger overlay.
- **Controls**: Next/Prev arrows, ✕ close button, ESC key support.
- **Lock**: `overflow: hidden` on body when active.
- **Animation**: 0.25s Opacity/Scale.

### 4. Image Consistency
- Global CSS rule for `img { object-fit: cover; object-position: center 30%; }`.
- Exceptions for `.gallery-item img` (center center) and `.about-collage img` (center top).

# Navbar and Image Positioning Refinement

## Goal Description
Improve space management in the mobile navbar to prevent text truncation and adjust image positioning to ensure ceilings are not the primary focus (focusing more on interiors).

## Proposed Changes

### Navbar Refinements
- **[MODIFY] index.html, rooms.html, explore.html**
    - Replace "Discover" with "Home" and link to `index.html`.
    - Reorder links: Home | Spaces | Rooms | Gallery | Contact.
    - Set mobile logo height to 28px.
    - Set link font size to 11px and padding to `0 8px`.
    - Ensure "Contact" is fully visible.
    - Set navbar pill padding to `8px 12px`.
    - Implement conditional visibility for "Gallery" and "Contact" labels on very small screens.

### Image Positioning
- **[MODIFY] index.html, rooms.html, explore.html**
    - Shared Spaces: `object-position: center 70%`.
    - Room Cards: `object-position: center 60%`.
    - Gallery: `object-position: center 50%`.
    - Nearby Experiences: `object-position: center 50%`.
    - Hero Image: `object-position: center 40%`.
    - Global `object-fit: cover` and `width: 100%`.

## Verification Plan
### Automated Tests
- Check styles via browser inspection.

### Manual Verification
- Test mobile view on different screen sizes (320px, 375px, 414px) to ensure no link truncation.
- Verify image cropping across all pages.
- **Lightbox**: Click one image of each type (Shared, Room, Gallery, Experience) on each page. Verify Next/Prev through all images.
- **Transitions**: Check fade transitions between pages still work.
