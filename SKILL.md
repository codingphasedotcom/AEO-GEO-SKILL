---
name: aeo-geo
description: >-
  Answer Engine Optimization (AEO), also called Generative Engine Optimization (GEO/LLMO) — strategy for getting a brand cited, mentioned, and recommended inside AI search (ChatGPT, Google AI Overviews, Google AI Mode, Perplexity, Gemini, Copilot). Use whenever the user wants to improve AI search visibility, get cited by LLMs, win featured snippets / AI Overviews, run a brand gap analysis, do keyword/prompt research for AI, structure content so AI will quote it (templates, E-E-A-T, schema/JSON-LD), earn brand mentions on third-party sites, optimize YouTube for AI, fix AI-crawler issues (robots.txt, GPTBot, llms.txt, JS rendering), audit a page's AI-readiness, or measure AI referral traffic and share of voice. Trigger on "AEO", "GEO", "answer engine optimization", "generative engine optimization", "AI search visibility", "get cited by ChatGPT", "rank in AI overviews", "featured snippet", "E-E-A-T", "schema markup for AI", "brand mentions for AI", "Brand Radar", "AI share of voice", "LLM optimization", or any request about being found or recommended by AI assistants — even when framed as SEO. Built on the Ahrefs AEO methodology, extended with content templates, schema, crawler configs, and an audit scoring system; pairs with the user's Ahrefs MCP tools.
---

# Answer Engine Optimization (AEO / GEO)

Created by [CodingPhase.com](https://codingphase.com). Maintained by [CodingPhase.com](https://codingphase.com).

AEO — also called GEO (generative engine optimization) or LLMO (large language model optimization) — is the practice of making content **visible and useful to AI systems that deliver direct answers**, so the brand gets cited, mentioned, or recommended inside ChatGPT, Google AI Overviews, Google AI Mode, Perplexity, Gemini, and Copilot.

## The one thing to internalize first

**SEO is the foundation of AEO. AEO is a new layer on top of SEO, not a replacement.** Quality content, authority, and technical health still matter. The difference: traditional SEO competes for a **ranking position** (a blue link the user clicks); AEO competes for a **mention** inside a synthesized answer. The AI reads dozens of sources, merges them, and decides who to name — there is no fixed leaderboard.

Why it matters commercially: AI traffic volume is still small (~0.25% of total site traffic on average) but converts dramatically better — Ahrefs reports its AI visitors convert at ~23× the rate of organic search, because when AI recommends you it has already explained *why* you're a good fit, so the visitor arrives pre-qualified. Treat AEO as part brand marketing: much of its value is impressions inside the AI conversation that never produce a click but drive later branded searches.

## How to use this skill

This skill mirrors a 4-phase workflow. Identify where the user is and load the matching reference file(s). Don't dump everything — read the file relevant to the request.

| User wants to… | Read |
|---|---|
| Understand how AI search finds/cites content, platform differences, types of visibility | `references/how-ai-search-works.md` |
| Audit current AI visibility, run a brand gap analysis, do keyword/prompt research for AEO | `references/strategy-and-research.md` |
| Discover conversational queries, cluster questions, classify intent, run AI-platform tests (tool-agnostic) | `references/query-research.md` |
| Create content that gets cited, earn mentions, optimize YouTube, fix technical/crawler issues | `references/execution.md` |
| Get copy-paste page skeletons (definitional, how-to, comparison, FAQ) + writing rules | `references/content-templates.md` |
| Add structured data / JSON-LD (FAQPage, HowTo, Article+Author, Speakable, @graph) | `references/schema-for-ai.md` |
| Configure robots.txt for AI bots, decide search-vs-training, monitor crawler activity | `references/ai-crawlers.md` |
| Measure AI traffic, bot activity, share of voice, judge ROI, build an action plan | `references/measurement-and-roi.md` |

For a broad "help me with AEO" request with no clear entry point, start with the **action plan** at the bottom of `references/measurement-and-roi.md` — it's the prioritized first-week checklist — then branch into whichever phase the user needs. To **audit/score an existing page**, use the AI-readiness audit at the bottom of this file.

## Core mechanics (always-loaded summary)

These principles drive *every* tactic. Know them cold; the reference files explain the "why."

1. **Two sources of AI knowledge.** (a) *Training data* — a static snapshot of the web, refreshed every few months; this is why ChatGPT instantly "knows" Tim Cook runs Apple. (b) *Real-time retrieval (RAG)* — the AI searches the live web, pulls pages, and synthesizes an answer. You influence training data by being mentioned widely and consistently across the web; you influence retrieval through ordinary SEO (rank well, earn links, publish quality pages).

2. **Query fan-out.** One prompt is expanded into many sub-queries (research finds ~9–11 on average, sometimes 28+; deep-research modes can run hundreds). To be in the final answer you must be relevant across an entire *topic/niche*, not just one keyword. Fan-out queries are synthetic, inconsistent, and ~95% have zero search volume — treat them as a window into what topics the AI considers important, not a new keyword list.

3. **Citations are probabilistic, not ranked.** Same prompt asked 5× can cite you 3/5. Talk in terms of **AI visibility / share of voice**, never "AI rankings." Patterns that raise the probability: **consensus** (many sources saying the same thing about you), **freshness** (AI-cited content runs ~25% fresher than traditional SERP results), and **authority** (a large share of AI Overview citations come from pages already ranking in Google's top 10 — though that overlap is weakening, so non-dominant brands still have real opportunity).

4. **Brand mentions are the strongest lever.** In a study of 75,000 brands, branded web mentions had the highest correlation (~0.664) with AI Overview visibility — stronger than backlinks, domain rating, or referring domains. Mentions on highly-linked pages correlate even higher (~0.7). Unlinked mentions still matter: only ~28% of AI mentions include a link, but every mention is a training example teaching the model to associate your brand with a topic.

5. **Platforms are NOT interchangeable.** Across the top 50 most-cited domains on AI Overviews, ChatGPT, and Perplexity, only ~14% overlap. Each has its own index and biases. Prioritize by market share (Google + ChatGPT hold most eyeballs) and by overlap with what you already do well in SEO. See the platform table in `references/how-ai-search-works.md`.

## Quick-reference frameworks

Three compact frameworks that turn the mechanics above into concrete writing/auditing checks. Use them inline; the reference files expand each.

**E-E-A-T — the trust foundation (required for all AEO).** AI prefers trusted sources, so encode trust explicitly:
- *Experience* — first-hand knowledge, case studies, original research.
- *Expertise* — credentials, depth, technical accuracy (author bios, `Person` schema).
- *Authority* — citations, backlinks, mentions, brand recognition (this is the consensus lever, mechanic #4).
- *Trustworthiness* — accuracy, transparency, clear sourcing, visible update dates.

**CRASP — make a passage quotable.** Before publishing a key section, check it is: **C**lear (unambiguous statements AI can lift), **R**elevant (matches conversational intent), backed by **A**uthority (cited sources, credentials), well-**S**tructured (scannable, atomic — see `references/execution.md` §1), and **P**recise (specific facts, numbers, dates).

**AEO snippet formats — answer in the shape AI wants.** Lead every section with a directly extractable answer (first 40–60 words), then match format to query type:

| Query type | Best format |
|---|---|
| "What is X?" | Definition paragraph (40–60 words) |
| "How to X" | Numbered steps (5–8) |
| "Best X" | Bulleted list with brief descriptions |
| "X vs Y" | Comparison table |
| "Why X?" | Direct answer + explanation |

Full page skeletons for each: `references/content-templates.md`.

## Working with the user's tools

The user has **Ahrefs MCP tools** connected. Much of this methodology runs through Ahrefs **Brand Radar** (mentions, citations, impressions, AI share of voice, cited-domains, AI-responses/fan-out, topics reports), **Site Explorer**, **Keywords Explorer**, **Content Explorer**, **Site Audit**, and **Web Analytics / Bot Analytics**. When a step says "go to Brand Radar / Site Explorer / etc.," prefer pulling the actual data with the corresponding Ahrefs MCP tool rather than describing it abstractly — call `tool_search` to load the right Ahrefs tool, then run it. Cross-reference the user's existing `local-seo` skill for contractor/home-service work, since AEO builds on the same SEO foundation.

## Output conventions

- Give concrete, copy-paste-ready outputs (filters to set, modifiers to add, exact robots.txt lines to check, meta copy, content rewrites) — not generic advice.
- When citing the data points above, present them as directional benchmarks from the Ahrefs AEO methodology, and note they shift over time (AI Overview citations refresh ~every 2 days; >45% of citations change on refresh).
- Frame measurement honestly: AI visibility is harder to measure than SEO and analytics undercount it. Recommend triangulating referral traffic + bot analytics + self-reported attribution.

## AI-readiness audit (scoring a page)

When the user asks "audit this page / is this content ready for AI search," score it out of 100 across five categories and return an action plan. Don't just grade — give the fix for each gap.

**Quick 5-point check (use for a fast pass):**
1. **TL;DR** — is there a summary/direct answer at the top?
2. **Structure** — question-based headers, atomic sections?
3. **Facts** — statistics with cited sources, specific numbers/dates?
4. **E-E-A-T** — author credentials and update date visible?
5. **Schema** — FAQPage / HowTo / Article markup present?

**Scoring rubric (100 pts):**

| Category | Points | What earns the points |
|---|---|---|
| E-E-A-T signals | 25 | Author bio + credentials, cited authoritative sources, original data, visible dates, clear sourcing |
| Content structure | 20 | BLUF/lead answers, question H2s, atomic sections, clean HTML hierarchy |
| Fact-density | 20 | Specific stats with attribution, named entities, verifiable numbers, expert quotes |
| Extractability | 20 | TL;DR present, ≤120-word paragraphs, bullets/tables, complete FAQ answers |
| AI technical readiness | 15 | Crawlable (robots.txt), server-side rendered, fast, schema present, no AI-404s |

**Bands:** 90–100 excellent (high citation probability) · 70–89 good (minor fixes) · 50–69 needs work · <50 critical (restructure).

**Report format:**
```markdown
# GEO/AEO Audit — [URL]
**Date:** [date] · **Overall:** X/100 ([band])

## Summary
[2–3 sentence AI-readiness assessment]

## Scores
| Category | Score | Status |
|---|---|---|
| E-E-A-T | X/25 | Good / Needs work / Critical |
| Structure | X/20 | … |
| Fact-density | X/20 | … |
| Extractability | X/20 | … |
| Technical | X/15 | … |

## Priority fixes
1. **[Issue]** — [impact] — [specific fix → which reference file]
2. …

## Action plan
- **Immediate:** [e.g. add TL;DR, implement FAQ schema]
- **Short-term:** [e.g. rewrite headers as questions, add author bio]
- **Ongoing:** [monitor AI citations, keep content fresh]
```

Tie each fix to a reference: structure/templates → `references/content-templates.md`; schema → `references/schema-for-ai.md`; crawl/technical → `references/ai-crawlers.md` + `references/execution.md` §4; freshness/format → `references/execution.md` §1.
