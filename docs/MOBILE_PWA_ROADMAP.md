# Mobile and PWA Roadmap

## Strategy

Use a PWA-first, local-first approach. The app should remain usable as a static file or static site while becoming easier to use from a phone.

## Mobile UI Goals

- Make the calendar usable on phone-width screens.
- Keep date cells tappable without cramped text.
- Place the selected day detail below the calendar on small screens.
- Keep task actions touch-friendly.
- Avoid layouts where long task text overlaps buttons or controls.

## PWA Goals

- Add a web app manifest with name, short name, icons, theme color, and display mode.
- Add a service worker for offline caching of app shell files.
- Keep all checklist data local unless the user explicitly chooses an export or future sync option.
- Support install-to-home-screen behavior on mobile browsers where available.

## Current PWA Files

The app now includes:

- `manifest.webmanifest`
- `service-worker.js`
- `app-icon.svg`

These files must not change or migrate stored checklist data.

## Acceptance Criteria

- The app can be opened, refreshed, and used on a phone-sized viewport.
- The app shell loads offline after the first successful visit.
- Existing checklist data remains in the browser after reload.
- The PWA layer does not introduce account requirements.
