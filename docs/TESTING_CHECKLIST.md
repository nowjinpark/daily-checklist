# Testing Checklist

## Documentation Task

- Confirm every new planning document lives under `docs/`.
- Confirm documents are written in English.
- Confirm no personal task titles or descriptions from ignored backup files appear in docs.
- Confirm `README.md` links to `docs/README.md`.
- Confirm `README.ko.md` is unchanged unless a dedicated encoding task is requested.

## Current App Regression

- Open `index.html` directly in a modern browser.
- Select a date with existing data and confirm its tasks render.
- Add a regular task and confirm it appears only on that date.
- Add a Daily Independent task and confirm completion is tracked per date.
- Complete a Daily Shared task and confirm trash behavior matches the toggle.
- Add or inspect a duration task and confirm the date label is visible.
- Export a backup and confirm a JSON file downloads.

## Future Calendar Redesign

- Month navigation changes the visible month without changing stored data.
- Today button selects the current local date.
- Clicking a date updates the selected day detail panel.
- Calendar cells show read-only task indicators.
- Rendering a month does not create empty records in `checklistData`.
- Existing task editing and modals still work from the selected day detail panel.

## Future Mobile and PWA

- Test phone-width viewport.
- Confirm date cells and task actions are tappable.
- Confirm long task text wraps without overlapping controls.
- Confirm the app shell reloads offline after first load.
- Confirm stored checklist data remains after refresh and browser restart.

