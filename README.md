# Matsu RallyCon v0.7.1

Koma-zuka (roadbook) rally navigation web app.

## v0.7.1

### Numeric display refinement
- LEG / SPEED / NEXTまで numeric values use the same enlarged display size.
- LEG / SPEED / TARGET / NEXTまで remain centered for quick visual recognition.
- TOTAL remains centered with its existing adaptive sizing for larger values.
- No functional rally-navigation behavior was changed for this UI refinement.

### v0.7 foundation
- Automatically detects A4 and A5 roadbook PDFs when a PDF is loaded.
- Existing A4 route behavior is preserved.
- A5 KomaRen PDFs are parsed automatically on the device/browser and converted into the rally route.
- A5 roadbooks are handled as full-page displays with current-roadbook-row positioning.
- A4 and A5 PDFs can be switched back and forth with `LOAD PDF`.

### Verified roadbooks
- A4 KOMAREN Classic2026: 234 RB / 365.19 km
- A5 KOMAREN Classic2026: 234 RB / 365.19 km
- A5 第6回なのはなラリー: 66 RB / 177.33 km

### Rally navigation core
- GPS distance measurement with accuracy and abnormal-jump filtering.
- TOTAL / LEG / TARGET / NEXTまで distance model.
- Automatic NEXT progression and multiple-point skip handling.
- TARGET roadbook-cell auto-centering while preserving safe PDF pan limits.
- GPS loss/recovery handling and background/foreground recovery.
- Rally session persistence; reload restores as PAUSED rather than silently resuming.
- START long-press session reset with confirmation.
- Touch-safe distance correction controls.

### UI
- Existing v0.7 dashboard layout is preserved.
- TOTAL / LEG / SPEED on the left.
- Roadbook PDF in the center.
- RB / TARGET / NEXTまで / TIME / AUTO on the right.
- This release changes numeric display sizing/alignment only; overall layout is unchanged.

## Important

v0.7.1 is the formal release of the verified numeric-display refinement following real-device visibility testing.

The v0.7 production archive remains preserved separately.
The v0.6.50 stable baseline remains preserved separately.
