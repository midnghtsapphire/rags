# Content Generation - LLM Recommendations

**Use for:** Marketing copy, blog posts, social media, emails, articles, creative writing

---

## Recommended Models

### Premium Tier (Highest Quality)

**1. Anthropic Claude 3.5 Sonnet** - `anthropic/claude-3.5-sonnet`
- **Cost:** $3/M input, $15/M output
- **Best for:** High-quality marketing copy, brand voice consistency, long-form articles
- **Why:** Natural writing style, understands nuance, maintains consistent tone
- **Use when:** Customer-facing content, important blog posts, email campaigns

**2. OpenAI GPT-5** - `openai/gpt-5`
- **Cost:** Premium pricing
- **Best for:** Complex narratives, strategic content, whitepapers
- **Why:** Deep thinking, can handle complex requirements
- **Use when:** Strategic content, thought leadership pieces

### Budget Tier (High Volume)

**3. Google Gemini 2.5 Flash** - `google/gemini-2.5-flash`
- **Cost:** $0.075/M input, $0.30/M output (4x cheaper than Claude)
- **Best for:** Bulk content generation, social posts, product descriptions
- **Why:** Fast, cost-effective, good quality for volume work
- **Use when:** Need to generate 100+ social posts, ad variations, product descriptions

**4. Perplexity Sonar** - `perplexity/sonar`
- **Cost:** Mid-range
- **Best for:** SEO articles, fact-backed content, trending topics
- **Why:** Web-aware, cites sources, knows what's trending
- **Use when:** SEO content, review articles, news-based content

### Free Tier (Testing/Drafts)

**5. Arcee AI Trinity Large Preview** - `arcee-ai/trinity-large-preview:free`
- **Cost:** FREE
- **Best for:** Creative writing, storytelling, drafts
- **Why:** 400B parameters, excels at narrative
- **Use when:** Brainstorming, first drafts, creative experimentation

---

## Decision Matrix

| Task | Model | Why |
|------|-------|-----|
| Landing page copy | Claude 3.5 Sonnet | Brand voice critical |
| 100 social posts | Gemini 2.5 Flash | Volume + cost |
| SEO blog article | Perplexity Sonar | Needs citations + trending info |
| Email sequence | Claude 3.5 Sonnet | Persuasion + consistency |
| Product descriptions | Gemini 2.5 Flash | High volume |
| Whitepaper | GPT-5 | Complex strategic thinking |
| Creative story | Trinity Large | Free + creative |
| Ad copy variations | Gemini 2.5 Flash | Need 50+ variations |

---

## Workflow Recommendations

### For Marketing Campaigns:
1. **Brainstorm** with Trinity Large (free)
2. **Refine** with Claude 3.5 Sonnet (premium)
3. **Generate variations** with Gemini 2.5 Flash (budget)

### For SEO Content:
1. **Research** with Perplexity Sonar (web-aware)
2. **Write** with Claude 3.5 Sonnet (quality)
3. **Optimize** with Gemini 2.5 Flash (speed)

### For High-Volume Content:
1. **Template** with Claude 3.5 Sonnet (1 example)
2. **Batch generate** with Gemini 2.5 Flash (100+ items)
3. **QA spot-check** with Claude 3.5 Sonnet (quality control)

---

## Cost Optimization

**Monthly Budget: $50**
- Use Gemini 2.5 Flash for 80% of content (bulk)
- Use Claude 3.5 Sonnet for 15% (critical content)
- Use Trinity Large for 5% (experimentation)

**Monthly Budget: $200**
- Use Claude 3.5 Sonnet for 50% (quality)
- Use Gemini 2.5 Flash for 40% (volume)
- Use GPT-5 for 10% (strategic content)

**Monthly Budget: Unlimited**
- Use Claude 3.5 Sonnet as default
- Use GPT-5 for complex strategy
- Use Gemini 2.5 Flash only for high-volume tasks

---

## Project-Specific Recommendations

### OZ Marketing Suite
- **Primary:** Claude 3.5 Sonnet
- **Fallback:** Gemini 2.5 Flash
- **Reason:** Brand voice consistency critical

### Affiliate Marketing
- **Primary:** Perplexity Sonar
- **Fallback:** Gemini 2.5 Flash
- **Reason:** SEO + product reviews need citations

### Social Media Automation
- **Primary:** Gemini 2.5 Flash
- **Fallback:** Trinity Large
- **Reason:** High volume, lower stakes

---

## Tips

✅ **DO:**
- Use Claude for customer-facing content
- Use Gemini for high-volume tasks
- Use Perplexity for SEO and reviews
- Test with free models first

❌ **DON'T:**
- Use premium models for drafts
- Use free models for customer-facing content
- Use coding models for creative writing
- Forget to specify brand voice in prompts
