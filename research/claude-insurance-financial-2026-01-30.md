# Insurance & Financial Services - Domain-Specific LLMs

**Source:** Claude analysis  
**Last Updated:** 2026-01-30

---

## Recommended Models

### Contract Analysis & Compliance

**1. Anthropic Claude 3.5 Sonnet** - `anthropic/claude-3.5-sonnet`
- **Cost:** $3/M input, $15/M output
- **Best for:** Insurance contracts, compliance documents, policy analysis
- **Why:** Excellent at parsing complex legal/insurance language, careful about accuracy
- **Use when:** Analyzing policies, compliance review, contract interpretation

### Risk Assessment & Underwriting

**2. OpenAI GPT-4** - `openai/gpt-4-turbo`
- **Cost:** $2.50/M input, $10/M output
- **Best for:** Underwriting analysis, risk modeling
- **Why:** Strong mathematical reasoning for risk assessment
- **Use when:** Evaluating applications, risk calculations, underwriting decisions

### Financial Research & Regulatory Documents

**3. Cohere Command R+** - `cohere/command-r-plus`
- **Cost:** Mid-range
- **Best for:** Regulatory document retrieval, compliance research
- **Why:** Excellent RAG capabilities for grounding answers in regulatory docs
- **Use when:** Researching regulations, compliance questions, policy lookups

### Specialized Financial Models

**4. Bloomberg GPT** (if accessible)
- **Cost:** Enterprise only
- **Best for:** Financial analysis, market data, trading insights
- **Why:** Trained on 40+ years of financial data and regulations
- **Access:** Requires Bloomberg Terminal subscription (~$24K/year)

**5. FinGPT** (Open Source)
- **Cost:** FREE
- **Best for:** Financial sentiment analysis, market analysis
- **Why:** Fine-tuned on financial news, filings, SEC reports
- **Use when:** Analyzing market sentiment, financial news, earnings reports

---

## Task-Specific Recommendations

| Task | Primary Model | Why |
|------|---------------|-----|
| Insurance contract analysis | Claude 3.5 Sonnet | Best at legal nuance |
| Risk modeling | GPT-4 or o1 | Mathematical reasoning |
| Regulatory compliance | Claude 3.5 Sonnet | Careful accuracy |
| Client communication | Claude 3.5 Sonnet | Professional tone |
| Financial research | Cohere Command R+ | RAG expertise |
| Market analysis | Bloomberg GPT / FinGPT | Financial training |

---

## Critical Gaps & Solutions

### What LLMs CAN'T Do:
- ❌ Real-time access to insurance carrier rates
- ❌ Current Social Security rules (SSA.gov)
- ❌ Live policy pricing
- ❌ Carrier-specific underwriting guidelines

### How to Fill the Gaps:

**1. Build RAG System**
```
Insurance Products Database
    ↓
Embed current carrier rates, guidelines
    ↓
Update quarterly or via API
    ↓
Claude 3.5 Sonnet retrieves + analyzes
```

**2. Integrate APIs**
- **iPipeline:** Carrier integrations (enterprise pricing)
- **Firelight:** Life insurance data
- **NAIC:** Regulatory filings (free/paid)

**3. Web Scraping**
- Scrape SSA.gov for current rules
- Update Social Security benefit calculators
- Monitor regulatory changes

---

## Recommended Architecture

```
User Query
    ↓
Claude 3.5 Sonnet (reasoning + language understanding)
    ↓
RAG System (retrieve relevant policies, regulations)
    ↓
API Calls (carrier rates, SSA rules if available)
    ↓
GPT-4 (risk calculations, mathematical modeling)
    ↓
Claude 3.5 Sonnet (synthesize + communicate results)
```

---

## Use Cases

### Insurance Underwriting
- **Analyze application** → Claude 3.5 Sonnet
- **Calculate risk** → GPT-4
- **Check guidelines** → Cohere Command R+ (RAG)
- **Generate decision** → Claude 3.5 Sonnet

### Financial Planning
- **Analyze client situation** → Claude 3.5 Sonnet
- **Research products** → Cohere Command R+ (RAG)
- **Model scenarios** → GPT-4 or o1
- **Create recommendations** → Claude 3.5 Sonnet

### Compliance Review
- **Parse regulations** → Claude 3.5 Sonnet
- **Search precedents** → Cohere Command R+ (RAG)
- **Assess compliance** → Claude 3.5 Sonnet
- **Document findings** → Claude 3.5 Sonnet

---

## Cost Optimization

**For small agency (<100 cases/month):**
- Use Claude 3.5 Sonnet for everything
- Build simple RAG with key documents
- Estimated cost: $50-100/month

**For medium agency (100-500 cases/month):**
- Claude 3.5 Sonnet for analysis
- Cohere Command R+ for research
- GPT-4 for complex calculations
- Estimated cost: $200-500/month

**For large operation (500+ cases/month):**
- Consider fine-tuning Llama 3.3 70B on your specific products
- Use Claude for client-facing content
- Use fine-tuned model for internal analysis
- Estimated cost: $500-2000/month + fine-tuning costs

---

## Data Sources & Integrations

### Free Resources
- **SSA.gov:** Social Security rules, benefit calculators
- **NAIC:** Insurance regulatory filings
- **SEC EDGAR:** Financial filings
- **Federal Register:** Regulatory updates

### Paid APIs
- **iPipeline:** $$$$ - Carrier integrations
- **Firelight:** $$ - Life insurance data
- **Bloomberg Terminal:** $24K/year - Financial data
- **Alpha Vantage:** $50-600/mo - Market data

---

## Tips

✅ **DO:**
- Use Claude 3.5 Sonnet for anything client-facing
- Build RAG system for carrier guidelines
- Use GPT-4 for complex risk calculations
- Keep regulatory documents updated

❌ **DON'T:**
- Trust LLMs for real-time rates without verification
- Use general models for legal/compliance without RAG
- Skip human review on underwriting decisions
- Forget to update knowledge base quarterly
