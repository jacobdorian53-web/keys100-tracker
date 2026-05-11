# KEYS100 2026 — Team Tracker

Single-page tracker for the 2026 KEYS100 Ultramarathon (May 16–17, 2026, Key Largo → Key West).

**Live:** https://jacobdorian53-web.github.io/keys100-tracker/

## What it does

- Lists every checkpoint from the official 2026 Race Guide "Course Details & Meet-Up Locations" table (102 entries).
- **Default view** shows the 39 legal pass-off spots for a 100-mile team — from MM 99.8 START to MM 0 FINISH.
- Checkbox per checkpoint (done / not done).
- Dropdown to assign **Jacob**, **Josh**, **Aaron**, or **Darby** as the runner for that leg.
- Color-coded selectors + row tags (PASS-OFF, TEAM, TIMING, CROSS, CREW ONLY).
- Stats: assigned/done counts + leg-count per runner.
- Filters: by runner, by checkpoint type.

## Cloud sync (works across phones / laptops)

The source of truth is `data.json` in this repo. Anyone who opens the live URL pulls the latest version automatically (re-checked every 60 seconds while the tab is visible).

To **save changes**:
1. Click 🔑 in the controls and paste a GitHub personal access token.
   - Classic token: scope `public_repo`
   - Fine-grained token: `Contents: Read and write` on `keys100-tracker` repo only
2. Make your changes.
3. Click **💾 Save to cloud**.

The token is stored only in your browser's localStorage; it never leaves your device except to authenticate to `api.github.com`.

If you don't have a token, everything still works as a read-only viewer.

## How to use offline

Just open `index.html` in any browser. State falls back to `localStorage` if GitHub is unreachable.

## Data source

Pulled from the official 2026 KEYS100 Race Guide (PDF, May 2026), pages 14–18 — "Course Details and Meet-Up Locations".

## Notes

- Rows highlighted **blue** = official meet-up locations
- Rows highlighted **yellow** = timing equipment / scoring mats
- 3 spots are **team-exchange only** (less crowded): MM 95.1, 70.8, 57.4
- The course runs MM 100 → MM 0
- `data.json` is keyed by row index in `CHECKPOINTS`, so don't reorder the array without migrating
