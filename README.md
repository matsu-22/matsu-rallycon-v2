Matsu RallyCon v0.8.52 — KOMAREN KANTO 2026 KM-TOTAL FIX

基準：v0.8.51_KOMAREN_KANTO_2026_PDF_REPLACED

変更内容
- 内蔵A5 PDF「コマ練関東2026」のRB85〜RB102で、元PDF上に「#####」と表示されていたKM-TOTALを累積距離で補完。
- RB84のKM-TOTAL 218.69 kmを起点に、元PDFのKM-INTER値を順に加算し、KM-TOTAL欄に数値を表示。
- PDFは23ページを維持。RB85〜RB102以外のページ内容は意図的に変更していません。
- アプリのGPS計算、距離補正、セッション復元、ボタン配置、SmartRemote操作などの処理ロジックは変更していません。

検証
- PDFページ数：23ページ
- RB85〜RB102の18箇所すべてで「#####」を置換
- 置換後PDFから各KM-TOTAL数値をテキスト抽出できることを確認
- ZIP内は index.html と README.md
- JavaScript構文検査は作成後に実施

注意
- 本版は内蔵PDFのKM-TOTAL表示修正版です。実機で起動PDF表示とRB85〜RB102のNEXT/BACK移動を確認してください。
