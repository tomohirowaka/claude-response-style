# Changelog

## [1.4.0] - 2026-07-22

### Changed

- 公開・送付・レビュー前に、固有名、役職、日付、曜日、数値、URLを一次情報または案件の承認資料と照合するルールを追加
- 公式情報が競合する場合は推測で統合せず、役割を分けるか未確認として止める境界を追加
- Google Docs、メール、Web画面では入力値ではなく、読者に見える最終表示を確認するルールを追加
- 最終読解で、主体、見出しと本文の一致、同義反復を確認するゲートを追加
- `RULES.md` / `RULES.en.md` を同期

## [1.3.0] - 2026-07-21

### Changed

- 対象をチャット応答から、メール、資料、マニュアル、記事を含む AI 生成文全般へ拡張
- **§2 Specificity, Rhythm & Voice** を追加。事実保持、抽象語の具体化、意味に従うリズム、文体見本、AI 定型の点検を明文化
- AI 検出器の回避や機械的な文長比率を目的にせず、正確さ、具体性、読みやすさを判断基準に設定
- 医療・法務・技術仕様・承認済み定型文など、均一性と正確さが優先される用途の例外を追加
- 能動態優先の既存例を修正し、「〜と考えられる」など確度を示す留保を断定へ変えない境界を追加
- `RULES.md` / `RULES.en.md` を同期し、採用・不採用の判断根拠を調査メモに記録

## [1.2.0] - 2026-05-12

### Changed

- **§2 Visual Structure**: 引用ブロックの記号を `>` で統一すること、`▎`・`｜` などの代用記号を使わないことを明示
- **§2 Visual Structure**: 「箇条書きの記号」サブセクションを新設。`-` で統一、`・` や `*` と混在させないルールを追記

実運用で `▎` を使うケースと `・`・`-` の混在が観察されたため、v1.2 で記号を明示的に統一。

## [1.1.0] - 2026-05-12

### Changed

- **Emphasis section**: 「太字 3 箇所まで」を「**上限であって目標ではない**」と明示。実テストで太字ゼロに振れすぎる挙動が観察されたため、強調が要る場面では使うべきという判断基準を追記。RULES.md / RULES.en.md 両方を更新

## [1.0.0] - 2026-05-12

### Added

- 初版リリース（Initial release）
- `RULES.md` — 日本語 SSoT、7 セクション構成（Core Principle / Sentence & Paragraph / Visual Structure / Emphasis / Response Flow / What to Cut / Code Examples / Japanese-Specific Rules）
- `RULES.en.md` — English version
- `docs/research/2026-05-12-ai-response-cognitive-load.md` — 根拠調査レポート（28 ソース、Anthropic / Google / Microsoft / NN/G / 木下 / やさしい日本語）
- `README.md` — リポ概要・使い方
- MIT License
