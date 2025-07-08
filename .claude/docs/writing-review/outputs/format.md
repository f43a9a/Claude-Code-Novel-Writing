---
authority_level: "出力仕様定義"
target_audience: ["AI", "システム開発者"]
maintainer: "プロジェクトリード"
last_updated: "2025-07-08"
dependencies:
  - "[[writing-review]]"
  - "[[shared/instructions/quality-theory]]"
tags: ["writing-review", "output", "review-report", "template"]
---

# writing-review 出力フォーマット

## 📋 このファイルの役割
`/writing-review` コマンドが生成するレビューレポートの標準テンプレートを定義します。
辛口な批評と具体的な改善提案に特化した、実効性重視の品質向上を目的とします。

## 🎯 レビューレポート テンプレート

```bash
# メインレポート生成
cat > plots/{issue_number}/review_report.md <<EOF
# 📊 小説レビューレポート: {小説タイトル}

**レビュー日**: {date}
**Issue**: #{issue_number}
**ステータス**: レビュー・改善完了
**レビュー対象**: {review_scope}
**改善方針**: {improvement_approach}

---

## 🔍 品質評価結果

### 基本品質評価
- **プロット一貫性**: {consistency_status} - {consistency_detail}
- **文学的品質**: {literary_quality_status} - {literary_detail}
- **読者体験**: {reader_experience_status} - {reader_detail}

### 詳細分析

#### 📖 構造・内容分析
{structure_analysis}

#### 🎭 キャラクター分析
{character_analysis}

#### ✍️ 文体・表現分析
{style_analysis}

#### 🎯 最適読者層適合分析
{魅力最大化適合分析}

## ⚠️ 批判的品質分析

### 明確な問題点
**読者層ミスマッチ**: {現在の表現レベルではターゲット読者に達していない部分}
**表現の不十分さ**: {語彙・文体・描写の不適切な箱所}
**構造的劣化**: {物語展開・ペーシング・緊張感の不備}

### 根本的な改善要求
**キャラクターの平板化**: {個性不足・魅力不足・成長の不自然さ}
**テーマの涅長さ**: {無意味な繰り返し・深度不足・インパクト不足}
**読者体験の貧弱さ**: {感情移入できない箱所・飽きを感じる部分}

## 🔧 発見された改善ポイント

### 🔴 Critical Fix（修正必須）
{critical_issues_found}

### 🟡 Quality Enhancement（品質向上）
{quality_improvement_opportunities}

### 🟢 Appeal Amplification（魅力拡張）
{appeal_enhancement_possibilities}

## ⚡ 実行した改善

### Critical Fix（修正必須）
{critical_fixes_implemented}

### Quality Enhancement（品質向上）
{quality_enhancements_implemented}

### Appeal Amplification（魅力拡張）
{appeal_amplifications_implemented}

## 📈 改善効果分析

### 改善前後の比較
{before_after_comparison}

### 品質向上の定量評価
- **文字数変化**: {character_count_change}
- **表現豊かさ**: {expression_richness_change}
- **読みやすさ**: {readability_improvement}
- **感情的インパクト**: {emotional_impact_enhancement}

### 理論的根拠
{theoretical_justification}

## 🎯 最終評価

### 改善後の現実的評価
- **プロット一貫性**: {final_consistency_rating} - まだ残る矛盾と要改善点
- **文学的品質**: {final_literary_rating} - 依然不十分な表現領域
- **読者体験**: {final_reader_rating} - 更なる改善が必要な箱所
- **独自性**: {final_uniqueness_rating} - 隅没しやすい特徴と差別化不足

### 推奨される次のステップ
{next_steps_recommendation}

## 🚀 プロジェクト状況
- [x] Phase 1: concept（基本企画）
- [x] Phase 2: setting（世界観設定）
- [x] Phase 3: character（キャラクター設計）
- [x] Phase 4: structure（プロット構造設計）
- [x] Phase 5: validate（統合検証）
- [x] Phase 6: writing-generate（小説執筆）
- [x] Phase 7: writing-review（品質レビュー・改善）

## 📝 次のアクション
{next_action_recommendation}
EOF

# 対話記録ファイル生成  
cat > plots/{issue_number}/review_conversation.md <<EOF
# 💬 レビュー対話記録

**レビュー日**: {date}
**Issue**: #{issue_number}

## 対話履歴
{conversation_history}

## 決定事項
- **改善優先度**: {final_priority}
- **改善焦点**: {final_focus}
- **改善範囲**: {final_scope}
- **特別な調整**: {special_adjustments}

## AI分析・判断根拠
{ai_analysis_reasoning}

## 改善実行ログ
{improvement_execution_log}
EOF

# 改善版小説の生成（バージョン管理）
# 既存のファイルを確認して連番で保存
REVISION_NUM=01
while [ -f "outputs/{project_id}/output-writing-generate-revised${REVISION_NUM}.md" ]; do
  REVISION_NUM=$(printf "%02d" $((10#$REVISION_NUM + 1)))
done

cat > outputs/{project_id}/output-writing-generate-revised${REVISION_NUM}.md <<EOF
# 📖 {小説タイトル}（改善版）

**執筆日**: {original_writing_date}
**改善日**: {date}
**Issue**: #{issue_number}
**ステータス**: レビュー・改善完了
**文字数**: {improved_character_count}文字
**改善内容**: {improvement_summary}

---

{改善後の小説本文}

---

## 📊 改善履歴

### 実行した改善
{implemented_improvements_summary}

### 改善効果
{improvement_effects_summary}

### 品質向上の根拠
{quality_improvement_evidence}

## 🚀 次のステップ
追加の改善が必要な場合:
```bash
/writing-review {issue_number}
```

新しいプロジェクトを開始する場合:
```bash
/plot-concept "新しい小説アイデア"
```
EOF
```

## 📝 各セクションの詳細仕様

### 基本情報セクション
- **レビュー日**: 実行日時
- **Issue**: 対象のGitHub Issue番号
- **ステータス**: 「レビュー・改善完了」固定
- **レビュー対象**: 全体/部分等のレビュー範囲
- **改善方針**: 選択された改善アプローチ

### 品質評価結果セクション
客観的な品質分析：
- **プロット一貫性**: 元プロット設定との整合性評価
- **文学的品質**: 文体・表現・構成の質的評価
- **読者体験**: 最適読者層への適合度・魅力度評価

各項目で ❌重大な問題 / ⚠️改善必要 / ✅最低基準クリア の厄しい評価基準

### 詳細分析セクション

#### 構造・内容分析
物語構造の最適化評価：
- **narrative構造**: hit-patterns理論に基づく構造評価
- **プロット展開**: 論理的流れと読者関心維持の分析
- **テーマ統合**: 設定されたテーマの効果的表現度

#### キャラクター分析
人物描写の魅力度評価：
- **個性の明確さ**: character設定の効果的実装
- **成長軌道**: キャラクターアークの説得力
- **関係性**: キャラクター間の相互作用効果

#### 文体・表現分析
言語表現の品質評価：
- **文体一貫性**: 選択された文体の一貫した実装
- **語彙適合性**: 最適読者層への適切さ
- **表現技法**: 比喩・象徴・修辞技法の効果

#### 最適読者層適合分析
ターゲット読者への訴求力評価：
- **最適読者層期待**: 読者層固有の期待への対応
- **ジャンル要求**: ジャンル読者の期待充足度
- **感情的インパクト**: 読者の感情移入・カタルシス効果

### 改善ポイント・実行セクション

#### 3段階改善システム
**🔴 Critical Fix（修正必須）**:
- 論理的矛盾の発見と修正
- 明らかな設定不整合の解消
- 読解困難な表現の改善

**🟡 Quality Enhancement（品質向上）**:
- 読者の感情移入強化
- キャラクター魅力の向上
- 文体・表現の洗練

**🟢 Appeal Amplification（魅力拡張）**:
- 独創性の強化
- 市場差別化の向上
- 文学的価値の追加

### 改善効果分析セクション
定量的・定性的な改善効果の評価：
- **改善前後の比較**: 具体的な変更点と効果
- **品質向上の定量評価**: 測定可能な指標での評価
- **理論的根拠**: shared/instructions理論に基づく改善効果説明

## 🔄 動的要素の展開例

### 辛口品質評価の詳細展開例
```markdown
### 基本品質評価
- **プロット一貫性**: ⚠️改善必要 - 物語展開に不自然な飛躍、動機不明の行動が散見
- **文学的品質**: ❌重大な問題 - 平板で予測可能な表現、深みのないキャラクター描写
- **読者体験**: ⚠️改善必要 - ターゲット読者の期待レベルに未達、感情的インパクト不足
```

### 改善実行の詳細展開例
```markdown
### Quality Enhancement（品質向上）
#### 感情描写の深化
- **改善箇所**: 第3章15段落目
- **変更前**: 「悲しかった」
- **変更後**: 「胸の奥で何かが重くのしかかり、呼吸が浅くなった」
- **効果**: 読者の感情移入が深まり、主人公への共感が強化

#### 対話の自然さ向上
- **改善箇所**: 第1章の主人公とみどりの会話
- **変更内容**: 年齢に応じた自然な口調に調整
- **効果**: キャラクターの個性がより明確に表現
```

### 理論的根拠の展開例
```markdown
### 理論的根拠
- **ISFP文体理論**: 内向感情(Fi)機能を活かした真正性のある感情表現の強化
- **fantasy表現技法**: 魔法的現実主義による日常と非日常の自然な融合
- **young_adult読者適合**: 等身大成長物語として共感しやすい表現の最適化
```

## ⚙️ テンプレート変数

実際の実装時に置換される変数：
- `{小説タイトル}`: concept.mdで設定されたタイトル
- `{date}`: レビュー実行日時
- `{issue_number}`: 対象GitHub Issue番号
- `{review_scope}`: レビュー対象範囲（全体/部分）
- `{improvement_approach}`: 選択された改善アプローチ
- `{品質評価の詳細}`: 各品質指標の具体的評価結果
- `{改善実行の詳細}`: 実際に行われた修正内容
- `{改善効果の分析}`: 定量的・定性的な改善効果
- `{改善後の小説本文}`: 修正が適用された最終的な小説テキスト

## 📊 品質指標

### 必須要素の確認
- [ ] 基本情報5項目がすべて記載されている
- [ ] 品質評価が客観的に実行されている
- [ ] 改善ポイントが具体的に特定されている
- [ ] 実際の改善が実行されている
- [ ] 改善効果が分析されている

### 推奨要素の確認
- [ ] 理論的根拠が明確に説明されている
- [ ] 改善前後の比較が具体的である
- [ ] 次のステップが適切に提案されている
- [ ] 対話記録が適切に保存されている

---

**実装方針**: レビューレポート上でのワンストップな品質管理を実現し、改善理論に基づく包括的な小説品質向上を提供