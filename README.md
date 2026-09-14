# Matsu RallyCon v0.6.32

Based directly on v0.6.30. This build keeps the v0.6.29 UI baseline and v0.6.30 GPS core. The PDF viewport remains top-aligned, but vertical pan bounds now allow the full rendered page to be scrolled to its true bottom. This fixes the issue where downward scrolling stopped around the fourth roadbook cell even though each page contains six cells.

Compass, GPS, independent TOTAL/LEG corrections, AUTO NEXT, and bottom controls are retained.

Install: replace the repository root `index.html` with this one. Keep the included PDF, icon, and manifest in the repository root.
