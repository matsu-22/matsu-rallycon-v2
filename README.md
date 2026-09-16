Matsu RallyCon v0.8.9 UNIVERSAL PDF

v0.8.9 追加：iPhone Safari / iOS の MediaSession を利用した Bluetooth リモコン連携の試作版。
- NEXT（nexttrack）→ 既存の NEXT 処理
- BACK（previoustrack）→ 既存の BACK 処理
- 初回のユーザー操作後に無音のメディアセッションを開始し、メディアキーを受け取れる状態を作る
- 音声は出さない（音量0）
- 既存のPDFタップ送り、スワイプ、ピンチ、ダブルタップ、ページ境界・位置復元を維持
- 既知A5/A4のRB操作も既存NEXT/BACK処理をそのまま利用

注意：この版は iPhone 実機での Bluetooth リモコン受信を目的とした試作。Safari / ホーム画面Webアプリ / iOSのバージョンやメディア再生状態によって挙動が変わる可能性があるため、実機確認を前提とする。
