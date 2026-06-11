---
name: learning-resource-map-skill
description: Use when creating or revising a study guide that maps a curriculum, syllabus, topic list, standard, or learning objectives to one or more books, courses, papers, documentation sites, or other reference resources. The skill helps produce a readable, evidence-backed Markdown guide with a learning order, per-topic resource mapping, supplemental research terms, gradable review questions, and multilingual support when useful.
---

# Learning Resource Map Skill

## Purpose

Create a high-quality Markdown study guide that maps a source topic list to target learning resources. The guide should help a learner know what to read first, where each source topic is covered, what is missing, what to search for, and how to check understanding.

## Workflow

1. Read the source topic list and preserve its topic hierarchy.
2. Identify the target resource precisely: title, edition/version, author/owner, ISBN/DOI/URL when available.
3. Research current and authoritative metadata, table of contents, section names, and resource scope.
4. Decide the learner-friendly reading order. Put this near the top of the output.
5. Build the source-order mapping after the reading order. For every source topic, include:
   - target resource location
   - what the learner can learn there
   - gaps or weak coverage
   - supplemental search terms when the target resource is insufficient
   - gradable confirmation questions
6. Add appendices for source evidence, supplemental resources, and caveats.
7. Verify that every source topic is represented and that the output is usable without reading the research notes first.

## When To Read References

- For the expected Markdown structure, read `references/output-structure.md`.
- For research and citation discipline, read `references/research-checklist.md`.
- For supplemental keyword and question design, read `references/question-design.md`.

## Quality Rules

- Lead with the learner's path, not with bibliography or evidence.
- Keep source-topic order for the mapping section, even if the learning order differs.
- Move evidence, URLs, ISBN metadata, and caveats to appendices unless they are needed immediately.
- Prefer official or primary sources for target resource metadata and table of contents.
- Use supplemental materials when the target resource does not cover a source topic.
- Include Japanese terms when supporting Japanese-speaking learners and the Japanese term is common or differs from a direct English loanword.
- Make confirmation questions concrete enough to be graded by an AI or human without guessing the intent.

## Validation Checklist

Before finishing:

- The reading order appears before the source-order mapping.
- Every source topic and important subtopic appears in the guide.
- Each target-resource reference includes chapter, section, item, page, URL, or equivalent locator when available.
- Missing coverage is explicit and actionable.
- Supplemental search terms are specific, not generic.
- Confirmation questions ask for comparisons, traces, calculations, examples, state changes, or definitions with required terms.
- Appendix evidence supports the resource identity and scope.
