# /writing-review コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
writing-generateで執筆された小説の品質を総合的にレビューし、自然言語対話を通じて具体的な改善を実行する

## 基本構文
```bash
# 基本的な使用方法
/writing-review {issue-number}

例:
/writing-review 42
/writing-review 43 キャラクターの魅力をもっと出したい
/writing-review 44 文体を調整したい - 具体的な改善要望
/writing-review - 対話形式でプロジェクト選択からレビューまで
```

## 処理フロー

### 1. 入力理解と前段階統合処理
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- 既存小説の品質・一貫性・魅力度の多角的評価
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/writing-review/inputs/input-processing.md）

### 2. 品質評価理論を活用した総合レビュー
以下の特定理論ファイルを参照してレビュー実行：

**基本品質評価**:
- **プロット一貫性**: 元プロット設定との整合性確認
- **文学的品質**: 文体・表現・構成の客観的評価
- **読者体験**: AIによる最適読者層判定に基づく魅力度分析

**前段階理論継承による専門評価**:
- **character_creation/** 全技法の実装確認: plot-character段階で設計された心理的深度・関係性動力学・個性の小説内表現品質評価
- **character-expression**: キャラクター音声・対話の一貫性評価（語尾・決まり文句・感情表現・相手別使い分けの実装確認）
- **structure_design/** 全技法の実装確認: plot-structure段階で設計されたアーク統合・テーマ表現・伏線システム・感情カーブの執筆内実現度評価
- **conte_techniques/** 演出技法の実装確認: conte段階で設計された視覚的演出・感情演出・描写技法の小説内具現化品質評価

**発展的品質評価**:
- **キャラクター魅力**: `hit-patterns/character-patterns.md` + `character_mbti_patterns/{type}.md` 統合による人物描写の原型一貫性・認知機能表現評価
- **構造最適化**: `hit-patterns/story-patterns.md` + `structure_design/` 全技法による物語展開の理論的完成度・読者満足度分析
- **文体品質評価**: `writing_style/{style}.md` の理論を活用した文体一貫性・表現効果・技法適切性分析
- **表現技法評価**: `writer_mbti_patterns/{type}.md` と `genre/{genre}.md` の統合的表現分析、前段階設定との整合性確認

### 3. 対話による改善方針確認
AI分析結果をユーザーと共有し、shared/instructions の理論に基づいて確認：

**自然な対話による問題提起**:
- AI分析で特定した改善ポイントについて自然に説明
- ユーザーの意図と一致するか確認、必要に応じて優先度調整
- 固定的な評価ではなく、分析結果に応じた柔軟な改善提案

**具体的改善案の提示**:
- 抽象的な「〜を強化」ではなく具体的な修正内容を提示
- 改善前後の比較例を示した分かりやすい説明
- shared/instructions の各ファイルの知見を活用した理論的根拠

### 4. 改善実行と品質確認（最終ステップ）
確定した改善方針に従って実際の小説修正を実行し、PRコメントによる品質向上フィードバックを提供します。

詳細なテンプレート仕様: @.claude/docs/writing-review/outputs/format.md

## 新しいレビューアプローチ

### 統合品質改善システムの実用的活用
`@.claude/docs/shared/quality-improvement-system.md` の3段階改善システムを小説レビューに適用：

**writing-reviewでの活用方法**:
- **Critical Fix**: 執筆された小説の基本的問題修正
- **Quality Enhancement**: 文章品質・表現技術・読者エンゲージメント向上
- **Appeal Amplification**: 文学的価値・エンターテイメント性・記憶定着の強化

詳細な改善手法: @.claude/docs/shared/quality-improvement-system.md

### 自然言語対話によるレビュー
細かいオプション指定ではなく、生成AIの理解能力を最大活用：

**柔軟な改善要望対応**:
- 「キャラクターの魅力をもっと出したい」「文体をもう少し軽快に」
- 「感情描写を深くしたい」「読者がもっと引き込まれるように」
- 「この部分が気になる」「全体的にブラッシュアップしたい」

**段階的改善サポート**:
- 重要な問題から順次改善 ↔ 全体一括改善
- 特定要素集中改善 ↔ バランス調整改善
- ユーザーの要望に応じた柔軟な改善方式

### 理論体系の実用活用
レビューと改善に特化した理論の活用：
- **editorial_review/**: 具体的改善技法と品質向上手法の実践的適用
- **genre/**: ジャンル期待値との照合と差別化提案
- **writing_style/**: 文体スタイルの一貫性と効果的活用の分析・改善
- **writer_mbti_patterns/**: 創作アプローチの一貫性強化
- **audience/**: 作品に最適化された読者層への訴求力最大化
- **character_mbti_patterns/**: キャラクター魅力の最適化

詳細: 以下の理論ファイルを参照

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/writing-review/inputs/input-processing.md

### 実装指針
- 実用的レビューガイドライン: @.claude/docs/writing-review/inputs/input-processing.md (実用的レビュー実装指針セクション)

### 出力仕様
- レビューレポート生成: @.claude/docs/writing-review/outputs/format.md

### 共通理論分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md
- 品質評価理論: 設定されたwriter MBTIタイプのみ参照
- 文体スタイル分析: 設定されたスタイルのみ参照

## エラーハンドリング
- 小説ファイル不足時の対話的な状況確認
- AI分析失敗時の再試行
- 改善実行失敗時の代替手法提案
- プロット一貫性チェックの自動実行

## ローカルファイル保存・更新（issue #139対応）

### ファイル更新システム
レビュー改善を実行してローカルファイルを更新：

**更新する操作**:
1. **ファイル読み込み**: 既存の小説ファイルを分析
2. **改善実行**: 品質向上のための具体的修正
3. **ファイル更新**: 改善版の小説をローカル保存
4. **レビュー記録**: 改善内容をレビューファイルに記録

## 出力
- **レビューレポート**: `outputs/{unique_id}/output-writing-review.md`（詳細なレビュー結果）
- **改善版小説**: `outputs/{unique_id}/output-writing-generate.md`（改善後の小説で更新）
- **対話記録**: `outputs/{unique_id}/review_conversation.md`（レビュー過程の対話履歴）

## レビューレポート生成
プロジェクト用ディレクトリ `outputs/{issue_number}/` にレビュー結果を保存：

```markdown
# 📊 小説レビューレポート: {小説タイトル}

**レビュー日**: {date}
**Issue**: #{issue_number}
**ステータス**: レビュー・改善完了

## 🔍 品質評価結果

### 基本品質評価
- **プロット一貫性**: {consistency_evaluation}
- **文学的品質**: {literary_quality}
- **読者体験**: {reader_experience}

### 発見された改善ポイント
{improvement_points_summary}

## 🔧 実行した改善

### Critical Fix（修正必須）
{critical_fixes_implemented}

### Quality Enhancement（品質向上）
{quality_enhancements_implemented}

### Appeal Amplification（魅力拡張）
{appeal_amplifications_implemented}

## 📈 改善効果
{improvement_effects_analysis}

```


---

**設計方針**: 従来の「評価だけ」から「実際に改善する」レビューへ転換。自然言語対話による柔軟な要望対応と、理論に基づく具体的改善実行で真の品質向上を実現