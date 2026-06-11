# Question Design

Confirmation questions should make the learner's understanding observable. They should also be gradable by an AI or human from the question text alone.

## Good Question Patterns

Use these forms:

- Compare A and B using specified criteria.
- Trace an algorithm or process on a small input.
- Show the state after a sequence of operations.
- Fill a table of time/space complexity.
- Define a term using required words.
- Give a minimal example or counterexample.
- Derive or apply a recurrence/formula.
- Explain why a method is appropriate under stated conditions.

## Bad Patterns

Avoid:

- "Understand X."
- "Explain X" with no expected angle.
- "Know the difference between A and B."
- "Research X."
- A bare list of topics with no task.

## Convert Vague Outcomes

Vague:

```markdown
- Understand ADT.
```

Better:

```markdown
1. Stack を例に、ADT とその実装の違いを説明せよ。答えには「操作仕様」と「内部表現」という語を含めること。
2. Stack ADT の `push`, `pop`, `peek` について、それぞれ操作後に満たすべき条件を述べよ。
```

Vague:

```markdown
- Learn MST.
```

Better:

```markdown
1. 頂点 `{A,B,C}`、辺 `AB=1`, `BC=2`, `AC=5` の重み付き無向グラフの MST を答えよ。
2. Prim 法と Kruskal 法で選ばれる辺の順序をそれぞれ答えよ。
3. Kruskal 法で Union-Find を使う理由を、同じ連結成分かどうかという観点で説明せよ。
```

## Keyword Design

Keywords should help the learner find the missing concept quickly.

Rules:

- Use the canonical English term when it is the standard in documentation, code, or papers.
- Add a Japanese term when supporting Japanese speakers and the Japanese term is commonly used.
- Do not add Japanese when it is only the English loanword with no practical difference, unless it improves search.
- Include implementation-specific keywords when the learning outcome requires coding.
- Include "vs" or "違い" keywords when the learner must compare concepts.

Examples:

- `abstract data type / 抽象データ型`
- `dictionary ADT / 辞書 ADT / 連想配列`
- `Floyd-Warshall algorithm / ワーシャルフロイド法`
- `minimum spanning tree / 最小全域木`
- `regular expression NFA / 正規表現 NFA`

## Minimum Question Set

For each supplemental block, include 2-4 questions.

At least one should require a concrete operation:

- compute
- trace
- compare
- construct
- update state
- classify

For advanced or conceptual topics, include at least one definition question and one comparison or consequence question.
