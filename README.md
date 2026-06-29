# aeo-geo

A Claude [Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for **Answer Engine Optimization (AEO)** — also called Generative Engine Optimization (GEO / LLMO).

It teaches Claude how to get a brand cited, mentioned, and recommended inside AI search (ChatGPT, Google AI Overviews, Google AI Mode, Perplexity, Gemini, Copilot): running brand gap analyses, doing keyword/prompt research for AI, structuring content so AI will quote it (templates, E-E-A-T, schema), winning featured snippets / AI Overviews, earning third-party mentions, optimizing YouTube for AI visibility, fixing AI-crawler issues, auditing a page's AI-readiness, and measuring AI referral traffic and share of voice.

Built on the Ahrefs AEO methodology, extended with content templates, JSON-LD schema patterns, AI-crawler configs, tool-agnostic query research, and a 100-point AI-readiness audit. Pairs with Ahrefs MCP tools.

**Created by [CodingPhase.com](https://codingphase.com). Maintained by [CodingPhase.com](https://codingphase.com).**

## What's inside

```
aeo-geo/
├── SKILL.md                         # Router + core mechanics + E-E-A-T/CRASP frameworks + AI-readiness audit
└── references/
    ├── how-ai-search-works.md       # RAG vs training data, query fan-out, platforms, visibility types
    ├── strategy-and-research.md     # Brand gap analysis + keyword/prompt research (BID formula)
    ├── query-research.md            # Tool-agnostic query discovery, question clustering, intent, AI-platform testing
    ├── execution.md                 # Cited content, earning mentions, YouTube, technical AEO
    ├── content-templates.md         # Copy-paste page skeletons (definitional, how-to, comparison, FAQ) + writing rules
    ├── schema-for-ai.md             # JSON-LD patterns (FAQPage, HowTo, Article+Author, Speakable, @graph)
    ├── ai-crawlers.md               # robots.txt configs, search-vs-training bots, crawler monitoring
    └── measurement-and-roi.md       # Tracking pillars, ROI, action plan
```

The skill uses progressive disclosure: `SKILL.md` is a lightweight router, and Claude loads the relevant reference file only when a task calls for it.

## Install

Download `aeo-geo.skill` from the [Releases](../../releases) page (or build it yourself — see below) and upload it to Claude under **Settings → Capabilities → Skills**.

## Build the `.skill` file from source

A `.skill` file is just a zip of the skill folder:

```bash
zip -r aeo-geo.skill aeo-geo
```

## License

MIT — see [LICENSE](LICENSE).
