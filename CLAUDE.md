---
authority_level: "最高権威 (システム全体方針)"
target_audience: ["全体"]
maintainer: "プロジェクトオーナー"
last_updated: "2025-07-07"
dependencies: []
note: "他ファイルが本ファイルを参照"
tags: ["system-core", "plot-construction", "writing-system", "guidelines"]
---

# Claude Code プロット構築・執筆統合システム

## 📋 このファイルの役割
プロット構築から小説執筆まで一貫した創作支援システム全体の**最高権威**方針定義です。
すべてのコマンド・ドキュメントは本ファイルの原則に従います。

## ⚡ トークン効率化設定
- 環境変数設定: `.env.claude` (トークン制限)
- コンパクト機能: `.claude/commands/compact-guide.md`
- 具体的なクエリ使用、複雑タスクの分割を推奨

## システムの特徴

このシステムは**段階的プロット構築から完成小説まで**を一貫して支援する統合創作環境です。

### 8段階創作フロー
- **Phase 1-5**: プロット構築（concept→setting→character→structure→validate）
- **Phase 6**: シーン演出設計（conte）
- **Phase 7**: 小説執筆（writing-generate）
- **Phase 8**: 品質改善（writing-review）

### 多元的創作理論の統合
- **ジャンルタイプ**: fantasy/slice_of_life - 対照的な世界観アプローチ
- **Writer MBTI思考パターン**: 6種類 - 創作者の認知機能に基づくアプローチ
- **Character MBTI原型**: 16種類 - キャラクター設計の多様性確保
- **読者層タイプ**: young_adult/adult/literary - 対象読者に応じた調整
- **Hit-patterns理論**: 古典的物語構造の現代的活用
- **自由な組み合わせ**: 固定リンクなし、創作者の個性を最大限活用

### システムの使命
各創作アプローチの**本来の特性を活かす**ことが使命です：
- **Writer MBTI**: 創作者の認知機能に応じた最適な創作プロセス
- **Character MBTI**: 16原型による多様で魅力的なキャラクター設計
- **ジャンル理論**: fantasy/slice_of_lifeの本質的魅力の最大化
- **Hit-patterns**: 普遍的物語構造の効果的実装

## 基本ルール

### 絶対原則
1. **段階順序の厳守**: 各段階を順次完了（スキップ禁止）
2. **AI自然理解重視**: ルールベース・疑似関数の完全排除
3. **個性尊重**: 創作者の独自性を損なわない柔軟な支援
4. **実用性確保**: 執筆可能レベルのプロット・完成小説の生成
5. **実際の改善実行**: 「評価だけ」でなく具体的な品質向上を実現
6. **短編執筆の原則**: 明示的な依頼がない限り、短編（5000-10000文字）を執筆

### 実行指針
- **プロット構築**: @.claude/commands/plot-concept.md, plot-setting.md, plot-character.md, plot-structure.md, plot-validate.md
- **演出設計**: @.claude/commands/conte.md
- **執筆系**: @.claude/commands/writing-generate.md, writing-review.md
- **理論体系**: 条件に応じて必要なファイルのみ参照

## 品質方針

### 評価軸
- **一貫性**: 全段階を通じた論理的整合性
- **完成度**: 執筆・読者体験に使用可能な詳細さ
- **個性**: Writer MBTI思考パターンの効果的な反映
- **実用性**: 読者にとっての価値・魅力
- **改善実効性**: 実際に品質が向上する具体的改善

### 改善方針（issue #32対応）
- **具体的修正実行**: 抽象的「〜を強化」でなく「ファイル:行:修正内容」レベルの改善
- **段階的品質向上**: Critical Fix → Quality Enhancement → Appeal Amplification
- **読者体験重視**: 理論的完成度より実際の読みやすさ・面白さ
- **自然言語対話**: 複雑オプションでなく対話による柔軟な要望対応

## 統合創作システム

### プロット構築システム（Phase 1-5）
```bash
# 基本的な5段階フロー
/plot-concept "小説アイデア"      # AI判断による構成決定
/plot-setting 42                # ジャンル特性に基づく世界観構築
/plot-character 42              # MBTI原型による魅力的キャラクター設計
/plot-structure 42              # 効果的な物語構造設計
/plot-validate 42               # 統合検証と実際の改善実行
```

### 演出設計システム（Phase 6）
```bash
# 映像的絵コンテ理論による演出設計
/conte 42                       # 映像的演出設計
```

### 執筆システム（Phase 7-8）
```bash
# 自然言語対話による執筆・改善
/writing-generate 42            # AIがプロットを基に小説を執筆
/writing-review 42              # AIが実際の改善を実行
```

### 理論体系の活用
効率的な理論参照（必要なファイルのみ）：
- **hit-patterns/**: 古典的物語理論
- **genre/**: ジャンル固有の特性（fantasy, slice_of_life）
- **writer_mbti_patterns/**: 認知機能ベース創作アプローチ
- **audience/**: 読者層別特性
- **character_mbti_patterns/**: キャラクター機能分析
- **conte_techniques/**: 映像演出技法
- **structure_design/**: 構造設計技法

**参照方法**: 全ファイル読み込みでなく、設定に応じた個別参照

## ファイル管理方針

### ローカルファイル保存
- 各創作プロジェクトをローカルディレクトリで管理
- 段階完了時のファイル保存・更新
- 最終完了時の統合ファイル生成

### ファイル管理
```
outputs/{project-id}/
├── output-plot-concept.md      # 基本企画書
├── output-plot-setting.md      # 世界観設定書
├── output-plot-character.md    # キャラクター設計書
├── output-plot-structure.md    # プロット構造設計書
├── output-plot-validate.md     # 検証結果
├── output-conte.md             # 絵コンテ設計書
├── output-writing-generate.md  # 完成小説
├── output-writing-review.md    # レビュー・改善記録
├── writing_conversation.md     # 執筆過程の対話履歴
└── review_conversation.md      # レビュー過程の対話履歴
```

## 現代的配慮

### 拡張された理論基盤
- **Writer MBTI**: 2種類→6種類への拡張（ENFP, ENTP, INFP, ESTJ追加）
- **Character MBTI**: 6種類→16種類への拡張（全MBTI原型の完備）
- **WHY/HOW分析**: ジャンル・Hit-patterns理論の深化
- **Template統合**: 散在ファイルの template/ ディレクトリ統合

### 技術的改善
- **validateステップ改善**: 形式的評価から実際の改善実行へ（issue #32対応）
- **自然言語対話重視**: 複雑オプションから対話による柔軟な要望対応へ
- **段階的品質向上**: Critical/Quality/Appeal の3段階改善システム
- **トークン効率化**: 環境変数制限、コンパクト機能、個別ファイル参照（issue #64対応）

## 実装済み機能（2025-07-01現在）

### ✅ 完成済み
- プロット構築システム（plot-concept, setting, character, structure, validate）
- 執筆システム（writing-generate, writing-review）
- 理論体系（writer MBTI 6種類, character MBTI 16種類, genre WHY/HOW分析）
- validateステップ改善（実際の修正実行）
- Template統合・整理

### 🔄 継続的改善
- 理論ファイルの動的活用
- ユーザーフィードバックに基づく機能向上
- AI分析精度の継続的向上

---

**統合創作支援により、プロット構築から完成小説まで、創作者の個性を活かした高品質な作品創出を実現すること**