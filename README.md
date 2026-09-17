# Matsu RallyCon v0.8.24
UNIVERSAL PDF + A5 RALLY VIEW

## 変更点
- v0.8.23のA5コマ練縦RALLY VIEW、PDF表示モード縦RALLY VIEWを維持。
- v0.8.23で確認済みの縦RALLY VIEW送り補正を維持。
- **縦画面のヘッダーではバージョン文字を非表示**にし、「Matsu RallyCon」だけを表示。
- これにより、中央の時刻表示とバージョン文字が重なって見にくくなる問題を解消。
- 横画面では従来どおり「Matsu RallyCon v0.8.24 UNIVERSAL PDF + A5 RALLY VIEW」を表示。
- GPS、距離、PDF描画、NEXT/BACK、START、RALLY VIEWの送り量など、その他の動作は変更していない。

## 表示
### 縦画面
- 左：Matsu RallyCon
- 中央：現在時刻
- 右：GPS / CAP
- バージョン文字：非表示

### 横画面
- 従来どおりアプリ名＋バージョンを表示。

## 既存機能
- A5コマ練縦RALLY VIEW
- PDF表示モード縦RALLY VIEW
- 縦RALLY VIEW自由スクロール
- START / NEXT / BACK
- GPS / GPS距離補正 / TOTAL / LEG / AUTO NEXT
- PDF固定送り / 自由スクロール / ページ境界履歴
- PDFタップ / ピンチ / ダブルタップ
- A4/A5 PDF処理 / 未知PDFの表示
- 縦RALLY VIEW送り補正 80.0～110.0% / 0.1%刻み

## 検証
- index.html内のインラインJavaScript 2ブロックを抽出してnode --checkで構文確認。
- v0.8.23との差分を確認し、表示上のバージョン分離とAPP_VERSION更新以外のコード変更がないことを確認。
- 既存の縦RALLY VIEW / PDF / GPS / START / NEXT / BACK関連コードを確認。
- VERSION.txt / README / HTMLのバージョン表記を一致確認。
- ZIP整合性を確認。
- PDF取扱説明書を生成し、PDFレンダリング結果を確認。
- iPhone実機でのv0.8.24表示確認は未実施。
