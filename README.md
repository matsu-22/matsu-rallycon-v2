# Matsu RallyCon v0.8.51 — KomaRen Kanto 2026 PDF replacement

## Change
- Replaced only the embedded/default A5 roadbook PDF with `【コマ図（A5）】コマ練関東2026.pdf`.
- Updated the visible app/version labels to v0.8.51 so the delivered build is identifiable.

## Intentionally unchanged
- GPS distance calculation and v0.8.49 GPS resume logic.
- v0.8.50 page-lifecycle diagnostic behavior and its persisted log.
- TOTAL / LEG / TARGET / NEXT / SPEED, PDF viewport restore, rally navigation, AUTO, SmartRemote, and session save/restore logic.
- The newly embedded PDF is the only replaced payload; no route parsing or GPS logic was intentionally changed.

## Validation
- Embedded PDF bytes checked against the supplied PDF by SHA-256.
- JavaScript syntax checks should be run on all script blocks before use.
- This is based on v0.8.50 PAGE LIFECYCLE DIAGNOSTIC and remains a diagnostic/test build, not a claim that background GPS limitations are fixed.
