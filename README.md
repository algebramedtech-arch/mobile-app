# ALGEBRA MedTech — all-in-one interactive prototype

This package upgrades the existing ALGEBRA MedTech mobile/tablet prototype while preserving its existing navigation, sample product catalogue, surgeon presentation, hospital visit log, local storage, CSV/JSON exports, brand assets and PWA installation files.

## Included in this build

- Responsive, branded interface for Android phones and tablets
- Interactive procedural 3D body schematic with pointer/touch rotation and zoom
- Body-region selection for head/neck, shoulder, upper limb, spine, thorax, pelvis/hip, lower limb, foot/ankle
- Toggleable schematic layers: bones, muscles, joints, ligaments, nerves, vessels and a sample implant plate/screw overlay
- Motion Lab with play/pause, angle slider and illustrative knee, elbow and shoulder movement
- Searchable sample orthopaedic product catalogue; add demo entries
- Surgeon/product presentation view with print/save-to-PDF through the browser
- Hospital visit and follow-up notes stored locally on the device
- Export visit logs as CSV and product data as JSON
- PWA manifest, app icons, logo and service worker cache

## Deploy to the existing GitHub Pages repository

1. Download and unzip this package.
2. Open the existing repository `algebramedtech-arch/algebra-medtech-app` on GitHub.
3. Upload/replace `index.html`, `manifest.json`, `sw.js`, and upload the `assets/` and `icons/` folders with their contents at the repository root.
4. Commit the changes to `main` and wait for GitHub Pages to finish deploying.
5. Open `https://algebramedtech-arch.github.io/algebra-medtech-app/` in Chrome. Remove the old home-screen shortcut, then use Chrome's Install app / Install and create shortcut option again.

## Important limits

This is a working software prototype, not a complete clinical anatomy product. The body and tissue layers are procedural schematic geometry, not medically accurate individual bones, muscles, ligaments, nerves or vessels. Motion is illustrative and is not a validated biomechanical simulation. The implant overlay is a generic visual example, not a surgical guide. Realistic anatomy requires suitable original or properly licensed 3D models and clinical review; real implant models/specifications should come from approved manufacturer documentation.

The app loads Three.js from a CDN, so the 3D viewer requires an internet connection. The service worker caches the app shell, but does not guarantee offline operation of the 3D engine. Data is saved in the current browser/device only; there is no staff login, encryption, cloud sync, multi-user access or managed backup. GitHub Pages is public, so do not enter patient-identifiable, confidential hospital, or sensitive business information.

## Main files

- `index.html` — app interface and interactive demo logic
- `manifest.json` — PWA install metadata
- `sw.js` — app-shell caching
- `assets/algebra-logo.png` — supplied ALGEBRA MedTech logo
- `icons/` — 192 px and 512 px install icons
