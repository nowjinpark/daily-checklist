# Vibe Coding Guide

## Start Here

Before changing the app:

1. Read `README.md`.
2. Read `docs/PROJECT_CONTEXT.md`.
3. Read `docs/DATA_PRESERVATION.md`.
4. Inspect `index.html` for the current rendering and storage flow.

## Development Rules

- Preserve personal data and ignored local files.
- Do not parse ignored backup files into committed fixtures or docs.
- Keep `localStorage` keys compatible unless there is a dedicated migration task.
- Prefer small, reversible changes.
- For UI changes, reuse existing task behavior before rewriting logic.
- Treat calendar summaries as read-only.

## Good AI Session Prompt

Use a prompt like this for future work:

```text
Inspect the current app first. Preserve localStorage data and ignored backup files. Implement only the requested change, keep the existing task data shape compatible, and verify date/task flows before finishing.
```

## Review Checklist

- Did the change avoid personal data exposure?
- Did it preserve `checklistData`, `dailyTasks`, `trash`, and `sendToTrash`?
- Did it avoid creating empty records while rendering calendar summaries?
- Does the app still work by opening `index.html` directly?
- Are task creation, editing, completion, deletion, trash, and backup still usable?

