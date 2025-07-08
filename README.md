# 📚 Plot-System: 統合創作支援システム

Claude Codeを活用した**プロット構築から小説執筆まで**の一貫した創作支援システム

## 🌐 AI Writers Gallery

**Plot-Systemで生成された作品を公開するWebサイト**

- **URL**: [GitHub Pages でホスト予定]
- **技術**: Jekyll + GitHub Pages
- **特徴**: 読書に集中できるミニマルデザイン
- **場所**: `docs/` ディレクトリ

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
- GitHub CLI（認証済み）
- Git（基本操作の理解）

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

## 🔧 ファイル管理

### ローカル保存
- 各創作プロジェクトがローカルディレクトリで管理される
- 段階完了時のファイル保存・更新
- プロジェクトID別の整理された構造

## 🎯 主要な改善点

### Issue #32対応: validateステップ改善
- **従来**: 形式的評価で「A評価・優秀」と評価して終わり
- **改善後**: 実際の修正を実行する3段階改善
  - 🔴 Critical Fix: 論理矛盾・設定不整合の修正
  - 🟡 Quality Enhancement: 読者体験・感情移入の強化
  - 🟢 Appeal Amplification: 独創性・市場競争力の向上

### Issue #33対応: 執筆システム追加
- **writing-generate**: AIが実際に小説を執筆
- **writing-review**: AIが実際に品質改善を実行
- **自然言語対話**: 複雑オプションでなく自然な相談

## 📊 現在の実装状況

### ✅ 完成済み（2025-07-07）
- **プロット構築システム**: 5段階フロー完備
- **映像演出設計**: conte段階の追加（映像的絵コンテ理論による演出強化）
- **執筆システム**: writing-generate, writing-reviewコマンド
- **理論体系**: Writer MBTI 6種類, Character MBTI 16種類
- **ジャンル理論**: WHY/HOW分析による深化
- **Template統合**: 散在ファイルの整理
- **validateステップ改善**: 実際の修正実行

### 🔄 継続的改善
- 理論ファイルの動的活用
- ユーザーフィードバックに基づく機能向上
- AI分析精度の継続的向上

## 🎯 利用シーン

### 個人創作者
- **完全な創作自動化**: アイデア → プロット → 完成小説
- **創作技法学習**: AI執筆プロセスから技法を学習
- **効率的創作**: 手動執筆の時間的負担を大幅軽減

### 教育・学習
- **創作理論実践**: MBTI・ジャンル・物語構造理論の体験
- **段階的学習**: プロット → 執筆の体系的習得
- **品質改善技法**: 具体的改善プロセスの学習

### プロフェッショナル
- **商業企画**: 出版企画書 + 実際の原稿生成
- **編集協働**: 理論に基づく品質改善
- **教材作成**: 創作ワークショップの実用教材

## ⚠️ 注意事項

### 段階順序
- 各段階は順次完了する必要がある
- 前段階未完了時は次段階を実行できない
- validateやreviewで問題が見つかった場合は実際の修正を実行

### 技術要件
- Claude Code環境が必須
- GitHub CLI認証が必要
- 日本語での自然言語対話

## 🤝 貢献・フィードバック

このシステムは継続的に改善されています。機能リクエストやバグ報告をお待ちしています：

- GitHub Issueの作成
- プルリクエストの提出
- 使用感のフィードバック

## 📄 ライセンス

このプロジェクトは[MIT License](./LICENSE)の下で公開されています。

---

**Plot-System v2.0.0**  
**プロット構築から完成小説まで、創作者の個性を活かした一貫した創作支援を実現します。**