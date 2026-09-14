# Matsu RallyCon v0.6.28

Based directly on v0.6.12. The layout, PDF viewer, GPS, independent TOTAL/LEG corrections, AUTO NEXT, and bottom controls are retained.

Compass update: on iPhone Safari, `webkitCompassHeading` is adjusted using the current iPhone screen orientation so landscape use follows the screen-top / bike-forward direction. `window.orientation` is used on iPhone, with `screen.orientation.angle` as fallback. Compass accuracy is shown when Safari supplies it.

Install: replace the repository root `index.html` with this one. Keep the included PDF, icon, and manifest in the repository root.
