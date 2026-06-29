# Schema Markup for AI

Structured data (JSON-LD) that helps AI engines identify content type, extract facts, and validate authority. **Honest framing first:** there's no confirmed data that schema *directly* lifts AI citation (see `references/execution.md` §4.6) — but it's low-cost, it helps traditional SEO (which is the AEO foundation), and it makes your facts machine-extractable. Add appropriate types on pages you already maintain for SEO; don't over-invest in schema *alone* for AEO.

## Table of contents
1. Priority schema types for AEO/GEO
2. High-impact types (FAQPage, HowTo, Article+Author, Speakable)
3. Implementation patterns (@graph, e-commerce)
4. Validation & common mistakes

---

## 1. Priority schema types for AEO/GEO

| Priority | Schema type | AI use case |
|----------|-------------|-------------|
| 1 | FAQPage | Direct Q&A extraction |
| 2 | HowTo | Step-by-step instruction |
| 3 | Article / BlogPosting | Content attribution + freshness (`dateModified`) |
| 4 | Product + Review | E-commerce answers, spec/rating extraction |
| 5 | Organization | Brand knowledge & publisher trust |
| 6 | Person | Author authority (E-E-A-T) |
| 7 | LocalBusiness | Location queries |
| 8 | BreadcrumbList | Topic hierarchy / site structure |

These pair with the content templates in `references/content-templates.md`: definitional/FAQ pages → FAQPage; how-to pages → HowTo; everything → Article+Author.

---

## 2. High-impact types

### FAQPage
Questions should match real user queries (use the clustering method in `references/query-research.md` §2). Answers must be **complete and standalone** — the whole `text` may be lifted by AI. Keep each 50–300 words.

```json
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "What is [topic]?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Complete answer that stands alone. Include key facts, figures, and context — this entire text may be extracted by AI."
      }
    },
    {
      "@type": "Question",
      "name": "How does [topic] work?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Comprehensive but concise explanatory answer."
      }
    }
  ]
}
```

### HowTo
Step names = scannable action phrases; step text = complete, independently understandable instructions. Add `totalTime` when you can.

```json
{
  "@context": "https://schema.org",
  "@type": "HowTo",
  "name": "How to [Action]",
  "description": "Brief overview of what this guide teaches.",
  "totalTime": "PT30M",
  "step": [
    {
      "@type": "HowToStep",
      "position": 1,
      "name": "Step name (action verb)",
      "text": "Detailed, actionable instructions for this step.",
      "image": "https://example.com/step1.jpg"
    },
    {
      "@type": "HowToStep",
      "position": 2,
      "name": "Next step name",
      "text": "Detailed instructions."
    }
  ]
}
```

### Article + Author (E-E-A-T signal)
`author` (Person with credentials + `sameAs`), `publisher` (Organization), and an accurate `dateModified` are the AI-relevant fields — they encode expertise, trust, and freshness.

```json
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "Article title (max ~110 chars)",
  "description": "Comprehensive summary.",
  "image": "https://example.com/image.jpg",
  "datePublished": "2026-01-08T08:00:00Z",
  "dateModified": "2026-06-29T10:00:00Z",
  "author": {
    "@type": "Person",
    "name": "Author Name",
    "url": "https://example.com/author/name",
    "jobTitle": "Subject matter expert",
    "description": "Brief bio establishing expertise.",
    "sameAs": [
      "https://linkedin.com/in/authorname",
      "https://twitter.com/authorname"
    ]
  },
  "publisher": {
    "@type": "Organization",
    "name": "Publisher Name",
    "logo": { "@type": "ImageObject", "url": "https://example.com/logo.png" }
  },
  "mainEntityOfPage": { "@type": "WebPage", "@id": "https://example.com/article-url" }
}
```

### Speakable (voice / AI extraction hint)
Marks the sections best suited to voice reading and summary extraction — point it at your TL;DR / key-takeaway blocks.

```json
{
  "@context": "https://schema.org",
  "@type": "WebPage",
  "name": "Page title",
  "speakable": {
    "@type": "SpeakableSpecification",
    "cssSelector": [".tldr", ".key-takeaway", "#summary"]
  }
}
```

---

## 3. Implementation patterns

### Combined `@graph` for a content page
One block linking Article + FAQPage + BreadcrumbList + Organization + Person via `@id` references. This is the cleanest way to ship multiple types on one page.

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Article",
      "@id": "https://example.com/page#article",
      "headline": "Complete guide to [topic]",
      "author": { "@id": "https://example.com/#author" },
      "publisher": { "@id": "https://example.com/#org" },
      "datePublished": "2026-01-08",
      "dateModified": "2026-06-29"
    },
    {
      "@type": "FAQPage",
      "@id": "https://example.com/page#faq",
      "mainEntity": []
    },
    {
      "@type": "BreadcrumbList",
      "@id": "https://example.com/page#breadcrumb",
      "itemListElement": [
        { "@type": "ListItem", "position": 1, "name": "Home", "item": "https://example.com/" },
        { "@type": "ListItem", "position": 2, "name": "Category", "item": "https://example.com/category/" },
        { "@type": "ListItem", "position": 3, "name": "Page title" }
      ]
    },
    {
      "@type": "Organization",
      "@id": "https://example.com/#org",
      "name": "Company Name",
      "url": "https://example.com",
      "logo": "https://example.com/logo.png"
    },
    {
      "@type": "Person",
      "@id": "https://example.com/#author",
      "name": "Author Name",
      "jobTitle": "Expert title"
    }
  ]
}
```

### E-commerce product page
`Product` (with `offers` and `aggregateRating`) + `FAQPage`. Ratings must be real and match visible content (see mistakes below).

```json
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Product",
      "name": "Product Name",
      "description": "Detailed product description.",
      "image": ["image1.jpg", "image2.jpg"],
      "brand": { "@type": "Brand", "name": "Brand" },
      "offers": {
        "@type": "Offer",
        "price": "99.99",
        "priceCurrency": "USD",
        "availability": "https://schema.org/InStock"
      },
      "aggregateRating": { "@type": "AggregateRating", "ratingValue": "4.5", "reviewCount": "127" }
    },
    {
      "@type": "FAQPage",
      "mainEntity": [
        {
          "@type": "Question",
          "name": "What is included with [Product]?",
          "acceptedAnswer": { "@type": "Answer", "text": "Complete list of what's included…" }
        }
      ]
    }
  ]
}
```

---

## 4. Validation & common mistakes

**Pre-publish checklist:**
- [ ] Passes Google's Rich Results Test
- [ ] Schema matches the visible content exactly (no claims that aren't on the page)
- [ ] `dateModified` is accurate (and reflects a *meaningful* update — see `references/execution.md` §1)
- [ ] Author has real, verifiable credentials
- [ ] FAQ questions match real search queries
- [ ] All URLs are absolute and HTTPS
- [ ] Images are accessible and properly sized

**Common mistakes:**

| Mistake | Why it hurts AI visibility |
|---------|----------------------------|
| FAQ questions no one searches | AI won't surface irrelevant Q&A |
| Exaggerated / fake ratings | Damages trust signals; risks manual action |
| Missing author info | Weakens E-E-A-T |
| Stale `dateModified` | AI prefers fresh content |
| Schema not matching content | Validation failures, ignored markup |
| Overly complex nesting | Harder to parse |

**Lower AI impact (skip unless query-relevant):** Event, Recipe, Video, Music — only worth it when your content *is* that type.
