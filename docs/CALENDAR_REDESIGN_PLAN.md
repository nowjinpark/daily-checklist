# Calendar Redesign Plan

## Goal

Turn the app's base experience into a calendar-first checklist: users see a monthly calendar, select a date, and manage that date's tasks in a detail area.

## Current Status

A first calendar-first UI has been added to `index.html`. The app now shows a monthly calendar, date selection, read-only task indicators, and a selected-day detail panel that reuses the existing task editor.

## Target Experience

- Show a monthly calendar as the main screen.
- Provide previous month, next month, and today controls.
- Highlight today and the selected date.
- Clicking a date selects it and opens that date's task detail view.
- Keep the current category and task editing workflow available for the selected date.
- Show compact indicators in each date cell, such as total task count, completed count, or a small status marker.

## Data Behavior

- Keep using `checklistData`, `dailyTasks`, `trash`, and `sendToTrash`.
- The selected date should continue to drive the existing task renderer.
- Calendar summary helpers must be read-only. They must not call helpers that create new date entries while drawing a month.
- Creating, editing, checking, deleting, restoring, and backing up tasks should continue to use the existing save flow.

## Suggested UI Structure

- Header: app title, backup button, trash button.
- Calendar toolbar: current month label, previous/next buttons, today button.
- Calendar grid: seven weekday columns and month date cells.
- Day detail panel: selected date label, task categories, add category/task controls, and task detail modal.
- Trash view: may remain a separate view, but should preserve a clear path back to the calendar.

## Implementation Phases

1. Add read-only task summary functions for a given date.
2. Build the calendar grid and connect date selection to the existing date state.
3. Move the existing category renderer into the selected day detail panel.
4. Update styling for desktop and mobile calendar layouts.
5. Add regression checks for date creation, task counts, and existing task editing.
