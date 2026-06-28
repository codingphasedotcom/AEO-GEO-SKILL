# AEO Execution

The actual work: create content that gets cited, earn mentions on other people's pages, optimize YouTube, and clear the technical path so AI can crawl you.

## Table of contents
1. Create content that gets cited (data + 4 structure principles + 2 amplifiers)
2. Earn mentions & citations (3 tiers + how to find targets + auditing mentions)
3. YouTube optimization for AI (3 steps)
4. Technical AEO (6 checks)

---

## 1. Create content that gets cited

### What the data says AI cites
- **Length doesn't matter.** Across 174,000+ AIO-cited pages, word-count↔citation correlation is ~0.04 (basically zero). Over half (53.4%) of cited pages are under 1,000 words. Stop padding to 3,000 words for AEO — AI cares whether the page answers the question.
- **Freshness matters a lot.** AI-cited content is ~25.7% fresher than traditional organic results. For ChatGPT specifically, 89.7% of top-cited pages were updated in 2025 and ~76% within the last 30 days. Content untouched for 6 months is already at a disadvantage. (But don't just change the publish date — Google detects that; make *meaningful* updates.)
- **Format matters.** ~43.8% of ChatGPT-cited pages are listicles (best X, top X, comparisons, reviews) — they give clear structured recommendations AI can lift. Also heavily cited: data-driven content with original stats (AI loves citing specific numbers) and comparison "X vs Y" pages (they map to how people ask AI).

Takeaway: keep content **fresh**, **focused**, and lean into formats AI can use.

### Structure: write for humans; AI is trained on what humans value
There's no special "AI format." But four principles help both:

1. **BLUF — Bottom Line Up Front.** Start every section with the answer, not backstory. Humans scan in an F-pattern (read the start, skim the middle); LLMs similarly weight the beginning and end of a passage over the middle. Don't bury the key point three paragraphs in.
   - Weak: "Over the past few years, link-building strategies have evolved significantly…"
   - Strong: "The most effective way to build backlinks in 2026 is to create original research."

2. **Atomic content.** Every section should stand on its own. AI chunks content into pieces and you can't control where the chunks fall — if each section is self-contained, the meaning survives. Test: read any H2 fully out of context; if it doesn't make sense alone, rewrite it.

3. **Entity-rich writing.** AI understands text via entities (brands, products, people, places, specific concepts) and their relationships. Give it more to work with.
   - Weak: "This tool helps with SEO."
   - Strong: "Ahrefs Keywords Explorer helps you find keywords with low difficulty and high traffic potential."

4. **Simple & declarative.** Short sentences, clear subject-verb-object, one idea per sentence. Not dumbing down — making it easy to parse. If a sentence needs two reads, simplify.

### Two amplifiers
- **Name your ideas to beat originality-flattening.** LLMs absorb original concepts without crediting the source, folding them into general knowledge. Counter by labeling ideas with the brand: not "content scoring matrix" but "the [Brand] Content Scoring Matrix." Define it explicitly and distribute it widely (blog, social, podcasts, Reddit). The more places it appears with your name attached, the harder it is to flatten.
- **Refresh "sleeper pages."** Pages that used to rank well and have declined already have the backlinks/authority — they just need a refresh, and freshness is a strong AI signal. Find them: Site Explorer → your domain → **Top pages** → sort by **traffic change** → look for pages with significant declines **and** a decent number of backlinks. Verify it's a content issue, not a links issue: if the page never had referring domains, updating won't help; if it has links and stale content, high-potential.

---

## 2. Earn mentions & citations

A lot of SEO/AEO isn't on your site — it's getting mentioned on the pages AI already pulls from. Branded web mentions had the strongest correlation (~0.664) with AIO visibility in a 75,000-brand study; mentions on **highly-linked** pages correlate ~0.7. Where you're mentioned matters as much as how often.

### Tier 1 — Third-party editorial content (hardest, most valuable)
Industry publications, review sites (Wirecutter, TechRadar), listicles/comparison posts on authoritative blogs, YouTube reviews. These are exactly what AI loves to cite (~43.8% of ChatGPT citations are listicles/comparisons).
- Find target sites: Brand Radar → enter your domain → **cited domains** report → see the top sites AI cites for your topics (e.g., kbb.com for cars, CNET for tech, niche blogs).
- Don't wait for a page to be cited — target pages that already have many links and cover your topic; they'll likely get cited eventually. **Content Explorer**: search your title + `title:best` or `title:versus`, add a **minus operator before your brand name** to surface listicles/comparisons where you're absent, then filter for a good number of referring domains.

### Tier 2 — User-generated content & community platforms
Reddit, Quora, niche forums. Reddit is one of ChatGPT's most-cited sources and a foundational LLM training source. **Don't spam** — find threads where people ask questions your product/expertise genuinely answers and contribute a real answer. Find them via Brand Radar cited-domains (does reddit.com show up for your space? which threads is AI pulling from?). To find niche Reddit pages already ranking: Site Explorer → reddit.com → **Organic keywords** → filter top-5 rankings → add your niche terms to the include filter. Same trick works for niche forums and Q&A sites.

### Tier 3 — Your own properties
Additional owned domains (Ahrefs owns detailed.com, bloggerjet) can be citation sources if authoritative. Even without multiple sites, the principle holds: your YouTube channel, podcast, and LinkedIn content are all indexed and can surface as AI sources. More positive, topically-relevant places your brand appears = more training examples.

### Audit your mentions regularly
Mentions disappear (pages update, lists refresh) and AI can pick up wrong info from outdated sources. In Brand Radar, track overall mention trends over time; investigate drops. Watch **sentiment** — are responses accurate and positive? If you spot misinformation, **update your own content first**, then reach out to the publisher for a correction. The faster you fix it, the less time AI has to learn the bad info.

---

## 3. YouTube optimization for AI

Why it gets its own lesson: YouTube is the most-cited domain in Google AI Overviews, and YouTube mentions have a ~0.737 correlation with ChatGPT visibility — the strongest single factor studied. (GPT-4 was trained on 1M+ hours of YouTube transcripts — AI doesn't just cite YouTube, it *learns* from it.)

### Step 1 — Find what's already working (search hits, not viral hits)
A viral hit spikes then dies once the algorithm exhausts interested viewers. A **search hit** earns consistent Google + YouTube search traffic month after month — and if Google already ranks a video for a keyword, AI Overviews likely cite it too. Search-hit titles are also clearer about content. Find them: Site Explorer → enter `www.youtube.com/watch` → **Organic keywords** → filter **top-3** rankings → add niche terms to the include filter.

### Step 2 — Create videos that rank (checklist)
1. **Title contains the searched keyword** — not clickbait. If the keyword is "How to use Google Docs," put it in the title. Save creativity for the thumbnail (title = keyword, thumbnail = the click).
2. **Description is a real summary** with the target keyword in the first couple of lines. Google, AI, and viewers all read it.
3. **Add timestamps** → they become YouTube chapters, which can surface in Google for specific queries. Free extra visibility for ~2 minutes of work.
4. **Say the keyword in the video.** Google understands audio/video (per VP of Search Liz Reid). If the video is about "best protein powder for repair," actually say those words.
5. **Match the ranking format.** If tutorials dominate the SERP, make a tutorial; if listicles rank, make a listicle. Match the searcher's intent.

### Step 3 — Layer in AI visibility
Brand Radar → enter a popular brand/YouTube channel → **topics** report → set filter where **domain mentioned = youtube.com** → see which queries AI pulls YouTube videos into → create content around those topics. Rank the same way as above. Remember every published video is potential training data — even uncited videos are absorbed.

---

## 4. Technical AEO

Not about rewriting code — about making sure AI can **access and understand** content. ~5.9% of 140M sites block GPTBot (OpenAI's crawler), often unintentionally — millions invisible to ChatGPT.

1. **robots.txt** — beyond Googlebot, there are now many AI bots. Key ones: **GPTBot** and **OAI-SearchBot** (OpenAI), **ClaudeBot** (Anthropic), **Google-Extended** (Google). Check `yourdomain.com/robots.txt` for `Disallow` rules next to any of those. Watch for inherited template rules and platform defaults — Cloudflare's "instruct AI bot traffic with robots.txt" feature is now on by default and auto-adds AI blocks. Ahrefs **Site Audit** flags blocking rules.

2. **llms.txt (note, don't prioritize).** A proposed standard like robots.txt that summarizes your site for AI at `yourdomain.com/llms.txt`. As of now **no major LLM provider officially supports it** (OpenAI doesn't use it; Anthropic publishes one but hasn't confirmed crawlers read it; Google hasn't adopted it). Won't hurt, but robots.txt matters far more right now.

3. **JavaScript rendering.** Gemini and Copilot can render JS; **ChatGPT's crawler does not**. If content relies on JS to load (SPAs, some React/Angular), ChatGPT sees an empty shell. Fix: **server-side rendering** (server sends fully-rendered HTML). If you already do SSR for SEO, you're covered. Quick test: disable JS in your browser, load your page — if content disappears, you have a problem.

4. **Page speed.** Matters *more* for AI retrieval than for SEO: AI fetches/parses/chunks pages on the fly, and a slow page can be dropped before it's even scored. If core web vitals are already optimized, you're most of the way there.

5. **Clean HTML structure.** AI parses by following HTML. Use proper hierarchy (one H1, H2 for main sections, H3 for subsections); keep paragraphs to one idea. This makes BLUF / atomic / entity-rich content technically parsable — each section should stand alone because AI may chunk at any heading boundary.

6. **Schema markup (mixed evidence).** Article, FAQPage, HowTo, LocalBusiness schema help engines understand content. No confirmed data that it directly improves AI citation, but it doesn't hurt — keep it if you use it for SEO; add appropriate types on new pages, but don't over-invest for AEO alone.

7. **Optimize AI-hallucinated URLs.** AI assistants invent URLs that 404 — they send visitors to 404s ~2.87× more often than Google Search, and ChatGPT is the biggest offender (~1% of clicked URLs 404). Check analytics for pages getting AI-referrer traffic but returning 404; for consistent hallucinated URLs, set up a redirect to the most relevant real page to capture otherwise-lost traffic.
