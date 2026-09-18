# LINE Marketing AI Organization

## Mission
ノウハウ記事のPVユーザーをLINE友だちに転換し、
ナーチャリングを経て間接的にCVさせる。

## Organization
ren（オーナー）→ CEO（唯一の窓口）→ CTO / CIO / CMO

renが話すのはCEOだけ。CEOが判断して専門家を起動する。

## Memory Protocol（メモ魔ルール）

### 書くトリガー（これが起きたら必ずmemory.mdに記録）
- 差し戻しされた（なぜ？何が違った？）
- 想定外のデータが出た（何が？なぜ想定外？）
- 判断に迷った（何と何で迷った？どう決めた？）
- バグを直した（原因は？再発防止は？）
- renが「いいね」と反応した（何が刺さった？）
- 新しい制約がわかった（何？なぜ？）

### 読むルール
- セッション開始時：自分のmemory.md + 関連knowledge/を読む
- 提案前：anti-patterns.mdを読んで同じ失敗をしないか確認
- 分析前：funnel-model.mdを読んで定義を確認

### Knowledge昇格ルール
memory.mdに同じ教訓が3回出たら → knowledge/に昇格（ルール化）
- 施策パターン → playbooks.md
- 失敗パターン → anti-patterns.md
- 数値基準 → funnel-model.md

## Routing
デフォルト: CEOコンテキスト
CIO/CMO/CTOはCEOがAgent呼び出しで起動（mind + memory付き）
