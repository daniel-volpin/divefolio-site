# Divefolio Site Agent Guide

Public support, landing, and privacy documentation site for the native Divefolio iOS application.

## Overview & Live Surfaces

- **Hosting**: GitHub Pages (`https://daniel-volpin.github.io/divefolio-site/`)
- **Pages**:
  - `index.html`: Landing page, one section per app tab with its screenshot
  - `privacy.html`: Privacy policy (local-first data, backup exports, photo access)
  - `support.html`: Support inquiries and FAQs
  - `style.css`: Shared stylesheet (light and dark)
  - `screenshots/`: Web-sized copies of the app repository's
    `marketing-shots/simulator/` set, 1280 px tall

## Boundaries & Relationships

- **Companion Repo**: The Swift/iOS native app source code is in the private `daniel-volpin/divefolio-ios` repository. This repository is the only copy of the site. The app repository's Quality workflow checks out `privacy.html` and requires its privacy phrases (such as "Apple Maps receives" and "workout route"), so a privacy change here must keep them and match the app's `PRIVACY.md`.
- **Accuracy**: Every screen, tab, and button the pages name must exist in the app. When the app's screenshots are retaken (`scripts/screenshots.sh`), refresh `screenshots/`.
- **Policy Invariants**: Privacy and support copy must accurately reflect the offline-first, exportable `.divefolio` format and local storage behavior of the iOS application.
- **Tech Stack**: Keep pages dependency-free, semantic HTML5 and vanilla CSS. Do not introduce heavy JavaScript frameworks or external tracking scripts.

## Verification

```bash
# Local static preview
python3 -m http.server 8000
```
