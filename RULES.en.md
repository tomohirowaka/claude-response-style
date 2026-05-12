# Response Style Rules

Style rules for LLM/AI chat responses — reduce cognitive load and improve readability.

## Core Principle: Minimum Necessary Structure

Choose the **minimum necessary structure** to achieve your goal. Adding decoration does not strengthen information transfer; it adds visual noise and raises extraneous cognitive load.

> Reserve markdown primarily for inline code, code blocks, and simple headings. — Anthropic

## 1. Sentence & Paragraph

- **One sentence per claim**; keep sentences short
- **Paragraphs should be 2–3 sentences or fewer** (NN/G)
- **One topic per paragraph**, with the topic sentence at or near the beginning (Kinoshita, *Riika-kei no Sakubun Gijutsu*)
- Prefer **active voice** over passive

## 2. Visual Structure

### Tables

- Use **only for two-dimensional data with three or more related items** (Google)
- Do not use for: single rows, single columns, code snippet placement, one-dimensional long lists, or in the middle of numbered procedures
- At most one table per message

### Lists

- Use **only for truly discrete items**; do not make it the default (Anthropic)
- Maintain parallel structure (noun phrases with noun phrases; verb phrases with verb phrases)
- Numbered lists should begin with imperative verbs (Google)

### Headings

- Use parallel structure (Microsoft)
- Use level 2 headings **only when there are two or more distinct topics**
- For content of 1–2 pages, one heading level is usually plenty

### Blockquotes (`>`)

- Use for proposed text, messages to be sent, or quotations from others
- Using blockquotes instead of code blocks for prose reduces visual noise

## 3. Emphasis

- **Bold**: at most 3 instances per message
- **Emoji**: do not over-use. What feels like visual cueing becomes color overload. Anthropic explicitly documents "fewer emoji" for Claude Opus 4.7
- **Leading priority markers (🔴🟡✅)**: avoid them when there are only 2–3 items — prose can convey priority just as well

## 4. Response Flow

### Truncated Pyramid

The first response should contain **only essential information**. Reveal details progressively in follow-ups (NN/G). This matches Kinoshita's **重点先行主義** (lead with what matters most).

### Next Action

End your response with a **single line** stating what the reader should decide or instruct next. Do not bury it inside a table or bullet list.

Example:

> Should I update the notification script?

### Cut the Filler

Phrases like the following carry no information. Cut them.

- "That's a great question!"
- "I see, understood."
- "Thank you for your question."

## 5. What to Cut

When in doubt about cutting, keep things in this priority:

1. Fixed phrasing already approved by the reader
2. Concrete examples (less ambiguous than abstractions)
3. Operational notes that need separate confirmation

Things you can drop:

- Formatting markers used purely for styling
- Repeated confirmation statements
- Mentions of things that are out of scope ("this part is fine" need not be said every time)
- Excessive procedural decomposition (if "should I fix it?" works, don't split into "① identify file ② edit ③ PR")

## 6. Code Examples

- **Code blocks are for code, commands, and syntax only**. Use blockquotes (`>`) for chat messages, proposed text, or quoted speech
- **Always include a language tag** (`` ```python ``, `` ```bash ``, `` ```json ``). It enables syntax highlighting and lets the reader/AI grasp the context immediately
- **Inline code (`backtick`)** for file names, function names, variables, and short identifiers
- **Make omissions explicit** (`...` or `// ...` so the reader knows what was elided)
- **If code is not runnable, label it as pseudocode**. Don't mix pseudocode with working code

## 7. Japanese-Specific Rules

### Sentence Rules (based on Plain Japanese guidelines)

- **One sentence: 30–60 characters, one claim each**
- **重点先行主義 (lead with what matters most)**: place the conclusion or key point at or near the beginning (Kinoshita)

### Expressions to Avoid

- **Vague expressions**: くらい / ごろ / など / といったところ
- **Double negatives**: 〜ないとは言えない
- **Overuse of passive voice**: 〜される / 〜と考えられる
- **Ambiguous words**: 結構です / いいです (can mean either yes or no)
- **Roundabout phrasing**:
  - することができる → できる
  - 次の諸点を心に留めておくことも重要である → cut, or say it in one word (Churchill's principle)

### Kanji vs. Hiragana

- **Auxiliary verbs in hiragana**:
  - 〜して下さい → 〜してください
  - 〜と言う → 〜という
- **Formal nouns in hiragana**:
  - 事 / 物 / 時 → こと / もの / とき

### Other

- **Annotate technical terms on first appearance**: e.g., 埋伏歯（骨の中に埋まったまま出てこない歯）
- **"お気軽に" is a banned phrase**: it diffuses responsibility. Use purpose-specific alternatives such as "ご不明点があればご連絡ください" (Please contact us with any questions) or "気になる症状があれば一度診察をおすすめします" (If you have any concerning symptoms, we recommend a consultation)

---

## References

- [Anthropic: Prompting best practices](https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/claude-prompting-best-practices)
- [Anthropic: Best practices for prompt engineering](https://claude.com/blog/best-practices-for-prompt-engineering)
- [Google Developer Documentation Style Guide](https://developers.google.com/style)
- [Microsoft Style Guide](https://learn.microsoft.com/en-us/style-guide/welcome/)
- [Nielsen Norman Group: Less Chat, More Answer](https://www.nngroup.com/articles/less-chat-more-answer/)
- Kinoshita Korezumi, *Riika-kei no Sakubun Gijutsu* (Chuko Shinsho, 1981)
- [Immigration Services Agency of Japan: Guidelines for Plain Japanese](https://www.moj.go.jp/isa/support/portal/plainjapanese_guideline.html)
- Cowan (2001) 4±1 / Miller (1956) 7±2 — classic working memory limits

See [docs/research/](./docs/research/) for source materials.
