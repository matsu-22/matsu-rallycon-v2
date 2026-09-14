# Matsu RallyCon v0.6.36

Based on the verified v0.6.35 build. UI and PDF viewport behavior are preserved. This build hardens the distance/session core without changing the dashboard layout.

## v0.6.36 PC-side hardening
- TOTAL / LEG / NEXTまで use one consistent corrected-distance model.
- ±10m correction is applied to TOTAL and therefore also to NEXTまで / AUTO NEXT.
- AUTO NEXT has an explicit internal trigger constant and handles skipped-over close roadbook points safely.
- BACK / NEXT no longer silently resets LEG; LEG is independently reset with its existing 0 button.
- START / STOP remains pause/resume; screen Wake Lock is requested while running and reacquired after returning from background when supported.
- Session state is saved locally and restored as PAUSED after a reload; a reload never silently resumes motion or GPS measurement.
- Existing GPS loss/recovery behavior from v0.6.35 is preserved.
- UI, CSS, PDF rendering and PDF pan/viewport behavior are unchanged.
