# CIO Memory

## データソース確認済み
- ダッシュボードのフルフロー（load_data_from_sheets→バナーCSV→タグ補完→prepare_data）が正
- funnel_summary = PU経由のみ（バナー除外）
- summary = SEO全体（PU+バナー+ボタン）
- analysis_engine単体はタグ補完が抜けるので過少

## 異常検知パターン
- PU CTR 1%台 → 計算式バグ（正常は13%）
- CTR高×FR低 → LP遷移先URL間違いの可能性
- リカバリーウェア: CTR 21.86% vs FR 2.87% → 構造的問題

## 教訓
- find_missing_tags → overrideの処理順序は絶対
- 3日データ÷3×31で月間換算はNG → 前月ベースラインで
- summary/funnel_summaryの混在禁止（定義が違う）
