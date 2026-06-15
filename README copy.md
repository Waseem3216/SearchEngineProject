# XYMZ Search! Retro Pro

This version preserves the original early-web layout and upgrades it with professional static functionality.

## Start

Open `index.html` directly in a browser.

Or run a local server:

```bash
python3 -m http.server 8000
```

Then visit:

```text
http://localhost:8000
```

## What changed

- Maintained the original retro search-engine design
- Removed the visitor counter
- Recolored the XYMZ logo with unique non-Google colors
- Added many animations and 3D hover/float effects
- Added a functional static search engine over an internal XYMZ index
- Added categories/channels: Web, Images, MP3, Games, Shareware, Forums, Business, Retro
- Added advanced search controls
- Added search suggestions
- Added result previews, bookmarks, saved searches, and JSON export
- Added a command box with Ctrl/Cmd + K
- Added an agentic AI-style chatbox that asks what users are looking for and runs searches
- Replaced external searching with an internal XYMZ-only search button
- Added functional forms/modals: Submit URL, Email signup, FAQ, ads, footer links
- Added localStorage persistence for theme, saved searches, bookmarks, and history

## Note

The site is static. The built-in search engine searches the local XYMZ index in `script.js`.
All results stay inside XYMZsuite.com. No Google, DuckDuckGo, Bing, or other search engine is used.

## Result-click behavior

Result titles now open inside a local XYMZ virtual result viewer instead of navigating to fake domains.
The displayed URLs are intentionally fictional for the retro search-engine illusion. Use the "Search Real Web" button for an actual external search.


## XYMZ-only result behavior

This build does not send users to Google, DuckDuckGo, Bing, or fake external domains.
Every result title opens a virtual result page inside the XYMZ Search interface.
All displayed result URLs use the XYMZsuite.com domain, for example:

```text
https://www.XYMZsuite.com/images/media/birdwatcher-central/
```

Because this is a static site, accuracy comes from the internal `XYMZ_INDEX` dataset inside `script.js`.
To make results accurate for more topics, add more real curated entries to that internal index.


## Important internal-search fix

This version keeps every result inside `https://www.XYMZsuite.com`.

- Result titles no longer navigate to real browser paths.
- Result clicks open an internal XYMZsuite virtual result viewer.
- `vercel.json` and `_redirects` are included so deployed paths like `/images/forum/...` route back to `index.html` instead of showing a 404.
- The search can import public knowledge/image results into XYMZsuite cards when the browser allows CORS/network access.
- It does not open Google, Bing, DuckDuckGo, or any external search-engine result page.
- For image searches, XYMZsuite renders image cards internally and can pull public Wikimedia image results into the site.
