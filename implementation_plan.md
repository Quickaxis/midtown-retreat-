# Architecture Restructuring: Midtown Retreat

The goal is to restructure the Midtown Retreat website from a single long page into three separate, focused pages: Home, Rooms & Amenities, and Explore & Book.

## User Review Required

> [!IMPORTANT]
> - All styles and scripts will be duplicated across the three pages for consistency, but if you'd prefer a separate `styles.css` and `scripts.js`, please let me know. For now, I'll keep them internal to each file as per the existing structure.
> - The active page highlighting in the navbar will be implemented using a CSS class `.active` and a JS check (or hardcoding per page).

## Proposed Changes

### Global Changes
- **Navbar Links**: Update all links to point to the correct files and anchors (e.g., `index.html#spaces`, `rooms.html#gallery`).
- **Footer**: Update with social links, phone number, and "Designed by Aetheron Core" text.
- **Page Transitions**: Add fade-in (0.4s) on page load and fade-out (0.2s) on internal link clicks.
- **Back to Top**: Add floating gold button appearing after 300px scroll.

### index.html (Home)
- **Sections**: Navbar, Hero, About, Shared Spaces, Footer.
- **Image Fixes**:
  - About section collage: 3/4 aspect ratio, 20px border-radius.
  - Shared Spaces: Fixed height (220px mobile / 260px desktop), `object-position: center top`.
- **SEO**: Title: "Midtown Retreat | Homestay in Dibrugarh", Meta description: "A cozy escape in the heart of Dibrugarh..."

### rooms.html (Rooms & Amenities)
- **Sections**: Navbar, Your Room Awaits (Room Cards), Everything You Need (Amenities), What Stillness Looks Like (Gallery), Footer.
- **Image Fixes**:
  - Room cards: 4/3 aspect ratio.
  - Gallery images: 4/3 aspect ratio, Implement Lightbox.
- **Amenities**: 2x4 grid on mobile.
- **SEO**: Title: "Rooms & Amenities | Midtown Retreat"

### explore.html (Explore & Book)
- **Sections**: Navbar, Beyond the Retreat (Experiences), Heartfelt Stays (Reviews), House Rules, Your Escape Is Waiting (CTA), Footer.
- **Image Fixes**:
  - Experiences cards: 180px fixed height, mini-card layout on mobile (image left, text right).
- **Reviews**: 18px quote font size on mobile, vertical scroll.
- **Booking CTA**: Side-by-side buttons on mobile, 52px heading.
- **SEO**: Title: "Explore & Book | Midtown Retreat"

## Verification Plan

### Automated Tests
- None specified.

### Manual Verification
- **Navigation**: Click every link in the navbar across all three pages to ensure correct redirection and anchor scrolling.
- **Mobile Responsiveness**: Use browser dev tools (e.g., iPhone 12 Pro) to verify:
  - Header font sizes (clamping).
  - Amenities 2x4 grid.
  - Mini-card layout for nearby experiences.
  - Booking CTA buttons side-by-side.
- **Lightbox**: Click gallery images and verify overlay, arrows, and close button.
- **Page Transitions**: Verify fade transitions between pages.
