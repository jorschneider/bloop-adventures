# 2 Year Old Adventures

Rainy-day stops for toddlers, mapped subway-style.

- **`index.html` — NYC**: 200 stops, home base 79 St & Broadway.
- **`dc.html` — Washington, DC**: 94 stops around the District and close-in
  suburbs, home base Gallery Place–Chinatown.

Use the NYC/DC toggle in the header to switch cities. Saved stops are kept
per city.

## Running it

It's static pages with no build step:

```sh
# open directly
open index.html

# or serve it
python3 -m http.server 8000   # then visit http://localhost:8000
```

## Features

- **Map + list** — Leaflet map and card list stay in sync; click a stop for a
  detail sheet with hours, pricing, website, and directions.
- **Filters** — category lines (Play, Museums, Animals, Books, Classes, Shows),
  day of week, travel time from home, indoor/outdoor, open play vs. classes,
  price ceiling, and "adults enjoy too".
- **Quick toggles** — Open today, Free, and ♥ Saved.
- **Saved stops** — tap the heart on any card (or Save in the detail sheet);
  favorites persist in `localStorage`.
- **Surprise me** — picks a random stop matching your current filters, for
  when nobody can decide.
- **Search** — matches names, descriptions, categories, and addresses.
- **Dark mode** — follows your system theme, including the map tiles.

## Data

Venue data lives inline in each page (the `D` array). The
`nyc-toddler-*.json` files are the source research notes the NYC list was
compiled from. Hours and prices drift — always check the venue website
before heading out.
