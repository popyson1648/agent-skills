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

Use this pattern:

```markdown
## <source topic number>. <source topic title>

対応箇所:

- <target location>
- <target location>

<1-3 sentences describing what is covered.>

補助学習（本書外で調べること）:

調べるキーワード:

- <term>
- <term / Japanese term>

確認質問:

1. <gradable question>
2. <gradable question>
```

Only include the supplemental block when coverage is missing, weak, or likely difficult.

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
- supplemental resources
- known limitations
- edition/version assumptions

## Style

- Prefer prose plus short lists over large tables when the guide is for reading.
- Use tables only for compact comparisons.
- Keep each topic self-contained.
- Do not delete important details just to reduce length.
- Avoid "補うこと" as a bare list of nouns; use keywords plus confirmation questions.
