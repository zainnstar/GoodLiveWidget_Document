# ウィジェット一覧

GoodLiveWidget で利用できるウィジェットの一覧です。  
すべて **ウィジェット一覧パネル** から追加し、**インスペクタ** で編集します。

---

## 進行・表示

| ウィジェット | 概要 | 詳細 |
| ------------ | ---- | ---- |
| カウンター | 数値の表示・加減算 | [counter.md](counter.md) |
| セットリスト | 歌枠の曲順・現在曲表示 | [setlist.md](setlist.md) |
| テロップ | 固定テキスト表示 | [utility-widgets.md](utility-widgets.md) |
| 二重テロップ | 2 系統のテロップ | [utility-widgets.md](utility-widgets.md) |
| メモ | 自由記述テキスト | [utility-widgets.md](utility-widgets.md) |
| 時計 | 壁時計表示 | [utility-widgets.md](utility-widgets.md) |
| エンドロール | エンディング用スクロール | [utility-widgets.md](utility-widgets.md) |

---

## 配信連動

| ウィジェット | 概要 | 詳細 |
| ------------ | ---- | ---- |
| コメントオーバーレイ | チャット装飾表示 | [comment-overlay.md](comment-overlay.md) |
| 高評価数 | YouTube 高評価カウンター | [streaming-widgets.md](streaming-widgets.md) |
| 登録者数 | 登録者数表示 | [streaming-widgets.md](streaming-widgets.md) |
| あいさつカウンター | 初コメ等の挨拶集計 | [streaming-widgets.md](streaming-widgets.md) |
| 出席スタンプ | 初コメでカレンダーにスタンプ | [streaming-widgets.md](streaming-widgets.md) |
| スタンプ | 手動スタンプ配置 | [streaming-widgets.md](streaming-widgets.md) |
| コミュニティアンケート | 投票結果表示 | [streaming-widgets.md](streaming-widgets.md) |

---

## ツール・ゲーム

| ウィジェット | 概要 |
| ------------ | ---- |
| ビンゴ | ビンゴ進行 |
| ルーレット | ルーレット抽選 |
| ダイス | サイコロ |
| ストップウォッチ | 経過時間計測 |
| タイマー | カウントダウン |

詳細: [その他ツール](utility-widgets.md)

---

## クリエイティブ

| ウィジェット | 概要 | 詳細 |
| ------------ | ---- | ---- |
| お絵描き | キャンバス描画 | [paint.md](paint.md) |
| ペンライト | ネオン風ペンライト演出 | [utility-widgets.md](utility-widgets.md) |
| パーティクル | パーティクルエフェクト | [utility-widgets.md](utility-widgets.md) |

---

## 共通の仕組み

```text
C++ ウィジェット状態
    ↓ WebSocket JSON
OBS ブラウザソース (data/html/)
    ↓ DOM + CSS
画面上のオーバーレイ
```

- 複数ウィジェットを同一レイヤーに配置可能
- トランスフォームで位置・サイズ・回転を個別設定
- プロファイル JSON にシリアライズして保存

---

## レイヤーと OBS

1 レイヤー = OBS ブラウザソース 1 枚。  
レイヤーを分けると OBS 上で独立して移動・クロマキー等が可能です。
