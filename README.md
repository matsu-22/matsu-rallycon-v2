# Matsu RallyCon v0.8.47 GPS BACKGROUND DIAGNOSTIC TEST

## Purpose
This is a diagnostic build based directly on v0.8.46. It records iPhone Safari/WebKit background/foreground GPS callback behavior. It does not add background distance inference and does not intentionally change the existing GPS distance calculation, LOST/recovery logic, PDF data, or rally controls.

## Diagnostic access
On narrow/portrait screens the existing v0.8.46 CSS hides the STATUS text. Therefore this diagnostic build does NOT depend on STATUS for access. Tap the `Matsu RallyCon` brand name at the top 5 times within about 1.8 seconds to open the diagnostic panel.

## What is recorded
- visibilitychange / pageshow / pagehide
- watchPosition start / armed / error / stop
- GPS callback latitude/longitude/accuracy/speed and callback gap
- resumeFromBackground
- getCurrentPosition request / success
- visibility/running/GPS state/sample count/TOTAL at each event

## Test
1. Start the app and confirm the normal PDF/rally screen is displayed.
2. Turn GPS ON and START.
3. Confirm TOTAL is updating normally.
4. Put the iPhone in the background and move/ride for a measured period.
5. Return to RallyCon.
6. Tap the top `Matsu RallyCon` brand 5 times.
7. Inspect the event order and callback `gap=...s`.

## Important
This is a cause-finding diagnostic build, not a production GPS fix. Do not infer or fabricate background distance from elapsed time. v0.8.46 remains the baseline.
