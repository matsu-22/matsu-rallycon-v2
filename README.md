# Matsu RallyCon v0.7.1 DEV

Koma-zuka (roadbook) rally navigation web app.

## v0.7.1 DEV

### Numeric display refinement
- TOTAL / LEG / SPEED / TARGET / NEXT are centered.
- LEG / SPEED / NEXT numeric values use one unified, slightly larger display size.
- No functional behavior or overall dashboard layout was changed.
- This remains a DEV build pending real-world visibility confirmation.

## v0.7

### A4 / A5 automatic PDF support
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
- Existing v0.6.x rally dashboard layout is preserved.
- TOTAL / LEG / SPEED on the left.
- Roadbook PDF in the center.
- RB / TARGET / NEXTまで / TIME / AUTO on the right.
- UI/CSS layout is unchanged for the v0.7 milestone.

## Important

v0.7 is the first milestone release that combines the established A4 rally behavior with automatic A5 roadbook detection and parsing in the same app.

The v0.6.50 stable baseline remains preserved separately.
