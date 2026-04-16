# Per-cohort semester rosters

Each subdirectory here is named for one cohort (e.g. `f2025`, `s2026`).
Inside each, `hertie-semester.yml` is the canonical roster for that cohort.

**One file per semester. Nothing ever deleted.**

The DSL sync Action reads the relevant file based on the `semester` parameter
passed to the workflow — so historical cohorts remain sync-capable but are
only touched when explicitly invoked.

## Adding a new semester

Use the "New Semester" workflow in the [gh-org-strategy](https://github.com/hertie-data-science-lab/gh-org-strategy/actions)
repo to auto-create a new cohort directory and populate the roster template.

## Editing a roster

Edit the relevant `semesters/{code}/hertie-semester.yml`. Push. The sync
Action fires automatically (or wait for the weekly Monday cron).
