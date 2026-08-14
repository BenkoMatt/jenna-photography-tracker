# Jenna's Photography Tracker

A mobile-first web app for tracking photography shoot mileage and scheduling upcoming shoots.

## Features

### Shoot Log
- Log completed shoots with date, client name, category, names of people photographed, miles driven, and notes
- Summary dashboard: total shoots, total miles, this month's shoots, this month's miles
- Sortable entries (by date, client, or miles)
- Mobile: stacked card layout / Desktop: sortable table with total mileage footer
- Delete entries with confirmation dialog

### Calendar
- Monthly calendar grid with prev/next/today navigation
- Click any date to schedule a future shoot
- Scheduled shoots appear as color-coded tags on the calendar
- Modal shows existing shoots for the selected date with inline delete
- "All Scheduled Shoots" list below the calendar

### Design
- Editorial photography aesthetic — Cormorant Garamond serif headings + Inter body text
- Warm palette: cream background, charcoal text, muted gold and dusty rose accents
- Color-coded category system (11 categories, each with its own hue)
- Mobile-first responsive layout (bottom-sheet modals, 16px input font to prevent iOS zoom, 44px touch targets)
- Toast notifications (no native alert/confirm dialogs)
- Aperture SVG favicon
- `prefers-reduced-motion` support

## Data Storage

All data is stored in the browser's `localStorage`:
- `jenna_shoots` — completed shoot log entries
- `jenna_schedule` — upcoming scheduled shoots

No server or backend required. Each device keeps its own data.

## Usage

Open `index.html` in any modern browser. It works offline once loaded.

For mobile use, you can:
1. Open the file directly in a mobile browser
2. Host it on any static file server and bookmark the URL
3. Add it to your home screen for app-like behavior

## Categories

Portrait, Wedding, Engagement, Family, Senior, Event, Newborn, Maternity, Boudoir, Commercial, Other

## Tech

- Single self-contained HTML file (no build step, no external JS dependencies)
- Google Fonts via `<link>` (Cormorant Garamond + Inter)
- Modern CSS: variables, grid, flexbox, `clamp()`, container queries
- Vanilla JavaScript (IIFE, no frameworks)

## License

MIT