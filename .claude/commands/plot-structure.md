# /plot-structure コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
concept企画・世界観・キャラクター設計を基に、古典的物語理論を活用した効果的なプロット構造設計とGitHub Issue更新

## 基本構文
```bash
# 基本的な使用方法
/plot-structure {issue-number}

例:
/plot-structure 42
/plot-structure 43 --style intuitive
/plot-structure 44 --approach three-act
/plot-structure - 段階的な対話でプロット構造を設計
```

## 処理フロー

### 1. 入力理解と前段階統合処理
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- 既存要素の一貫性確認と構造設計の基盤構築
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/plot-structure/inputs/input-processing.md）

### 2. 古典的物語理論を活用した総合分析
以下の特定理論ファイルを参照して分析：

**物語構造分析**:
- **前段階の活用**: concept/setting/character段階で適用済みの構造理論を活用
- **構造要素統合**: 前段階で確立された要素を統合的に構造化
- **キャラクター機能**: 前段階で設計されたキャラクター原型・関係性を構造に反映

**創作アプローチ適用**:
- **思考パターン適用**: `writer_mbti_patterns/{type}.md` の理論を適用
- **ジャンル最適化**: `genre/{genre}.md` の理論を活用
- **最適読者層調整**: AIによる最適読者層判定に基づく構造調整

### 3. プロット構造確認・調整
AI分析結果をユーザーと共有し、shared/instructions の理論に基づいて確認：

**自然な対話による確認**:
- AI分析で特定した構造要素について自然に説明
- ユーザーの意図と一致するか確認、必要に応じて調整提案
- 固定的な質問ではなく、分析結果に応じた柔軟な対話

**理論的裏付けの共有**:
- 採用した物語構造理論の根拠を分かりやすく説明
- shared/instructions の各ファイルの知見を活用した補強提案

### 4. プロット構造書生成（最終ステップ）
指定されたテンプレートに従ってプロット構造書を作成し、プロジェクト管理を開始します。

詳細なテンプレート仕様: @.claude/docs/plot-structure/outputs/format.md

## 分析の基盤理論

以下の shared/instructions 配下の理論体系を動的に参照・適用：

### 理論ファイルの活用

#### 基盤理論による構造設計
- **hit-patterns/story-patterns.md**: 序章で「ordinary world」、転回点で「call to adventure」、クライマックスで「ordeal」の古典的配置実装
- **hit-patterns/structural-patterns.md**: setup-payoff・conflict-resolution・tension-release サイクルの効果的配置設計
- **hit-patterns/character-patterns.md**: hero・mentor・threshold guardian等の原型機能を構造的役割として配置
- **genre/{genre}.md**: ジャンル固有の構造特性と読者期待（fantasy=world-building重視、slice_of_life=character interaction重視、slapstick_comedy=setup-payoff重視）の反映
- **writer_mbti_patterns/{type}.md**: 認知機能に基づく構造アプローチ（ISFP=感情重視・ENTP=可能性探索重視）
- **audience/**: 作品に最適化された読者層の複雑度・展開速度・満足条件の調整

#### 専門構造技法の統合適用
**前段階継承技法**:
- **character_creation/** 全技法: plot-character段階で確立された心理的深度・関係性動力学を構造展開に有機的統合
- plot-character段階で設定されたMBTI原型・心理層・関係性を構造的な対立・成長・解決に自然に発展

**高度構造設計技法**:
- **structure_design/character_arc_integration.md**: キャラクター心理変化と物語進行の相互強化システム、4段階統合（確立→挑戦→変化→統合）
- **structure_design/theme_expression_design.md**: 4層テーマ統合（確立→構造統合→体験具現→多層深化）を説教的でない自然な表現で実装
- **structure_design/foreshadowing_systems.md**: 4層伏線システム（設定→構築→回収→統合管理）の戦略的配置と効果的回収設計
- **structure_design/emotional_curve_design.md**: 章ごとの感情起伏・緊張調整・クライマックス設計による読者エンゲージメント最適化

### 理論の適用
- 各プロット要素に応じて最適な理論を選択・組み合わせ
- 前段階で適用された技法の継承・発展による一貫性確保
- 理論ファイルの内容を反映
- 固定的なルールではなく、柔軟な指針として活用

詳細: 以下の理論ファイルを参照

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/plot-structure/inputs/input-processing.md

### 実装指針
- 構造設計ガイドライン: @.claude/docs/plot-structure/instructions/implementation-guide.md

### 出力仕様
- GitHub Issue・ローカルファイル: @.claude/docs/plot-structure/outputs/format.md

### 共通理論分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md

## エラーハンドリング
- 前段階ファイル不足時の対話的な情報収集
- AI分析失敗時の再試行
- プロット構造生成失敗時の代替処理
- 理論適用の一貫性チェック

## 出力
- GitHub Issue更新: （構造設計結果とプロット構造書の案内）
- ローカルファイル: `outputs/{issue_number}/output-plot-structure.md`（詳細テンプレート: @.claude/docs/plot-structure/outputs/format.md参照）

## 次のステップ
```bash
# 統合検証と最終プロット書生成
/plot-validate {issue_number}
```

---

**設計方針**: AIの自然言語理解能力を最大限活用し、古典的物語理論に基づく包括的なプロット構造分析を実現