# Matsu RallyCon v0.8.48 GPS RESUME / WAKELOCK TEST

## Purpose
Based directly on the verified v0.8.47 diagnostic R2 build. This test isolates the iPhone foreground-resume path.

### Change in this version
- Screen Wake Lock is requested asynchronously on resume instead of being awaited before GPS recovery.
- Wake Lock request/result/error is logged. A 3-second diagnostic timeout prevents it from blocking the GPS path.
- `getCurrentPosition()` request is issued immediately after resume. GPS error code/message is now logged.
- Existing GPS distance calculation, LOST/recovery rules, PDF, UI, remote controls, and embedded PDF data are otherwise unchanged.

### Test
1. GPS ON and START.
2. Confirm TOTAL is running.
3. Put iPhone in background for about 60-90 seconds.
4. Return to RallyCon.
5. Open diagnostics by tapping the top `Matsu RallyCon` title 5 times.
6. Check whether `GET_CURRENT_POSITION_REQUEST` appears immediately after `RESUME_FROM_BACKGROUND`, and whether `GET_CURRENT_POSITION_OK` or `GET_CURRENT_POSITION_ERROR` follows.
7. Also check `WAKELOCK_*` entries.

This is still a diagnostic/test build. Do not treat it as the production baseline until the resume behavior is verified.
