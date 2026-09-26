# Matsu RallyCon v0.8.50 PAGE LIFECYCLE DIAGNOSTIC

## Purpose
Diagnostic-only build based directly on v0.8.49 GPS RESUME ROBUST. It investigates the observed PAGEHIDE -> BOOT -> PAGESHOW(persisted=false) sequence and session persistence after page recreation.

## Diagnostic behavior
- Normal app UI and GPS/PDF behavior are unchanged.
- Tap the top “Matsu RallyCon” brand 5 times to open the diagnostic panel.
- The panel reads a lifecycle log stored in localStorage.
- Logs BOOT, pageshow/pagehide persisted state, visibilitychange, beforeunload, navigation type, and whether the rally session exists after boot.
- The diagnostic log is intentionally persisted so a later BOOT can reveal what was recorded before the page was recreated.

## Intentionally unchanged
- GPS distance calculation and v0.8.49 GPS resume logic.
- TOTAL / LEG / TARGET / NEXT / SPEED.
- PDF, embedded A5 PDF, viewport restore, rally navigation, AUTO, SmartRemote.
- Existing session save/restore implementation.

## Test target
Determine whether the observed BOOT is a normal page recreation with a surviving localStorage session, and whether the session is restored to the expected paused state. This build does not attempt to fix the lifecycle issue.
