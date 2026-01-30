# Universal OZ - ChatGPT Stack

**Source:** ChatGPT recommendations  
**Last Updated:** 2026-01-30  
**Use for:** General-purpose tasks across all projects

---

## Stack Overview

This is ChatGPT's recommended "TRUE Ideal Router" for Mechatronopolis projects.

---

## API Configuration

```yaml
universal_oz_chatgpt:
  
  architecture_design:
    primary: openai/gpt-5
    use_for: "App idea → architecture, system design, product strategy"
    
  automation_agents:
    primary: mistral/mistral-large
    use_for: "Automation / agents, tool-calling, workflow orchestration"
    
  seo_content:
    primary: perplexity/sonar
    use_for: "SEO / reviews / affiliate content, trending topics"
    
  knowledge_base:
    primary: cohere/command-r-plus
    use_for: "Knowledge base / docs, RAG systems, document Q&A"
    
  premium_writing:
    primary: anthropic/claude-3.5-sonnet
    use_for: "Premium writing, marketing copy, brand voice"
    
  data_analysis:
    primary: anthropic/claude-3-opus
    use_for: "Data / tables / CSV, structured data reasoning"
    
  coding:
    primary: google/gemini-2.5-pro
    use_for: "Coding, refactoring, architecture"
    
  bulk_tasks:
    primary: google/gemini-2.5-flash
    fallback: z-ai/glm-4.7-flash
    use_for: "Cheap bulk tasks, high-volume generation"
    
  visual_coding:
    primary: kimi/vision
    fallback: llava
    use_for: "Image → UI/code, screenshot to React"
    
  vision_alt_text:
    primary: openai/gpt-4-vision
    use_for: "Vision alt text, image analysis"
    
  long_documents:
    primary: writer/palmyra-x5
    use_for: "Long docs, 1M token context processing"
```

---

## Task Routing Matrix

| Task | Model | Why |
|------|-------|-----|
| App idea → architecture | GPT-5 | Best at system design thinking |
| Automation / agents | Mistral Large | Best tool-calling |
| SEO / reviews / affiliate | Perplexity | Web-aware, cites sources |
| Knowledge base / docs | Cohere Command R+ | RAG expertise |
| Premium writing | Claude Sonnet | Brand voice consistency |
| Data / tables / CSV | Claude Opus | Structured data king |
| Coding | Gemini Pro | #1 coding benchmarks |
| Cheap bulk tasks | Gemini Flash / GLM | Cost-effective volume |
| Image → UI/code | Kimi Vision / LLaVA | Visual coding |
| Vision alt text | GPT-4 Vision | Best image understanding |
| Long docs | Palmyra X5 | 1M token context |

---

## Implementation Example

```typescript
// ChatGPT Universal Router
export class ChatGPTUniversalRouter {
  static selectModel(task: string): string {
    const routes = {
      'architecture': 'openai/gpt-5',
      'automation': 'mistral/mistral-large',
      'seo': 'perplexity/sonar',
      'knowledge_base': 'cohere/command-r-plus',
      'writing': 'anthropic/claude-3.5-sonnet',
      'data_analysis': 'anthropic/claude-3-opus',
      'coding': 'google/gemini-2.5-pro',
      'bulk': 'google/gemini-2.5-flash',
      'visual_coding': 'kimi/vision',
      'vision': 'openai/gpt-4-vision',
      'long_docs': 'writer/palmyra-x5'
    };
    
    return routes[task] || 'anthropic/claude-3.5-sonnet';
  }
}
```

---

## Cost Estimates

### Light Usage (10M tokens/month)
- Bulk tasks (60%): Gemini Flash - $45
- Premium writing (20%): Claude Sonnet - $60
- Coding (10%): Gemini Pro - $12.50
- Architecture (10%): GPT-5 - Premium pricing
- **Estimated Total:** $150-250/month

### Medium Usage (50M tokens/month)
- Bulk tasks (50%): Gemini Flash - $187.50
- Premium writing (20%): Claude Sonnet - $300
- Coding (15%): Gemini Pro - $93.75
- Automation (10%): Mistral Large - $100-150
- Architecture (5%): GPT-5 - Premium pricing
- **Estimated Total:** $700-1000/month

### Heavy Usage (100M tokens/month)
- Bulk tasks (40%): Gemini Flash - $300
- Premium writing (20%): Claude Sonnet - $600
- Coding (20%): Gemini Pro - $250
- Automation (10%): Mistral Large - $200-300
- Specialized (10%): Various - $200-400
- **Estimated Total:** $1500-2500/month

---

## When to Use This Stack

✅ **Use ChatGPT Universal Stack for:**
- General-purpose projects
- When you need web-aware content (Perplexity)
- When SEO and affiliate content is priority
- When you want "research-lab level" capabilities
- When cost optimization is important (Gemini Flash for bulk)

❌ **Don't use for:**
- Domain-specific work (insurance, healthcare, etc.) - use specialized stacks
- When you need multilingual support - use Claude stack or specialized models
- When you need local deployment - use Llama-based stacks

---

## Comparison with Claude Stack

| Feature | ChatGPT Stack | Claude Stack |
|---------|---------------|--------------|
| Architecture | GPT-5 | GPT-5 |
| Automation | Mistral Large | Mistral Large |
| SEO Content | ✅ Perplexity | ❌ Not included |
| Writing | Claude Sonnet | Claude Sonnet |
| Data Analysis | Claude Opus | Claude Opus |
| Coding | Gemini Pro | Gemini Pro / DeepSeek V3 |
| Bulk Tasks | Gemini Flash | Gemini Flash / DeepSeek V3 |
| Cost Focus | Balanced | More cost-conscious |

**Key Difference:** ChatGPT stack includes Perplexity for SEO/web-aware content, which Claude's stack doesn't emphasize.

---

## Testing Recommendations

1. **Start with this stack** for general projects
2. **Compare with Claude stack** on same tasks
3. **Track which performs better** for your specific use cases
4. **Switch to specialized stacks** for domain work (insurance, healthcare, etc.)

---

## Notes

- This is a "research-lab level stack, not hobbyist" per ChatGPT
- Focuses on best-in-class for each capability
- Balances quality and cost
- Web-aware content is a key differentiator
