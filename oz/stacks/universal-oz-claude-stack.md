# Universal OZ - Claude Stack

**Source:** Claude recommendations  
**Last Updated:** 2026-01-30  
**Use for:** Cost-optimized general-purpose tasks with domain flexibility

---

## Stack Overview

This is Claude's recommended stack emphasizing cost optimization and domain-specific capabilities.

---

## API Configuration

```yaml
universal_oz_claude:
  
  architecture_design:
    primary: openai/gpt-5
    secondary: anthropic/claude-opus-4.5
    use_for: "System architecture, complex planning, product strategy"
    
  coding:
    primary: google/gemini-2.5-pro
    secondary: deepseek/v3
    budget: z-ai/glm-4.7-flash
    use_for: "Code generation, refactoring, debugging"
    
  premium_writing:
    primary: anthropic/claude-3.5-sonnet
    budget: google/gemini-2.5-flash
    use_for: "Marketing copy, blog posts, brand voice"
    
  data_analysis:
    primary: anthropic/claude-3-opus
    use_for: "Tables, CSV, structured data, spreadsheets"
    
  automation_agents:
    primary: mistral/mistral-large-2
    secondary: moonshotai/kimi-k2.5
    budget: liquid/lfm2.5-1.2b-thinking:free
    use_for: "Tool-calling, agent loops, workflow automation"
    
  reasoning:
    primary: openai/o1
    budget: liquid/lfm2.5-1.2b-thinking:free
    use_for: "Complex reasoning, multi-step planning"
    
  rag_knowledge:
    primary: cohere/command-r-plus
    secondary: writer/palmyra-x5
    use_for: "RAG systems, document Q&A, knowledge bases"
    
  visual_processing:
    primary: openai/gpt-4-vision
    secondary: google/gemini-2.5-flash
    use_for: "Image analysis, alt text, visual understanding"
    
  visual_coding:
    primary: moonshotai/kimi-k2.5
    secondary: llava
    use_for: "Screenshot → code, UI mockup → components"
    
  bulk_tasks:
    primary: google/gemini-2.5-flash
    secondary: deepseek/v3
    budget: z-ai/glm-4.7-flash
    use_for: "High-volume tasks, cost-sensitive work"
```

---

## Task Routing Matrix

| Task | Primary | Secondary | Budget |
|------|---------|-----------|--------|
| Architecture | GPT-5 | Claude Opus 4.5 | - |
| Coding | Gemini Pro | DeepSeek V3 | GLM 4.7 Flash |
| Writing | Claude Sonnet | - | Gemini Flash |
| Data Analysis | Claude Opus | - | - |
| Automation | Mistral Large 2 | Kimi K2.5 | LiquidAI |
| Reasoning | o1 | - | LiquidAI |
| RAG/Knowledge | Cohere R+ | Palmyra X5 | - |
| Vision | GPT-4 Vision | Gemini Flash | - |
| Visual Coding | Kimi K2.5 | LLaVA | - |
| Bulk Tasks | Gemini Flash | DeepSeek V3 | GLM Flash |

---

## Implementation Example

```typescript
// Claude Universal Router with Cost Tiers
export class ClaudeUniversalRouter {
  static selectModel(task: string, priority: 'quality' | 'cost' | 'speed'): string {
    const routes = {
      architecture: {
        quality: 'openai/gpt-5',
        cost: 'anthropic/claude-opus-4.5',
        speed: 'anthropic/claude-opus-4.5'
      },
      coding: {
        quality: 'google/gemini-2.5-pro',
        cost: 'deepseek/v3',
        speed: 'z-ai/glm-4.7-flash'
      },
      writing: {
        quality: 'anthropic/claude-3.5-sonnet',
        cost: 'google/gemini-2.5-flash',
        speed: 'google/gemini-2.5-flash'
      },
      data_analysis: {
        quality: 'anthropic/claude-3-opus',
        cost: 'anthropic/claude-3-opus',
        speed: 'anthropic/claude-3-opus'
      },
      automation: {
        quality: 'mistral/mistral-large-2',
        cost: 'liquid/lfm2.5-1.2b-thinking:free',
        speed: 'moonshotai/kimi-k2.5'
      },
      bulk: {
        quality: 'google/gemini-2.5-flash',
        cost: 'z-ai/glm-4.7-flash',
        speed: 'z-ai/glm-4.7-flash'
      }
    };
    
    return routes[task]?.[priority] || 'anthropic/claude-3.5-sonnet';
  }
}
```

---

## Cost Optimization Strategy

### Tier 1: Free Models (Development & Testing)
- LiquidAI LFM2.5-1.2B-Thinking - Lightweight reasoning
- Arcee AI Trinity Large Preview - Creative writing
- Monthly Cost: **$0**

### Tier 2: Budget Models ($0.07-0.50/M tokens)
- DeepSeek V3 ($0.14-0.55) - Coding, reasoning
- Z.AI GLM 4.7 Flash ($0.07/$0.40) - Bulk tasks
- Google Gemini 2.5 Flash ($0.075/$0.30) - General purpose
- Monthly Cost: **$50-200** (10M tokens)

### Tier 3: Premium Models ($2.50-15/M tokens)
- Claude 3.5 Sonnet ($3/$15) - Premium content
- Claude Opus ($3/$15) - Data analysis
- Gemini 2.5 Pro ($1.25/$5) - Complex coding
- Mistral Large 2 ($2-4) - Automation
- Monthly Cost: **$200-1000** (1M tokens)

---

## Cost Estimates

### Light Usage (10M tokens/month)
- Bulk (70%): DeepSeek V3 / Gemini Flash - $30
- Writing (20%): Claude Sonnet - $60
- Coding (10%): Gemini Pro - $12.50
- **Estimated Total:** $100-150/month

### Medium Usage (50M tokens/month)
- Bulk (50%): DeepSeek V3 / Gemini Flash - $100
- Writing (20%): Claude Sonnet - $300
- Coding (20%): Gemini Pro / DeepSeek V3 - $100
- Automation (10%): Mistral Large 2 - $100
- **Estimated Total:** $600-800/month

### Heavy Usage (100M tokens/month)
- Bulk (40%): DeepSeek V3 / Gemini Flash - $200
- Writing (20%): Claude Sonnet - $600
- Coding (25%): Gemini Pro / DeepSeek V3 - $200
- Automation (10%): Mistral Large 2 - $200
- Specialized (5%): Various - $100
- **Estimated Total:** $1300-1800/month

---

## Key Advantages

### Cost Optimization
- **DeepSeek V3** - Competitive with GPT-4 at fraction of cost
- **Free tier models** - LiquidAI for testing/development
- **Flexible tiers** - Quality/Cost/Speed options

### Domain Flexibility
- Easy to extend with specialized models
- Built-in support for multilingual (Mistral, Qwen)
- Local deployment options (Llama, DeepSeek)

### Future-Proof
- Includes emerging models (DeepSeek V3, Claude Opus 4.5)
- Open weights options (Llama, Mistral)
- Fine-tuning ready

---

## When to Use This Stack

✅ **Use Claude Universal Stack for:**
- Cost-sensitive projects
- When you need flexible quality/cost tiers
- When domain-specific work is planned (easier to extend)
- When local deployment might be needed
- When multilingual support is important

❌ **Don't use for:**
- When SEO/web-aware content is critical (no Perplexity)
- When cost is not a concern (ChatGPT stack might be simpler)

---

## Comparison with ChatGPT Stack

| Feature | Claude Stack | ChatGPT Stack |
|---------|--------------|---------------|
| Cost Focus | ✅ Highly optimized | Balanced |
| Free Tier | ✅ LiquidAI included | ❌ Not emphasized |
| Budget Options | ✅ DeepSeek V3, GLM | Gemini Flash only |
| SEO Content | ❌ Not included | ✅ Perplexity |
| Multilingual | ✅ Mistral, Qwen | ❌ Not emphasized |
| Local Deployment | ✅ Llama, DeepSeek | ❌ Not emphasized |
| Flexibility | ✅ 3-tier system | Single tier |

**Key Difference:** Claude stack is more cost-conscious with multiple tiers and domain extensibility.

---

## Testing Recommendations

1. **Start with budget tier** for prototyping
2. **Upgrade to quality tier** for production
3. **Compare costs** with ChatGPT stack on same tasks
4. **Track which tier** gives best value for your use cases
5. **Extend with specialized stacks** for domain work

---

## Notes

- Emphasizes cost optimization without sacrificing quality
- Includes emerging cost-effective models (DeepSeek V3)
- Built for extensibility to specialized domains
- Three-tier system (quality/cost/speed) for flexibility
