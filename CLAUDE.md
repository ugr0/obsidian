# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## リポジトリの性質

学習記録用の **Obsidian vault** (Markdown ノート集)。コードプロジェクトではないため、ビルド・テスト・lint はありません。作業は Markdown の追加・編集が中心です。

## フォルダ構成

| フォルダ | 内容 | git |
| --- | --- | --- |
| `Notes/` | 知識ベース本体 (サブフォルダ禁止) | 追跡 |
| `1XX_*/` | Public ノート | 除外 |
| `2XX_*/` | Private ノート | 除外 |
| `002_Templates/`, `Files/` | テンプレ・添付 | 除外 |

ルール: フォルダ名は `番号_名前` 形式 (`0XX` = Obsidian 関連、`1XX` = Public、`2XX` = Private)。

## ノート作成ルール

新規ノートはデフォルトで `Notes/` 直下に作られます (`.obsidian/app.json`)。

- **`Notes/` にサブフォルダを作らない** — 名前衝突を検知するための意図的な制約。
- **衝突したら Prefix かタグで解消** — タイトルを長くしない。
- **ファイル名は簡潔に**、ただし衝突しすぎない程度に。

### Prefix 一覧

| Prefix | 意味 |
| --- | --- |
| `_books_` | 本・外部記事 |
| `_people_` | 人物 |
| `_idx_` | 一覧ページ |

### タグの付け方

- タイトルに含まれる語をタグにしない (例: `🦀Rust` に `Rust` タグは不要)。
- 用語が複数の意味を持つ場合のみタグで分類。内容が膨らむならページを分ける。

### ストック型 / フロー型

このリポジトリは **ストック型** (普遍的・更新前提) のみ。フロー型 (Slack やりとり、調査レポート等) は Notion 側で管理する方針。

## 編集時の注意

- **wikilink のリネームは手動で追従**: CLI からファイル名を変えても Obsidian の自動リンク更新は走りません。`grep -rl '\[\[旧名\]\]' Notes` でリンク元を確認してから変更してください。
- **空ファイル (0 B) は削除しない** — 未執筆スタブとして意図的に残されています。
- **`README.md` は 1 行のまま** — 説明を追加しない方針。

## Obsidian 環境メモ

- vim モード有効、`alwaysUpdateLinks: true` (Obsidian 内での操作時のみ)。
- 有効プラグイン: dataview、obsidian-git、templater、kanban、periodic-notes 等 (`.obsidian/community-plugins.json`)。
- `bases` コアプラグインが有効で、ルートに `*.base` が生成されることがあります。
