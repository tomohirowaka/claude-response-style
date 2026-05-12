# Changelog

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
