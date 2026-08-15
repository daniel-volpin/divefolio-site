# Divefolio Site Agent Guide

Public support, landing, and privacy documentation site for the native Divefolio iOS application.

## Overview & Live Surfaces

- **Hosting**: GitHub Pages (`https://daniel-volpin.github.io/divefolio-site/`)
- **Pages**:
  - `index.html`: App overview and features
  - `privacy.html`: Privacy policy (local-first data, backup exports, photo access)
  - `support.html`: Support inquiries and FAQs
  - `style.css`: Shared stylesheet

## Boundaries & Relationships

- **Companion Repo**: The Swift/iOS native app source code is located in `apps/divefolio-ios`.
- **Policy Invariants**: Privacy and support copy must accurately reflect the offline-first, exportable `.divefolio` format and local storage behavior of the iOS application.
- **Tech Stack**: Keep pages dependency-free, semantic HTML5 and vanilla CSS. Do not introduce heavy JavaScript frameworks or external tracking scripts.

## Verification

```bash
# Local static preview
python3 -m http.server 8000
```
