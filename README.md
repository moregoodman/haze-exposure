# Haze Exposure Calculator — PM2.5 (NEA Live)

A single-file web tool that estimates your **cumulative inhaled PM2.5 from outdoor exposure** on a haze day in Singapore — walks between the bus stop and home, office or school, commutes, and exercise.

**Live version:** hosted on GitHub Pages from this repository (see the URL in the repo's "About" section, or the link below once Pages is enabled).

## What it does

- **Fetches official readings** — hourly regional 1-hour PM2.5 from Singapore's National Environment Agency (NEA), via the [data.gov.sg](https://data.gov.sg) open data API, by date and region (Central, North, South, East, West, or national average). Historical dates work too.
- **Outdoor exposure only** — the dose counts just your outdoor trips, matched to the NEA concentration recorded during each trip's hour.
- **Activity matters** — standing/waiting (×1.0), walking (×1.5), brisk walk/cycling (×2.5), jogging/running (×3.5) breathing factors.
- **Masks matter** — no mask, cloth (≈50% filtered), surgical (≈65%), KN95 (≈80%), N95/FFP2 (≈90%), applied directly to the inhaled dose.
- **Outputs** — daily inhaled dose (µg·h/m³), 24-hour equivalent average, average PM2.5 during your trips, and a risk level read against WHO and Singapore 24-hour guidelines, raised one band for sensitive persons.
- **Works offline** — if the NEA fetch is unavailable, readings can be typed into the hourly grid manually. No data leaves the device; everything is computed in the browser.

## Using the tool

1. Pick a date and your region, and the hourly readings load automatically.
2. Add your outdoor trips: start time, minutes, activity.
3. Choose the mask you wear, if any.
4. Read your dose and risk level.

## Running it yourself

Download `index.html` and open it in any modern browser. No installation, server, or build step required. An internet connection is only needed for the automatic NEA fetch — manual entry works offline.

## Licence

Free public use under the Creative Commons Attribution 4.0 licence ([CC BY 4.0](https://creativecommons.org/licenses/by/4.0/)). You may use, copy, modify and redistribute this tool for any purpose, including commercially, provided you credit **"Haze Exposure Calculator — PM2.5 (NEA Live)"**.

PM2.5 readings: National Environment Agency (Singapore) via data.gov.sg open data.

## Caveats

Breathing factors, mask filtration percentages and activity adjustments are practical estimates, not official figures. Hourly readings are treated as constant within each hour. This is a screening tool for personal awareness, **not medical advice**.
