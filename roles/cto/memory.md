# CTO メモリ

## Winutデータ収集システム — 構成詳細

### BigQuery テーブル構成
ソース（winut_function_v2）:
- accounts — アカウント情報
- linefriends — LINE追加ユーザーデータ
- measurements — 離脱タグデータ

データマート（popup_mart_v3）:
- daily_data — 日次×離脱タグ別の基本指標
- account_sum_answer — 日次×設問別の回答数
- daily_user_log — 日次×シナリオのステップ通過率

### 運用手順
アカウント追加: BQ SQLでINSERT（id連番、重複厳禁）
ジャンル追加: スケジュールドクエリのSQL追記

## Star Office — 既知の問題
- Flask dev server長時間稼働→静的ファイル500エラー（再起動で復旧）
- macOS TCC制限でtasks.json読めない問題あり（未解決）

## 環境の落とし穴
- Python 3.9.6: from __future__ import annotations 必須
- Streamlit Cloud: Python 3.13強制、numpy>=2.1.0必須
- GitHubパス制限: ":" を含むファイルパスはpush不可
- google-generativeai は deprecated → google-genai を使え
