# /plot-character コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
concept企画・世界観設定を基に、キャラクター原型理論を活用した魅力的なキャラクター設計とGitHub Issue更新

## 基本構文
```bash
# 基本実行（AI推薦アプローチを使用）
/plot-character {Issue番号}

# アプローチ強制指定
/plot-character {Issue番号} --approach relationship
/plot-character {Issue番号} --approach individual
/plot-character {Issue番号} --approach ensemble

例:
/plot-character 9
/plot-character 9 --approach relationship
```

## 処理フロー

### 1. 入力理解と前段階統合処理
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- 推薦構成（ジャンル・思考パターン・作品魅力最大化戦略）と世界観設定の確認
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/plot-character/inputs/input-processing.md）

### 2. プロフェッショナル・キャラクター創作技法を活用した総合分析
以下の特定理論ファイルを参照して分析：

**プロフェッショナル・キャラクター創作技法の適用**:
- **基盤技法統合**: `character_creation/character-foundation.md` の5段階統合システム（プロファイリング・心理・動機設計）
- **表現技法統合**: `character_creation/character-expression.md` の5層表現システム（音声・外見・関係性・統合戦略）

**前段階理論との統合**:
- **キャラクター原型**: 前段階で適用済みの原型理論を詳細プロファイリングに活用
- **MBTI原型活用**: `character_mbti_patterns/` の16種類原型を詳細プロファイリングに統合
- **ジャンル特性反映**: `genre/` ディレクトリの理論を外見・音声設計に活用（slapstick_comedy含む）
- **読者共感設計**: AIによる最適読者層判定を動機・関係性設計に反映

### 3. プロフェッショナル・レベルのキャラクター設計確認と補強
AI分析結果をユーザーと共有し、character_creation技法とshared/instructions理論に基づいて確認：

**商業作品レベルの設計確認**:
- **7段階詳細プロファイリング**: 基本情報から統合戦略まで各段階の設計結果を自然に説明
- **5層心理構造**: 認知・感情・防衛・発達・無意識層の統合的心理設計の妥当性確認  
- **関係性ダイナミクス**: 6層関係性設計による魅力的人間関係の構築確認
- **動機・目標システム**: 5層動機構造による説得力ある行動原理の確認
- **口調・話法設計**: キャラクター固有の話し方・語尾・決まり文句の詳細設計確認

**統合的品質確保**:
- **一貫性チェック**: 各要素間の論理的整合性・矛盾回避の確認
- **読者魅力度**: 商業作品として求められる魅力・共感度の最適化
- **成長可能性**: 物語展開での発展・深化への拡張性確保
- **プロフェッショナル基準**: 出版業界レベルでの品質基準達成確認

### 4. GitHub Issue更新と管理継続（最終ステップ）
指定されたテンプレートに従ってGitHub Issueを更新し、プロジェクト管理を継続します。

詳細なテンプレート仕様: @.claude/docs/plot-character/outputs/format.md

## 分析の基盤理論

以下の shared/instructions 配下の理論体系を動的に参照・適用：

### プロフェッショナル・キャラクター創作技法
- **character_creation/**: 商業作品レベルの専門的キャラクター創作手法
  - character-foundation.md: 5段階統合システム（プロファイリング・心理・動機設計）
  - character-expression.md: 5層表現システム（音声・外見・関係性・統合戦略）

### 従来理論ファイルの統合活用
- **hit-patterns/**: 古典的物語理論（構造・要素・キャラクター原型）
- **character_mbti_patterns/**: 16種類キャラクターMBTI原型との統合
- **genre/**: ジャンル固有の特性と手法
- **writer_mbti_patterns/**: 認知機能に基づく創作アプローチ
- **audience/**: 作品に最適化された読者層特性と期待

### 統合技法の適用
- 各キャラクター設計に応じて最適な技法・理論を選択・組み合わせ
- プロフェッショナル技法と従来理論の有機的統合
- 商業作品として求められる品質基準の確保
- 固定的なルールではなく、創造的・柔軟な指針として活用

詳細: 以下の理論ファイルを参照

## 関連ドキュメント

### プロフェッショナル・キャラクター創作技法
- 基盤技法統合: @.claude/docs/shared/instructions/character_creation/character-foundation.md
- 表現技法統合: @.claude/docs/shared/instructions/character_creation/character-expression.md

### 入力処理
- 入力処理と対話指針: @.claude/docs/plot-character/inputs/input-processing.md

### 出力仕様
- GitHub Issue更新テンプレート: @.claude/docs/plot-character/outputs/format.md

### 従来理論分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md
- キャラクターMBTI原型: 設定されたMBTIタイプのみ参照

## エラーハンドリング
- 入力不足時の対話的な情報収集
- AI分析失敗時の再試行
- GitHub Issue更新失敗時の代替処理
- キャラクター設定矛盾検出時の修正提案

## 出力
- GitHub Issue更新（詳細分析と進行管理を統合）
- ローカルファイル `outputs/{issue_number}/output-plot-character.md`（GitHub Issue更新と同一内容をローカル保存）

## GitHub Issue・ローカルファイル共通フォーマット
GitHub Issue更新とローカルファイルどちらにもGitHub Issue・ローカルファイル共通テンプレート（@.claude/docs/plot-character/outputs/format.md）と完全に同じ詳細内容を出力：

```markdown
# 🎭 キャラクター設計書: {title}

**作成日**: {date}
**Issue**: #{issue_number}
**ステータス**: character完了
**前段階**: concept.md, setting.md

---

## 👥 主要キャラクター設計

### 主人公: {protagonist_name}
{主人公の詳細設計}

### 重要人物: {key_character_name}
{重要人物の詳細設計}

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

### 作品魅力最大化戦略
{audience_consideration}

```


---

**設計方針**: AIの自然言語理解能力を最大限活用し、プロフェッショナル・キャラクター創作技法と従来理論の統合により、商業出版レベルの包括的で魅力的なキャラクター設計を実現