# Travelogue Codex ガイド

## 目的
- このリポジトリは、MkDocs ベースの旅行記録サイトを管理するためのものです。
- 主な対象は `docs/` 配下の Markdown ファイルと、`mkdocs.yml` のサイト設定です。

## 作業ルール
- ユーザー向けの説明、レビューコメント、コミットメッセージ案は、特に指定がない限り日本語を使ってください。
- 既存の文体やフォルダ構成を崩さない、小さく安全な変更を優先してください。
- 旅行の事実は推測で補わないでください。行程、金額、地名が不明な場合は TODO を残すか、ユーザーに確認してください。
- ファイル名の規則は現在のリポジトリに合わせ、`docs/Travel/` 配下では `YYMMDD_旅行名.md` の形式を基本としてください。

## リポジトリ構成
- `docs/index.md` はサイトのトップページです。
- `docs/Travel/` には旅行ごとの Markdown と `travel-template.md` を置きます。
- `docs/Museum/` には施設訪問ごとの Markdown と `museum-template.md` を置きます。
- `docs/Map/` には地図ページと関連メモを置きます。
- `mkdocs.yml` には MkDocs / Material のサイト設定があります。
- `requirements.txt` にはローカル環境と CI で使う Python 依存関係を定義します。

## 推奨コマンド
- 依存関係のインストール: `pip install -r requirements.txt`
- ローカル確認: `mkdocs serve`
- ビルド確認: `mkdocs build`

## コンテンツ上の注意
- 案内ページを更新するときは、パス名とファイル名が実際のリポジトリと大文字小文字まで一致しているか確認してください。
- README のセットアップ手順は、可能な範囲で CI の挙動と揃えてください。
- 旅行写真は `docs/Travel/images/YYMMDD_旅行名/` に置き、旅行記とギャラリーで同じファイルを参照してください。
- 共通の素材や地図ファイルへの参照は `docs/assets/...` 形式を優先し、未作成ならその状態が分かるようにしてください。

## リポジトリ内コンテキスト
- 共有メモは `.agents/memory.md` に置きます。
- 繰り返し使う手順は `.agents/skills/` に置きます。
