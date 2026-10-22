Matsu RallyCon v0.8.55 — REMOTE TOTAL ADJUST

基準：ユーザー提供のGitHub版 ZIP（matsu-rallycon-v2-main）を維持し、既存の内蔵PDF・GPS・コマ図処理を保持。

変更内容
- ブラウザに届くキーボード／リモコン入力でTOTAL距離を10m単位で増減できる処理を追加。
- 左／下：TOTALを10m減らす。右／上：TOTALを10m増やす。
- AudioVolumeDown / AudioVolumeUp がWebページへ配信される環境では、それらも減算／加算として扱う。
- 既存の adjustTotal() を使用し、表示更新と既存の自動コマ送り判定を利用。
- GPS計算、PDF、NEXT/BACK、SmartRemoteの既存処理は変更していない。
- バージョン表記を v0.8.55 に統一。

注意・未検証事項
- Androidが音量キーをOS側で処理している場合、Webページにはキーイベントが届かないため、この変更だけでは上下ボタンを捕捉できない可能性がある。
- 物理リモコンを接続したAndroid実機での動作確認は未実施。ブラウザが入力イベントを渡す場合に限り動作する。
