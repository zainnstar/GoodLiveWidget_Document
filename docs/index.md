# GoodLiveWidget

**YouTube / Twitch ライブ配信向けオーバーレイ管理ソフト**

GoodLiveWidget は、配信進行管理と OBS オーバーレイ表示を **ひとつのアプリ** で行うためのツールです。  
ImGui のドッキングパネルでウィジェットを編集し、内蔵 HTTP / WebSocket サーバー経由で OBS ブラウザソースにリアルタイム反映します。

---

## 主な特徴

- **Widget List + Inspector** — ウィジェットの追加・レイヤー管理・詳細編集を直感的に操作
- **OBS ブラウザソース連携** — レイヤーごとの URL を接続パネルからコピー、または OBS へドラッグ＆ドロップ
- **配信連携** — YouTube / Twitch のライブチャット取得、ライブログ、視聴者・コメント分析（SQLite）
- **豊富なウィジェット** — カウンター、セットリスト、コメントオーバーレイ、テロップ、お絵描きなど
- **CEF プレビュー** — アプリ内で OBS と同じ HTML を確認（レイヤー単位・単体ウィジェット・コメントシェイプ一覧）
- **プロファイル対応** — 配信内容ごとにウィジェット構成を JSON で保存・切り替え

---

## GoodLiveClimax との違い

| 観点 | GoodLiveClimax | GoodLiveWidget |
| ---- | -------------- | -------------- |
| 目的 | 3D ライブ演出（Unity） | 配信オーバーレイ・進行管理 |
| 出力 | Spout2 映像 | OBS ブラウザソース（HTML） |
| UI 単位 | アセット / ノード | ウィジェット / レイヤー |
| 規模 | 大規模（多数パネル・ノード） | コンパクト（パネル・ウィジェット中心） |

---

## ドキュメントの読み方

1. [インストール](installation.md) — 動作環境とセットアップ
2. [クイックスタート](getting-started.md) — 初回起動から OBS 表示まで
3. [パネル一覧](panels/overview.md) — UI 各パネルの役割
4. [ウィジェット一覧](widgets/overview.md) — 利用可能なウィジェット

---

## ダウンロード

[Booth ページ（GoodLuckLab Shop）](https://goodlucklabshop.booth.pm/)
