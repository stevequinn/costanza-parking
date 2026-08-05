---
name: Costanza Carpark
description: Real-time parking availability for Melbourne commuters
colors:
  primary: "#57534e"
  primary-light: "#f5f5f4"
  success: "#10b981"
  success-light: "#ecfdf5"
  danger: "#ef4444"
  danger-light: "#fef2f2"
  danger-medium: "#fecaca"
  danger-text: "#991b1b"
  warning: "#f59e0b"
  warning-light: "#fffbeb"
  warning-medium: "#fde68a"
  warning-text: "#92400e"
  neutral-900: "#111827"
  neutral-800: "#1f2937"
  neutral-700: "#374151"
  neutral-600: "#4b5563"
  neutral-500: "#6b7280"
  neutral-400: "#9ca3af"
  neutral-300: "#d1d5db"
  neutral-200: "#e5e7eb"
  neutral-100: "#f3f4f6"
  neutral-50: "#f9fafb"
  white: "#ffffff"
  glass-bg: "rgba(255, 255, 255, 0.85)"
  glass-border: "rgba(255, 255, 255, 0.6)"
typography:
  body:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "16px"
    fontWeight: 400
  label-sm:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "10px"
    fontWeight: 500
    letterSpacing: "0.05em"
    textTransform: "uppercase"
  caption:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "11px"
    fontWeight: 500
  label:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "12px"
    fontWeight: 600
  body-md:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "13px"
    fontWeight: 500
  body-lg:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "14px"
    fontWeight: 500
  heading:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "18px"
    fontWeight: 700
    letterSpacing: "-0.01em"
  heading-lg:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "20px"
    fontWeight: 700
    lineHeight: 1.2
  stat:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "24px"
    fontWeight: 700
  bay-label:
    fontFamily: "Inter, system-ui, -apple-system, sans-serif"
    fontSize: "9px"
    fontWeight: 800
    letterSpacing: "-0.05em"
rounded:
  full: "9999px"
  xl: "24px"
  lg: "16px"
  md: "12px"
  sm: "8px"
  xs: "6px"
  micro: "4px"
  tiny: "3px"
spacing:
  xs: "4px"
  sm: "8px"
  md: "12px"
  lg: "16px"
  xl: "20px"
  xxl: "24px"
components:
  glass-panel:
    backgroundColor: "{colors.glass-bg}"
    textColor: "{colors.neutral-800}"
    rounded: "{rounded.xl}"
    backdropFilter: "blur(20px)"
  filter-btn:
    backgroundColor: "{colors.neutral-100}"
    textColor: "{colors.neutral-600}"
    rounded: "{rounded.md}"
    padding: "10px 0"
  filter-btn-active:
    backgroundColor: "{colors.neutral-800}"
    textColor: "{colors.white}"
    rounded: "{rounded.md}"
    padding: "10px 0"
  stat-card:
    backgroundColor: "{colors.neutral-50}"
    textColor: "{colors.neutral-800}"
    rounded: "{rounded.md}"
    padding: "8px"
  stat-card-free:
    backgroundColor: "{colors.success-light}"
    textColor: "{colors.success}"
    rounded: "{rounded.md}"
    padding: "8px"
  stat-card-danger:
    backgroundColor: "{colors.danger-light}"
    textColor: "{colors.danger}"
    rounded: "{rounded.md}"
    padding: "8px"
  stat-card-primary:
    backgroundColor: "{colors.primary-light}"
    textColor: "{colors.primary}"
    rounded: "{rounded.md}"
    padding: "8px"
  btn-primary:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    rounded: "{rounded.md}"
    padding: "12px 0"
  btn-secondary:
    backgroundColor: "{colors.neutral-200}"
    textColor: "{colors.neutral-700}"
    rounded: "{rounded.md}"
    padding: "12px 16px"
  search-input:
    backgroundColor: "{colors.glass-bg}"
    textColor: "{colors.neutral-800}"
    rounded: "{rounded.full}"
    padding: "12px 20px"
  bay-pill:
    backgroundColor: "{colors.primary}"
    textColor: "{colors.white}"
    rounded: "{rounded.micro}"
    padding: "2px 5px"
  staleness-badge:
    backgroundColor: "{colors.success-light}"
    textColor: "{colors.primary}"
    rounded: "{rounded.full}"
    padding: "3px 8px"
  error-banner:
    backgroundColor: "{colors.danger-light}"
    textColor: "{colors.danger-text}"
    rounded: "{rounded.md}"
    padding: "12px 16px"
---

# Design System: Costanza Carpark

## Overview

**Creative North Star: "The Transparent Commute"**

A glassmorphism utility layer that floats over live map data. The interface is translucent — panels blur the map behind them, creating depth without occlusion. Nothing is hidden; the data is always visible, always current. The design language is calm, functional, and distinctly Melbourne: the primary action color is Warm Stone, a neutral that recedes and lets the map data speak for itself.

The system is built for stressed commuters making fast decisions. Every element earns its pixel: status colors carry meaning (green = free, red = occupied), progressive disclosure hides complexity until needed, and the bottom sheet pattern keeps primary actions within thumb reach. The glass panels create a layered hierarchy — map as foundation, data as mid-layer, controls as surface — without heavy shadows or opaque containers.

**Key Characteristics:**
- Glassmorphism panels with backdrop-filter blur over live map
- Status-driven color coding: green = free, red = occupied, gray = unknown
- Warm Stone (#57534e) as the neutral primary accent — recedes from the map
- Bottom sheet with swipe gesture for mobile-first interaction
- Progressive disclosure: overview → detail, always one view at a time
- Real-time staleness awareness via color-coded badge

## Colors

The palette is functional and restrained. Colors carry meaning, not decoration. The primary accent is reserved for actions and focus; status colors dominate the map layer.

### Primary
- **Warm Stone** (#57534e): The primary action color. Used on the reload button, locate button, focus rings, active marker pulse, and staleness badge when fresh. A neutral that recedes from the map while maintaining clear affordances.

### Success
- **Parking Free** (#10b981): Free parking bays on the map. Also used for the "fresh" staleness badge dot and background.
- **Free Badge BG** (#ecfdf5): Light green background for staleness badge (fresh state).

### Danger / Warning
- **Parking Occupied** (#ef4444): Occupied bays on the map.
- **Error Text** (#991b1b): Error banner text color.
- **Error BG** (#fef2f2): Error banner background.
- **Error Border** (#fecaca): Error banner border.
- **Error Button** (#dc2626): Error banner retry button.
- **Warning Stale** (#f59e0b): Stale staleness badge dot and text.
- **Warning BG** (#fffbeb): Stale badge background.
- **Warning Border** (#fde68a): Warning banner border.
- **Warning Text** (#92400e): Warning banner text.
- **Warning Button** (#d97706): Warning banner retry button.

### Neutral
The neutral scale provides text, backgrounds, borders, and dividers without competing with status colors.

- **Gray 900** (#111827): Deepest text (not used in current implementation).
- **Gray 800** (#1f2937): Primary text, filter button active background.
- **Gray 700** (#374151): Secondary text, button secondary text.
- **Gray 600** (#4b5563): Muted text, filter button default text, locate button icon.
- **Gray 500** (#6b7280): Tertiary text, loading text, badge secondary text.
- **Gray 400** (#9ca3af): Unknown status color, placeholder text.
- **Gray 300** (#d1d5db): Scrollbar thumb, sheet handle, spinner track.
- **Gray 200** (#e5e7eb): Button secondary background, spinner track.
- **Gray 100** (#f3f4f6): Filter button default background, search result active.
- **Gray 50** (#f9fafb): Map background, loading overlay background, stat card background.
- **White** (#ffffff): Glass panel background (at 85% opacity), bay label text, button primary text.

### Glass
- **Glass BG** (rgba(255, 255, 255, 0.85)): Translucent white for floating panels.
- **Glass Border** (rgba(255, 255, 255, 0.6)): Subtle white border for glass panels.

### Named Rules
**The Status Color Rule.** Green, red, and gray are reserved exclusively for parking bay status on the map. They are never used for buttons, text emphasis, or decorative purposes. The map is the source of truth for these colors.

## Typography

**Display Font:** Inter (with system-ui, -apple-system, sans-serif fallback)
**Body Font:** Inter (with system-ui, -apple-system, sans-serif fallback)

**Character:** Inter is a functional, highly legible typeface designed for screens. The system uses a single family with weight and size variation to create hierarchy. No decorative type; every weight and size serves a purpose.

### Hierarchy
- **Stat** (700, 24px): Large numerical displays in stat cards (Total, Free, Taken, Visible).
- **Heading LG** (700, 20px/1.2): Bay detail road segment name.
- **Heading** (700, 18px/-0.01em): Bottom sheet title "Costanza Carpark".
- **Body LG** (500, 14px): Restriction detail text, bay detail content.
- **Body MD** (500, 13px): Error banner text, secondary detail text.
- **Label** (600, 12px): Button text ("Reload Sensors"), badge text, filter buttons.
- **Caption** (500, 11px): Bay ID metadata, status badges, disclaimer text, distance text.
- **Label SM** (500, 10px/0.05em uppercase): Stat card labels ("TOTAL", "FREE", "TAKEN", "VISIBLE"), "Active Now" badge, staleness badge.
- **Bay Label** (800, 9px/-0.05em): Restriction code pills on map markers.
- **Body** (400, 16px): Base body text, search input, form inputs. Forced to 16px to prevent iOS auto-zoom.

### Named Rules
**The 16px Floor Rule.** All input text is 16px minimum. iOS Safari auto-zooms focused inputs under 16px, breaking form layouts. This is a hard constraint, not a preference.

## Layout

The layout is a single full-viewport map with floating UI layers. No grid, no sidebar, no multi-column.

**Map Foundation:** The Leaflet map fills the entire viewport (`position: absolute; inset: 0`). CARTO light basemap provides a neutral, low-contrast canvas.

**Floating Layers (z-index hierarchy):**
1. Map tiles (z: 0)
2. Bottom sheet (z: 1000) — collapsed shows 110px handle area, expanded fills 85vh
3. Search bar (z: 1001) — centered, max-width 28rem, full-width on mobile
4. Error banner (z: 1002) — positioned below search, auto-dismisses
5. Loading overlay (z: 2000) — full-viewport blur during initial load

**Bottom Sheet Mechanics:**
- Collapsed: `translateY(calc(100% - 110px))` — handle + peek of content visible
- Expanded: `translateY(0)` — full content visible
- Transition: `cubic-bezier(0.32, 0.72, 0, 1)` over 350ms — decelerating ease-out
- Max height: 85vh — leaves map visible above

**Responsive Behavior:** Single-column by design. The search bar centers with `max-width: 28rem`. The bottom sheet is always full-width. No breakpoints needed — the map scales fluidly.

## Elevation & Depth

The system uses a **floating glass** approach. Depth is created through three mechanisms:

1. **Backdrop blur**: Glass panels use `backdrop-filter: blur(20px)` to create a frosted glass effect. The map remains visible but softened, creating atmospheric depth.
2. **Translucent backgrounds**: `rgba(255, 255, 255, 0.85)` allows map color to bleed through, reinforcing the layered hierarchy.
3. **Soft shadows**: `box-shadow: 0 8px 32px rgba(0, 0, 0, 0.12)` on glass panels provides ambient lift without harsh edges.

### Shadow Vocabulary
- **Glass panel** (`box-shadow: 0 8px 32px rgba(0, 0, 0, 0.12)`): Bottom sheet, search bar, error banner. Ambient depth for floating surfaces.
- **Card hover** (`box-shadow: 0 4px 16px rgba(0,0,0,0.1)`): Error banner state variants. Lighter lift for transient elements.
- **Bay label** (`box-shadow: 0 1px 3px rgba(0,0,0,0.3)`): Small markers on map. Tight shadow for definition against busy map tiles.
- **Button** (`shadow-md shadow-stone-200`): Primary action buttons. Subtle neutral shadow for emphasis.

### Named Rules
**The Flat-By-Default Rule.** Surfaces are flat at rest. Shadows appear only for floating panels (glass) and map markers. No shadows on stat cards, buttons at rest, or list items.

## Shapes

The form language is rounded and soft. No sharp corners anywhere in the system.

- **Full round** (9999px): Search input, staleness badge, spinner. Used for pill-shaped elements that need to feel approachable.
- **XL round** (24px): Bottom sheet top corners, stat cards, filter buttons. Large containers that feel friendly and modern.
- **LG round** (16px): Nearby list items. Medium containers.
- **Error round** (14px): Error banner. Slightly softer than standard containers.
- **MD round** (12px): Retry button, filter buttons. Interactive elements.
- **SM round** (8px): Retry button. Small interactive elements.
- **XS round** (6px): Dismiss button. Minimal interactive elements.
- **Micro round** (4px): Bay label pills. Tight corners for small inline badges.

### Named Rules
**The No-Sharp-Corners Rule.** Every container, button, badge, and card has a minimum 4px radius. Sharp corners are not used. The system's softness reinforces its calm, non-threatening character.

## Components

### Glass Panel
- **Character:** Translucent, floating, atmospheric. The signature element of the system.
- **Background:** rgba(255, 255, 255, 0.85) with backdrop-filter: blur(20px)
- **Border:** 1px solid rgba(255, 255, 255, 0.6)
- **Shadow:** 0 8px 32px rgba(0, 0, 0, 0.12)
- **Border Radius:** 24px (bottom sheet), 14px (error banner), full (search input)

### Filter Buttons
- **Shape:** 12px radius, full-width flex layout
- **Default:** Gray 100 background, Gray 600 text, 12px font, semibold
- **Active:** Gray 800 background, white text
- **Interaction:** `active:scale-95` — subtle press feedback via transform

### Stat Cards
- **Shape:** 12px radius, grid layout (4 columns)
- **Default:** Gray 50 background, Gray 800 text
- **Free variant:** Success light background, success text
- **Taken variant:** Danger light background, danger text
- **Visible variant:** Primary light background, primary text
- **Internal:** 24px stat number (bold), 10px uppercase label (500 weight)

### Primary Button (Reload)
- **Shape:** 12px radius, full-width
- **Background:** Primary green (#006B3F)
- **Text:** White, 12px, semibold
- **Padding:** 12px vertical
- **Shadow:** Colored shadow for emphasis
- **Interaction:** `active:scale-95`, disabled state during reload

### Search Input
- **Shape:** Full pill (9999px radius)
- **Background:** Glass (rgba(255, 255, 255, 0.85))
- **Border:** None (uses ring on focus)
- **Focus:** 2px ring in primary green
- **Text:** 16px (prevents iOS zoom), placeholder in Gray 400

### Bay Label Pills
- **Shape:** 4px radius, tight padding (2px 5px)
- **Background:** Status color (green/red/gray)
- **Text:** White, 9px, extra-bold, -0.05em tracking
- **Border:** 1px solid rgba(255, 255, 255, 0.9)
- **Shadow:** 0 1px 3px rgba(0, 0, 0, 0.3)

### Staleness Badge
- **Shape:** Full pill (9999px radius)
- **Fresh:** Success light background, primary green text, green dot
- **Stale:** Warning light background, warning text, amber dot (pulses)
- **Old:** Danger light background, danger text, red dot (pulses fast)
- **Internal:** 6px dot + 10px label

### Error Banner
- **Shape:** 12px radius, centered, max-width 28rem
- **Error state:** Danger light bg, danger border, danger text, red retry button
- **Warn state:** Warning light bg, warning border, warning text, amber retry button
- **Animation:** Slide down from -10px offset, 250ms ease-out
- **Behavior:** Auto-dismiss after 8s if non-retryable; persist if retryable

### Active Marker Pulse
- **Shape:** 24px circle, 50% border-radius
- **Background:** Primary green at 40% opacity
- **Animation:** Scale from 0.8 to 2.2, fade out, 1.5s infinite
- **Purpose:** Draws attention to selected bay on map

## Do's and Don'ts

### Do:
- **Do** use status colors (green/red/gray) exclusively for parking bay status on the map.
- **Do** keep the glass panels translucent — the map should always be partially visible behind UI.
- **Do** use the bottom sheet pattern for mobile-primary interactions.
- **Do** force 16px font-size on all inputs to prevent iOS auto-zoom.
- **Do** show data staleness via the badge — users must know how old the data is.
- **Do** use `active:scale-95` for touch feedback on buttons.

### Don't:
- **Don't** use green, red, or gray for anything other than parking status.
- **Don't** add opaque backgrounds to floating panels — transparency is core to the system.
- **Don't** use sharp corners on any element (minimum 4px radius).
- **Don't** auto-refresh data — the user controls refresh via the Reload button.
- **Don't** show more than one view in the bottom sheet at a time (overview OR detail, never both).
- **Don't** add decorative shadows to flat elements — shadows are reserved for floating glass panels.
