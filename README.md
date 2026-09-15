# Matsu RallyCon v0.6.49

### v0.6.49
- 上部バー中央に現在の日付と時刻を表示。既存のトップバーのグリッド領域を変更せず、中央絶対配置で追加。
- バックグラウンド復帰時、および復帰に伴う画面レイアウト再計算後に、現在のRBのターゲットコマを再センタリング。
- 既存のGPS距離計算、PDF表示、UI配置、操作仕様は維持。
- 3桁のRB（100～234）は18pxへ自動縮小し、RB番号が見切れないように調整。既存レイアウトの列幅は変更しない。
- 3桁のTOTAL（100.00km以上）は52pxへ自動縮小し、365.19kmまで見切れないように調整。
- 既存の2桁以下のTOTAL/RB表示サイズ、UIレイアウト、PDF表示、操作ロジックは変更なし。
- TOTAL / LEGの数字をタップすると、任意のkm値を直接入力して設定可能。
- ±10m補正の長押しは時間に応じて10m → 50m → 100m → 500mへ段階的に加速し、大幅な距離修正を短時間で行える。短いタップは従来どおり10mを1回だけ補正。

### v0.6.42
- RBが前進したとき、LEGの基準を新しいTARGETへ再同期。
- TARGET通過後に次のRBへ進んだ場合は、通過済み距離をLEGへ即時反映。
- 例：TOTAL 2.76kmでRB3（TARGET 4.48km）へ進んだ場合、LEGは2.76km、NEXTまで1.72km。
- LEGの±10m補正は新しいRBへの前進時にいったん0へ戻し、現在のTOTALを新しいLEG基準として再構築。
- BACKでは既存のLEG値を変更しない。
- UI/CSS/PDF表示は変更なし。

SPEED display is rounded to whole km/h for at-a-glance rally readability; internal GPS speed remains unchanged.

Distance correction and reset controls are hardened for glove/touch use: ±10m buttons repeat while held, TOTAL/LEG 0 buttons require a long press and confirmation, and app UI text selection/callouts are disabled.

Based on the verified v0.6.37 build. UI and existing PDF rendering/pan behavior are preserved; only TARGET-change auto-centering is added. This build hardens the distance/session core without changing the dashboard layout.

## v0.6.40 PC-side hardening
- TOTAL / LEG / NEXTまで use one consistent corrected-distance model.
- ±10m correction is applied to TOTAL and therefore also to NEXTまで / AUTO NEXT.
- AUTO NEXT has an explicit internal trigger constant and handles skipped-over close roadbook points safely.
- BACK / NEXT no longer silently resets LEG; LEG is independently reset with its existing 0 button.
- START / STOP remains pause/resume; screen Wake Lock is requested while running and reacquired after returning from background when supported.
- Session state is saved locally and restored as PAUSED after a reload; a reload never silently resumes motion or GPS measurement.
- Existing GPS loss/recovery behavior from v0.6.35 is preserved.
- Background/foreground handling was strengthened: while RUNNING, returning to the app requests a fresh high-accuracy position fix and re-acquires Wake Lock; if the browser dropped the geolocation watch, the app attempts to restart it.
- Page visibility/page show events save session state before hiding and trigger a resume fix after returning. This does not claim guaranteed continuous background GPS; browser/OS policies can throttle or suspend hidden pages.
- UI and CSS are unchanged. Existing PDF rendering, zoom, manual pan and scroll limits are preserved; TARGET-change auto-centering is the only PDF viewport behavior added.

- TARGET roadbook-cell centering: when RB changes via START / NEXT / BACK / AUTO NEXT, the corresponding roadbook cell is automatically brought toward the vertical center of the PDF viewport. Existing pan limits remain enforced, so edge cells stop at the safe scroll boundary. Manual pan/zoom behavior and the dashboard UI are unchanged.

## v0.6.40
- START button long-press (1.6s) provides a confirmation dialog for full rally-session reset.
- Reset clears rally session state only; PDF and AUTO setting are retained.
- Reset stops GPS, releases wake lock, resets RB to the first target (2.65 km), and clears saved session.
- Session restore accepts legacy v0.6.38/v0.6.39 session records and saves them as v0.6.41.
- Existing UI/CSS/PDF and GPS/PDF behavior remain unchanged.

## v0.6.41 touch-operation hardening
- TOTAL / LEG −10m and ＋10m: short tap = one 10m correction; hold = repeated 10m corrections.
- TOTAL / LEG 0: short tap does nothing; long press opens a confirmation dialog before zeroing.
- START long-press reset remains confirmation-protected.
- Rally UI text selection and long-press callouts are disabled; PDF canvas behavior is unchanged.
- UI layout/CSS geometry and existing PDF rendering behavior are otherwise preserved.




- v0.6.49: RB 3桁表示をさらに縮小して確実に収まるよう調整。TOTAL/LEGの直接数値入力は表示数字の長押し（700ms）で起動し、短いタップでは入力画面を開かない。


## v0.6.49
- TOTAL / RB / TARGET / LEG の数値表示を枠内に確実に収めるため、表示幅に応じて数値フォントを調整。
- LEG の数値を右詰め表示。
- 既存のPDF表示、GPS、セッション、操作ロジックは変更なし。
