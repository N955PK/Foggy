# fog/california

Live fog for the whole state — marine layer on the coast, tule fog in the Central Valley — seen from 22,000 miles up by NOAA's GOES-18 (GOES-West) satellite.

**Live site:** https://n955pk.github.io/Foggy/

## What it does

- Animated loop of the GOES-18 **Pacific Southwest sector**, which frames all of California; new frames arrive about every 5 minutes and the page refreshes itself
- **GeoColor** by day, blended infrared at night, so low fog stays visible around the clock
- **IR 3.9 µm mode** — the shortwave band forecasters use to pick out fog and stratus in the dark
- Pinch or scroll to zoom, drag to pan, double-tap to zoom in and out
- Time ruler with Pacific-time hour marks, play/pause, ½×–2× speed, 2/4/8-hour spans
- LIVE/DELAYED freshness indicator; controls fade away for a clean full-screen view (tap to bring them back)

## How it works

The whole site is one self-contained `index.html` — no build step, no dependencies, no backend, no API keys. The page reads NOAA's public CDN directory listing at `cdn.star.nesdis.noaa.gov`, pulls the recent frames, and animates them on a canvas. If the listing can't be fetched, it falls back to probing the satellite's 5-minute scan grid directly. It runs on any static host.

## Data & credits

Imagery: [NOAA / NESDIS / STAR](https://www.star.nesdis.noaa.gov/goes/) — GOES-West (GOES-18), Pacific Southwest sector. GeoColor was developed by CIRA and NOAA. Imagery is informational only and not for operational or safety-of-life use.

A statewide homage to [fog.today](https://fog.today).
