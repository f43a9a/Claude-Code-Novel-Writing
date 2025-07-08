# /plot-validate コマンド定義

## コマンド概要
**あなたは経験豊富な小説編集者として、以下のタスクを実行してください：**
全段階(concept/setting/character/structure)の統合検証と一貫性確認を実施し、最終プロット書生成とGitHub Issue更新

## 基本構文
```bash
# 基本的な使用方法
/plot-validate {issue-number}

例:
/plot-validate 42
/plot-validate 43 --detail comprehensive
/plot-validate 44 --format complete
/plot-validate - 段階的な対話で統合検証を実施
```

## 処理フロー（改善版）

### 1. 基礎品質確認と Critical Fix
- GitHub Issue #{issue-number} 全体の読み込みと統合分析
- **論理的矛盾・設定不整合の特定と修正**：従来の形式的チェックではなく実用的問題の発見
- **執筆実現可能性の検証**：文字数制約・技術的困難度・描写の具体性確認
- 重大な問題がある場合は**具体的修正版を生成**（詳細: 編集的レビュー理論を必要に応じて参照critical-improvement-techniques.md）

### 2. 統合品質改善システムの適用
`@.claude/docs/shared/quality-improvement-system.md` の3段階改善システムを全段階統合検証に適用：

**適用方法**:
- **Critical Fix**: 全段階統合時の論理矛盾・設定不整合の修正
- **Quality Enhancement**: 統合プロット書の読者体験最適化  
- **Appeal Amplification**: 最終プロット書の独自性・魅力強化

詳細な改善手法: @.claude/docs/shared/quality-improvement-system.md

### 3. 統合検証と改善案生成

### 4. 改善案の生成と検証完了
統合分析に基づく具体的な改善提案と最終検証：

**段階的改善案の生成**:
- 🔴 Critical Fix: 論理矛盾・執筆不可能な設定の改善案提示
- 🟡 Quality Enhancement: 読者体験向上のための具体的改善案  
- 🟢 Appeal Amplification: さらなる魅力拡張の提案（ユーザー選択制）

**統合検証書の生成**:
- 改善案を含む詳細な検証結果の記録
- 品質評価と推奨事項の明確化
- 最終プロット統合版としての検証完了

**注意**: validateステップ自体は既存ファイルを修正せず、改善案の提示と統合検証が主目的です。実際の修正はユーザーの判断で個別に実行してください。

詳細な改善手法: @.claude/docs/shared/instructions/editorial_review/critical-improvement-techniques.md

## 新しい評価基準（改善版）

### 3段階品質評価システム
従来のA/B/C/D評価から実用的改善指向へ変更：

**基本完成度（必須要件）**:
- ✅ 執筆開始可能レベル
- ⚠️ 軽微な修正推奨  
- ❌ 重大な問題あり（Critical Fix必要）

**読者魅力度（品質向上）**:
- 🌟🌟🌟 非常に魅力的（そのまま執筆推奨）
- 🌟🌟 十分魅力的（軽微な向上案あり）
- 🌟 改善の余地あり（Quality Enhancement推奨）

**市場競争力（発展性）**:
- 🏆 独創性が高く差別化できる
- 📈 標準的だが魅力がある  
- 📊 ありがちだが悪くない（Appeal Amplification検討）

### 改善提案の分類
**🔴 Critical Fix（修正必須）**:
- 論理的矛盾の解消
- 明らかな設定の不整合
- 執筆不可能な構造的問題

**🟡 Quality Enhancement（品質向上）**:
- 読者の感情移入強化
- シーンの臨場感向上
- キャラクターの魅力増加

**🟢 Appeal Amplification（魅力拡張）**:
- 独創性の強化
- 市場差別化の向上
- 文学的価値の追加

### 理論体系の実用的活用
shared/instructions配下の理論を改善提案生成に活用：

#### 編集技法による専門的検証
- **editorial_review/critical-improvement-techniques.md**: 4段階改善システム（Critical Fix→Quality Enhancement→Appeal Amplification→統合調整）の体系的適用
- **editorial_review/plot-consistency-validation.md**: 4層論理検証（基盤論理・因果関係・時間整合性・情報一貫性）による構造的問題検出
- **editorial_review/character-authenticity-review.md**: 4層真正性検証（心理的・行動的・社会的・発達的リアリズム）によるキャラクター問題特定
- **editorial_review/reader-experience-analysis.md**: 読者体験シミュレーションによる感情移入・理解度・満足度の具体的評価
- **editorial_review/professional-editorial-standards.md**: 品質基準による評価と改善方針策定

#### 横断的理論による統合検証
**前段階理論の継承・検証**:
- **character_creation/** 全技法: plot-character段階で適用された心理的深度・関係性動力学・個性設計の一貫性維持確認
- **structure_design/** 全技法: plot-structure段階で設計されたアーク統合・テーマ表現・伏線システム・感情カーブの実装品質評価

**基盤理論による最終確認**:
- **前段階成果物**: 全段階で適用された理論の統合確認・最適化
- **genre/{genre}.md**: ジャンル読者の期待値との照合と差別化提案、WHY/HOW分析による深化可能性評価
- **writer_mbti_patterns/{type}.md**: 創作アプローチの一貫性と独自性強化、認知機能の効果的活用状況確認
- **audience/**: 作品に最適化された読者層への訴求力最大化、語彙・内容・構造の適切性評価
- **character_mbti_patterns/{type}.md**: 設定されたMBTI原型の自然で魅力的な表現、認知機能の一貫した反映確認

詳細: 編集的レビュー理論を必要に応じて参照

**重要**: validateコマンド実行時は必ず上記editorial_reviewディレクトリ内の全ての改善技法ファイルを参照・適用してください

## 関連ドキュメント

### 入力処理
- 入力処理と対話指針: @.claude/docs/plot-validate/inputs/input-processing.md

### 実装指針
- 統合検証ガイドライン: @.claude/docs/shared/instructions/editorial_review/professional-editorial-standards.md

### 出力仕様
- GitHub Issue・ローカルファイル: @.claude/docs/plot-validate/outputs/format.md

### 共通理論分析
- 物語構造: @.claude/docs/shared/instructions/hit-patterns/story-patterns.md
- 構造要素: @.claude/docs/shared/instructions/hit-patterns/structural-patterns.md
- キャラクター原型: @.claude/docs/shared/instructions/hit-patterns/character-patterns.md

## エラーハンドリング
- 前段階ファイル不足時の対話的な情報収集
- AI分析失敗時の再試行
- 最終プロット書生成失敗時の代替処理
- 統合検証の一貫性チェック

## 出力
- GitHub Issue更新: （統合検証結果と最終プロット書の案内）
- ローカルファイル: `outputs/{issue_number}/output-plot-validate.md`（統合検証詳細レポート）
- 最終成果物: `outputs/{issue_number}/plot_complete.md`（GitHub Issue更新と同一内容をローカル保存）

## GitHub Issue・ローカルファイル共通フォーマット
GitHub Issue更新とローカルファイルどちらにもGitHub Issue・ローカルファイル共通テンプレート（@.claude/docs/plot-validate/outputs/format.md）と完全に同じ詳細内容を出力：

```markdown
# 📚 統合検証・最終プロット書: {title}

**作成日**: {date}
**Issue**: #{issue_number}
**ステータス**: validate完了
**前段階**: concept.md, setting.md, character.md, structure.md

---

## ✅ 統合検証結果

### 全体整合性
{全段階の一貫性分析結果}

### 要素統合評価
{各要素間の調和確認結果}

### 品質評価
{理論に基づく最終品質評価}

## 📖 最終プロット書

### 作品概要
{企画から構造まで統合した作品概要}

### 詳細設計
{執筆に使用可能な詳細プロット}

### 理論的根拠
{適用した全理論の統合説明}

## 🎯 推奨改善点
{発見された改善提案がある場合}

```


---

**設計方針**: 従来の「理論チェックで終わり」から「具体的改善案の提示」アプローチへ転換。読者体験重視の実用的品質向上提案と統合検証による真の価値創出を実現