# Project Context

## What This App Does

Daily Checklist is a single-file browser app for managing day-by-day tasks. It runs from `index.html`, uses vanilla HTML/CSS/JavaScript, and stores user data in the browser with no backend account or external service.

The current interface is centered on a date input. Selecting a date renders that day's categories and tasks.

## Current Storage Keys

The app currently persists state in `localStorage` with these keys:

- `checklistData`: date-keyed day records with categories, regular tasks, duration task instances, and daily independent completion states.
- `dailyTasks`: global daily recurring tasks split into `independent` and `shared`.
- `trash`: removed Daily Shared tasks when the trash setting is enabled.
- `sendToTrash`: boolean setting for Daily Shared task completion behavior.

Any future implementation must preserve these keys unless a dedicated migration plan exists and has been backed up and tested.

## Task Types

- `Regular`: appears only on the selected date.
- `Daily (Independent)`: appears every day, with completion tracked separately per date.
- `Daily (Shared)`: appears every day until completed, then is removed globally or moved to trash.
- `Duration`: appears across a date range and can repeat weekly, monthly, or yearly.

## Known Issues

- Some visible labels and `README.ko.md` text appear to have encoding damage.
- The app is currently one large HTML file, which makes future changes harder to review.
- Existing backup JSON files are ignored personal artifacts and should not be parsed into documentation or committed.
- Rendering a date currently may initialize that date's data. Calendar month summaries must avoid creating empty date records.

## Safe Change Rules

- Inspect storage behavior before changing rendering or task logic.
- Keep existing data shape compatible.
- Do not copy personal checklist text from local backup files into docs, tests, fixtures, commits, or screenshots.
- Back up browser data before any data-model or persistence change.

