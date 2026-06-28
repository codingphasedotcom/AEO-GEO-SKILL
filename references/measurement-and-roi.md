# Measurement, ROI & Action Plan

AI visibility is harder to measure than SEO and analytics undercount it — but you're not flying blind. Triangulate three tracking pillars, judge ROI honestly, then run the prioritized action plan.

## Table of contents
1. Three tracking pillars (referral traffic, bot activity, self-reported attribution)
2. Is AEO worth it? (ROI framing)
3. How to know if you're making progress
4. AI misinformation risk
5. The AEO action plan (first week + ongoing) ← good entry point for a broad request

---

## 1. Three tracking pillars

No single source gives the full picture. Used together: referral traffic shows what AI sends you, bot analytics show what AI pays attention to, self-attribution shows what drives revenue.

### Pillar 1 — AI referral traffic
Clicks from ChatGPT/Perplexity/Claude/etc. landing on your site, shown as referral visits in GA4 or Ahrefs Web Analytics. **Caveat: undercounted.** Many platforms strip referral data, so visits show as direct traffic. Specifics: ChatGPT search-result source links pass referral data, but in-content links on paid accounts use a `no-referrer` attribute (invisible); Claude tracks properly; Perplexity tracks on web but not its desktop app; Copilot tracks on web but not Windows; Grok passes nothing. Treat referral data as a directional trend, not a precise count.

Set up a custom channel in GA4: Admin → Data Display → Channel Groups → copy the default → add a channel "AI traffic" → set source to a regex including `chat.openai.com`, `perplexity`, `gemini.google.com`, `copilot.microsoft.com`, `claude.ai`, `deepseek.com`. Then Reports → Acquisition → Traffic Acquisition → select the new group. Simpler alternative: **Ahrefs Web Analytics** has a built-in AI search channel (no setup) and separates *unknown* from *direct* traffic (GA4 doesn't), giving a clearer origin picture.

What to watch: (a) which pages get AI traffic — these are the pages AI already recommends; keep them updated, accurate, with clear CTAs. (b) Important pages getting **zero** AI traffic that should — investigate (content issue, crawl issue, or AI just hasn't surfaced the topic yet).

### Pillar 2 — AI bot activity
Track the crawlers themselves, not the humans. AI bots hit your pages far more than humans do, so the most-crawled pages are your strongest citation candidates. Two bot types: **training bots** (GPTBot, Google-Extended — feed model training) and **search/citation bots** (ChatGPT-User, OAI-SearchBot — fetch pages in real time and can drive referral traffic). Track via server logs, or more easily **Ahrefs Bot Analytics** (Cloudflare integration, works on the free Cloudflare plan) showing which AI bots visit, how often, which pages. Look for patterns: a citation bot repeatedly hitting a page = that page is likely a source in AI responses; important pages bots ignore = discoverability problem (revisit internal linking / site structure).

### Pillar 3 — Self-reported attribution (often the most important)
Much AI impact never shows in analytics: someone asks ChatGPT, gets your name, then types your URL directly (→ direct traffic) or Googles your brand (→ organic). The only way to capture it: **ask**. Add a "How did you hear about us?" question to sign-up / checkout / post-purchase, with options like ChatGPT, Perplexity, AI assistant, Google AI Overviews. (Ahrefs: ~3% of conversions came from AI over the past year by self-report, converting far above organic — invisible without asking.) If you do one thing from this section, add that question.

Plus, **Brand Radar** continues tracking AI share of voice across platforms (set up in the strategy phase).

---

## 2. Is AEO worth it?

By raw traffic, AI search is still small: AI referral traffic averages ~0.25% of total site traffic, and Google sends ~210× more traffic than the top AI platforms combined. But:
- **Conversion quality is dramatically higher.** Ahrefs' AI visitors convert at ~23× the rate of organic search. Vercel sees ~10% conversion from AI traffic; Tally calls AI its largest acquisition channel (helped add ~$1M ARR). AI recommendations arrive pre-qualified — the AI already explained why you fit.
- **It's growing fast** — ~9.7× since last year; ChatGPT up ~85% since January, now sending more traffic than Reddit or LinkedIn.
- **The real value is brand awareness inside the conversation** — every recommendation/mention is an impression that often drives a later branded search or social engagement, even with no click. AEO is a new layer on top of SEO; brands that build it early gain a compounding advantage.

The honest downside: it's not perfectly measurable — like brand marketing, you can't trace every billboard to a sale, but it shapes how people think of you. Can't-measure ≠ not-working.

---

## 3. How to know if you're making progress
Return to the Brand Radar baseline (from the strategy phase) and check four things:
1. **AI share of voice** — moved relative to competitors? Grew = working; flat while a competitor grew = dig into why.
2. **Cited domains** — new domains citing you that weren't before? Validates the mention-earning work.
3. **Topic coverage** — closed the gaps you identified? New topics where you now appear?
4. **Mention sentiment** — is AI saying accurate, positive things? Critical, because AI synthesizes from everywhere, not just your site.

Cadence: quick **monthly** Brand Radar check; deeper **quarterly** competitive audit.

---

## 4. AI misinformation risk
AI is vulnerable to planted misinformation. In an Ahrefs test (fake luxury brand, three contradicting sources across a blog, Reddit, and Medium, asked of 8 platforms), Gemini and Perplexity repeated the misinformation in ~37–39% of answers (fake founders, cities, pricing as "fact"); ChatGPT was more robust (<7%, citing the official FAQ in 84% of answers). Implication: **fill every information gap about your brand with specific, official content** — an FAQ that directly answers common questions, with specific numbers/dates/facts, because when AI must choose between vague truth and specific fiction it tends to pick the specific fiction. Monitor what AI says; if it's wrong, publish content on your own site that directly contradicts it, then get the third-party source corrected.

---

## 5. The AEO action plan

For a broad "help me start with AEO" request, this is the entry point. **This week:**
1. **Check robots.txt for AI bot access** (~5 min) — the most common technical blocker. Make sure GPTBot, OAI-SearchBot, ClaudeBot, Google-Extended aren't disallowed. → see `references/execution.md` §4.
2. **Set up AI analytics** — create the GA4 AI traffic channel or use Ahrefs Web Analytics, and add the "How did you hear about us?" question now so you measure from day one. → §1 above.
3. **Update your top 5–10 pages for freshness** — AI-cited content is ~25.7% fresher than traditional SERP results. Make meaningful updates (new stats, current examples), not just date changes. → `references/execution.md` §1.
4. **Run your brand gap analysis** — set up Brand Radar, find where you stand before optimizing. → `references/strategy-and-research.md` §1.
5. **Identify your top 10 mention-earning targets** — use cited-domains and Content Explorer to find pages where a mention would move AI visibility most. → `references/execution.md` §2.

**Ongoing:** monthly Brand Radar check + quarterly competitive audit, then rinse and repeat.

The biggest advantage available right now is simply starting before competitors do — AI search is still early, the tools and data are improving, and the opportunity only grows.
