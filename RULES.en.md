# Response Style Rules

Style rules for LLM/AI chat responses, email, documents, manuals, articles, and other prose — reduce cognitive load and improve readability.

## Core Principle: Minimum Necessary Structure

Choose the **minimum necessary structure** to achieve your goal. Adding decoration does not strengthen information transfer; it adds visual noise and raises extraneous cognitive load.

> Reserve markdown primarily for inline code, code blocks, and simple headings. — Anthropic

Do not make text look human for its own sake. The goal is to help the reader understand the content accurately and move toward the necessary decision or action. Never alter facts, qualifications, or approved wording merely to improve style.

## 1. Sentence & Paragraph

- **One sentence per claim**; keep sentences short
- **Paragraphs should be 2–3 sentences or fewer** (NN/G)
- **One topic per paragraph**, with the topic sentence at or near the beginning (Kinoshita, *Riika-kei no Sakubun Gijutsu*)
- Prefer **active voice** when the actor is known. Do not turn qualifications such as "is believed" or "may" into unsupported certainty

## 2. Specificity, Rhythm & Voice

### Put facts before style

- Preserve facts, figures, names, conditions, and uncertainty from the input
- Do not invent experience, emotion, numbers, or causation to make prose feel natural
- If the source lacks the detail needed to support a claim, cut the vague praise or label it as unverified
- Do not add deliberate variation to medical, legal, technical, or approved fixed text when accuracy and consistency take priority

### Replace abstraction with evidence

Words such as "careful," "reassuring," "high-quality," "contribution," "value," and "growth" do not help the reader judge the claim by themselves. When they matter, explain them through an action, audience, outcome, number, or source.

Examples:

- "We respond carefully" → state the response time, verification method, or scope
- "A high-quality article" → state the sources, review process, or information the reader will gain
- "We contribute to the community" → state who receives what and what change is intended

If an adjective or conclusion cannot be made concrete, cut it instead of replacing it with another abstraction. A paragraph that adds no new information should be removed or merged with a neighboring paragraph.

### Let meaning control rhythm

- Use a short sentence for a conclusion or turn; use the length needed to explain a condition or reason
- Do not repeat the same sentence length, syntax, or paragraph size mechanically
- Do not mix short and long sentences to a fixed ratio or insert errors and hesitations as a performance of humanity
- When transitions or endings repeat, rebuild the relationships between sentences instead of cycling synonyms
- Read the result aloud and fix monotony, breathless passages, and breaks in meaning

Sentence and paragraph length targets are readability guidelines, not uniformity targets. Prefer the role of each sentence over the visual waveform of the whole piece.

### Use voice samples carefully

When writing samples from a person or organization are available, study their vocabulary, cadence, and information order. Do not copy distinctive phrases superficially; adapt the underlying choices to the current reader and purpose.

### Audit formulaic AI patterns

When several of these patterns appear together, revise at the paragraph level rather than swapping isolated words:

- praise, restating the question, or extended throat-clearing before the substance
- transitions that do not explain the relationship between ideas
- unsupported significance claims such as "a pivotal step" or "new possibilities"
- vague attribution such as "experts say" or "many people"
- cycling synonyms for the same subject
- uniformly sized paragraphs, excessive headings, or bullet-heavy avoidance of prose
- generic conclusions that do not follow from the body

These are not banned phrases in isolation. Keep them when they have a clear role and evidence. The standard is less empty or difficult prose, not evasion of AI detectors.

After rewriting, audit the result again for abstractions that were merely rephrased, formulaic language that survived, and certainty introduced by the edit.

## 3. Visual Structure

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
- **Use `>` only**. Do not substitute `▎` or `｜` (they don't render as standard Markdown blockquotes)
- Using blockquotes instead of code blocks for prose reduces visual noise

### Bullet markers

- **Use `-` only**. Do not mix `・` or `*`
- For nested lists, use indented `-` to create hierarchy

## 4. Emphasis

- **Bold**: **up to 3 instances per message** (a ceiling, not a target). Use bold when emphasis matters. Zero use makes it harder for the reader to locate the core point. Rule of thumb: bold a word if the reader will likely scan back to find it
- **Emoji**: do not over-use. What feels like visual cueing becomes color overload. Anthropic explicitly documents "fewer emoji" for Claude Opus 4.7
- **Leading priority markers (🔴🟡✅)**: avoid them when there are only 2–3 items — prose can convey priority just as well

## 5. Response Flow

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

## 6. What to Cut

When in doubt about cutting, keep things in this priority:

1. Fixed phrasing already approved by the reader
2. Concrete examples (less ambiguous than abstractions)
3. Operational notes that need separate confirmation

Things you can drop:

- Formatting markers used purely for styling
- Repeated confirmation statements
- Mentions of things that are out of scope ("this part is fine" need not be said every time)
- Excessive procedural decomposition (if "should I fix it?" works, don't split into "① identify file ② edit ③ PR")

## 7. Code Examples

- **Code blocks are for code, commands, and syntax only**. Use blockquotes (`>`) for chat messages, proposed text, or quoted speech
- **Always include a language tag** (`` ```python ``, `` ```bash ``, `` ```json ``). It enables syntax highlighting and lets the reader/AI grasp the context immediately
- **Inline code (`backtick`)** for file names, function names, variables, and short identifiers
- **Make omissions explicit** (`...` or `// ...` so the reader knows what was elided)
- **If code is not runnable, label it as pseudocode**. Don't mix pseudocode with working code

## 8. Japanese-Specific Rules

### Sentence Rules (based on Plain Japanese guidelines)

- **One sentence: 30–60 characters, one claim each**
- **重点先行主義 (lead with what matters most)**: place the conclusion or key point at or near the beginning (Kinoshita)

### Expressions to Avoid

- **Vague expressions**: くらい / ごろ / など / といったところ
- **Double negatives**: 〜ないとは言えない
- **Overuse of passive voice**: make the actor explicit when possible, but retain phrases such as 〜と考えられる when they communicate evidence and uncertainty
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
- [conorbronsdon/avoid-ai-writing](https://github.com/conorbronsdon/avoid-ai-writing) — structured audits and second-pass review of formulaic AI patterns (MIT)
- [blader/humanizer](https://github.com/blader/humanizer) — rhythm and vocabulary calibration from writing samples (MIT)
- [aaaronmiller/humanize-writing](https://github.com/aaaronmiller/humanize-writing) — sentence length, paragraph structure, and read-aloud rhythm checks (MIT)
- [Shun Hashimoto, "How to create a winning self-promotion statement with AI"](https://x.com/Lifelighter1/status/2036356742041178348) — practitioner observations on uniform rhythm, abstraction, and generic prose

See [docs/research/](./docs/research/) for source materials.
