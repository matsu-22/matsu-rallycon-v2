# Matsu RallyCon v0.7.5 UNIVERSAL PDF

v0.7.4 UNIVERSAL PDFをベースに、GPS距離補正の％上下操作を改善。

## GPS距離補正
- 50～150%、1%刻み
- 通常タップ：±1%
- 長押し：約0.45秒後から連続して±1%
- 長押しを続けると約1.5秒後にさらに高速化
- 上限150%・下限50%で停止
- 既存のGPS距離計算・補正反映は変更しない

## PDFの扱い
- A5 KomaRen形式：従来どおり自動解析
- A4形式：従来どおり
- 長良のような超縦長1ページ：LONG PDF表示
- その他、A4/A5として判定できないPDF：PDF DISPLAY表示
- フォールバック形式では距離・RB番号の自動パースを行わず、PDFそのものを表示

## ラリコン機能
- GPS ON/OFF
- GPS距離計測
- GPS距離補正
- TOTAL / LEG / TIME
- GPS LOST / 復帰
- セッション保存・復元
- START長押しリセット

## 通常のコマ練形式
A5コマ図は従来どおり距離・RB等の自動解析を行い、TARGET / NEXT / AUTO NEXTを使用。

## バージョン管理
本版の対応取扱説明書は v0.7.5 UNIVERSAL PDF です。
