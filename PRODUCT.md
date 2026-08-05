# Product: Costanza Carpark

<!-- impeccable:product-schema 1 -->

## Platform

web

## Users

Melbourne commuters — people actively commuting by car who need to find on-street parking in real-time. They are often driving or about to drive, time-pressed, and making quick decisions under stress.

## Product Purpose

Show live parking availability across Melbourne using the city's official sensor network. Success means a commuter can find a free bay near their destination fast enough to act on it, with confidence in the data.

## Positioning

Real-time occupancy from Melbourne's official sensor infrastructure (data.melbourne.vic.gov.au) — not estimated, not historical, not crowdsourced. The data comes directly from the city's own bay sensors.

## Operating Context

- Used on mobile devices, often one-handed while in a car or walking
- Primary workflow: search address → scan map for green dots → tap to see restrictions → navigate to bay
- Time-critical: data decays in minutes; freshness matters
- Melbourne-specific: timezone logic for parking restrictions (AEST/AEDT), zone-based rule system
- Works offline after initial load (IndexedDB caching of bay geometry and restrictions)

## Capabilities and Constraints

- **Single HTML file** — no build step, no framework, no server required
- **Data sources**: Melbourne on-street parking bays (GeoJSON), Victorian parking restrictions (CKAN), live bay sensors (EXPLORE API)
- **Web Worker** processes sensor enrichment off the main thread
- **IndexedDB** caches bay geometry and restrictions (7-day TTL)
- **Performance**: capped at 5000 markers, requestIdleCallback rendering, canvas mode
- **Map**: Leaflet with CARTO light basemap, polygon rendering at zoom ≥19
- **Search**: Nominatim geocoding scoped to Melbourne
- **Known limitation**: sensor data capped at 10,000 records per fetch; manual refresh only

## Evidence on Hand

- `parking.html` — complete working implementation with live API integration
- Real API endpoints confirmed working: data.melbourne.vic.gov.au, discover.data.vic.gov.au, nominatim.openstreetmap.org

## Product Principles

1. **Data freshness over completeness** — stale data is worse than no data; always show age
2. **Zero friction** — no accounts, no setup, no tutorial; open and use
3. **Mobile-first, one-handed** — every interaction within thumb reach
4. **Melbourne-native** — timezone-aware restrictions, zone system, local conventions
5. **Transparent uncertainty** — sensor says vehicle presence only; always verify via street signs

## Accessibility & Inclusion

- Keyboard navigation for search results (Arrow/Enter/Escape)
- ARIA roles on search combobox and listbox
- Touch targets ≥44px
- `user-scalable=no` prevents pinch-to-zoom (accessibility concern for low-vision users)
