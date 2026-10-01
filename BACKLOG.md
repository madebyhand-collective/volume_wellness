# Volume — Backlog

## Add to Google Calendar button (no account connection)
- User chose "no connection at all" for Google Calendar integration (declined shared OAuth and workspace connector registration).
- Build a small button/link on scheduled workouts that opens Google Calendar with the event pre-filled, using the public template URL:
  `https://calendar.google.com/calendar/render?action=TEMPLATE&text=<label>&dates=<YYYYMMDDTHHMMSSZ>/<YYYYMMDDTHHMMSSZ>&details=<...>`
- Natural placements:
  - Upcoming workout commitments in `src/components/home/AccountabilityPanel.jsx` (upcoming list, lines ~67–71).
  - The confirmation step of `src/components/insights/ScheduleSessionDialog.jsx`.
  - The Accountability page (`src/pages/Accountability.jsx`) where scheduled commitments are listed.
- Build the start/end UTC stamps from the commitment's `due_date` + `due_time` (default end = start + 45 min, matching the session cap).