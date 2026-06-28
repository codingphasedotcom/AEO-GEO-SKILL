# aeo-geo

A Claude [Agent Skill](https://docs.claude.com/en/docs/agents-and-tools/agent-skills/overview) for **Answer Engine Optimization (AEO)** — also called Generative Engine Optimization (GEO / LLMO).

It teaches Claude how to get a brand cited, mentioned, and recommended inside AI search (ChatGPT, Google AI Overviews, Google AI Mode, Perplexity, Gemini, Copilot): running brand gap analyses, doing keyword/prompt research for AI, structuring content so AI will quote it, earning third-party mentions, optimizing YouTube for AI visibility, fixing AI-crawler issues, and measuring AI referral traffic and share of voice.

Built on the Ahrefs AEO methodology. Pairs with Ahrefs MCP tools.

**Created by [CodingPhase.com](https://codingphase.com). Maintained by [CodingPhase.com](https://codingphase.com).**

## What's inside

```
aeo-geo/
├── SKILL.md                         # Router + always-loaded core mechanics
└── references/
    ├── how-ai-search-works.md       # RAG vs training data, query fan-out, platforms, visibility types
    ├── strategy-and-research.md     # Brand gap analysis + keyword/prompt research (BID formula)
    ├── execution.md                 # Cited content, earning mentions, YouTube, technical AEO
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
