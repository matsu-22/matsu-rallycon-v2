# Matsu RallyCon v0.8.11

UNIVERSAL PDF版 + Bluetooth左右TOTAL補正

## 今回の変更
- v0.8.11でBluetoothリモコン左右の動作を変更。
- リモコン右（NEXT）→ TOTAL ＋10m。
- リモコン左（BACK）→ TOTAL −10m。
- リモコン左右ではPDFスライド／RB NEXT/BACKを行わず、画面上のTOTAL「＋10m／−10m」と同じ補正処理を実行。
- v0.8.9～v0.8.10で実機確認済みのBluetooth NEXT/BACK受信基盤を継続利用し、v0.8.11で左右の割り当てをTOTAL補正へ変更。
- iPhone SafariのMediaSessionを利用し、BluetoothメディアリモコンのNEXT/BACK受信をTOTAL補正へ接続。
- リモコン右（NEXT）→ TOTAL ＋10m、リモコン左（BACK）→ TOTAL −10m。
- PDFのスライド移動、認識済みロードブックのNEXT/BACKは、画面上のNEXT/BACK操作を使用。
- v0.8.8のPDFタップNEXT/BACK、スワイプ、ピンチ、ダブルタップズーム、ページ境界位置復元を維持。

## 実機確認
- v0.8.10まで：ユーザー所有のBluetoothメディアリモコン＋iPhoneでNEXT/BACK受信を確認済み。
- v0.8.11：左右＝TOTAL ±10mへの変更はコード／静的検証済み。iPhone実機での変更後テストは未実施。

## 現時点の制限
- VOL+/VOL−はiOSのシステム側の音量／カメラ操作として扱われ、Safari Webページへの入力として確認できないため、v0.8.11でも割り当てない。
- FULL native iOS appではなく、既存のWebアプリを維持したMediaSession方式。

## 既存機能
GPS、TOTAL/LEG、AUTO NEXT、セッション保存、START長押しリセット、A4/A5コマ図、A4 2-up PDF、未知PDFフォールバック、PDFコマ送り量設定などは従来どおり。
