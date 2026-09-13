# Matsu RallyCon v0.6.3 GPS FIX

PDFコマ図表示＋GPS走行距離・LEG・速度・CAP。

## v0.6.3
- GPS watchPosition の引数順を修正（成功・エラー・オプション）
- 高精度GPS、10秒タイムアウト、最大1秒のキャッシュを設定
- GPSエラーを「許可」「測位不能」「タイムアウト」に分けて表示
- 既存のGPS監視を再開始時に停止
- v0.6.2のPDF/コマ図機能は維持

PDFはリポジトリ直下の `KOMAREN_Classic2026.pdf` を自動検索します。
