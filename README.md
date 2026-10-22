Matsu RallyCon v0.8.55 — GPS Correction 0.1% + TOTAL/RB Sync

基準：ユーザー指定の GitHub ZIP（matsu-rallycon-v2-main）

変更内容
- GPS距離補正を50.0〜150.0%の範囲で0.1%刻みに変更。モーダル表示、連続押し、セッション復元表示も小数1桁に統一。
- TOTALを減らしたとき、TOTAL距離より先にある最初のターゲットコマへRB表示を戻すように変更。
- アプリのタイトル、APP_VERSION、VERSION.txt、README、Web App Manifestの名前とバージョンをv0.8.55へ統一。
- セッション保存キーと旧バージョン互換リストは維持。既存セッション復元への不要な影響を避けるため。
- 内蔵PDFおよび既存のPDF表示、GPS距離積算、NEXT/BACK、AUTO NEXT、SmartRemoteの処理は今回の変更対象外。

検証
- JavaScript構文検査（node --check）を実施。
- ZIP整合性検査を実施。
- 変更差分を確認。

注意
- 実機でのGPS走行・TOTAL減算・NEXT/BACK・AUTO NEXT・SmartRemote・セッション復元の最終確認は別途必要です。
