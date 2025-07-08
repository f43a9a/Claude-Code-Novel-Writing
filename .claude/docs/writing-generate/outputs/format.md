---
authority_level: "出力仕様定義"
target_audience: ["AI", "システム開発者"]
maintainer: "プロジェクトリード"
last_updated: "2025-07-01"
dependencies:
  - "[[writing-generate]]"
  - "[[shared/instructions/creative-theory]]"
tags: ["writing-generate", "output", "novel", "template"]
---

# writing-generate 出力フォーマット

## 📋 このファイルの役割
`/writing-generate` コマンドが生成する小説ファイルの標準テンプレートを定義します。
執筆完了小説と進行管理を統合した、一元的なプロジェクト管理を目的とします。

## 🎯 小説ファイル テンプレート

```bash
# メインファイル生成
cat > plots/{issue_number}/novel.md <<EOF
---
layout: post
title: "{小説タイトル}"
author: "{ai_writer_name}"  # 例: vampire-intj, infj-visionary
date: {publication_date} +0900  # 公開予定日時
genres: 
  - {primary_genre}  # 例: gothic-horror, fantasy, mystery
  - {secondary_genre}  # 例: literary, slice-of-life
mbti_type: {writer_mbti_type}  # 例: VAMPIRE-INTJ, INFJ
excerpt: "{作品の短い紹介文（150文字程度）}"
tags:
  - {tag1}  # 例: 血液美学, 魔法, 推理
  - {tag2}
  - {tag3}
---

# 📖 {面白い小説タイトル}

**執筆日**: {date}
**Issue**: #{issue_number}
**ステータス**: 小説執筆完了
**文字数**: {character_count}文字
**文体**: {selected_style}
**執筆範囲**: {writing_scope}

---

{完成した小説本文}

<!-- more -->
EOF

# 執筆情報ファイル生成（管理用）
cat > plots/{issue_number}/writing_metadata.md <<EOF
# 📊 執筆管理情報

**執筆日**: {date}
**Issue**: #{issue_number}

## 基盤データ
- **concept.md**: {concept_summary}
- **setting.md**: {setting_summary}  
- **character.md**: {character_summary}
- **structure.md**: {structure_summary}

## 適用理論
- **文体理論**: {writer_mbti_pattern} - {style_approach}
- **ジャンル技法**: {genre} - {genre_techniques}
- **最適読者層調整**: {魅力最大化戦略} - {魅力最大化適応}
- **構造実装**: {story_structure} - {structure_implementation}

## 執筆方針
- **重点要素**: {focus_elements}
- **表現技法**: {expression_techniques}
- **文体特徴**: {style_characteristics}

## 品質指標
- **プロット一貫性**: {plot_consistency_check}
- **文学的品質**: {literary_quality_assessment}
- **読者体験**: {reader_experience_evaluation}

## 対話記録
{conversation_history}

## 決定事項
- **執筆範囲**: {final_scope}
- **文体方針**: {final_style}
- **重点要素**: {final_focus}
- **特別な調整**: {special_adjustments}

## AI判断根拠
{ai_reasoning_summary}
EOF
```

## 📝 各セクションの詳細仕様

### フロントマターセクション（Jekyll用メタデータ）
- **layout**: 「post」固定
- **title**: 小説タイトル（引用符で囲む）
- **author**: AI作家名（_authorsコレクションと一致）
- **date**: 公開予定日時（+0900 JST）
- **genres**: 主要・副次ジャンルのリスト
- **mbti_type**: AI作家のMBTIタイプ
- **excerpt**: 作品紹介文（150文字程度）
- **tags**: 作品の特徴的タグ（3-5個）

### 基本情報セクション
- **執筆日**: 実行日時
- **Issue**: 対象のGitHub Issue番号
- **ステータス**: 「小説執筆完了」固定
- **文字数**: 生成された小説の文字数
- **文体**: 選択・適用された文体タイプ
- **執筆範囲**: 全体/部分等の執筆対象範囲

### 小説本文セクション
実際に生成された完成小説：
- プロット構造に忠実な展開
- キャラクター設定を活かした描写
- 世界観設定の自然な統合
- 選択された文体での一貫した表現
- `<!-- more -->`タグで記事概要の区切りを設定

### 執筆情報セクション（別ファイル管理）
詳細な執筆情報は `writing_metadata.md` ファイルで管理：
- 基盤データ、適用理論、執筆方針
- 品質指標、対話記録、AI判断根拠
- 公開用ファイルには含めない（管理者用情報）

## 🔄 動的要素の展開例

### 適用理論の詳細展開例
```markdown
- **文体理論**: ISFP - 美的感性重視アプローチ
  - 基盤理論: 内向感情(Fi)による真正性のある感情表現
  - 実装効果: キャラクターの内面描写が深く、感情的共鳴が強い
  
- **ジャンル技法**: fantasy - 魔法的現実主義
  - 基盤理論: 現代的ファンタジー表現技法
  - 実装効果: 日常と非日常の自然な融合による親しみやすさ

- **読者層調整**: young_adult - 等身大成長物語
  - 基盤理論: 13-25歳読者の心理的ニーズ
  - 実装効果: 共感しやすいキャラクター設定と成長軌道
```

### 品質指標展開例
```markdown
- **プロット一貫性**: ✅ 優秀
  - 構造的整合性: 三幕構成が正確に実装
  - キャラクター一貫性: 設定された性格・動機が全体で一貫
  - 世界観統合: setting.mdの詳細が自然に織り込まれている

- **文学的品質**: ⭐⭐⭐ 高品質
  - 文体統一性: 選択された文体が全体で一貫
  - 表現豊かさ: 比喩・象徴の効果的活用
  - 読みやすさ: 対象読者層に適した語彙・文体
```

## ⚙️ テンプレート変数

### フロントマター変数
- `{面白い小説タイトル}`: concept.mdで設定されたタイトルを魅力的に改善（感情・謎・感覚要素を含む）
- `{ai_writer_name}`: 最適なAI作家名（vampire-intj等）
- `{publication_date}`: 公開予定日時（YYYY-MM-DD HH:MM:SS）
- `{primary_genre}`: 主要ジャンル（gothic-horror, fantasy等）
- `{secondary_genre}`: 副次ジャンル（literary, slice-of-life等）
- `{writer_mbti_type}`: AI作家のMBTIタイプ
- `{excerpt}`: 作品紹介文（150文字程度）
- `{tag1}, {tag2}, {tag3}`: 特徴的タグ（血液美学、魔法等）

### 基本情報変数
- `{date}`: 執筆実行日時
- `{issue_number}`: 対象GitHub Issue番号
- `{character_count}`: 生成された小説の文字数
- `{selected_style}`: 決定された文体タイプ
- `{writing_scope}`: 執筆対象範囲（全体/章/シーン等）
- `{完成した小説本文}`: 実際に生成された小説テキスト

### 管理用変数（metadata.mdファイル）
- `{適用理論の詳細}`: 使用された創作理論とその効果
- `{品質評価結果}`: 自動品質チェックの結果
- `{conversation_history}`: 執筆過程の対話履歴

## 📊 品質指標

### 必須要素の確認（公開用ファイル）
- [ ] フロントマターが完全に設定されている
- [ ] Jekyll公開用メタデータが適切である
- [ ] 基本情報セクションが記載されている
- [ ] 小説本文が完成している（空でない）
- [ ] `<!-- more -->`タグが適切に配置されている
- [ ] 「おわり」等の読後感を損なう表現が除去されている

### 推奨要素の確認（管理用ファイル）
- [ ] writing_metadata.mdが生成されている
- [ ] プロット設定との一貫性が確保されている
- [ ] 選択された文体が一貫して実装されている
- [ ] 品質指標が具体的に評価されている
- [ ] 対話記録が適切に保存されている

### 公開準備の確認
- [ ] 作家名が_authorsコレクションに存在する
- [ ] ジャンルが既定のものを使用している
- [ ] 公開日時が適切に設定されている
- [ ] excerptが魅力的で150文字程度である

---

**実装方針**: 公開前提のJekyll対応フォーマットで即座に公開可能な小説ファイルを生成し、管理情報は別ファイルで分離管理することで、読者体験と管理効率を両立