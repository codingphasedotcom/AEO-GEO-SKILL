# AI Crawlers & Bot Management

The deep-dive companion to `references/execution.md` §4.1. Goal: make sure the AI bots you *want* can reach your content, and decide deliberately about the ones you don't. ~5.9% of 140M sites block GPTBot — often unintentionally via inherited templates or platform defaults (Cloudflare now auto-adds AI blocks). Don't be invisible by accident.

## Table of contents
1. Crawler overview (search vs training)
2. robots.txt configurations (balanced / max visibility / max protection)
3. Crawl behavior & what AI indexes
4. Strategic decision matrix
5. Implementation, monitoring & verification
6. Emerging crawlers to watch

---

## 1. Crawler overview

The key distinction is **search/citation bots** (let these in for AI visibility) vs **training bots** (block only if you care about your content being used for model training — blocking them does *not* improve, and may reduce, your presence in answers).

| Crawler | Company | Purpose | Default recommendation |
|---------|---------|---------|------------------------|
| Googlebot | Google | Traditional search indexing | **Always allow** |
| Bingbot | Microsoft | Bing + Copilot search index | **Always allow** |
| OAI-SearchBot | OpenAI | ChatGPT Search results | Allow (visibility) |
| ChatGPT-User | OpenAI | User-requested page fetch | Allow (UX) |
| PerplexityBot | Perplexity | Search & answers | Allow (visibility) |
| ClaudeBot | Anthropic | Claude features | Allow (visibility) |
| GPTBot | OpenAI | Model **training** | Block if training is a concern |
| Google-Extended | Google | Gemini **training** | Block if concern; allow for AI reach |
| CCBot | Common Crawl | Open dataset collection | Consider blocking |
| Bytespider | ByteDance | TikTok / training | Consider blocking |
| FacebookBot | Meta | Meta AI training | Consider blocking |

```
SEARCH / CITATION (allow for visibility):
  Googlebot · Bingbot · OAI-SearchBot · ChatGPT-User · PerplexityBot · ClaudeBot

TRAINING (block only if data protection matters):
  GPTBot · Google-Extended · CCBot · Bytespider · FacebookBot
```

---

## 2. robots.txt configurations

### Balanced (recommended for most) — allow search, block training
```txt
# ===== AI SEARCH CRAWLERS — ALLOW =====
User-agent: OAI-SearchBot
Allow: /

User-agent: ChatGPT-User
Allow: /

User-agent: PerplexityBot
Allow: /

User-agent: ClaudeBot
Allow: /

# ===== AI TRAINING CRAWLERS — BLOCK =====
User-agent: GPTBot
Disallow: /

User-agent: Google-Extended
Disallow: /

User-agent: CCBot
Disallow: /

User-agent: Bytespider
Disallow: /

User-agent: FacebookBot
Disallow: /

# ===== TRADITIONAL SEARCH — ALLOW =====
User-agent: Googlebot
Allow: /

User-agent: Bingbot
Allow: /

User-agent: *
Allow: /

Sitemap: https://example.com/sitemap.xml
```

### Maximum visibility — allow everything
```txt
User-agent: *
Allow: /

Sitemap: https://example.com/sitemap.xml
```

### Maximum protection — traditional search only, block all AI
```txt
User-agent: Googlebot
Allow: /

User-agent: Bingbot
Allow: /

User-agent: GPTBot
Disallow: /

User-agent: OAI-SearchBot
Disallow: /

User-agent: ChatGPT-User
Disallow: /

User-agent: Google-Extended
Disallow: /

User-agent: PerplexityBot
Disallow: /

User-agent: ClaudeBot
Disallow: /

User-agent: CCBot
Disallow: /

User-agent: *
Disallow: /
```

> Note: blocking search/citation bots (OAI-SearchBot, PerplexityBot, ClaudeBot) removes you from those AI answers entirely. Only choose "maximum protection" if staying out of AI is an explicit business decision.

---

## 3. Crawl behavior & what AI indexes

| Crawler | Respects robots.txt | Crawl rate | JS rendering |
|---------|---------------------|------------|--------------|
| Googlebot | Yes | Adaptive | Yes (2nd wave) |
| GPTBot | Yes | Unknown | Limited |
| OAI-SearchBot | Yes | Unknown | Limited |
| ChatGPT-User | Yes | On-demand | **No** (treat as no-JS) |
| PerplexityBot | Yes | Moderate | Limited |
| ClaudeBot | Yes | Unknown | Limited |
| CCBot | Generally yes | Heavy | No |

**Typically indexed:** body content, headings (H1–H6), meta descriptions, alt text, JSON-LD structured data, tables, lists.

**Often missed:** JavaScript-rendered content, content behind tabs/accordions, lazy-loaded media, PDF content, video transcripts not in HTML, iframe content.

Implication: server-side render anything important (see `references/execution.md` §4.3), and keep critical content in the initial HTML, not hidden behind interaction.

---

## 4. Strategic decision matrix

| Business type | Strategy | Reasoning |
|---------------|----------|-----------|
| Publisher / blog | Allow search, block training | Keep traffic, protect content from training |
| E-commerce | Allow all | Maximum product visibility |
| SaaS | Allow search, consider training | Brand visibility; may protect proprietary docs |
| Enterprise B2B | Selective allow | Control information flow |
| Personal brand | Allow all | Maximum reach |
| Research / academic | Allow all | Citation and reach |

**Four questions to decide:**
1. Is being cited by AI valuable to you? Yes → allow search crawlers.
2. Concerned about training on your content? Yes → block GPTBot, Google-Extended.
3. Do users ask AI to read your pages? Yes → allow ChatGPT-User.
4. Is your content frequently updated / time-sensitive? Yes → allow all search crawlers for freshness.

---

## 5. Implementation, monitoring & verification

**Audit current config:**
```bash
# View current robots.txt
curl -s https://yoursite.com/robots.txt

# Test specific bot access (does it get 200 or 403?)
curl -A "GPTBot" -I https://yoursite.com/
curl -A "OAI-SearchBot" -I https://yoursite.com/
```

**Monitor crawler activity in server logs:**
```bash
grep -E "GPTBot|OAI-SearchBot|ChatGPT-User|PerplexityBot|ClaudeBot" access.log \
  | awk '{print $1, $7}' | sort | uniq -c | sort -rn
```
(Easier alternative: Ahrefs **Bot Analytics** via the free Cloudflare integration — see `references/measurement-and-roi.md` §1 Pillar 2.)

**Block at the WAF if robots.txt isn't enough (Cloudflare example):**
```
(cf.client.bot and http.user_agent contains "GPTBot")
```

**Verify after changes:**
```bash
curl -s https://yoursite.com/robots.txt | grep -A2 "GPTBot"
curl -A "GPTBot" -s -o /dev/null -w "%{http_code}\n" https://yoursite.com/
```

**Track impact:** AI referral traffic, brand mentions in AI responses (manual testing — see `references/query-research.md` §4), and overall organic traffic (confirm no negative side effects).

---

## 6. Emerging crawlers to watch

| Bot | Company | Status | Notes |
|-----|---------|--------|-------|
| MistralBot | Mistral AI | Emerging | European AI |
| DeepSeekBot | DeepSeek | Emerging | Chinese AI |
| GrokBot | xAI | Active/expanding | Grok / X |
| MetaAI-SearchBot | Meta | Expected | Meta AI search |

Recommendation: re-check your robots.txt against new user-agents **quarterly** — the crawler landscape shifts fast.
