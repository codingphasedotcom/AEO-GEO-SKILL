# How AI Search Works

Covers the mechanics of finding/citing content, how platforms differ, and the types of AI visibility. This is the foundation that makes every tactic make sense.

## Table of contents
1. Two sources of AI information
2. Query fan-out (the single most important concept)
3. How AI decides what to cite (probabilistic citation)
4. Platform differences (with a comparison table)
5. The three types of AI visibility

---

## 1. Two sources of AI information

**Training data** — the static snapshot of books, websites, PDFs, social media, and YouTube transcripts the model learned from. Refreshed roughly every ~6 months. This is why ChatGPT answers "Who is the CEO of Apple?" instantly without searching. Problem: anything launched recently isn't in it yet.

**Real-time retrieval (RAG — retrieval-augmented generation)** — when the question needs fresh or specific information, the AI searches the live web via APIs, pulls back pages, reads them, and generates an answer from what it found. Each retrieved page carries its own probabilities.

**Two ways to influence what AI says about a brand:**
- Be mentioned so widely and consistently across the web that you're baked into **training data**.
- Make sure your pages surface when AI searches the web in real time — which is **SEO** (rank in Google, earn backlinks, publish quality content).

---

## 2. Query fan-out

Search evolved from one-to-one (one query → one result set) to many-to-one (different phrasings → same results) to **one-to-many** in AI search: a single prompt is expanded into many sub-queries run simultaneously behind the scenes.

Example: "Plan me a 5-day trip to Japan in November" fans out into "best neighborhoods to stay in Tokyo," "November weather in Kyoto," "Japan Rail Pass worth it," etc. The AI pulls from many sources and merges them into one answer.

**Numbers:** research (Seer Interactive / others) finds an average prompt triggers ~9–11 fan-out queries, some up to 28; ChatGPT deep-research ran 420 searches for a single "red phone case" query.

**Strategic implication:** to appear in the final answer you must be relevant across an **entire topic/niche**, not one keyword. A "how to start a podcast" page that skips equipment, hosting, and promotion loses to one that covers them.

**Caveats (per Ahrefs' Despina):** fan-out queries are synthetic (AI-generated in the moment), inconsistent (same prompt → different fan-outs), and ~95% have zero search volume. **Do not** treat them as a keyword list to optimize for one-by-one. Treat them as a **window into the topics AI considers important** for a question. You can view ChatGPT/Perplexity fan-out queries in Ahrefs Brand Radar's **AI responses** report.

---

## 3. How AI decides what to cite

Traditional rankings are relatively stable. AI citations are **probabilistic**: built on probabilities stacked on probabilities, plus a temperature setting that adds randomness so answers vary. Ask the same question 5× and you might be cited 3/5. There is no fixed position — talk about **AI visibility**, not rankings.

Patterns that increase citation probability:
- **Consensus** — if many web sources say the same thing about you, AI repeats it more confidently.
- **Freshness** — AI-cited content is ~25% fresher than typical SERP results; AI actively favors recent info, especially for topics that change.
- **Authority** — pages already ranking in Google's top 10 have a big head start. Historically ~76% of AI Overview citations came from top-10 pages (a more recent study puts it closer to ~38% as AIOs pull more from YouTube/Reddit). Notably, ~14% of AIO-cited pages don't rank in Google's top 100 at all, and ChatGPT's overlap with Google is even lower — so brands weak in traditional search still have a path in.

**Tie-together:** AI pulls from training data + real-time retrieval → fans the query out → merges and scores results → generates a probabilistic answer shaped by consensus, freshness, and authority. "Earn more mentions" = consensus. "Cover the whole topic" = fan-out. "SEO is the foundation" = authority overlap.

---

## 4. Platform differences

Only ~7 of the top 50 most-cited domains appear on all three of AI Overviews, ChatGPT, and Perplexity (~14% overlap). Optimizing for one platform can leave you invisible on others.

| Platform | Cites / favors | Overlap with Google top 10 | Notes |
|---|---|---|---|
| **Google AI Overviews** | Authoritative/established sites — health, finance, encyclopedic, Google-owned (YouTube ~5.6% of all AIO citations), Reddit | Historically ~76%, now ~38% and falling | Rapidly adding YouTube; pulls more from Reddit/YouTube over time |
| **Google AI Mode** | YouTube (top by a wide margin), then Google & Wikipedia; cites Quora ~3.5× more than AIOs; heavy Facebook/Instagram | — | Only ~13.7% citation overlap with AI Overviews despite ~86% semantic similarity — same answers, different sources |
| **ChatGPT** | Publishers & media — Reddit, Wikipedia, Amazon, Forbes, Business Insider, Wired; median DR of top-cited pages ~90 | Only ~8–10% | High-authority bias partly from OpenAI licensing deals |
| **Perplexity** | Most aligned with traditional Google search | ~28.6% | If you already rank in Google, expect the fastest AI visibility here |

**Prioritization:** (1) market share — Google's AI features + ChatGPT dominate; Perplexity is growing but smaller. (2) Overlap with your SEO strengths — already ranking in Google? Lean into AI Overviews + Perplexity. ChatGPT rewards publisher/editorial authority, so a Forbes/Reddit/niche-review mention can matter more than your own page's ranking.

To see top domains per platform: Ahrefs Brand Radar → blank search → **cited domains** report → filter by platform.

---

## 5. The three types of AI visibility

Visibility is a spectrum, not binary. Which type matters depends on the business.

1. **Cited & linked** — AI links your page in its sources; user can click through. Best for direct traffic, easiest to measure.
2. **Mentioned but not linked** — your brand is named, no link. No direct click, but word-of-mouth recommendation at scale → drives later branded searches. Every such mention is also a training example reinforcing the brand↔topic association ("peanut butter → jelly," "Tesla → electric cars").
3. **Not visible at all** — not in the conversation. Important to detect, because you can't fix what you don't know is broken.

**Link rates:** only ~28% of AI mentions include a link on average. By platform: Perplexity ~51.6%, AI Mode ~36.8%, ChatGPT ~26.9%, AI Overviews ~10.7%. But weighted by search volume, *linked* mentions cluster on the highest-traffic queries (e.g., on Perplexity links appear in ~78% of impressions despite ~51% of mentions; on Gemini ~71% of impressions vs ~16.8% of mentions). Citations are rare but land where the eyeballs are.

**Response types matter too:** step-by-step guides (opportunity for service/how-to brands to be the recommended expert), direct factual answers (authority play for publishers; rarely a click), and video citations (YouTube is heavily cited; creators can surface directly).

**Measuring the gap:** Ahrefs Brand Radar → search your site → compare mentions vs citations vs impressions vs share of voice across platforms. The gap between impressions and mentions is the opportunity: if AI answers questions about your topic but doesn't name you, that's where to focus.
