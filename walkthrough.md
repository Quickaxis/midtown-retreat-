# Walkthrough - Navbar Visibility & Dynamic Styling

I have fixed the visibility issues on the navbar and implemented dynamic styling for a better user experience across all pages.

## Changes Made

### 1. Unified Navbar Visibility
- **Non-Hero Pages (`rooms.html`, `explore.html`)**: Set the default link color to `#1a1a1a` (dark) to ensure perfect contrast against the white/glass background.
- **Dynamic Transition (`index.html`)**: 
    - Implemented an `IntersectionObserver` that monitors the hero section.
    - Links are **white** when overlapping the hero image.
    - Links smoothly switch to **dark** (`#1a1a1a`) once the user scrolls past the hero section.
- **Improved Hover/Active States**: Standardized across all pages:
    - **Hover**: `#0d4a47` (Teal)
    - **Active**: `#c9a84c` (Gold)

### 2. Dot Separator Removal
- Identified that the "invisible dots" were actually default bullet points appearing due to missing `list-style: none` rules on some pages.
- Applied global `list-style: none` to all `ul` elements site-wide.
- Verified that all dot separators or bullets between navigation links are now completely removed, providing a clean, spaced-out layout.

## Verification Scenarios

### On Index Page
- **Start**: Navbar links are white on the hero.
- **Scroll**: As the hero leaves the viewport, the links turn dark.
- **Return**: Links turn back to white when returning to the top.

### On Other Pages
- Links are consistently dark and clearly visible.
- No bullet points or dots appear in the navbar.

## Final Sync
- All changes committed and pushed to GitHub [`main`](https://github.com/Quickaxis/midtown-retreat-.git).
