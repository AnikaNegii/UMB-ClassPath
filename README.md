# UMB ClassPath — High-Fidelity Prototype

**Group:** UMB ClassPath (Anika & Dhairya)  
**Course:** UX/HCI

## Live Demo

> Deploy this folder to GitHub Pages. All pages link to each other — no server or build step required.

## Figma Design Reference
 
The visual layout and interaction design for this prototype is based on the following Figma mockup:
 
🔗 **[View Figma Prototype](https://www.figma.com/make/uTB3IFU88uvxa6I1DKb8Ra/Start-New-Project?p=f&t=XDcj37XeC3vzEmhF-0&fullscreen=1&preview-route=%2Fpreview%2Ffastest)**
 
The Figma file served as the primary design reference for screen layouts, color system, typography, component styling, and interaction flows. The HTML prototype implements the same screens as functional, navigable pages with working features such as live room search, route saving via localStorage, interactive floor maps, and step-by-step navigation.
 
---

## View on GitHub Pages

https://anikanegii.github.io/UMB-ClassPath/index.html

---

## Prototype Screens & User Flows

| File | Screen | Task |
|------|--------|------|
| `index.html` | Home Screen | Entry point — hero section with app icon, Continue CTA, Browse Maps, My Routes, Recent |
| `search.html` | Search for Room | Dual-field search (Start Location + Destination) with live dropdown suggestions for both fields |
| `select-choices.html` | Select Choices | Displays filtered matches with room type tags |
| `room-details.html` | Room Details | Building, Floor, Room Type, Capacity — Get Directions / View Map |
| `route-options.html` | Route Type | Fastest Route vs Accessible Route selection with icon cards and time badges |
| `map.html` | Floor Map | SVG floor plan with dashed route, destination info card, floor tabs, Start Navigation CTA |
| `navigate.html` | Follow Route | Step-by-step turn-by-turn navigation with progress bar, tap header to advance |
| `routes.html` | My Routes | Saved routes list — persistent via localStorage |

## Task Card Coverage

- **Task Card 1 — Find a room:** Home → Search → Select → Room Details → Route Type → Map → Navigate
- **Task Card 2 — Accessible route (no stairs):** Route Type screen lets users choose Accessible (Elevator) route
- **Task Card 3 — Save a route:** "Save this route" on Room Details → persists in My Routes

---

## UI Changes

The prototype was updated from a phone-shell mockup to a full website layout, then redesigned to match Figma mockups:

- Removed the phone border/shell (dark bezel, status bar, fixed 360px width) — layout now fills the browser as a normal website with a max-width container
- Added a sticky top navbar with the ClassPath logo icon and hamburger menu, consistent across all pages
- Replaced the blue color system with `#2563eb` (a cleaner, more modern blue) — purple tones removed throughout
- Redesigned the home screen with a centered hero section: large app icon, bold title, tagline, description, and a prominent Continue button matching the Figma splash screen
- Redesigned the search screen to match the Figma "Where are you going?" layout — two separate labeled fields (Start Location and Destination), each with live dropdown suggestions that appear as you type, a swap button between them, and a Continue button that activates only once a destination is selected
- Redesigned route cards on the Route Type screen with large icon squares, descriptive text, and pill-style time badges
- Added a destination info card on the map screen showing building name, room/floor, and route type badge
- Updated the navigation screen with a large gradient header showing the current instruction prominently
- Applied consistent rounded corners (14–16px), subtle card shadows, and refined spacing across all screens

---

## AI Use Disclosure

**Tools used:** Claude (Anthropic) via Kiro for HTML/CSS/JS prototype generation and iterative UI spec-driven development

**Process:** Claude generated the initial code structure, SVG floor map rendering, and JavaScript routing logic based on paper prototype sketches and Design B aesthetic. Subsequent sessions used Claude to remove the phone shell, apply Figma mockup styling, and implement the dual-field search with live suggestions.

**Human design decisions that deviated from or built upon AI suggestions:**
- Preserved the dedicated Route Type screen with explicit Fastest vs Accessible choice, matching the paper prototype — specifically requested to address accessibility feedback from Participants 2 & 3
- Chose the "DM Sans" typeface for its clean, modern readability
- Directed the color change from the original blue to match the Figma mockups, then requested a shift away from purple to a cleaner blue (`#2563eb`)
- Provided Figma mockup images to guide the visual redesign of the home, search, route, map, and navigation screens
- Structured the floor map SVG to match the room numbering layout from the paper prototype (W-2-134, 132/134 block, surrounding rooms)
- Decided to make navigation interactive (tap to advance steps) rather than static, based on Participant 1's feedback about wanting step-by-step directions
- Added "Stop" and "Arrived" buttons based on Participant 1's feedback about needing a way to exit navigation
- Chose localStorage for route persistence so saved routes survive page refreshes, addressing Participant 4's request for reusable routes
- Requested the dual-field search with live dropdowns for both Start and Destination fields, matching the Figma search screen design
