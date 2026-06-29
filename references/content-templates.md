# Content Templates for AEO/GEO

Copy-paste page skeletons that AI systems extract and cite well. Each maps to a query type AI gets a lot of. Pair these with the structure principles in `references/execution.md` §1 (BLUF, atomic sections, entity-rich, simple/declarative) — the templates give the shape; those principles give the prose.

## Table of contents
1. Definitional template ("What is X?")
2. How-to template (process / tutorial)
3. Comparison template ("X vs Y")
4. FAQ-optimized template (question clusters)
5. Writing guidelines for AI extraction
6. Length targets

---

## 1. Definitional template

**Best for:** "What is X?" queries, concept explanations. These are the highest AI-citation-potential cluster (see `references/query-research.md` §2).

```markdown
# What is [Topic]? [Subtitle with context]

**TL;DR:** [Topic] is [concise 1-sentence definition]. [1–2 sentences on why it matters or its key application].

## Definition

[Topic] is [expanded definition in 2–3 sentences, including key characteristics].

> **Quick definition:** [≤15-word definition built for snippet extraction]

## How [Topic] works

[Plain-language explanation. One idea per sentence.]

### Key components

| Component | Purpose | Example |
|-----------|---------|---------|
| [Item 1] | [What it does] | [Concrete example] |
| [Item 2] | [What it does] | [Concrete example] |

## Benefits of [Topic]

1. **[Benefit 1]**: [1–2 sentences].
2. **[Benefit 2]**: [1–2 sentences].
3. **[Benefit 3]**: [1–2 sentences].

## Common use cases

- **[Use case 1]**: [Brief description].
- **[Use case 2]**: [Brief description].

## FAQ

### What is the difference between [Topic] and [Related topic]?
[Clear answer in 2–3 sentences.]

### Who should use [Topic]?
[Audience, with examples.]

## Summary

[2–3 sentence recap — another extraction opportunity.]

---
*Last updated: [Date] | Author: [Name, credentials]*
*Sources: [Key sources for credibility]*
```

---

## 2. How-to template

**Best for:** process queries, tutorials, step-by-step guides. Eligible for `HowTo` schema (`references/schema-for-ai.md` §HowTo) and step-by-step AI answers.

```markdown
# How to [Action]: [Subtitle with benefit]

**TL;DR:** To [action], [high-level steps in one sentence]. Takes ~[time] and requires [key requirements].

## Quick overview

| | |
|---|---|
| **Time required** | [X minutes/hours] |
| **Difficulty** | [Beginner / Intermediate / Advanced] |
| **What you'll need** | [Key requirements] |
| **Expected result** | [What the reader achieves] |

## Before you start

### Prerequisites
- [Requirement 1]
- [Requirement 2]

## Step-by-step

### Step 1: [Action verb + what]
[1–2 sentences on this step.]

**How to do it:**
1. [Sub-step a]
2. [Sub-step b]

> **Pro tip:** [Helpful insight.]

### Step 2: [Action verb + what]
[1–2 sentences.]

**Warning:** [Common mistake to avoid.]

## Troubleshooting

### [Common problem]
**Cause:** [Why it happens.]
**Solution:** [How to fix it.]

## FAQ

### How long does it take to [action]?
[Direct answer with context.]

## Summary

You've learned how to [action]. Key steps:
1. [Step 1 recap]
2. [Step 2 recap]

---
*Last updated: [Date] | Author: [Name, credentials]*
```

---

## 3. Comparison template

**Best for:** "X vs Y" queries and decision content. Comparison/listicle formats are disproportionately cited — ~43.8% of ChatGPT citations are listicles/comparisons (see `references/execution.md` §1).

```markdown
# [Option A] vs [Option B]: What you need to know in 2026

**TL;DR:** [Option A] is best for [use case]; [Option B] excels at [other use case]. Choose A if [criteria]; choose B if [other criteria].

## Quick comparison

| Feature | [Option A] | [Option B] |
|---------|------------|------------|
| **Best for** | [Use case] | [Use case] |
| **Price** | [Range] | [Range] |
| **Ease of use** | [Rating] | [Rating] |
| **Key strength** | [Advantage] | [Advantage] |
| **Key weakness** | [Drawback] | [Drawback] |

## [Option A] overview
### What is [Option A]?
[2–3 sentence definition.]

**Pros:** [Advantage 1], [Advantage 2], [Advantage 3]
**Cons:** [Drawback 1], [Drawback 2]
**Best for:** [Specific users] because [reason].

## [Option B] overview
*(same structure)*

## Detailed comparison

### [Criteria 1]: A vs B
[2–3 paragraphs.] **Winner:** [Option X] — [one-sentence reason].

### [Criteria 2]: A vs B
[2–3 paragraphs.] **Winner:** [Option X] — [one-sentence reason].

## Which should you choose?

**Choose [Option A] if:** [condition 1], [condition 2].
**Choose [Option B] if:** [condition 1], [condition 2].

## FAQ
### Is [Option A] better than [Option B]?
[Nuanced "it depends on…" answer.]

## Conclusion

**Our recommendation:** For [common use case], we recommend [Option X] because [reason]. If [alternative scenario], [Option Y] wins.

---
*Last updated: [Date] | Author: [Name, credentials]*
*Methodology: [How the comparison was conducted]*
```

---

## 4. FAQ-optimized template

**Best for:** question clusters and comprehensive topic coverage. Doubles as the misinformation defense from `references/measurement-and-roi.md` §4 — a specific, official FAQ is what AI reaches for when it would otherwise pick specific fiction. Eligible for `FAQPage` schema.

```markdown
# [Topic]: Frequently asked questions

**TL;DR:** This guide answers the most common questions about [topic], including [key areas]. Last updated [Date].

## Quick answers

| Question | Short answer |
|----------|--------------|
| [Question 1]? | [≤10-word answer] |
| [Question 2]? | [≤10-word answer] |

## Detailed FAQ

### Basic questions
#### What is [topic]?
[2–3 sentence standalone answer.]

#### Why is [topic] important?
[Complete answer with specific benefits.]

### How-to questions
#### How do I [common action]?
[Brief step list.]

#### How much does [topic] cost?
[Price range + factors that affect it.]

### Comparison questions
#### What's the difference between [X] and [Y]?
[Clear distinction in 2–3 sentences.]

### Troubleshooting questions
#### What if [common problem]?
[Solution-focused answer.]

## Still have questions?
[CTA — contact, related resources.]

---
*Last updated: [Date] | Expert: [Name, credentials]*
```

---

## 5. Writing guidelines for AI extraction

**Lead with the answer (BLUF).**
- Weak: "In this article, we'll explore what SEO means…"
- Strong: "SEO (search engine optimization) is the practice of improving website visibility in search results."

**Use complete sentences** — AI extracts standalone statements, not fragments.
- Weak: "Benefits: faster, cheaper, better"
- Strong: "The main benefits are faster processing, lower costs, and improved quality."

**Be specific with numbers.**
- Weak: "This can significantly improve results"
- Strong: "This typically improves results by 25–40% within 3 months"

**Attribute claims** (consensus + authority signal).
- Weak: "Studies show that…"
- Strong: "According to a 2025 Ahrefs study of 75,000 brands…"

**Format for scanning:** bullets for 3+ items, bold key terms on first use, paragraphs under ~4 sentences (≤120 words), tables for comparisons, clear question-based H2s.

---

## 6. Length targets

Length itself barely correlates with citation (~0.04 across 174k AIO-cited pages — see `references/execution.md` §1). Optimize the **snippet target**, not the word count.

| Content type | Typical full length | Snippet target (lead answer) |
|--------------|---------------------|------------------------------|
| Definition | 1,500–2,500 words | 40–60 words |
| How-to | 1,500–3,000 words | 45–50 words |
| Comparison | 2,000–3,500 words | 40–50 words |
| FAQ | 1,500–2,500 words | 40–50 words per answer |

The full-length ranges reflect what tends to cover a topic comprehensively (which helps with query fan-out, `references/how-ai-search-works.md` §2) — not a length requirement for citation.
