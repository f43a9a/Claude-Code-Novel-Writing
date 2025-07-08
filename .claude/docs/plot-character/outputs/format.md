---
authority_level: "出力仕様定義"
target_audience: ["AI", "システム開発者"]
maintainer: "プロジェクトリード"
last_updated: "2025-07-01"
dependencies:
  - "[[plot-character]]"
  - "[[shared/instructions/hit-patterns]]"
tags: ["plot-character", "output", "github-issue", "character-design"]
---

# plot-character 出力フォーマット

## 📋 このファイルの役割
`/plot-character` コマンドが生成するGitHub Issue更新とローカルファイルの標準テンプレートを定義します。
詳細分析と進行管理を統合した、一元的なプロジェクト管理を目的とします。

## 🎯 GitHub Issue・ローカルファイル共通テンプレート

GitHub Issue更新とローカルファイル保存に全く同じ詳細内容を使用：

```bash
gh issue comment {issue_number} --body "$(cat <<EOF
# 🎭 キャラクター設計書: {タイトル}

**作成日**: {YYYY-MM-DD形式}
**Issue**: #{issue_number}
**ステータス**: character完了
**前段階**: concept.md, setting.md

---

## 👥 主要キャラクター設計

### 主人公: {protagonist_name}

#### 1. 基本情報
* **氏名／呼称**: {full_name_and_nicknames}
* **年齢・性別・所属**: {age_gender_affiliation}
* **一人称・二人称**: {personal_pronouns}

#### 2. 人物像（外見＋非言語）
* **外見的特徴**: {physical_appearance}
* **非言語サイン**: {non_verbal_mannerisms}

#### 3. 声・話し方
* **トーン／語彙レベル**: {speech_tone_vocabulary}
* **口癖・発話テンポ**: {speech_habits_tempo}

#### 4. 内面
* **核心信念・価値観**: {core_beliefs_values}
* **弱点・トリガー**: {weaknesses_triggers}
* **好き／嫌い**: {likes_dislikes}

#### 5. 目的・動機
* **短期目標**: {short_term_goals}
* **長期目標**: {long_term_goals}
* **隠された欲求・葛藤**: {hidden_desires_conflicts}

#### 6. 関係性
* **主要な他キャラとの関係**: {key_relationships}
* **物語上の役割**: {story_function}

#### 7. 備考
{additional_notes}

### 重要人物: {key_character_name}

#### 1. 基本情報
* **氏名／呼称**: {key_full_name_nicknames}
* **年齢・性別・所属**: {key_age_gender_affiliation}
* **一人称・二人称**: {key_personal_pronouns}

#### 2. 人物像（外見＋非言語）
* **外見的特徴**: {key_physical_appearance}
* **非言語サイン**: {key_non_verbal_mannerisms}

#### 3. 声・話し方
* **トーン／語彙レベル**: {key_speech_tone_vocabulary}
* **口癖・発話テンポ**: {key_speech_habits_tempo}

#### 4. 内面
* **核心信念・価値観**: {key_core_beliefs_values}
* **弱点・トリガー**: {key_weaknesses_triggers}
* **好き／嫌い**: {key_likes_dislikes}

#### 5. 目的・動機
* **短期目標**: {key_short_term_goals}
* **長期目標**: {key_long_term_goals}
* **隠された欲求・葛藤**: {key_hidden_desires_conflicts}

#### 6. 関係性
* **主人公との関係**: {relationship_to_protagonist}
* **物語上の役割**: {key_story_function}

#### 7. 備考
{key_additional_notes}

## 🔄 キャラクター関係性

### 人間関係マップ
{relationship_dynamics_detailed}

### 感情的動力学
{emotional_dynamics}

### 対立・協力構造
{conflict_cooperation_structure}

## 🎯 キャラクター原型分析

### 適用した原型理論
{applied_archetype_theories}

### キャラクター設計の根拠
{character_design_rationale}

### character_mbti_patterns活用
{character_mbti_application}

## 📈 成長軌道設計

### キャラクターアーク
{character_arc_design}

### 物語構造との適合
{story_structure_compatibility}

### テーマ表現への貢献
{theme_expression_contribution}

## 📚 理論的根拠

### hit-patterns適用
{hit_patterns_application}

### ジャンル特性反映
{genre_character_adaptation}

### 最適読者層配慮
{audience_consideration}

## 🎓 プロフェッショナル・キャラクター創作技法適用

### 統合的キャラクター設計
- **@character_creation/character-profiling-methods.md**: 7段階プロファイリングシステムによる詳細設計
- **@character_creation/psychological-depth-techniques.md**: 5層心理構造による内面の深度構築
- **@character_creation/voice-and-dialogue-design.md**: 5層音声・対話設計による個性的表現
- **@character_creation/relationship-dynamics-design.md**: 6層関係性設計による魅力的人間関係
- **@character_creation/motivation-and-goals-framework.md**: 5層動機・目標システムによる行動原理
- **@character_creation/appearance-and-mannerisms.md**: 4層外見・振舞い設計による視覚的個性
- **@character_creation/character-integration-strategies.md**: 5段階統合戦略による一貫性確保

### 商業作品レベルの品質確保
- **心理学的妥当性**: 現代心理学知見に基づく説得力ある人格構築
- **読者共感度**: 普遍的人間性と個性的特徴の最適バランス
- **記憶定着性**: 印象的で忘れにくい個性的要素の戦略的配置
- **成長可能性**: 物語展開での発展・深化への拡張性確保

## 🎯 作品魅力最大化戦略

### 最適読者層の分析
**ターゲット読者**: {AIが分析した最適な読者層}
**選定理由**: {なぜこの読者層が最適か}
**年齢幅**: {具体的な年齢範囲と理由}

### 表現レベル最適化
**語彙選択**: {この作品に最適な語彙レベル}
**文体アプローチ**: {最も効果的な文体とその理由}
**複雑さ調整**: {テーマの深さと表現の複雑さのバランス}

### テーマ深度設計
**核心テーマ**: {この作品の最も魅力的なテーマ}
**深さレベル**: {どの程度まで掘り下げるべきか}
**アプローチ方法**: {テーマを魅力的に表現する手法}

### 面白さ要素強化
**主要魅力ポイント**: {この作品の最大の売り}
**差別化要素**: {他作品にない独自性}
**読者体験設計**: {読者にどんな体験を提供するか}

## 進行状況
- [x] Phase 1: concept（基本企画）
- [x] Phase 2: setting（世界観設定）
- [x] Phase 3: character（キャラクター設計）
- [ ] Phase 4: structure（プロット構造設計）
- [ ] Phase 5: validate（統合検証）

## 次のステップ
```bash
/plot-structure {issue_number}
```

## 進行状況更新
- [x] Phase 1: concept（基本企画）
- [x] Phase 2: setting（世界観設定）
- [x] Phase 3: character（キャラクター設計）
- [ ] Phase 4: structure（プロット構造設計）
- [ ] Phase 5: validate（統合検証）

## 次のステップ
```bash
/plot-structure {issue_number}
```
EOF
)"
```

## 🎯 {output-type} テンプレート

```bash
{output-generation-command} \
  --title "{output-title-format}" \
  --body "$(cat <<EOF
# 📋 {output-section-title}

## 基本情報
- **{info-field-1}**: {info-value-1}
- **{info-field-2}**: {info-value-2}
- **{info-field-3}**: {info-value-3}
- **{info-field-4}**: {info-value-4}

## AI分析結果

### {analysis-section-1}
{analysis-content-1}

### {analysis-section-2}
{analysis-content-2}

### {analysis-section-3}
{analysis-content-3}

## 🎯 {domain-specific-analysis-title}

### {domain-analysis-section-1}
{domain-analysis-content-1}

### {domain-analysis-section-2}
{domain-analysis-content-2}

## 📚 参考となる{theory-type}

### {reference-section-1}
{reference-content-1}

### {reference-section-2}
{reference-content-2}

## 全体印象
{overall-impression}

## 進行状況
- [{completion-status-1}] Phase 1: concept（基本企画）
- [{completion-status-2}] Phase 2: setting（世界観設定）
- [{completion-status-3}] Phase 3: character（キャラクター設計）
- [{completion-status-4}] Phase 4: structure（プロット構造設計）
- [{completion-status-5}] Phase 5: validate（統合検証）

## 次のステップ
```bash
/{next-command} {issue_number}
```
EOF
)" \
  --assignee @me
```

## 📝 各セクションの詳細仕様

### 基本情報セクション
- **{info-field-1}**: {field-description-1}
- **{info-field-2}**: {field-description-2}
- **{info-field-3}**: {field-description-3}
- **{info-field-4}**: {field-description-4}

### AI分析結果セクション
各判定の根拠を自然な言葉で説明：
- {analysis-requirement-1}
- {analysis-requirement-2}
- {analysis-requirement-3}

### {domain-specific-analysis-title}セクション

#### {domain-analysis-section-1}
{theory-name}理論に基づく{analysis-type}の分析：
- **{analysis-element-1}**: {element-description-1}
- **{analysis-element-2}**: {element-description-2}
- **{analysis-element-3}**: {element-description-3}
- **{analysis-element-4}**: {element-description-4}

#### {domain-analysis-section-2}
- **{theory-application-1}**: {application-description-1}
- **{theory-application-2}**: {application-description-2}
- **{theory-application-3}**: {application-description-3}

### 進行状況セクション
5段階のプロット構築プロセスの進捗管理：
- [{current-stage-status}] {current-stage}: 完了マーク
- [ ] {remaining-stage-1}, {remaining-stage-2}, etc.: 未完了チェックボックス

### 次のステップセクション
次に実行すべきコマンドの明示:
```bash
/{next-command} {issue_number}
```

## 🔄 動的要素の展開例

### {domain-specific-analysis-title}の詳細展開例
```markdown
- **{example-analysis-element-1}**: {example-description-1}
  - 基盤理論: {example-theory-1}
  - {domain-specific-benefit}: {example-benefit-1}
  
- **{example-analysis-element-2}**: {example-description-2}
  - 基盤理論: {example-theory-2}
  - {domain-specific-benefit}: {example-benefit-2}

- **{example-analysis-element-3}**: {example-description-3}
  - 基盤理論: {example-theory-3}
  - {domain-specific-benefit}: {example-benefit-3}
```

### {reference-section-1}展開例
```markdown
- **{reference-pattern-1}**: {pattern-description-1}
  - {pattern-detail-1}
  - {pattern-detail-2}

- **{reference-pattern-2}**: {pattern-description-2}
  - {pattern-detail-1}
  - {pattern-detail-2}
```

## ⚙️ テンプレート変数

実際の実装時に置換される変数：
- `{variable-1}`: {variable-description-1}
- `{variable-2}`: {variable-description-2}
- `{variable-3}`: {variable-description-3}
- `{domain-specific-variable}`: {domain-variable-description}
- `{analysis-results}`: {analysis-description}
- `{theory-applications}`: {theory-description}
- `{overall-impression}`: 全体印象
- `{issue_number}`: 作成されたIssue番号

## 📊 品質指標

### 必須要素の確認
- [ ] 基本情報{field-count}項目がすべて記載されている
- [ ] AI分析結果が論理的に説明されている
- [ ] {domain-specific-analysis-title}が{theory-name}理論に基づいている
- [ ] 進行状況チェックリストが正確である

### 推奨要素の確認
- [ ] {reference-type}との関係が具体的に説明されている
- [ ] {domain-specific-requirement}が明確である
- [ ] 次のステップが実行可能である
- [ ] 全体として読みやすく構造化されている

---

**実装方針**: {output-type}上でのワンストップなプロジェクト管理を実現し、{theory-name}理論に基づく包括的な{domain}分析を提供