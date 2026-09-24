# Matsu RallyCon v0.8.49 GPS RESUME ROBUST

## Purpose
Production candidate focused only on GPS recovery after iPhone/Safari foreground return. Built directly from v0.8.46 golden master.

## Changes
- Removed the `await requestWakeLock()` dependency from `resumeFromBackground()`. Wake Lock is requested asynchronously and cannot delay GPS recovery.
- On foreground resume while GPS is enabled, immediately marks GPS LOST so the first valid post-resume fix is handled by the existing LOST→recovery path.
- Keeps `watchPosition` as the primary recovery path. `getCurrentPosition()` is only a helper and never blocks the watch.
- Added a short resume de-duplication guard because `visibilitychange` and `pageshow` can both trigger around the same return.
- Added a resume token so a late `getCurrentPosition()` result from an older resume cannot overwrite a newer recovery state.

## Intentionally unchanged
- GPS distance calculation, correction rate, accuracy threshold, speed-jump rejection, and straight-line recovery calculation.
- TOTAL / LEG / TARGET / NEXT / SPEED display.
- PDF loading, embedded A5 PDF, viewport restore, rally navigation, AUTO, SmartRemote mappings.
- Session save/restore data structure.
- No estimated background distance is added.

## Important finding carried forward
Real iPhone/Safari tests showed normal ~1 s foreground callbacks, stopped callbacks in background, and delayed/inconsistent GPS callbacks after foreground return. v0.8.48 also showed that `getCurrentPosition()` can return immediately in some resumes but may remain pending while `watchPosition()` later resumes. Therefore no recovery path depends on `getCurrentPosition()` completing.

## Page lifecycle note
v0.8.46 contains both `visibilitychange` and `pageshow/pagehide` handlers. A diagnostic run also observed PAGEHIDE→BOOT→PAGESHOW(persisted=false), indicating a full page recreation/reload rather than a simple visibility transition. This candidate does not alter session restore semantics; that separate lifecycle behavior should be tested independently to avoid mixing two causes.

## Verification
- Built from the exact v0.8.46 index.html, not from a diagnostic build.
- Embedded A5 PDF SHA-256: f1432c1e575478146e2b6035e2c23eb96b2686f13755a1b6589ac61ede207a39
- v0.8.46 and v0.8.49 embedded PDF hashes are identical.
- JS syntax checked with Node.js.
