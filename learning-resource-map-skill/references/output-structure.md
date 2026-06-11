# Output Structure

Use this structure for a study guide unless the user requests another format.

## 1. Title

Name the source topic list and the target learning resource.

Example:

```markdown
# <Source> を <Target Resource> で学ぶ
```

## 2. Opening

State what the guide is for in 2-4 sentences.

Do:

- Explain that learning should follow the reading order.
- Explain that the mapping section follows the source topic order.
- Mention supplemental keywords and confirmation questions when included.

Avoid:

- Starting with bibliography.
- Starting with research methodology.
- Long caveats before the learner knows what to do.

## 3. Learning Order

Put this near the top.

Include:

- Ordered list of target resource chapters/sections.
- Short reason only when it clarifies dependency.
- Optional "skip for now" or "read later" notes.

The learning order may differ from the source topic order. That is expected.

## 4. Source-Order Mapping

Preserve the source topic hierarchy.

Use this heading pattern. Keep heading levels at 4 or less unless the user requests another structure:

```markdown
## <major part, if any>

### <source topic number>. <source topic title>

#### 対応箇所

- <target location>
- <target location>

<1-3 sentences describing what is covered.>

#### 見る問題

- <problem or exercise locator>

#### 補助資料

S01, S11

#### 調べるキーワード

- <term>
- <term / Japanese term>

#### 確認質問

1. <gradable question>
2. <gradable question>
```

Only include `見る問題` when the target resource has relevant exercises or items. Only include `補助資料`, `調べるキーワード`, and `確認質問` when coverage is missing, weak, or likely difficult. Use `直接対応なし` under `補助資料` when no listed supplemental material directly supports the topic.

## 5. Review Checklist

Add a short checklist aligned with the source learning outcomes.

Good checklist items:

- "Can trace BFS and DFS on a graph with a cycle."
- "Can compare hash table and balanced tree lookup, insertion, and ordered traversal."

Avoid vague items:

- "Understand graphs."
- "Know algorithms."

## 6. Appendix

Put these at the end:

- target resource metadata
- source links
- table-of-contents sources
- supplemental materials numbered as `S01`, `S02`, etc.
- known limitations
- edition/version assumptions

For supplemental materials, include the ID, title/name, URL when available, and a short purpose. Use `補助資料` for the section title in Japanese guides, not `補助学習` or `補助教材`.

## Style

- Prefer prose plus short lists over large tables when the guide is for reading.
- Use tables only for compact comparisons.
- Keep each topic self-contained.
- Use heading levels instead of bare label lines for repeated blocks such as `対応箇所`, `補助資料`, `調べるキーワード`, and `確認質問`.
- Do not write redundant labels under `補助資料`; list only IDs such as `S01, S11` or `直接対応なし`.
- Do not delete important details just to reduce length.
- Avoid "補うこと" as a bare list of nouns; use keywords plus confirmation questions.
