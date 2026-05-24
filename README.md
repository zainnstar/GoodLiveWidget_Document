# GoodLiveWidget ドキュメント

GoodLiveWidget の公式ユーザードキュメントです。

- 公開サイト: https://zainnstar.github.io/GoodLiveWidget_Document/
- リポジトリ: https://github.com/zainnstar/GoodLiveWidget_Document

## ローカルプレビュー

```bash
pip install -r requirements.txt
mkdocs serve
```

ブラウザで http://127.0.0.1:8000/ を開いてください。

## 構成

- `docs/` … Markdown 原稿
- `mkdocs.yml` … サイト設定・ナビゲーション
- `.github/workflows/deploy.yml` … main への push で `gh-pages` ブランチへ自動デプロイ

## GitHub Pages の設定（初回のみ）

リポジトリ **Settings → Pages** で次を選んでください。

- **Source**: Deploy from a branch
- **Branch**: `gh-pages` / `/ (root)`

「GitHub Actions」ソースのままだと、ワークフローと競合して更新が反映されないことがあります。
