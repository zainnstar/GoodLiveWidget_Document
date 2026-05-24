# よくある質問（FAQ）

---

## インストール・起動

??? question "起動しない / CEF エラーが出る"
    以下を確認してください。

    - `GoodLiveWidget.exe` と同じフォルダに `libcef.dll`、`bootstrap.exe`、`.pak` ファイルがあるか
    - ZIP を不完全な状態で展開していないか
    - ウイルス対策ソフトが DLL を隔離していないか

??? question "設定が消えた"
    ユーザーデータは `userdata/` に保存されます。  
    アップデート時に **userdata フォルダを上書き・削除していないか** 確認してください。

---

## OBS 連携

??? question "OBS に何も表示されない"
    以下を順に確認してください。

    1. [接続パネル](panels/connection.md) でサーバーが「稼働中」か
    2. ブラウザソース URL が正しいか（例: `http://127.0.0.1:21760/1`）
    3. ウィジェットが追加され、表示 ON になっているか
    4. 「シーンがアクティブになったときに再読み込み」にチェックがあるか
    5. GoodLiveWidget を OBS より **後から** 起動した場合、シーンを切り替えて再読み込み

??? question "OBS へドラッグができない"
    - OBS を **管理者権限なし** で起動する
    - 設定パネルの OBS WebSocket ポート（既定 4455）が OBS と一致しているか
    - 手動で URL コピー → ブラウザソース追加も可能

??? question "複数レイヤーはどう使う？"
    レイヤー 1 = `/1`、レイヤー 2 = `/2` … と OBS ブラウザソースを分けます。  
    OBS 上で個別に位置・クロマキー・フィルタをかけやすくなります。

---

## 配信連携

??? question "YouTube に接続できない"
    - 入力モード（ハンドル / ライブ ID / チャンネル ID）が正しいか
    - 配信が実際にライブ中か
    - 配布物に StreamHost 関連ファイルが含まれているか（配信連携ビルド）

??? question "Twitch OAuth トークンの取得方法"
    `chat:read` スコープ付き IRC 用トークンが必要です。  
    Twitch Token Generator 等のツールで取得し、設定パネル／配信連携パネルに入力してください。

??? question "視聴者分析にデータがない"
    一度以上配信連携で接続し、チャットイベントが発生している必要があります。  
    `userdata/profiles/streaming.db` がプロファイル隣に作成されているか確認してください。

??? question "コメント分析が空"
    設定で **コメントを DB に記録する** が ON か確認してください（**既定 OFF**）。  
    ON にした **後** の配信コメントのみ `comment_archive.db` に記録されます。

---

## ウィジェット・プレビュー

??? question "プレビューが真っ白 / CEF が利用できない"
    CEF 同梱ビルドかどうか確認してください。  
    プレビューは配信者確認用で、OBS 本番とは別 CEF インスタンスです。

??? question "コメントオーバーレイにコメントが出ない"
    1. [配信連携](panels/streaming-integration.md) で接続している、または [コメントテスト](panels/comment-test.md) でイベント送信
    2. ウィジェットのフィルタ（通常/有料）が適切か
    3. 最大表示件数を超えていないか

---

## その他

??? question "ポート 21760 が使えない"
    設定パネルで WebSocket ポートを変更できます。  
    変更後は OBS ブラウザソースの URL も合わせて更新してください。

??? question "GoodLiveClimax との関係"
    同じ GoodLuckLab 系の配信ツールですが、用途が異なります。  
    Climax は 3D 演出（Unity + Spout2）、Widget は OBS オーバーレイ（HTML + WebSocket）です。
