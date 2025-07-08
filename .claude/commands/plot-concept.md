# /plot-concept コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
小説アイデアを分析し、hit-patterns理論を活用したAI判断による最適な構成の決定

## 基本構文
```bash
# 自然言語での入力に対応
/plot-concept {あなたの小説アイデア}

例:
/plot-concept 海を舞台にしたファンタジー作品を作りたいです
/plot-concept 高校生の日常を描く恋愛もの
/plot-concept [URL] - 参考記事から企画
/plot-concept [ファイルパス] - 既存ファイルから企画
/plot-concept - 対話形式で企画作成
```

## 処理フロー

### 1. 入力理解と対話による情報収集
- 自然言語入力から企画の要素を理解
- 明確に含まれる情報（世界観、主人公、読者層等）を把握
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/plot-concept/inputs/input-processing.md）

### 2. hit-patterns理論を活用した総合分析
以下の特定理論ファイルを参照して分析：

**基本構成の判定**:
- **ジャンル**: `genre/` ディレクトリの各理論に基づく柔軟判断（fantasy, slice_of_life, slapstick_comedy等）
- **思考パターン**: `mbti_patterns/` の認知アプローチ理論を適用
- **作品魅力最大化**: この作品を最も面白くする要素の特定と戦略設計

**ヒット要素分析**:
- **物語構造**: `hit-patterns/story-patterns.md` の古典的パターン理論を適用（コメディ向けには `hit-patterns/comedy-patterns.md` も参照）
- **構造要素**: `hit-patterns/structural-patterns.md` の要素理論を活用
- **キャラクター原型**: `hit-patterns/character-patterns.md` のアーキタイプ理論を参照（コメディ向けには `hit-patterns/slapstick-archetypes.md` も参照）
- **市場差別化**: 各理論を総合した独自性分析

### 3. ヒット要素の確認と補強
AI分析結果をユーザーと共有し、shared/instructions の理論に基づいて確認：

**自然な対話による確認**:
- AI分析で特定した各要素（ジャンル、パターン、魅力最大化戦略、ヒット要素）について自然に説明
- ユーザーの意図と一致するか確認、必要に応じて調整提案
- 固定的な質問ではなく、分析結果に応じた柔軟な対話

**理論的裏付けの共有**:
- 採用した古典的理論の根拠を分かりやすく説明
- shared/instructions の各ファイルの知見を活用した補強提案

### 4. ローカルファイル保存（最終ステップ）
指定されたテンプレートに従ってローカルファイルとして分析結果を保存します。

詳細なテンプレート仕様: @.claude/docs/plot-concept/outputs/format.md

## 分析の基盤理論

以下の shared/instructions 配下の理論体系を参照・適用：

### 理論ファイルの活用
- **hit-patterns/**: 古典的物語理論（構造・要素・キャラクター原型）
- **genre/**: ジャンル固有の特性と手法
- **mbti_patterns/**: 認知機能に基づく創作アプローチ
- **作品魅力最大化分析**: AIによる最適読者層判定と面白さ要素強化戦略

### 理論の適用
- 各企画に応じて最適な理論を選択・組み合わせ
- 理論ファイルの内容を反映
- 固定的なルールではなく、柔軟な指針として活用

詳細: 以下の理論ファイルを参照

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/plot-concept/inputs/input-processing.md

### 出力仕様
- GitHub Issue テンプレート: @.claude/docs/plot-concept/outputs/format.md

### ヒットパターン分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md

## エラーハンドリング
- 入力不足時の対話的な情報収集
- AI分析失敗時の再試行
- ファイル保存失敗時の代替処理

## 出力
- ローカルファイル `outputs/{unique_id}/output-plot-concept.md`（分析結果のローカル保存）

## ローカルファイルフォーマット
ローカルファイルに保存するテンプレート（@.claude/docs/plot-concept/outputs/format.md）に従った詳細内容：

```markdown
# 📋 プロット構築プロジェクト: {title}

## 基本情報
- **タイトル**: {title}
- **ジャンル**: {genre}
- **思考パターン**: {mbti_pattern}
- **読者層**: {audience}
- **推定文字数**: {recommended_length}

## AI判断理由

### ジャンル: {genre}
{genre_reason}

### 思考パターン: {mbti_pattern}
{mbti_reason}

### 読者層: {audience}
{audience_reason}

## 🎯 ヒット要素分析

### コアとなる魅力
{hit_elements の詳細展開}

### 古典的理論との関係
- **物語構造**: {story_patterns}
- **キャラクター原型**: {character_archetypes}
- **市場差別化**: {market_differentiation}

## 📚 参考となる古典的パターン

### 物語構造の応用
{classical_structure_applications}

### キャラクター原型の活用
{character_archetype_applications}

## 全体印象
{overall_impression}

```


---

**設計方針**: AIの自然言語理解能力を最大限活用し、hit-patterns理論に基づく包括的な企画分析を実現