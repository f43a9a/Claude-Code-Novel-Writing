# /plot-setting コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
concept企画を基に、ジャンル理論を活用した詳細な世界観・設定構築とGitHub Issue更新

## 基本構文
```bash
# 基本実行（AI推薦ジャンルを使用）
/plot-setting {Issue番号}

# ジャンル強制指定
/plot-setting {Issue番号} --genre fantasy
/plot-setting {Issue番号} --genre slice_of_life
/plot-setting {Issue番号} --genre slapstick_comedy

例:
/plot-setting 9
/plot-setting 9 --genre fantasy
```

## 処理フロー

### 1. 入力理解と前段階統合処理
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- 推薦ジャンル・思考パターン・魅力最大化戦略の確認
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/plot-setting/inputs/input-processing.md）

### 2. ジャンル理論を活用した総合分析（issue #48強化版）
以下の特定理論ファイルを参照して分析：

**世界観構築の判定**:
- **ジャンル特性**: `genre/` ディレクトリの各理論に基づく世界観設計
- **思考パターン対応**: `mbti_patterns/` の認知アプローチを世界構築に適用
- **魅力最大化戦略**: この世界観を最も面白くする要素の特定と強化

**設定要素分析**:
- **物語構造**: `hit-patterns/story-patterns.md` の構造理論を設定基盤に適用
- **構造要素**: `hit-patterns/structural-patterns.md` の要素理論を世界システムに活用
- **制約設計**: 各理論を総合した物語的制約の構築

**因果関係・動機の深掘り分析（issue #48重点対応）**:
- **WHY分析**: 世界観の各要素がなぜそうなっているかの背景を詳細分析
- **HOW分析**: 設定された制約や仕組みがどのように機能するかの仕組み解明
- **動機源泉の特定**: キャラクターの行動動機を自然に生む世界観要素の設計
- **因果連鎖の構築**: 一つの出来事が次の展開を必然的に生む仕組みの設計

### 3. 世界観設定の確認と補強
AI分析結果をユーザーと共有し、shared/instructions の理論に基づいて確認：

**自然な対話による確認**:
- AI分析で構築した世界観要素（基本設定、ジャンル固有要素、制約系、因果関係）について自然に説明
- ユーザーの意図と一致するか確認、必要に応じて調整提案
- 固定的な質問ではなく、構築結果に応じた柔軟な対話

**因果関係の確認と深化（issue #48対応）**:
- **動機の妥当性**: キャラクターが行動したくなる理由が世界観から自然に生まれているか確認
- **制約の論理性**: なぜその制約が存在するのか、どう機能するのかの説明と確認
- **展開の必然性**: 設定から物語展開が自然に生まれる仕組みの確認と調整

**理論的裏付けの共有**:
- 採用したジャンル理論の根拠を分かりやすく説明
- shared/instructions の各ファイルの知見を活用した設定補強提案
- WHY/HOW分析の結果と因果関係構築の理論的根拠を提示

### 4. GitHub Issue更新と管理継続（最終ステップ）
指定されたテンプレートに従ってGitHub Issueを更新し、プロジェクト管理を継続します。

詳細なテンプレート仕様: @.claude/docs/plot-setting/outputs/format.md
## 分析の基盤理論

以下の shared/instructions 配下の理論体系を参照・適用：

### 理論ファイルの活用
- **hit-patterns/**: 古典的物語理論（構造・要素・キャラクター原型）
- **genre/**: ジャンル固有の特性と手法
- **mbti_patterns/**: 認知機能に基づく創作アプローチ
- **audience/**: 読者層別の特性と期待

### 理論の適用
- 各世界観設定に応じて最適な理論を選択・組み合わせ
- 理論ファイルの内容を反映
- 固定的なルールではなく、柔軟な指針として活用

詳細: 以下の理論ファイルを参照

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/plot-setting/inputs/input-processing.md

### 実装指針
- 世界観構築実装: @.claude/docs/plot-setting/instructions/world-building.md
- ジャンル統合方法: @.claude/docs/plot-setting/instructions/genre-integration.md

### 出力仕様
- GitHub Issue更新テンプレート: @.claude/docs/plot-setting/outputs/format.md

### 共通理論分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md

## エラーハンドリング
- 入力不足時の対話的な情報収集
- AI分析失敗時の再試行
- GitHub Issue更新失敗時の代替処理
- 世界観矛盾検出時の修正提案

## 出力
- GitHub Issue更新（詳細分析と進行管理を統合）
- ローカルファイル `outputs/{issue_number}/output-plot-setting.md`（同一内容をローカル保存）

## ローカルファイル生成（issue #48強化版）
プロジェクト用ディレクトリ `outputs/{issue_number}/` にoutput-plot-setting.mdを保存：

```markdown
# 🌍 世界観設定書: {title}

**作成日**: {date}
**Issue**: #{issue_number}
**ステータス**: setting完了

## 🎭 ジャンル特性適用
{ジャンル理論に基づく世界観分析}

## 🏛️ 基本設定
{時代・場所・環境・社会システムの詳細}

## 🔗 因果関係・世界の仕組み
{重要な出来事の因果構造・行動と結果の法則・キャラクター動機の源泉}

## ⚖️ 制約・ルール
{物理的・社会的・システム的制約とその背景・WHY/HOW}

## 🎯 物語への影響
{主人公の行動制約と動機・葛藤の源と発展・成長の機会と障害・予想される展開パターン}

## 📚 理論的根拠
{適用した古典的理論の説明・WHY/HOW分析結果}

```


---

**設計方針**: AIの自然言語理解能力を最大限活用し、ジャンル理論に基づく包括的な世界観設定分析を実現