# Data Preservation

## Non-Negotiable Rule

Never delete, overwrite, expose, or migrate existing user checklist data without an explicit backup and a tested restore path.

## Protected Data

The protected data includes:

- Browser `localStorage` data for this app.
- Ignored `checklist-backup-*.json` files.
- Screenshots and local recovery/debug files.
- Any task titles, descriptions, dates, categories, or completion states from personal backups.

## Backup Before Change

Before persistence or calendar-rendering changes:

1. Open the current app in the browser profile that contains the real data.
2. Use the app's Backup button to export a fresh JSON backup.
3. Keep the backup outside commits.
4. Verify the app still loads after the change.
5. Verify existing date-specific tasks and daily tasks are still visible.

## Restore and Import Requirements

A future import/restore feature should:

- Accept the same shape exported by the Backup button.
- Validate that the imported JSON includes the expected top-level keys.
- Preview what will be replaced before writing to `localStorage`.
- Offer a fresh export of the current state before replacing it.
- Avoid merging by default unless a separate merge policy is designed.

## Calendar-Specific Safety

The calendar view must not create records for every displayed date. Month rendering should read summaries from existing data only. New date records should be created only when the user edits that selected date or adds data to it.

