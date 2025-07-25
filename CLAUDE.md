# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## リポジトリ概要

このリポジトリは Marp を使用してプレゼンテーションスライドを作成するための作業用リポジトリです。

## Marpプロジェクト構造

現在は初期状態のリポジトリで、以下の構造が想定されます。
- `*.md` - Marp 形式の Markdown スライドファイル
- `package.json` - Marp ツールとその依存関係（今後追加予定）
- `.marprc.yml` または `marp.config.js` - Marp 設定ファイル（今後追加予定）

## よく使うコマンド

### Marpの初期セットアップ（必要に応じて）
```bash
npm init -y
npm install --save-dev @marp-team/marp-cli
```

### スライドのビルド
```bash
# HTMLへの変換
npx marp slide.md

# PDFへの変換
npx marp slide.md --pdf

# PPTXへの変換
npx marp slide.md --pptx

# 開発中のプレビュー（ホットリロード付き）
npx marp -s .
```

## Marpスライドの基本構造

Marp スライドは通常の Markdown に以下のような frontmatter を追加します。

```markdown
---
marp: true
theme: default
paginate: true
---

# スライドタイトル

---

## 次のスライド
```

## 開発時の注意事項

1. 新しいスライドファイルは `.md` 拡張子で作成する
2. スライドの区切りは `---` を使用する
3. テーマやスタイルのカスタマイズは frontmatter で指定する
4. 画像は相対パスで参照し、リポジトリ内に含める