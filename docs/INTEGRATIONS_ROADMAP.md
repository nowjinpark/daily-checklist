# Integrations Roadmap

## Strategy

Start with account-free export before account-based sync. The first integration target is one-way `.ics` export.

## Phase 1: ICS Export

Add a way to export selected tasks or date ranges as an `.ics` calendar file that can be imported into Apple Calendar, Google Calendar, Outlook, or other calendar apps.

Current baseline: `index.html` includes one-way ICS export for either the selected date or the current visible month.

Recommended scope:

- Export selected date.
- Export current month.
- Include task title as event summary.
- Include task description when present.
- Keep export one-way and non-destructive.

## Phase 2: Optional Calendar API Sync

Later, consider direct Google Calendar or Outlook integration. This requires OAuth, API credentials, consent screens, token storage, and clear privacy documentation.

## Phase 3: Optional Task App Integration

Possible future integrations:

- Notion
- Todoist
- Apple Reminders through platform-specific workflows
- Manual JSON import/export between devices

## Privacy Rules

- Do not send checklist data to external services without explicit user action.
- Prefer exports that the user downloads or imports manually.
- Document what data leaves the browser before adding any API integration.
