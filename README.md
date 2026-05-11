# KEYS100 2026 — Team Tracker

Single-page tracker for the 2026 KEYS100 Ultramarathon (May 16–17, 2026, Key Largo → Key West).

## What it does

- Lists every checkpoint from the official 2026 Race Guide "Course Details & Meet-Up Locations" table — ~100 entries from MM 99.8 down to MM 0 (finish line at Higgs Beach).
- Checkbox per checkpoint (done / not done).
- Dropdown selector per checkpoint to assign **Jacob**, **Josh**, **Aaron**, or **Darby** as the runner for that leg.
- Tags rows as `MEET-UP`, `TIMING`, or `CROSS` (highway crossing) for quick scanning.
- Stats bar shows total checked + how many legs each runner is assigned.
- Filters: by runner (or "unassigned only") and by checkpoint type (meet-ups only / timing mats only).
- State auto-saves to browser `localStorage` — close the tab and come back, your data is still there.
- Export current state to JSON.

## How to use

Open `index.html` in any browser. That's it. No build step, no dependencies.

## Data source

Pulled from the official 2026 KEYS100 Race Guide (PDF, May 2026), pages 14–18 — "Course Details and Meet-Up Locations".

## Notes

- Rows highlighted **blue** = official meet-up locations.
- Rows highlighted **yellow** = timing equipment / scoring mats.
- The course runs MM 100 → MM 0; sort order in the table matches the direction of the race.
- `state` is keyed by row index in `CHECKPOINTS`, so don't reorder the array without migrating localStorage.
