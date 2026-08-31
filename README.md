# Points Router

A free, browser-only tool for deciding which Chase Ultimate Rewards flight
redemption is actually worth it.

Live version: publish `index.html` anywhere static (or just open it locally)
— there's no backend, no build step, and no API keys.

## Why this exists, and what it isn't

A true point.me-style engine — live award-seat search across 150+ airlines —
needs paid data feeds (Seats.aero's API is a paid Pro feature) or scraping
that violates airline terms of service. Neither is a "free, for me" option,
so this tool doesn't try to search live availability.

What it does instead: you manually check a cash fare and one or more award
options (see "How to find the numbers" below), enter them, and it ranks the
options by **cents-per-point (cpp)** — cash saved per Ultimate Rewards point
spent, after any active transfer bonus — and flags which ones clear a value
threshold worth transferring for.

## Features

- Reference table of Chase Ultimate Rewards' airline/hotel transfer
  partners and ratios
- Add multiple quotes (cash price, program, miles required, taxes/fees,
  transfer bonus %) for the same trip
- Auto-ranks by cents-per-point, highlights the best option, flags poor
  value against an adjustable baseline (default 1.5¢/point)
- Everything is saved to your browser's `localStorage` — nothing leaves
  your machine, no account, no server

## How to find the numbers

1. **Cash price** — Google Flights or the airline's own site, same
   route/cabin/dates.
2. **Award space** — log into the partner program directly
   (united.com, aircanada.com/aeroplan, flyingblue.com, ba.com,
   singaporeair.com, etc.) — the most reliable source for real saver space.
3. **Cross-check** — seats.aero's free web search or point.me's free tier
   (15 results/search) to scan multiple programs at once.
4. **Before transferring** — recheck the seat is still there. Chase
   transfers are instant but final; never transfer speculatively.

## Running it

Just open `index.html` in a browser. To host it somewhere shareable, any
static host works (GitHub Pages, Netlify, etc.) since it's a single
self-contained file.
