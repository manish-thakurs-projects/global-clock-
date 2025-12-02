# Global Clock with Spotify

A minimal, responsive web app that shows live time and date across multiple time zones, with a built–in Spotify playlist player for background music.

This project is built as a single static HTML file using vanilla HTML, CSS, and JavaScript. No build tools, no dependencies.

---

## Features

- 🌍 **Global Time Zones**
  - Uses `Intl.supportedValuesOf('timeZone')` to list all supported IANA time zones.
  - Shows the first 50 time zones by default (for performance).

- 🔍 **Live Search**
  - Search any timezone by name (e.g., `Asia/Kolkata`, `America/New_York`).
  - Dynamically filters the list and renders up to 50 matching time zones.

- ⏱️ **Real-Time Clock Cards**
  - Each card shows:
    - Time zone name (formatted nicely with spaces instead of underscores).
    - Current time (HH:MM:SS, 12-hour format).
    - Current date (weekday, day, month, year).
  - Auto-updates every second.

- 🕰️ **Focused Clock Modal**
  - Click any clock card to open a fullscreen modal for that time zone.
  - Shows:
    - Large digital time display.
    - Full date.
    - Time zone name.
  - Updates every second while the modal is open.

- 🎵 **Embedded Spotify Player**
  - Integrated Spotify embed player inside the modal.
  - Currently linked to a specific playlist:
    - `https://open.spotify.com/embed/playlist/3sJYo4FraKnU7ceSC12YyT`
  - Plays in the background while you explore time zones.

- 📱 **Responsive Design**
  - Grid layout on larger screens, single-column layout on smaller devices.
  - Large modal time shrinks for smaller viewports to stay readable.
  - Custom dark theme with a neon-like accent color.

- 🧼 **Clean UI**
  - Sticky search bar at the top.
  - Card hover effect for better interactivity.
  - Scrollbar hidden for a clean, immersive feel.

---

## Tech Stack

- **HTML5** – Markup and structure.
- **CSS3** – Layout, responsive design, and theming.
- **Vanilla JavaScript (ES2023)** – DOM manipulation, time updates, and search.
- **Intl API** – `Intl.supportedValuesOf('timeZone')`, `toLocaleTimeString`, `toLocaleDateString` for accurate time zone handling.
- **Spotify Embed** – `<iframe>` based embedded playlist.

---

## Getting Started

### Prerequisites

- Any **modern browser** that supports:
  - `Intl.supportedValuesOf('timeZone')` (most recent Chromium, Firefox, Safari).
- An internet connection (required for Spotify embed and playlist streaming).

> Note: On older browsers that don’t support `Intl.supportedValuesOf`, the time zone list may not load correctly.

### Run Locally

1. Create a project folder and save the file as `index.html` (or use the existing one).
2. Open the file in a browser:
   - Option 1: Double-click `index.html`.
   - Option 2: Right-click > “Open With” > your browser.
