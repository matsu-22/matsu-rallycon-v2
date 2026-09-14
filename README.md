# Matsu RallyCon v0.6.35

Based on the verified v0.6.33 build. UI and PDF viewport behavior are preserved. This build strengthens the rally-distance and timing core: GPS distance is counted only while the stage is running, STOP/START pauses do not add parked distance, GPS references are rebuilt across pauses, and TIME resumes from the previous elapsed value instead of resetting.


## v0.6.35 GPSロスト／復帰
- GPSロスト中は最後の正常測位点を保持し、距離を推定加算しない。
- GPS復帰時はロスト前の正常測位点から復帰地点までの直線距離を1回だけ加算。
- 復帰時の異常な速度ジャンプは距離に加算せず、新しい正常地点を基準に再開。
- 長時間ロスト（10分超）は経路を推定せず再アンカー。
- 5秒以上GPS更新がない場合はGPS LOST表示。UI/PDF表示は変更なし。
