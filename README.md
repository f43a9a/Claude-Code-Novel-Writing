# 📚 Plot-System: 統合創作支援システム

Claude Codeを活用した**プロット構築から小説執筆まで**の一貫した創作支援システム

## 🎯 システム概要

Plot-Systemは、AIの自然言語理解能力を最大限活用し、8段階のプロセスを通じて**プロット構築から完成小説まで**を一貫してサポートする統合創作環境です。

### ✨ 特徴

- **8段階創作フロー**: concept → setting → character → structure → validate → conte → writing-generate → writing-review
- **多元的理論統合**: Writer MBTI(6種) × Character MBTI(16種) × ジャンル(6種) × 文体(6種) × 読者層(3種)
- **自然言語対話**: 複雑オプションではなく自然な相談による柔軟な創作支援
- **実際の改善実行**: 「評価だけ」でなく具体的な品質向上を実現
- **ローカルファイル管理**: プロジェクト別の整理された保存システム

## 🏗️ システム構成

```
plot-system/
├── CLAUDE.md                           # システム全体方針定義
├── README.md                           # このファイル
├── docs/                               # AI Writers Gallery（Jekyll サイト）
│   ├── _config.yml                     # Jekyll 設定
│   ├── _layouts/                       # レイアウトテンプレート
│   ├── _posts/                         # 公開作品
│   ├── _authors/                       # AI 作家情報
│   └── assets/                         # CSS・画像等
├── template/                           # テンプレートファイル群
├── .claude/
│   ├── commands/
│   │   ├── plot-concept.md             # Phase 1: 基本企画
│   │   ├── plot-setting.md             # Phase 2: 世界観設定
│   │   ├── plot-character.md           # Phase 3: キャラクター設計
│   │   ├── plot-structure.md           # Phase 4: プロット構造設計
│   │   ├── plot-validate.md            # Phase 5: 統合検証・改善
│   │   ├── conte.md                    # Phase 6: 映像演出設計
│   │   ├── writing-generate.md         # Phase 7: 小説執筆
│   │   └── writing-review.md           # Phase 8: 品質レビュー・改善
│   └── docs/
│       ├── shared/instructions/        # 理論体系
│       │   ├── hit-patterns/           # 古典的物語理論
│       │   ├── genre/                  # ジャンル理論（fantasy, slice_of_life, mystery, romance, sci_fi, fairy_tale）
│       │   ├── writing_style/          # 文体理論（literary, conversational, descriptive, minimalist, poetic, journalistic）
│       │   ├── writer_mbti_patterns/   # 創作者思考パターン（6種）
│       │   ├── audience/               # 読者層理論（3種）
│       │   └── character_mbti_patterns/ # キャラクター原型（16種）
│       ├── plot-*/                     # 各コマンドの詳細ドキュメント
│       └── writing-*/                  # 執筆コマンドのドキュメント
└── outputs/                            # プロジェクト保存ディレクトリ
```

## 🚀 クイックスタート

### 前提条件
- Claude Code環境

### 基本的な使い方

#### 🎬 Phase 1-5: プロット構築

```bash
# 1. 基本企画（AIが自動でジャンル・MBTI・読者層を判定）
/plot-concept "時間が止まる能力を持つ女子高生の日常"

# 2. 世界観設定（AIが判定したジャンルに基づく）
/plot-setting 42

# 3. キャラクター設計（MBTI原型による多様なキャラ）
/plot-character 42

# 4. プロット構造設計（効果的な物語構造）
/plot-structure 42

# 5. 統合検証・改善（実際の修正を実行）
/plot-validate 42
```

#### 🎭 Phase 6: 映像演出設計

```bash
# 6. 絵コンテ設計（映像的演出設計）
/conte 42
# → 対話例: 「感情的なクライマックスを重視してください」
```

#### ✍️ Phase 7-8: 小説執筆・改善

```bash
# 7. AIが小説を執筆（自然言語対話で要望相談）
/writing-generate 42
# → 対話例: 「軽快な文体で全体を書いてください」

# 8. AIがレビュー・改善実行（実際の品質向上）
/writing-review 42
# → 対話例: 「キャラクターの魅力をもっと出したい」
```

### 🎨 自然言語対話の例

```bash
# 複雑なオプションではなく自然な相談
/writing-generate 42 "第2章だけ、もう少し詩的な感じで"
/writing-review 42 "感情描写を深くしたい"

# AI側の対応例
AI: 「プロット設定を確認しました。ISFP思考パターンとファンタジー設定ですね。
     詩的で美的な表現を重視した文体で第2章を執筆します。
     特に重視したい要素はありますか？」
```

## 📋 理論体系

### ジャンルタイプ（6種類）

| ジャンル | 特徴 | 主要要素 |
|----------|------|----------|
| `fantasy` | ファンタジー | 魔法・異世界・冒険・複雑な世界観 |
| `slice_of_life` | 日常系 | 現実的・日常生活・等身大の成長・気づき |
| `mystery` | ミステリー | 論理的推理・謎解き・社会批判・探偵要素 |
| `romance` | 恋愛 | 感情的関係・心理描写・成長・ハッピーエンド |
| `sci_fi` | SF | 科学技術・未来予測・哲学的探求・革新性 |
| `fairy_tale` | 童話 | 道徳教訓・象徴的表現・魔法的要素・普遍的価値 |

### 文体スタイル（6種類）

| 文体 | 特徴 | 主要要素 |
|------|------|----------|
| `literary` | 文芸的 | 言語美・哲学的深み・芸術性・文学的伝統 |
| `conversational` | 会話的 | 親しみやすさ・自然な語り口・読者との対話 |
| `descriptive` | 描写的 | 五感的詳細・臨場感・感覚的表現・没入感 |
| `minimalist` | 簡潔 | 言語経済性・含意的表現・本質重視・効率性 |
| `poetic` | 詩的 | 韻律・イメージ・音響美・感情的強度 |
| `journalistic` | 報道的 | 客観性・事実重視・明確性・信頼性 |

### Writer MBTI思考パターン（6種類）

| タイプ | アプローチ | 特徴 |
|--------|------------|------|
| `INTJ` | 戦略的マスタープロット | 構造重視・論理的・長期的視点 |
| `ISFP` | 感情体験重視プロット | 体験重視・感情的・美的価値 |
| `ENFP` | インスピレーション駆動 | 創造的・エネルギッシュ・可能性重視 |
| `ENTP` | 革新的アイデア展開 | 概念的・実験的・論理的創造 |
| `INFP` | 価値観・真実性重視 | 内面的・真正性・個人的価値 |
| `ESTJ` | 実務的・効率的構築 | 組織的・実用的・目標達成重視 |

### Character MBTI原型（16種類）

全16のMBTI原型に対応したキャラクター設計指針：
- 各原型の性格特性・物語機能・成長軌道
- 他原型との関係性・相性分析
- ジャンル別活用法・現代的配慮

### 読者層タイプ（3種類）

| タイプ | 対象年齢 | 特徴 |
|--------|----------|------|
| `young_adult` | 13-25歳 | 成長・冒険・等身大の体験 |
| `adult` | 18-65歳 | エンターテイメント・複雑さ・深い人間関係 |
| `literary` | 全年齢 | 芸術性・哲学的深み・美的価値 |

## 📁 出力ファイル構成

各プロジェクトは`outputs/{project-id}/`ディレクトリに保存されます：

```
outputs/42/
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
