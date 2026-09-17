# Matsu RallyCon v0.8.16

UNIVERSAL PDF + 縦画面RALLY VIEW / A5連続スクロール / PDF表示TOTAL・SPEED

## v0.8.16変更点
- 縦画面A5の連続スクロール表示を維持。
- PDF表示モード（距離/RB解析なし）の縦画面A5でも、RALLY VIEWの情報バーを表示。
- 情報バーにはTOTAL kmとSPEED km/hを表示。PDF表示モードでもGPSをONにすればGPS距離・速度を確認できる。
- START前も情報バーを表示し、START後は従来どおり上部ヘッダーと下部操作バーを隠してコマ図を最大表示。
- PDF表示モードでは距離/RB解析そのものは行わず、TOTAL/SPEED表示だけを追加。
- GPS OFF時はTOTALは現在値、SPEEDはGPS速度がなければ0として表示。
- 横画面は変更せず、従来の表示・操作を維持。
- A5以外のPDF表示も今回変更しない。

## 操作
- 縦画面・A5：コマ図を上下スワイプして自由に連続スクロール。
- 縦画面・A5 PDF表示モード：距離解析なしでPDFを連続表示し、TOTAL / SPEEDを情報バーで確認可能。
- 走行中：TOTAL / SPEEDを常時確認可能。
- 既存のGPS、TOTAL/LEG、AUTO NEXT、PDF読み込み、A4/A5解析等は維持。

## 重要な仕様
- PDF表示モードのTOTAL/SPEED表示は「距離/RB解析を追加する」ものではない。表示値はMatsu RallyConの既存GPS距離・速度表示を使用する。
- PDF表示モードではAUTO NEXTによるRB進行などの距離解析機能は使用しない。
- 縦画面以外では今回のRALLY VIEW表示変更は発生しない。

## 確認事項
- JavaScript構文チェックを実施。
- v0.8.15との差分を確認し、変更箇所をPDF表示モードの情報バー表示に限定。
- 横画面の分岐、A5連続表示、PDF表示モードのページ連続表示を確認。
- v0.8.13のGPS LOST→復帰時の直線距離補正を維持。
- iPhone実機でのv0.8.16確認が必要。
