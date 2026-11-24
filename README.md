# Starchart Astrology

A single-page astrology app that casts **sun charts** from a date and place of birth, with written interpretations, saved profiles, two-person comparisons (synastry), daily forecasts and printable chart sheets.

## Features

- **Sun chart**: the Sun's sign is the first house (solar whole-sign houses), so no birth time is needed. An optional birth time gives an exact Moon position and the Ascendant (rising sign).
- **Places**: about 150 built-in cities with IANA time zones, so historical daylight saving is handled automatically. Places not on the list can be entered as coordinates plus a UTC offset.
- **Reading**: covers the Sun, Moon and rising sign, each planet's sign and solar house, the balance of elements and modalities, and the major aspects.
- **Saved profiles**: when the page runs as a Claude artifact, each person's profiles are kept in their own private area of their Claude account. Otherwise they are kept in the browser's `localStorage`.
- **Compare**: a bi-wheel with Ease, Spark and overall scores, plus sections on core natures, emotional fit, attraction, communication and the key contacts between the two charts.
- **Daily forecast**: transits to the natal chart for any day, with a 7-day strip, the Moon's sign changes and Mercury retrograde notes.
- **Astrocartography**: a world map of each planet's MC, IC, AC and DC lines at the moment of birth. You can check any place by tapping the map or choosing a city, and the app ranks the listed cities by nearby lines. This needs a birth time. The world outline (Natural Earth, public domain, via `world-atlas`) loads from jsDelivr; if it can't load, cities are shown as dots instead.
- **Printouts**: A4 HTML sheets with an ink-on-white wheel for a single chart or a comparison, plus an SVG of the wheel.

## Accuracy

Planet positions use Paul Schlyter's low-precision orbital elements, including the main lunar, Jupiter, Saturn and Uranus perturbation terms. They are accurate to a few arc-minutes from 1900 to 2100. Everything is calculated in the browser.

## Running it

Open `index.html` in a browser. There is nothing to install or build. Fonts load from Google Fonts. Account storage and file downloads use the Claude artifact runtime (`window.claude`). Without that runtime, profiles fall back to `localStorage`, and downloads are only available inside Claude.

Astrology is for reflection and fun rather than prediction.
