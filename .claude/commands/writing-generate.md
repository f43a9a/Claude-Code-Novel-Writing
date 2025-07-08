# /writing-generate コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
plot-systemで構築された高品質プロットを基に、実際の小説を自然言語対話を通じて執筆する

## 基本構文
```bash
# 基本的な使用方法
/writing-generate {issue-number}

例:
/writing-generate 42
/writing-generate 43 全体を軽快な文体で
/writing-generate 44 第2章だけ詩的に - 部分執筆要望
/writing-generate - 対話形式でプロジェクト選択から執筆まで
```

## 処理フロー

### 1. 入力理解と前段階統合処理
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/writing-generate/inputs/input-processing.md）

### 2. 創作理論を活用した執筆設計
以下の特定理論ファイルを参照して執筆方針を決定：

**文体選択・表現設計**:
- **文体スタイル分析**: `writing_style/` 配下の6種類を評価し最適文体を提案
  - literary, conversational, descriptive, minimalist, poetic, journalistic
  - プロット内容・ジャンル・読者層・MBTI思考パターンとの適合性を総合判断
- **MBTI思考パターン**: `writer_mbti_patterns/{type}.md` の理論に基づく文体最適化
- **ジャンル表現技法**: `genre/{genre}.md` の理論を適用した描写手法
- **読者層最適化**: AIによる最適読者層分析に基づく語彙・複雑度調整

**構造・内容設計**:
- **物語構造**: `hit-patterns/story-patterns.md` の理論を適用した展開設計
- **キャラクター表現**: `hit-patterns/character-patterns.md` の理論を活用した人物描写
- **統合的執筆**: 各理論を総合した自然で魅力的な小説生成

### 3. 文体選択と執筆方針の対話確認
AI分析結果をユーザーと共有し、shared/instructions の理論に基づいて確認：

**文体提案と選択対話**:
- **最適文体の提案**: プロット分析に基づく推奨文体とその理由を説明
- **文体比較検討**: 候補となる2-3の文体の特徴と効果を比較提示
- **ユーザー選択**: 提案文体の採用 or 別文体の希望 or カスタム調整の対話
- **文体決定**: 最終的な文体スタイルと具体的な表現方針を確定

**執筆方針の総合確認**:
- 決定した文体・構造・表現技法について自然に説明
- ユーザーの意図と一致するか確認、必要に応じて調整提案
- 固定的な質問ではなく、分析結果に応じた柔軟な対話

**理論的裏付けの共有**:
- 採用した創作理論の根拠を分かりやすく説明
- shared/instructions の各ファイルの知見を活用した執筆方針提示

**キャラクター音声・対話の一貫性確認**:
- **character-expression.md**: plot-character段階で設計された人格・背景設定から音声特性を自然に導出
- **創造的音声設計**: 固定パターンではなく、AIがキャラクター設定から論理的・創造的に音声特性を生成
- **柔軟な一貫性**: 核となる個性を保ちながら、状況・相手・感情に応じた自然な変化を許容
- **執筆品質確保**: 全編を通じた各キャラクターの音声表現の自然性と魅力確保

### 4. 小説執筆と品質確認（最終ステップ）
確定した方針に従って実際の小説を執筆し、**魅力的な見出し生成**を含めてGit/GitHub連携でプロジェクト管理を実行します。

**見出し改善システム**:
- 説明的タイトル → 感情・謎・感覚要素を含む魅力的タイトルに自動変換
- ジャンル別パターン適用（fantasy: 「〜の影」「〜への扉」/ slice_of_life: 「〜の午後」「〜という日常」）
- 読者の興味を引く表現で内容を完全に明かさない絶妙なバランス

詳細なテンプレート仕様: @.claude/docs/writing-generate/outputs/format.md

## 新しい執筆アプローチ

### 自然言語対話重視
従来の細かいオプション指定ではなく、生成AIの対話能力を最大活用：

**柔軟な文体・要望対応**:
- 文体選択: 「軽快な文体で」「もう少し詩的に」「会話的に親しみやすく」
- 表現調整: 「描写を詳しく」「簡潔にまとめて」「文学的に美しく」
- 執筆範囲: 「第2章だけ」「クライマックスを詳しく」「全体を一気に」
- 品質方針: 「読みやすく」「感情を重視して」「キャラクターを重視して」

**段階的執筆サポート**:
- 全体一括執筆 ↔ 章別・シーン別の段階的執筆
- 粗書き → 詳細化 → 最終調整の段階的品質向上
- ユーザーの好みに応じた柔軟な進行方式

### 理論体系の実用活用
shared/instructions配下の理論を執筆に直接適用：

#### 基本理論（全執筆に適用）
- **プロット書活用**: 前段階で構築された物語構造・キャラクター設計・世界観設定を忠実に実装
- **genre/{genre}.md**: ジャンル固有の表現技法・描写手法の適用
- **writing_style/{style}.md**: 文体スタイルに応じた言語表現・修辞技法の適用
- **writer_mbti_patterns/{type}.md**: 創作者の思考パターンに応じた文体最適化
- **audience/{audience}.md**: 対象読者層に適した語彙・文体・内容調整

#### 横断的専門技法（前段階から継承・発展）
**キャラクター描写時の専門技法適用**:
- **character_creation/psychological-depth-techniques.md**: 5層心理構造（認知・感情・防衛機制・発達歴・無意識）を対話・行動・内面描写に反映
- **character_creation/character-expression.md**: キャラクター固有の対話パターン・語彙選択・感情表現の一貫した実装
- **character_creation/relationship-dynamics-design.md**: キャラクター間の6層関係性（親密度・相互作用・権力関係）を場面ごとに具体化
- **character_mbti_patterns/{type}.md**: 確立されたMBTI原型の認知機能を行動・判断・反応に自然に反映

**構造展開時の専門技法適用**:
- **structure_design/character_arc_integration.md**: キャラクター成長と物語進行の有機的統合、発展段階の具体的描写
- **structure_design/foreshadowing_systems.md**: 4層伏線システム（設定・構築・回収・統合管理）の自然な実装
- **structure_design/emotional_curve_design.md**: 章ごとの感情起伏設計に基づく緊張・緩和・クライマックス描写
- **structure_design/theme_expression_design.md**: 4層テーマ統合（確立・構造統合・体験具現・多層深化）を説教的でない自然な表現で実装

**視覚的描写強化技法**:
- **conte_techniques/visual-storytelling.md**: 映像的絵コンテ理論による場面構成・視点・カット割り的な描写展開
- **conte_techniques/descriptive-methods.md**: 感覚的描写・空間描写・時間描写の具体的技法適用
- **conte_techniques/emotional-direction.md**: 感情演出・トーン・リズム・視点による読者体験設計

詳細: 以下の理論ファイルを参照

## 💬 文体選択対話の実例

### AI文体提案の例
```
プロット分析結果：
- ジャンル: slice_of_life (日常系)
- 読者層: young_adult
- MBTI思考パターン: ISFP (感情体験重視)

推奨文体: **conversational** (会話的文体)
理由: 
- 日常系の親しみやすさと会話的文体の自然さが相性良好
- young_adult読者層に適した親近感のある表現
- ISFP思考パターンの感情重視アプローチと調和

代替候補:
1. **descriptive** - より詳細な感覚描写で没入感を高める
2. **literary** - 文学的美しさで日常を詩的に昇華

どの文体で執筆しましょうか？カスタム調整のご希望もお聞かせください。
```

### ユーザー応答と調整例
```bash
# 提案受入れ
/writing-generate 42 "conversational文体で進めてください"

# 別文体希望
/writing-generate 42 "descriptive文体の方が良さそうです"

# カスタム調整
/writing-generate 42 "conversationalベースで、重要シーンだけdescriptive要素を加えて"
```

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/writing-generate/inputs/input-processing.md

### 実装指針
- 自然言語執筆ガイドライン: @.claude/docs/writing-generate/instructions/natural-writing.md
- 理論適用実装ガイド: @.claude/docs/writing-generate/instructions/theory-application.md

### 出力仕様
- 小説ファイル生成: @.claude/docs/writing-generate/outputs/format.md

### 共通理論分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md
- 文体理論: 設定されたwriter MBTIタイプのみ参照
- 文体スタイル: 設定されたスタイルのみ参照

## エラーハンドリング
- プロットファイル不足時の対話的な情報収集
- AI執筆失敗時の再試行
- 文字数制約との整合性チェック
- プロット一貫性の自動確認

## ローカルファイル保存（issue #139対応）

### ファイル保存システム
小説執筆完了時にローカルファイルとして保存：

**ディレクトリ構造**: `outputs/{unique_id}/` 形式
- 例: `outputs/42/`、`outputs/43/`、`outputs/98/`
- プロジェクト識別IDでシンプルに管理

**保存するファイル**:
1. **小説本文**: `output-writing-generate.md`
2. **執筆メタデータ**: `writing_conversation.md`（対話履歴）
3. **関連プロットファイル**: 既存のplot段階ファイル群

## 出力
- **メインファイル**: `outputs/{unique_id}/output-writing-generate.md`（完成小説）
- **管理情報**: `outputs/{unique_id}/writing_conversation.md`（執筆対話履歴）

## 小説ファイル生成
プロジェクト用ディレクトリ `outputs/{issue_number}/` に公開用小説を保存：

```markdown
---
layout: post
title: "{小説タイトル}"
author: "{ai_writer_name}"
date: {publication_date} +0900
genres: 
  - {primary_genre}
  - {secondary_genre}
mbti_type: {writer_mbti_type}
excerpt: "{作品の短い紹介文（150文字程度）}"
tags:
  - {tag1}
  - {tag2}
  - {tag3}
---

# 📖 {小説タイトル}

**執筆日**: {date}
**Issue**: #{issue_number}
**ステータス**: 小説執筆完了
**文字数**: {character_count}字
**文体**: {selected_style}
**執筆範囲**: {writing_scope}

---

{完成した小説本文}

<!-- more -->
```

詳細な執筆情報は `writing_metadata.md` ファイルで別途管理され、公開用ファイルには読者体験を重視したコンテンツのみ含まれます。


---

**設計方針**: AIの自然言語理解能力と対話能力を最大限活用し、創作理論に基づく高品質な小説執筆を実現。複雑なオプションではなく自然な対話による柔軟な執筆支援を提供