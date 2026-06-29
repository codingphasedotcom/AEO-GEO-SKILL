# Query Research for AEO/GEO (manual & tool methods)

The hands-on companion to `references/strategy-and-research.md` §2 (which is Ahrefs-centric). This file covers tool-agnostic discovery, question clustering, intent classification, and the manual AI-platform testing protocol — useful when you don't have Ahrefs open, or want to validate what AI actually says.

## Table of contents
1. Conversational query discovery (tools + process)
2. Question clustering (the 6-cluster framework)
3. Intent classification (4 types → content mapping)
4. AI platform testing protocol
5. Competitive citation / gap analysis

---

## 1. Conversational query discovery

AI prompts are longer and more contextual than keywords. Optimize for long-tail, scenario-based, multi-part questions.

```
Traditional search:      "best email marketing software"
Conversational equivalent: "What's the best email marketing software for a
  small e-commerce business with <10,000 subscribers that integrates with Shopify?"
```

### Tools
| Tool | Best for | Output |
|------|----------|--------|
| AnswerThePublic | Question discovery | Visual question maps |
| AlsoAsked | "People Also Ask" chains | Hierarchical questions |
| Semrush Keyword Magic | Volume + questions | Data-rich queries |
| Ahrefs (Questions filter) | Questions w/ search volume | See `strategy-and-research.md` §2 |
| Google Autocomplete | Real-time trends | Suggested queries |
| Reddit / Quora | Authentic phrasing | Real user language |

### Process — build a question map
```
1. Seed topic            → e.g. "email marketing"
2. Question variations    → what / how / why / when / where / who / which
     "what is email marketing", "how to do email marketing", …
3. Add modifiers          → for beginners, in 2026, vs [alt], examples,
                            best practices, mistakes to avoid
4. Mine People Also Ask   → click 3+ levels deep to find question chains
```

---

## 2. Question clustering

Group discovered questions into clusters; this maps the whole topic (critical for query fan-out — `references/how-ai-search-works.md` §2) and tells you which content templates to build.

```
Topic: [Main topic]
├── Cluster 1 — Definitions & basics   ("what is", "definition", "explained simply")
├── Cluster 2 — How-to & process       ("how to", "how does it work", "steps", "tutorial")
├── Cluster 3 — Comparisons            ("vs", "difference between", "alternatives", "best")
├── Cluster 4 — Problems & solutions   ("not working", "common mistakes", "fix", "troubleshooting")
├── Cluster 5 — Cost & value           ("how much", "is it worth it", "pricing", "free vs paid")
└── Cluster 6 — Advanced & specific    ("for [audience]", "advanced techniques", "examples")
```

### Prioritization
| Cluster | Search volume | AI citation potential | Priority | Template |
|---------|---------------|-----------------------|----------|----------|
| Definitions | High | Very high | 1 | Definitional |
| How-to | High | High | 2 | How-to |
| Comparisons | Medium | High | 3 | Comparison |
| Problems | Medium | Medium | 4 | How-to / FAQ |
| Cost/Value | Medium | Medium | 5 | FAQ / Comparison |
| Advanced | Low | Low | 6 | Definitional / FAQ |

Templates for each: `references/content-templates.md`.

---

## 3. Intent classification

```
1. INFORMATIONAL (Know)   what, why, how, guide, tutorial, learn
   AI behavior: synthesizes from multiple sources
   Optimize: comprehensive, authoritative content (+ get mentioned widely)

2. NAVIGATIONAL (Go)      [brand], login, official, website
   AI behavior: points to a specific destination
   Optimize: clear brand presence & site structure

3. COMMERCIAL (Compare)   best, top, vs, review, comparison
   AI behavior: presents options with analysis
   Optimize: comparison content, honest reviews, listicle inclusion

4. TRANSACTIONAL (Do)     buy, price, discount, download, sign up
   AI behavior: often defers to the website
   Optimize: clear CTAs, product pages (this is where organic clicks survive AI)
```

### Intent → content mapping
| Intent | Content type | Schema | Snippet format |
|--------|--------------|--------|----------------|
| Informational | Guide, explainer | Article, FAQPage | Paragraph, list |
| Navigational | Landing page | Organization, WebSite | Sitelinks |
| Commercial | Comparison, review | Product, Review | Table |
| Transactional | Product page | Product, Offer | Rich product |

Cross-reference the **BID + AI filter** in `references/strategy-and-research.md` §2.2–2.4 to decide whether to chase the *click* (traditional targeting) or the *mention* (AEO targeting) for each query.

---

## 4. AI platform testing protocol

The only way to know your real AI visibility is to ask the AIs. Do this manually (or via Ahrefs Brand Radar at scale).

**For each target query, test across:** ChatGPT (free + Plus), Perplexity, Google AI Overviews, Claude, Bing Copilot, Gemini.

**Document for each:**
1. Is your brand/site mentioned?
2. Is your content cited (linked)?
3. What sources *are* cited?
4. How is the answer structured (paragraph, list, table, video)?
5. What's missing from the answer that you could provide?

**Query variations to run for a topic:**
```
1. "What is [topic]?"
2. "How do I [action related to topic]?"
3. "Best [topic] for [use case]"
4. "[Your brand] vs [competitor]"
5. "[Topic] in 2026"
6. "Explain [topic] simply"
7. "[Topic] examples"
8. "Is [topic] worth it?"
```

Remember citations are **probabilistic** (`references/how-ai-search-works.md` §3) — run each query a few times; same prompt can cite you 3/5. Track frequency, not a single result.

---

## 5. Competitive citation / gap analysis

**Step 1 — Who's cited.** Run your target queries across platforms; record every cited domain; tally frequency by domain.

**Step 2 — Analyze cited content.** For top-cited competitors, note: structure (headers/formatting), depth (coverage, not just word count), authority signals (author, sources, original data), freshness (last updated), technical factors (speed, schema, crawlability).

**Step 3 — Find the gaps.** What topics do they cover that you don't? What formats are they using? What unique data/research do they have? How recent is their content? What E-E-A-T signals are present?

### Competitive content audit grid
| Factor | Competitor A | Competitor B | Your site | Gap |
|--------|--------------|--------------|-----------|-----|
| Topic coverage | | | | |
| Content depth | | | | |
| Freshness | | | | |
| Author authority | | | | |
| Source citations | | | | |
| Schema markup | | | | |
| FAQ sections | | | | |
| Original research | | | | |

### Turn gaps into actions
```
QUICK WINS (easy, high impact):
  add FAQ sections · update publish dates (meaningfully) · add author bios
MEDIUM EFFORT (moderate, solid impact):
  expand thin content · add original stats/data · implement schema
LONG-TERM (high effort, transformative):
  original research · thought leadership · build topical authority
```

This mirrors the **Fix / Build / Influence** prioritization in `references/strategy-and-research.md` §1.4 — use whichever framing fits the engagement.
