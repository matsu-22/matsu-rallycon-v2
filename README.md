# Matsu RallyCon v0.7.2 GPS DEV

Development build based on v0.7.1.

## Change in this DEV build
- Adds GPS distance correction from **50% to 150%** in **1% steps**.
- Default is **100%**.
- The correction is applied only to GPS distance accumulated **after the rate is changed**.
- Previously accumulated TOTAL/LEG distance is not recalculated when the rate changes.
- The correction rate is saved/restored with the rally session.
- GPS raw distance remains separate from corrected rally distance.
- GPS quality, loss/recovery, jump rejection, and speed calculations are unchanged.

## Existing v0.7.1 behavior preserved
- A4/A5 PDF auto-detection
- A5 KomaRen auto-parse
- Rally navigation core and current UI
- Embedded A4 startup PDF
- Classic2026: 234 RB / 365.19 km

This is a DEV build for real-device testing. Do not treat it as a production release until verified.
