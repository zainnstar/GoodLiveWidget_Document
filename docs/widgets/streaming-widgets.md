# 配信連動系ウィジェット

[配信連携パネル](../panels/streaming-integration.md) または Streaming Event Hub からデータを受け取るウィジェット群です。

---

## コメントオーバーレイ

チャットの装飾表示。詳細は [comment-overlay.md](comment-overlay.md)。

---

## 高評価数 / 登録者数

YouTube ライブメトリクス（`metrics_update`）を表示します。

| ウィジェット | 内容 |
| ------------ | ---- |
| 高評価数 | 同時刻の高評価数 |
| 登録者数 | チャンネル登録者数 |

[コメントテスト](../panels/comment-test.md) の **ライブメトリクスのみ** イベントで、実配信なしの更新テストが可能です。

---

## あいさつカウンター

視聴者の **初コメ・再訪** 等をカウントして表示します。  
Hub 経由の `streaming_widget_bridge` から更新されます。

---

## 出席スタンプ

**その日の初コメント** でカレンダーにスタンプが押されるウィジェットです。

- コメント連携: 配信連携 Hub から自動
- 手動操作: インスペクタからもスタンプ可能

---

## スタンプ

手動でスタンプを配置・管理するウィジェット。  
出席スタンプとは別の、自由配置型スタンプ UI です。

---

## コミュニティアンケート

YouTube コミュニティ投票（`poll_updated`）等の結果を OBS 上に表示します。

---

## 共通の前提

| 条件 | 内容 |
| ---- | ---- |
| 配信連携 | 多くは YouTube / Twitch 接続が必要 |
| コメントテスト | 開発・検証用の合成イベント注入 |
| 同時接続 | YouTube/Twitch 同時接続時は Hub liveId に注意 |

---

## 関連パネル

- [配信連携](../panels/streaming-integration.md)
- [コメントテスト](../panels/comment-test.md)
- [視聴者分析](../panels/viewer-analytics.md)
