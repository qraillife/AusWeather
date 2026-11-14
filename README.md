# AusWeather 3.1 — High-Quality Logo Edition

A responsive Australian weather web app, visually based on the supplied AusWeather concept image.

## What is included

- High-resolution custom AusWeather icon and transparent header logo
- Home dashboard with current temperature, condition, rain chance, wind, humidity, UV and a scenic blue header
- Hourly weather and seven-day forecasts
- Forecast tabs (7 day / hourly / details)
- Interactive radar map with recent RainViewer radar frames and playback (when available)
- Links to official BOM weather warnings and radar
- Australian location search, GPS, and saved locations
- Celsius/Fahrenheit, light/dark appearance
- Installable progressive web app (PWA) with offline app-shell caching
- Responsive design for iPhone, Android and desktop

## Publish with GitHub Pages

1. Unzip the package.
2. Upload **all the files and the `assets` folder** into the root of your `AusWeather` repository. Keep the filenames and folders as supplied.
3. Open GitHub repository **Settings → Pages**.
4. Choose **Deploy from a branch → main → /(root)** and save.
5. Visit `https://YOUR-USERNAME.github.io/AusWeather/` after GitHub Pages finishes publishing.
6. On iPhone, open that URL in **Safari**, tap **Share → Add to Home Screen**.

### Data sources and limitations

- Forecasts and current conditions: [Open-Meteo](https://open-meteo.com/). These are model-derived estimates, **not official BOM observations**.
- Radar frames: [RainViewer](https://www.rainviewer.com/) over a [Leaflet](https://leafletjs.com/) / [OpenStreetMap](https://www.openstreetmap.org/copyright) map. Radar frames are historical, not predictions; availability can vary. The Leaflet library is loaded from a CDN.
- Official BOM warnings and radar are **links** to BOM. AusWeather does not ingest or issue warnings or push alerts.
- The concept image includes native widgets and app-store badges. This web app does **not** include native iOS widgets or App Store / Play Store listings.
- Search, weather, and radar need an internet connection. The service worker only caches the interface for offline reopening.
- GPS works only on HTTPS sites (such as GitHub Pages) and after the user grants location permission.
- New icon assets: `assets/icon-32.png`, `assets/icon-180.png`, `assets/icon-192.png`, `assets/icon-512.png`, `assets/icon-1024.png`. Transparent header branding: `assets/logo-transparent.png`.
- AusWeather is independent and not affiliated with, endorsed by, or operated by the Australian Bureau of Meteorology.

## Updating

Replace the files in GitHub. When updating `sw.js`, change its cache version string to ensure old cached interface files are removed.

## Updating from AusWeather 3.0

1. Extract this ZIP and upload every file to the *root* of the existing GitHub repo, replacing matching files.
2. Upload `assets/` with all updated images, keeping the same paths.
3. Make sure GitHub Pages still deploys from `main` and `/(root)`.
4. Refresh the site. If iPhone Home Screen still shows the old icon, delete the old Home Screen shortcut and use Safari → Share → Add to Home Screen again (iOS may retain an old shortcut icon).

The app remains the same live-weather PWA as 3.0; this release upgrades branding and cache version.
