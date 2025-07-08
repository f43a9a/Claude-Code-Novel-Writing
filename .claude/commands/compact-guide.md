# コンパクト機能活用ガイド

## 基本的な使用方法

### 自動コンパクト
- コンテキストが95%に達した時点で自動実行
- 環境変数 `CLAUDE_CODE_AUTO_COMPACT=1` で有効化済み

### 手動コンパクト
```bash
# 基本的なコンパクト
/compact

# 特定のフォーカスでコンパクト
/compact Focus on code samples and API usage
/compact Focus on plot structure and character analysis
/compact Focus on recent changes and current task

# 履歴のクリア
/clear
```

## 戦略的活用

### タスク完了時のコンパクト
各段階完了時に実行:
```bash
# plot-concept完了後
/compact Focus on concept analysis results and character basics

# plot-structure完了後  
/compact Focus on plot structure and character arcs

# writing-generate完了後
/compact Focus on completed novel and key improvements needed
```

### 大きなタスク間でのリセット
```bash
# 新しいプロジェクト開始前
/clear

# 段階移行時
/compact Focus on essential information for next phase
```

## 使用するタイミング

1. **各段階完了時**: 不要な分析過程を削除
2. **エラー発生時**: 問題解決に集中
3. **新機能実装前**: コンテキストをクリーンに
4. **定期的**: 長時間作業時の効率維持

## コンパクト指示のテンプレート

### プロット段階用
- `Focus on plot structure, character development, and world-building details`
- `Focus on story conflicts, character arcs, and thematic elements`
- `Focus on scene structure, pacing, and emotional beats`

### 執筆段階用
- `Focus on writing quality, character voice, and narrative flow`
- `Focus on dialogue, descriptions, and scene transitions`
- `Focus on completed sections and revision notes`

### 技術的問題解決用
- `Focus on error messages, debugging steps, and solutions`
- `Focus on code changes, implementation details, and testing results`
- `Focus on current technical issue and resolution attempts`