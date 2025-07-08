---
authority_level: "出力フォーマット定義"
target_audience: ["AI", "システム開発者"]
maintainer: "プロジェクトリード"
last_updated: "2025-07-01"
dependencies:
  - "[[CLAUDE]]"
  - "[[plot-validate]]"
tags: ["output-format", "github-issue", "local-file", "final-deliverable"]
---

# 📤 plot-validate 出力フォーマット定義

## 📋 このファイルの役割

plot-validate コマンドの出力フォーマットを定義し、GitHub Issue完了・ローカルファイル生成・最終プロット書作成において一貫した品質と形式を確保します。

## 🎯 GitHub Issue・ローカルファイル共通フォーマット

GitHub Issue完了とローカルファイル保存に全く同じ詳細内容を使用：

```markdown
# 📚 統合検証・最終プロット書: {title}

**作成日**: {creation_date}
**Issue**: #{issue_number}
**ステータス**: validate完了・プロジェクト完了
**前段階**: concept.md, setting.md, character.md, structure.md

---

## ✅ 統合検証結果

### 🔍 総合評価: {overall_rating}

**品質レベル**: {quality_level} (A:優秀 / B:良好 / C:合格 / D:要改善)

### 📊 項目別評価

| 検証項目 | 評価 | 詳細 |
|---------|------|------|
| **論理的一貫性** | {consistency_rating} | {consistency_detail} |
| **ジャンル適合性** | {genre_rating} | {genre_detail} |
| **MBTI実装** | {mbti_rating} | {mbti_detail} |
| **最適読者層適合** | {魅力最大化評価} | {魅力最大化詳細} |
| **完成度** | {completeness_rating} | {completeness_detail} |

### 🎯 統合分析詳細

#### 基盤整合性 (hit-patterns理論適用)
{hit_patterns_analysis}

**確認項目**:
- ✅ 古典的物語構造との適合性
- ✅ 構造要素の統合性
- ✅ キャラクター原型の効果的活用

#### 創作一貫性 ({mbti_pattern}思考パターン)
{writer_mbti_analysis}

**確認項目**:
- ✅ 認知機能の全段階一貫適用
- ✅ 創作アプローチの効果的実装
- ✅ 思考パターン特性の最大活用

#### ジャンル完成度 ({genre}特性)
{genre_analysis}

**確認項目**:
- ✅ ジャンル固有要求の充足
- ✅ 読者期待との合致度
- ✅ ジャンル制約の適切な活用

#### 作品魅力価値 (最適読者層配慮)
{魅力最大化分析}

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

**確認項目**:
- ✅ 対象読者の期待充足
- ✅ 適切な複雑度・深み
- ✅ 共感・没入要素の実装

## 📖 最終プロット書

### 🎭 作品概要

**基本情報**:
- **タイトル**: {title}
- **ジャンル**: {genre}
- **思考パターン**: {mbti_pattern}
- **最適読者層**: {魅力最大化戦略}
- **推定文字数**: {estimated_length}

**作品コンセプト**:
{integrated_concept}

### 🌍 統合世界観

**設定概要**:
{integrated_setting}

**世界観の特色**:
- {setting_feature_1}
- {setting_feature_2}
- {setting_feature_3}

**物語制約とルール**:
{world_constraints}

### 👥 統合キャラクター設計

**主人公**: {protagonist_name}
{integrated_protagonist_design}

**重要人物**: 
{integrated_supporting_characters}

**人間関係ダイナミクス**:
{integrated_relationships}

**キャラクター成長統合**:
{integrated_character_arcs}

### 📖 統合プロット構造

**採用構造**: {structure_type}
{structure_rationale}

#### 第一幕: {act1_title} ({act1_percentage})
{integrated_act1_detail}

**主要シーン**:
1. **オープニング**: {opening_scene}
2. **扇動的事件**: {inciting_incident}
3. **プロットポイント1**: {plot_point_1}

#### 第二幕: {act2_title} ({act2_percentage})
{integrated_act2_detail}

**主要転換点**:
1. **ミッドポイント**: {midpoint}
2. **プロットポイント2**: {plot_point_2}

#### 第三幕: {act3_title} ({act3_percentage})
{integrated_act3_detail}

**クライマックス・解決**:
1. **クライマックス**: {climax}
2. **解決**: {resolution}

### 🎯 統合テーマ表現

**中心テーマ**: {central_theme}
{theme_integration}

**テーマの構造的表現**:
- **第一幕**: {theme_act1}
- **第二幕**: {theme_act2}
- **第三幕**: {theme_act3}

**サブテーマ**:
{sub_themes}

### 🕸️ 統合伏線システム

**主要伏線**:
{integrated_foreshadowing}

**回収システム**:
{payoff_system}

### 📈 感情カーブ・読者体験設計

**感情的流れ**:
{emotional_curve}

**{mbti_pattern}読者への最適化**:
{mbti_reader_optimization}

**最適読者層への配慮**:
{魅力最大化最適化}

## 📚 理論的統合根拠

### 適用理論の統合

**hit-patterns理論**:
{hit_patterns_integration}

**{mbti_pattern}思考パターン**:
{writer_mbti_integration}

**{genre}ジャンル理論**:
{genre_integration}

**最適読者層理論**:
{魅力最大化統合}

**character_mbti_patterns**:
{character_mbti_integration}

### 理論間の相乗効果

{theory_synergy}

## 🌟 作品の独自性と価値

### 差別化ポイント

{differentiation_points}

### 読者への提供価値

{reader_value}

## 💡 推奨改善点・発展可能性

### さらなる向上のために

{improvement_suggestions}

### 創作継続の指針

{creative_development_guidance}

## 📝 執筆活用ガイド

### このプロット書の使い方

**基本活用法**:
{basic_usage}

**執筆時の重点ポイント**:
{writing_focus_points}

**創作過程での活用**:
{creative_process_guidance}

### 推奨執筆アプローチ

**{mbti_pattern}らしい執筆法**:
{mbti_writing_approach}

**ジャンル特性の活用**:
{genre_writing_tips}

## 🎉 プロジェクト完了

### 達成された成果

✅ **5段階プロット構築完了**:
- [x] Phase 1: concept（基本企画）
- [x] Phase 2: setting（世界観設定）
- [x] Phase 3: character（キャラクター設計）
- [x] Phase 4: structure（プロット構造設計）
- [x] Phase 5: validate（統合検証）

✅ **品質保証**:
- 論理的一貫性の確保
- ジャンル・読者層適合性の確認
- 執筆可能レベルの完成度達成

✅ **理論的裏付け**:
- 古典的物語理論の現代的活用
- MBTI思考パターンの効果的実装
- 市場価値と独自性の両立

### 次のステップ

**執筆開始準備完了** 🚀

このプロット書を活用して、魅力的な物語の執筆を開始してください。

**成果物ファイル**:
- 📄 `plots/{issue_number}/plot_complete.md` - 統合最終プロット書
- 📋 `plots/{issue_number}/validate.md` - 統合検証詳細レポート
- 🎯 GitHub Issue #{issue_number} - プロジェクト管理記録

**お疲れ様でした！** 素晴らしいプロット書の完成です 🎊

---

**実装方針**: 全段階の統合価値を最大化し、執筆可能な最高品質のプロット書として、創作者の成功を支援する完成度を実現
```

## 📄 ローカルファイル生成詳細

### ファイル出力仕様

**validate.md** (統合検証レポート):
```
plots/{issue-number}/validate.md
- 統合検証の詳細分析
- 品質評価の根拠
- 改善提案（該当する場合）
```

**plot_complete.md** (最終プロット書):
```
plots/{issue-number}/plot_complete.md
- GitHub Issue と完全に同一内容
- 執筆に直接使用可能な完成度
- 全段階の統合された最終成果物
```

### GitHub Issue 完了処理

**Issue クローズ処理**:
```bash
gh issue comment {issue_number} --body "$(cat plot_complete.md)"
gh issue close {issue_number}
```

**完了ラベル付け**:
- `completed`: プロジェクト完了済み
- `plot`: プロット構築プロジェクト
- `{genre}`: ジャンル名

## 📊 出力品質基準

### 必須要素の確認

**統合検証部分**:
- [ ] 全5段階の一貫性確認結果
- [ ] 理論に基づく客観的評価
- [ ] 具体的な品質根拠の提示

**最終プロット書部分**:
- [ ] 全段階要素の統合表現
- [ ] 執筆に十分な詳細度
- [ ] 理論的裏付けの明示
- [ ] 創作者への実用的ガイド

**完了処理部分**:
- [ ] プロジェクト成果の明確化
- [ ] 次のステップの具体的提示
- [ ] 達成感と満足感の提供

### 品質レベル対応

**A (優秀)**: 全要素が高水準で統合、独自性も十分
**B (良好)**: 基準を満たし実用的、魅力的な内容
**C (合格)**: 最低基準満たし執筆開始可能
**D (要改善)**: 改善提案を含め段階的完成を支援

---

**実装方針**: 5段階プロット構築の集大成として、最高品質の統合プロット書を生成し、創作者の執筆成功を確実に支援