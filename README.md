## Language

- [English](./README.md)
- [한국어](./README.ko.md)

# Daily Checklist

A lightweight single-file checklist app built as my first vibe-coding project. It helps track day-by-day tasks in the browser with no backend and no account setup.

## Portfolio Summary

This project started as a simple personal productivity tool and grew into a richer daily planning app with multiple task behaviors, date-based views, and local backup support. For portfolio sharing, personal backup files and local-only data have been excluded from version control.

Suggested GitHub repository description:

> Single-file vibe-coded daily checklist app with date-based planning, recurring duration tasks, local backup, and browser-only storage.

## Features

- Date-based checklist view with separate categories for each day
- Default `Daily` category that always exists for recurring routines
- Multiple task types:
  - `Regular`: exists only on the selected date
  - `Daily (Independent)`: appears every day, but completion is tracked per date
  - `Daily (Shared)`: appears every day and disappears globally when completed
  - `Duration`: spans a date range and can repeat weekly, monthly, or yearly
- Drag-and-drop task reordering and cross-category moves
- Task detail modal with title and description editing
- Color and opacity controls for visual grouping
- Trash flow for completed shared daily tasks
- JSON backup export from the browser

## Tech Stack

- HTML
- CSS
- Vanilla JavaScript
- `localStorage` for client-side persistence

## Compatibility

- Works on both Windows and macOS
- Runs in modern browsers such as Chrome, Safari, and Arc
- No installation is required beyond opening the static app in a browser

## Privacy and Data Handling

- The app stores checklist data in the browser's `localStorage`.
- No backend, database, or external API is used.
- Personal backup JSON files, screenshots, and local recovery/debug files are excluded from this repository.

## Run Locally

Because this is a static app, you can run it in either of these ways:

1. Open `index.html` directly in your browser.
2. Or serve the folder with any static server.

Example with Python:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Project Structure

```text
.
|-- index.html
|-- README.md
|-- README.ko.md
`-- .gitignore
```

## What I Focused On

- Designing task behavior for different real-life planning needs
- Managing state entirely on the client without a framework
- Building an interactive UI with drag-and-drop and modal editing
- Keeping personal data out of the public portfolio version

## Future Improvements

- Split the single HTML file into separate HTML, CSS, and JavaScript files
- Add import/restore UI to the public version in a cleaner workflow
- Improve accessibility and mobile interactions
- Add lightweight tests for task creation and repeat logic
