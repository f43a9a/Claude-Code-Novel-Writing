# /conte コマンド定義

## コマンド概要
**あなたは経験豊富な映像監督・小説演出家として、以下のタスクを実行してください：**
plot構造設計を基に、映像的絵コンテ理論を活用した詳細なシーン演出設計とGitHub Issue更新

## 基本構文
```bash
# 基本的な使用方法
/conte {issue-number}

例:
/conte 42
/conte 43 --style cinematic
/conte 44 --focus emotional
/conte - 段階的な対話でシーン演出を設計
```

## 処理フロー

### 1. 入力理解と前段階統合処理
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- 各シーン・章・場面の構造的把握と演出ポイント特定
- 不足情報がある場合は自然な対話で補完（詳細: @.claude/docs/conte/inputs/input-processing.md）

### 2. 映像理論を活用した総合シーン分析
以下の特定理論ファイルを参照して分析：

**演出技法分析**:
- **映像コンテ理論**: `conte_techniques/visual-storytelling.md` の理論に基づく分析
- **描写技法**: `conte_techniques/descriptive-methods.md` の技法を適用
- **感情演出**: `conte_techniques/emotional-direction.md` の理論を参考に判定

**創作アプローチ適用**:
- **思考パターン適用**: `writer_mbti_patterns/{type}.md` の理論を演出に反映
- **ジャンル最適化**: `genre/{genre}.md` の理論を視覚的演出に活用
- **最適読者層調整**: AIによる最適読者層判定に基づく演出調整

### 3. シーン演出確認・調整
AI分析結果をユーザーと共有し、shared/instructions の理論に基づいて確認：

**自然な対話による確認**:
- AI分析で特定した演出要素について自然に説明
- ユーザーの意図と一致するか確認、必要に応じて調整提案
- 固定的な質問ではなく、分析結果に応じた柔軟な対話

**理論的裏付けの共有**:
- 採用した映像演出理論の根拠を分かりやすく説明
- shared/instructions の各ファイルの知見を活用した補強提案

### 4. 絵コンテ書生成（最終ステップ）
指定されたテンプレートに従って詳細な絵コンテ書を作成し、プロジェクト管理を開始します。

詳細なテンプレート仕様: @.claude/docs/conte/outputs/format.md

## 分析の基盤理論

以下の shared/instructions 配下の理論体系を動的に参照・適用：

### 理論ファイルの活用

#### 映像演出専門技法
- **conte_techniques/visual-storytelling.md**: 映像的絵コンテ理論による場面構成・視点・カット割り的な描写展開
- **conte_techniques/descriptive-methods.md**: 感覚的描写・空間描写・時間描写の具体的技法適用
- **conte_techniques/emotional-direction.md**: 感情演出・トーン・リズム・視点による読者体験設計

#### 前段階理論の継承・演出活用
**キャラクター表現の一貫性維持**:
- **character_creation/** 全技法: plot-character段階で確立された心理的深度・個性・関係性を演出表現に自然に反映
- **character_mbti_patterns/{type}.md**: 設定されたMBTI原型の認知機能を行動・反応・対話の演出に一貫して表現

**構造演出の効果的実装**:
- **structure_design/** 全技法: plot-structure段階で設計されたアーク・テーマ・伏線・感情カーブを視覚的演出に具体化
- **structure_design/emotional_curve_design.md**: 章ごとの感情設計を映像的緊張・緩和・クライマックス演出に変換

#### 基盤理論による演出最適化
- **genre/{genre}.md**: ジャンル固有の演出特性と読者期待（fantasy=壮大さ・slice_of_life=親密さ・slapstick_comedy=スピード感）の視覚的表現
- **writer_mbti_patterns/{type}.md**: 認知機能に基づく演出アプローチ（ISFP=感情重視・ENTP=可能性探索重視）
- **audience/{audience}.md**: 読者層別の演出期待（young_adult=分かりやすさ・adult=複雑さ）と効果

### 理論の適用
- 各シーン要素に応じて最適な演出理論を選択・組み合わせ
- 前段階で確立された理論要素の継承・発展による一貫性確保
- 理論ファイルの内容を反映
- 固定的なルールではなく、柔軟な指針として活用

詳細: 以下の理論ファイルを参照

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/conte/inputs/input-processing.md

### 実装指針
- 演出設計ガイドライン: @.claude/docs/conte/instructions/implementation-guide.md

### 出力仕様
- GitHub Issue・ローカルファイル: @.claude/docs/conte/outputs/format.md

### 演出理論分析
- 映像的語り: @.claude/docs/shared/instructions/conte_techniques/visual-storytelling.md
- 描写技法: @.claude/docs/shared/instructions/conte_techniques/descriptive-methods.md
- 感情演出: @.claude/docs/shared/instructions/conte_techniques/emotional-direction.md

## エラーハンドリング
- 前段階ファイル不足時の対話的な情報収集
- AI分析失敗時の再試行
- 絵コンテ生成失敗時の代替処理
- 演出理論適用の一貫性チェック

## 出力
- GitHub Issue更新: （絵コンテ分析結果と次段階への案内）
- ローカルファイル: `outputs/{issue_number}/output-conte.md`（GitHub Issue更新と同一内容をローカル保存）

## GitHub Issue・ローカルファイル共通フォーマット
GitHub Issue更新とローカルファイルどちらにもGitHub Issue・ローカルファイル共通テンプレート（@.claude/docs/conte/outputs/format.md）と完全に同じ詳細内容を出力：

```markdown
# 絵コンテ設計書: {title}

**作成日**: {date}
**Issue**: #{issue_number}
**ステータス**: conte完了
**前段階**: structure.md

---

## 🎬 シーン構成・全体設計

### 章・シーン分割
{プロット構造に基づく詳細なシーン分割}

### 全体演出方針
{映像的な全体演出・トーン・リズム方針}

## 🎭 詳細シーン絵コンテ

### SCENE-01: {scene_title}
**シーン目的**: {scene_purpose}
**全景**: {setting_and_staging}
**カット進行**: {detailed_cut_progression}
**描写重点**: {focus_areas}
**描写比率指針**: {percentage_guidelines}
**トーン・視点**: {tone_and_perspective}

[他のシーンも同様の形式で...]

## 📈 感情カーブ・緩急設計
{シーン間の感情的起伏・テンポ・リズム設計}

## 🎨 描写技法・演出指針
{具体的な描写技法・レトリック・表現方法}

## 📚 理論的根拠

### 映像演出理論適用
{適用した映像・絵コンテ理論}

### MBTI思考パターン反映
{思考パターンの演出への反映}

### ジャンル・読者層調整
{ジャンルと読者層に基づく演出調整}

```


---

**設計方針**: 映像的絵コンテ理論とAIの自然言語理解能力を融合し、「のっぺりしない」魅力的で緩急のある小説演出の実現