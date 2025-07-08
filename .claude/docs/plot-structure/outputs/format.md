---
authority_level: "出力フォーマット定義"
target_audience: ["AI", "システム開発者"]
maintainer: "プロジェクトリード"
last_updated: "2025-07-01"
dependencies:
  - "[[CLAUDE]]"
  - "[[plot-structure]]"
tags: ["output-format", "github-issue", "local-file"]
---

# 📤 plot-structure 出力フォーマット定義

## 📋 このファイルの役割

plot-structure コマンドの出力フォーマットを定義し、GitHub Issue更新とローカルファイル生成の両方において一貫した品質と形式を確保します。

## 🎯 GitHub Issue・ローカルファイル共通フォーマット

GitHub Issue更新とローカルファイル保存に全く同じ詳細内容を使用：

```markdown
# プロット構造設計書: {title}

**作成日**: {creation_date}
**Issue**: #{issue_number}
**ステータス**: structure完了
**前段階**: concept.md, setting.md, character.md

---

## 📋 設計概要

| 項目 | 内容 |
|------|------|
| **採用構造** | {structure_type} |
| **MBTI最適化** | {mbti_pattern} |
| **ジャンル** | {genre} |
| **最適読者層** | {魅力最大化戦略} |
| **推定文字数** | {estimated_length} |

## 📖 採用した物語構造

### {structure_type}

**選択理由**:
{structure_reasoning_detailed}

**理論的根拠**:
- **hit-patterns適用**: {hit_patterns_application}
- **{mbti_pattern}思考パターン**: {mbti_application}
- **{genre}ジャンル特性**: {genre_application}
- **最適読者層調整**: {魅力最大化戦略}

## 🎭 三幕構成・プロットポイント

### 第一幕: {act1_title} ({act1_percentage} - 約{act1_words}文字)

**目的**: {act1_purpose}

#### 主要シーン
1. **オープニング** ({opening_percentage})
   - {opening_description}
   - **キャラクター状態**: {character_initial_state}
   - **世界観提示**: {world_presentation}

2. **扇動的事件** ({inciting_percentage})
   - **事件**: {inciting_incident_detail}
   - **キャラクターへの影響**: {character_impact}
   - **物語への転換**: {story_transition}

3. **プロットポイント1** ({pp1_percentage})
   - **転換点**: {plot_point_1_detail}
   - **決断**: {character_decision}
   - **第二幕への移行**: {act2_transition}

### 第二幕: {act2_title} ({act2_percentage} - 約{act2_words}文字)

**目的**: {act2_purpose}

#### 前半: 新世界の探求 ({act2a_percentage})
- {act2a_description}
- **試練と学習**: {trials_and_learning}
- **仲間と敵**: {allies_and_enemies}

#### ミッドポイント: {midpoint_title} ({midpoint_percentage})
- **転換**: {midpoint_transformation}
- **新情報/視点**: {new_information}
- **ゲームチェンジ**: {game_changer}

#### 後半: 危機の深化 ({act2b_percentage})
- {act2b_description}
- **困難の増大**: {rising_difficulties}
- **内面的葛藤**: {internal_conflict}

#### プロットポイント2 ({pp2_percentage})
- **最大の危機**: {major_crisis}
- **失うもの**: {loss_stakes}
- **最終決戦への突入**: {final_battle_setup}

### 第三幕: {act3_title} ({act3_percentage} - 約{act3_words}文字)

**目的**: {act3_purpose}

#### クライマックス: {climax_title} ({climax_percentage})
- **最終対決**: {final_confrontation}
- **キャラクター成長の完成**: {character_growth_completion}
- **テーマの完全表現**: {theme_culmination}

#### 解決: {resolution_title} ({resolution_percentage})
- **新しい均衡**: {new_equilibrium}
- **成長の確認**: {growth_confirmation}
- **未来への示唆**: {future_implication}

## 🔄 キャラクターアーク統合

### {main_character_name}の成長軌道

**出発点**: {character_starting_point}
**成長の軌跡**:
1. **第一幕**: {act1_character_state} → {act1_character_growth}
2. **第二幕前半**: {act2a_character_growth}
3. **ミッドポイント**: {midpoint_character_transformation}
4. **第二幕後半**: {act2b_character_growth}
5. **第三幕**: {act3_character_completion}

**到達点**: {character_endpoint}

### 重要人物の機能
{important_characters_function}

## 🎯 テーマ表現設計

### 中心テーマ: {central_theme}

**構造的表現方法**:
- **第一幕**: {theme_act1_expression}
- **第二幕**: {theme_act2_expression}
- **第三幕**: {theme_act3_expression}

**表現技法**:
1. **直接的表現**: {direct_expression}
2. **象徴的表現**: {symbolic_expression}
3. **構造的表現**: {structural_expression}

### サブテーマ
{sub_themes_description}

## 🕸️ 伏線システム

### 主要伏線

1. **{foreshadowing_1_name}**
   - **配置**: {foreshadowing_1_placement}
   - **回収**: {foreshadowing_1_payoff}
   - **効果**: {foreshadowing_1_effect}

2. **{foreshadowing_2_name}**
   - **配置**: {foreshadowing_2_placement}
   - **回収**: {foreshadowing_2_payoff}
   - **効果**: {foreshadowing_2_effect}

### サブ伏線・暗示
{minor_foreshadowing_description}

### 回収タイミング戦略
{payoff_timing_strategy}

## 📈 感情カーブ設計

### 全体的な感情の流れ
```
感情レベル
     ↑
 10  |           ★(クライマックス)
     |          ∧∧
  8  |      ∧∧/  \
     |     /  \    \
  6  |    /    \    \∧
     |   /      \    ∨ \
  4  | ∧/        \     \∧
     |/           \     ∨ \
  2  ★             \      \
     |              \      \
  0  |───────────────────────────→
     開始  PP1  ミッド  PP2  クライマックス 終了
```

**感情要素**:
- **緊張感**: {tension_design}
- **共感**: {empathy_design}
- **カタルシス**: {catharsis_design}

## 🎨 {mbti_pattern}らしさの表現

### {mbti_pattern}思考パターンの活用

**認知機能との対応**:
- **主機能({primary_function})**: {primary_function_utilization}
- **補助機能({secondary_function})**: {secondary_function_utilization}
- **第三機能({tertiary_function})**: {tertiary_function_utilization}

### 読者体験の設計

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

**{mbti_pattern}読者が求める体験**:
- {mbti_reader_experience_1}
- {mbti_reader_experience_2}
- {mbti_reader_experience_3}

**提供する満足感**:
{satisfaction_provided}

## 📊 品質確認項目

### 構造的整合性 ✓
- [ ] 因果関係の論理性
- [ ] キャラクター動機の一貫性
- [ ] 世界観制約との適合性
- [ ] テーマ表現の効果性

### 読者体験最適化 ✓
- [ ] MBTI思考パターンへの適合
- [ ] ジャンル期待の充足
- [ ] 読者層ニーズへの対応
- [ ] 感情的満足度の確保

### 執筆実用性 ✓
- [ ] 詳細度の適切性
- [ ] 執筆指針の明確性
- [ ] 創作者の個性表現余地
- [ ] 理論と直感のバランス

## 進行状況
- [x] Phase 1: concept（基本企画）
- [x] Phase 2: setting（世界観設定）
- [x] Phase 3: character（キャラクター設計）
- [x] Phase 4: structure（プロット構造設計）
- [ ] Phase 5: validate（統合検証）

## 次のステップ
```bash
/plot-validate {issue_number}
```

---

**実装方針**: {structure_type}の特性を活かし、{mbti_pattern}思考パターンの読者に最適化された、執筆可能なレベルの詳細プロット構造設計書を提供
```

### 動的要素の説明

**{structure_type}**: 選択された構造理論
- 例: "三幕構成+ヒーローズ・ジャーニー要素"、"感情体験重視型構成"

**{structure_reasoning}**: 構造選択の根拠
- 例: "INTJ思考パターンに最適化された論理的展開"

**{mbti_optimization_point}**: MBTI適用の具体例
- 例: "戦略的伏線システム"、"感情的真実重視の展開"

## 📋 出力要素の動的生成ガイド

### テンプレート変数の設定方法
**基本情報変数**:
```
{title}: concept.mdから取得
{creation_date}: 実行日時
{issue_number}: 引数から取得
{mbti_pattern}: concept.mdから取得
{genre}: concept.mdから取得
{audience}: concept.mdから取得
```

**構造分析結果**:
```
{structure_type}: AI分析による構造選択結果
{structure_reasoning}: 選択根拠の説明
{mbti_optimization_point}: MBTI適用の具体例
{genre_adjustment}: ジャンル特性反映内容
{audience_adjustment}: 読者層調整内容
```

**プロット詳細**:
```
{act1_title}/{act2_title}/{act3_title}: 各幕のタイトル
{act1_percentage}: 文字数比率（例："25%"）
{inciting_incident}: 扇動的事件の説明
{plot_point_1}: 第一プロットポイント
{midpoint}: ミッドポイント転換
{plot_point_2}: 第二プロットポイント
{climax}: クライマックス
```

### 品質基準

**GitHub Issue更新**:
- 簡潔で要点が伝わる
- 次のアクションが明確
- 進捗状況が一目で分かる

**ローカルファイル**:
- 執筆に使用可能な詳細さ
- 理論的裏付けの明示
- 創作者の参考となる構造

---

**実装方針**: 理論的根拠を持ちながら実用的で、創作者が安心して執筆に移れるレベルの詳細なプロット構造設計書を生成