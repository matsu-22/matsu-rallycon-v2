Matsu RallyCon v0.8.54 — KOMAREN KANTO 2026 A5 HIGHLIGHT / DISTANCE FONT FIX

基準：Matsu RallyCon v0.8.53 KOMAREN KANTO A5 HIGHLIGHT

変更内容
- 内蔵A5 PDFを「コマ練関東2026_A5_蛍光ライン手修正版_距離表示フォント調整.pdf」に差し替え。
- 85〜102番を含むKM-TOTAL距離表示のフォントを調整した23ページ版を使用。
- 蛍光ブルーライン、道路図、矢印、注記、KM-INTER、コマ番号は今回変更していません。
- GPS計算、距離補正、セッション復元、ボタン配置、SmartRemote操作、PDF表示・解析ロジックは変更していません。
- v0.8.53までの保存セッション互換設定を維持。

検証
- 元PDF：23ページ、A5サイズ。
- 元PDFのテキスト抽出で「####」が0件であることを確認。
- 内蔵PDF Base64を今回の元PDFに置換。
- ZIP内ファイルは index.html と README.md。
- JavaScript構文検査は生成後に別途実施。

注意
- 実機で起動時の内蔵PDF、85〜102番のKM-TOTAL表示、NEXT/BACK、ページ切替、セッション復元を最終確認してください。
