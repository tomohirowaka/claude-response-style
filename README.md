# claude-response-style

LLM/AI チャット応答を**読みやすく・認知負荷を下げる**ためのスタイルルール集。

## なぜこのリポジトリ？

ChatGPT・Claude などの AI 応答は、放っておくと装飾過多になりがち。表・太字・絵文字・行頭マークを多用した「見た目は整って見えるが読みづらい」応答は、**外在的認知負荷（Sweller の Cognitive Load Theory）** を上げてしまう。

世界の研究と実務知見を横断すると、共通解は **"the minimum necessary structure"（最小限の構造で目的を達成する）** に収束する。このリポはその知見を、AI に与えるシステムプロンプト・スタイルガイドとして使える形に整理したもの。

## 使い方

### 1. システムプロンプト／グローバル CLAUDE.md に取り込む

```bash
git clone https://github.com/tomohirowaka/claude-response-style.git
```

`RULES.md` の内容を、Claude Code の `~/.claude/CLAUDE.md` や ChatGPT の Custom Instructions に貼り付ける、または参照リンクを置く。

### 2. プロジェクト単位で参照する

プロジェクトの `CLAUDE.md` に1行入れる:

```markdown
## Response Formatting
詳細は https://github.com/tomohirowaka/claude-response-style/blob/main/RULES.md を参照。
```

### 3. チーム共有のスタイルガイドとして使う

Collaborator 招待や Fork で自分たちの組織用に拡張してもよい。MIT ライセンスなので自由に改変・配布できる。

## ファイル構成

| ファイル | 内容 |
|---------|------|
| [RULES.md](./RULES.md) | スタイルルール本体（日本語・SSoT） |
| [RULES.en.md](./RULES.en.md) | English version |
| [docs/research/](./docs/research/) | ルール策定の根拠となる調査レポート |
| [CHANGELOG.md](./CHANGELOG.md) | 改訂履歴 |
| LICENSE | MIT |

## 出典（主要）

- Anthropic — [Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices), [Best practices for prompt engineering](https://claude.com/blog/best-practices-for-prompt-engineering)
- Google — [Developer Documentation Style Guide](https://developers.google.com/style)
- Microsoft — [Style Guide](https://learn.microsoft.com/en-us/style-guide/welcome/)
- Nielsen Norman Group — [Less Chat, More Answer](https://www.nngroup.com/articles/less-chat-more-answer/)
- 木下是雄『理科系の作文技術』中公新書、1981
- 出入国在留管理庁・文化庁 — [在留支援のためのやさしい日本語ガイドライン](https://www.moj.go.jp/isa/support/portal/plainjapanese_guideline.html)
- Cowan (2001) 4±1 / Miller (1956) 7±2 — 作動記憶の古典説

詳細は [docs/research/](./docs/research/) を参照。

## ライセンス

MIT License — 自由に使ってね。改変・再配布も歓迎。
