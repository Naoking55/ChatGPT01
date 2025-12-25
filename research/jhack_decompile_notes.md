## 現状の解析ログ（スナップショット）

### 到達点
- RPGツクールMZの「使いやすさの正体」は **イベント構造（ページ/条件/コマンド）** にある
- 実行エンジンや演出資産は不要。編集ツール側で再現可能
- MOTHER2はイベント進行型RPGのため、ツクール型モデルと親和性が高い

### 参考にしたMZデータ
- MapXXX.json / CommonEvents.json / System.json / MapInfos.json
- Enemies / Troops / Items / Skills / States は **辞書思想の参考**
- Animations / Classes は **不要**

### 現実的な難所（要警戒）
- 圧縮方式の再構築
- ポインタ再配置（サイズ増加時）
- SNES LoROM バンク境界

### 次にやること
- ツクール command ↔ MOTHER2 命令の **最小対応表** 作成
- JHackの Text / Event 周りのクラスをデコンパイルして照合
