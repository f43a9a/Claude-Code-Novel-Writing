# 📚 作品公開ガイド

## 概要

このガイドでは、Plot-Systemで生成された小説をAI Writers Galleryサイトに公開する手順を説明します。

## 🎯 公開フロー

### 1. 完成原稿の確認
- 執筆完了後、`outputs/{issue-number}/output-writing-generate.md` に原稿が保存されます
- レビュー済みの場合は `output-writing-review.md` を使用

### 2. メタデータの準備

以下のフロントマターを原稿の先頭に追加します：

```yaml
---
layout: post
title: "作品タイトル"
author: "ai-writer-name"  # 例: infj-visionary, enfp-dreamer
date: 2025-01-20 09:00:00 +0900  # 公開予定日時
genres: 
  - fantasy  # ジャンル（複数可）
  - mystery
mbti_type: INFJ  # 作家のMBTIタイプ
excerpt: "作品の短い紹介文（150文字程度）"
---
```

### 3. ファイルの移動

1. ファイル名を決定: `YYYY-MM-DD-url-friendly-title.md`
   - 例: `2025-01-20-office-locked-room-mystery.md`
   - 日付は公開日
   - タイトルは英数字とハイフンのみ

2. `docs/_posts/` ディレクトリへコピー

### 4. 自動公開の仕組み

- Jekyll の `future: false` 設定により、未来の日付の投稿は自動的に非公開
- 公開日時になると自動的にサイトに表示されます
- GitHub Pages が定期的にビルドするため、特別な操作は不要

## 📝 メタデータ詳細

### 必須フィールド

| フィールド | 説明 | 例 |
|----------|------|-----|
| `title` | 作品タイトル | "失われた記憶の図書館" |
| `author` | AI作家名（_authorsコレクションと一致） | "infj-visionary" |
| `date` | 公開日時（JST） | 2025-01-20 09:00:00 +0900 |
| `genres` | ジャンル（リスト形式） | - fantasy<br>- mystery |
| `mbti_type` | 作家のMBTIタイプ | INFJ |

### オプションフィールド

| フィールド | 説明 | 例 |
|----------|------|-----|
| `excerpt` | 作品紹介文 | "深い霧に包まれた森で..." |
| `tags` | その他のタグ | - 魔法<br>- 成長物語 |

## 🎨 AI作家一覧

| 作家名 | MBTI | 得意ジャンル |
|--------|------|-------------|
| infj-visionary | INFJ | fantasy, mystery |
| enfp-dreamer | ENFP | adventure, romance |
| isfp-artist | ISFP | slice-of-life, fantasy |
| intj-strategist | INTJ | mystery, sci-fi |
| entp-innovator | ENTP | sci-fi, adventure |
| infp-idealist | INFP | fantasy, romance |

## ✅ 公開前チェックリスト

- [ ] フロントマターが正しく設定されている
- [ ] ファイル名が規則に従っている（YYYY-MM-DD-title.md）
- [ ] author名が `_authors` コレクションに存在する
- [ ] ジャンルが既定のものを使用している
- [ ] excerptが設定されている（推奨）
- [ ] 本文に `<!-- more -->` が含まれている（推奨）

## 🚀 Tips

1. **予約公開**: 未来の日付を設定すれば、その日時に自動公開
2. **即時公開**: 現在または過去の日時を設定すれば即座に公開
3. **下書き保存**: `_drafts` フォルダに保存すれば非公開で保管可能

## 📅 推奨公開スケジュール

- 毎日1作品程度の公開を推奨
- 公開時間は朝9時または夕方18時が効果的
- 週末は特別企画作品の公開に適している

---

質問や問題がある場合は、GitHubのIssueで報告してください。