# AEO Strategy & Research

Two phases: **assess** (where does the brand stand, where are the gaps) then **discover** (which keywords and prompts to go after). Do the brand gap analysis first — it becomes the personalized roadmap for execution.

## Table of contents
1. Brand gap analysis (4 steps + 6 gap dimensions)
2. Keyword & prompt research for AEO (5 steps: build, vet/BID, AI filter, AI mention opportunities, prompt research)

---

## 1. Brand gap analysis

A brand gap analysis measures the difference between where a brand *should* show up (Google, AI results, across the web) and where it *actually* does — including how AI describes it and which competitors get cited instead.

### Step 1 — Map branded entities
List every way the brand is referred to: main brand name, sub-brands, product names, proprietary features, proprietary metrics, and associated personal brands. (Ahrefs example: brand = Ahrefs; products = Site Explorer, Brand Radar, AI Content Helper; metrics = Domain Rating, Traffic Potential; people = Tim Soulo, Patrick Stokes, Ryan Law, Glen Allsopp.) Each has its own visibility profile — you can repeat the audit for each.

Then connect each entity to the **topics and attributes** people should associate with it. LLMs infer meaning from how a brand is described, so clarify: what problems you solve, what qualities you're known for, what context you belong in. Quick method: keyword research for recurring adjectives/modifiers used alongside the brand or category ("affordable," "AI-powered," "enterprise-grade"). This is the benchmark for what the brand *should* be found for.

### Step 2 — Run the audit in Ahrefs
Enter the site in **Site Explorer** for baseline SEO metrics (DR, referring domains, organic keywords, traffic, traffic value). Then focus on the **AI citation metrics** → click into **Brand Radar** per platform. Four things to record:
- **Mentions** — times the brand is named in AI responses.
- **Citations** — times the website is cited as a source.
- **Impressions** — estimated exposure based on how often brand-containing responses are shown.
- **AI share of voice** — how often the brand is mentioned vs competitors.

Use Brand Radar **filters** to isolate scenarios: prompts mentioning your brand on a chosen platform; responses that mention you but **don't** cite your site (missed citation opportunities); add a competitor and filter for queries where *they're* mentioned but *you're not*; specific topics to see whether AI associates them with you or someone else.

### Step 3 — Identify gaps across 6 dimensions
(Framework from Ahrefs' Sreena.)
1. **Visibility gap** — you appear less often than competitors in search/AI.
2. **Narrative gap** — how AI/media describes you vs how you want to be positioned (e.g., AI calls a premium tool a "budget alternative," or your differentiator isn't coming through).
3. **Topic gap** — topics you should be associated with but aren't (a PM tool never surfaced for "remote team collaboration").
4. **Format gap** — content types AI cites (guides, videos, reviews, comparisons) that you don't produce. Competitors' cited YouTube content + none of yours = a format gap.
5. **Web mentions gap** — listicles, review sites, forums, publications that mention competitors but not you. (One of the strongest AI-visibility signals.)
6. **Demand gap** — branded queries / awareness searches in your space where your name never comes up.

As you audit, bucket each prompt into these dimensions — it sets up prioritization.

### Step 4 — Prioritize
You'll find more gaps than you can fix. Each opportunity is one of: **Fix** (improve something existing), **Build** (create new content/pages for uncovered opportunities), or **Influence** (strengthen offsite visibility via outreach/mentions). Weigh each by: How much demand could this drive? Does it support brand credibility? Does it improve AI-citation chances? Start with quick wins (a ranking page that needs a content update to close a topic gap; a missing listicle all competitors are on → close with outreach).

Most gaps cluster into one or two buckets — that tells you where to build systems. Run the **same audit on competitors** to mine new topics and quick wins (features you have but haven't created connecting content for). Save the baseline; it's the roadmap for the rest of the work.

---

## 2. Keyword & prompt research for AEO

There's heavy overlap with SEO keyword research; half the job is sorting which keywords are SEO vs AEO and treating each differently.

### Step 1 — Build the keyword list
Need two inputs: **seed keywords** (broad niche terms, 1–2 words) and **modifiers** (add-ons like "best," "how-to" that turn seeds into real searches). Fast start — ask an AI assistant:

> "I'm doing keyword research for my [type of site], which makes money through [revenue model]. My target audience is [group]. Give me 10 seed keywords that are 1–2 words max and 5+ modifiers that will help me surface appropriate content formats for keyword research. The seeds and modifiers should not share the same words."

Paste seeds into **Keywords Explorer → Matching terms** report, add modifiers via the **include** filter → hundreds/thousands of real keyword ideas.

### Step 2 — Vet with the BID formula
Before targeting any keyword, it must pass three tests:
- **B — Business potential.** If you rank #1, does it help the business? ("What is espresso?" has volume but no buyer intent; "best espresso machine under $500" shows intent + budget.)
- **I — Intent.** Google it; look at what ranks. If every top result is e-commerce and you have a blog post, you won't rank. Match the SERP intent or move on.
- **D — Difficulty.** Check referring domains and DR of top pages. More links / higher DR = tougher. A few low-DR sites in the top 10 is a good sign.

### Step 3 — Apply the AI filter
One more question: **Can AI fully satisfy the user for this query?** If the AI Overview is so complete there's no reason to click, the keyword may be a trap *for traditional targeting*. Data: AI Overviews appear on ~21% of all keywords, but ~58% of question queries, ~46% of 7+-word queries, and 99.9% of AIO-triggering keywords are informational. Google the keyword, stand in the searcher's shoes, ask "am I satisfied, or do I need to click?"

**Where organic clicks survive AI:** tools. "Backlink checker," "mortgage calculator," "word counter" → no AI Overview, because the user must actually *use* something. In Keywords Explorer → Matching terms, add modifiers: `calculator, checker, generator, tool, template, finder, planner, maker`. Or filter for **transactional** intent directly (buy / sign up / take action).

### Step 4 — Find AI mention opportunities
Keywords AI fully answers shouldn't be ignored — target them *differently*: aim to get the brand **mentioned in the AI response** instead of earning a click. Useful context: ~43.8% of AI-cited pages (AI Overviews + ChatGPT) are **listicles** — they help AI build consensus, so being on multiple lists = multiple sources recommending you.

Method: Brand Radar → enter your site → find your brand → hover the target AI platform → click **"others only"** (shows mention gaps where competitors appear but you don't) → filter queries containing `best, top, versus, review, alternative`. That's your shortlist of queries AI pulls brands from where you're absent. Revisit often: >45% of citations change when AI Overviews refresh, ~every 2 days.

### Step 5 — Prompt research
In ChatGPT / AI Mode / Perplexity people don't type keywords — they have conversations in natural language with full context ("I'm a small agency owner looking for a marketing platform, which should I choose?"). The same question asked 10 ways yields 10 answers with 10 different brands, and each prompt fans out into many zero-volume sub-queries that won't repeat. So you **can't** chase exact prompts one-by-one. If you're invisible for a topic, the fix is **building visibility across the entire topic** — which is what execution covers (`references/execution.md`).
