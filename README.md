# YouTube Music Auto Like Playlist Script

This JavaScript script automates liking songs in a YouTube Music playlist. It scrolls through the entire playlist to load all songs, skips already-liked ones, and verifies each like before moving on.

## Features

- **Automated liking:** Clicks the Like button only for unliked songs (`aria-pressed="false"`)
- **Full playlist loading:** Scrolls to the bottom repeatedly to force lazy-loaded songs into the DOM before processing
- **Skip already-liked songs:** Detects liked state via `aria-pressed`, active classes, and nearest liked containers — skips safely
- **Pre-click recheck:** Re-validates each button right before clicking in case the DOM updated during scroll
- **Post-click verification:** Confirms the button flipped to liked after clicking; warns in the console if it didn't
- **Random delays:** Waits 1–3 seconds between likes to mimic human behavior and reduce rate-limiting risk
- **Progress logging:** Logs every skip, like, and warning with song index and total count

## Instructions

1. Open the playlist you want to like in your browser (Chrome or any Chromium-based browser recommended)
2. Press `Ctrl` + `Shift` + `J` to open the Developer Console
3. If pasting is blocked, manually type `allow pasting` and press `Enter` to enable it
4. Copy the `Script` and paste it into the console, then press `Enter`
5. Done
