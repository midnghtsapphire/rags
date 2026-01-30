# Insurance & Financial Services Stack

**Source:** Claude domain analysis  
**Last Updated:** 2026-01-30  
**Use for:** Insurance underwriting, financial planning, compliance, risk assessment

---

## API Configuration

```yaml
insurance_financial_stack:
  
  contract_analysis:
    primary: anthropic/claude-3.5-sonnet
    use_for: "Insurance contracts, policy analysis, compliance documents"
    cost: "$3/$15 per M tokens"
    
  risk_assessment:
    primary: openai/gpt-4-turbo
    secondary: openai/o1
    use_for: "Underwriting analysis, risk modeling, mathematical reasoning"
    cost: "$2.50/$10 per M tokens"
    
  regulatory_research:
    primary: cohere/command-r-plus
    use_for: "Regulatory documents, compliance research, policy lookups"
    cost: "Mid-range"
    
  client_communication:
    primary: anthropic/claude-3.5-sonnet
    use_for: "Professional client communication, explanations, proposals"
    cost: "$3/$15 per M tokens"
    
  financial_analysis:
    primary: bloomberg-gpt  # If accessible
    fallback: fin-gpt  # Open source alternative
    use_for: "Market analysis, financial sentiment, SEC filings"
    cost: "Enterprise (Bloomberg) / FREE (FinGPT)"
    
  fine_tuned_custom:
    model: meta/llama-3.3-70b
    trained_on: "Your specific insurance products, carrier guidelines"
    use_for: "Internal underwriting logic, product-specific analysis"
    cost: "Infrastructure + fine-tuning costs"
```

---

## Task Routing

| Task | Model | Why |
|------|-------|-----|
| Policy contract analysis | Claude 3.5 Sonnet | Best at legal nuance |
| Risk calculations | GPT-4 / o1 | Mathematical reasoning |
| Compliance review | Claude 3.5 Sonnet | Careful accuracy |
| Regulatory research | Cohere Command R+ | RAG expertise |
| Client proposals | Claude 3.5 Sonnet | Professional tone |
| Market analysis | Bloomberg GPT / FinGPT | Financial training |
| Custom underwriting | Fine-tuned Llama 3.3 | Your specific logic |

---

## Implementation Example

```typescript
export class InsuranceFinancialRouter {
  static selectModel(task: string): string {
    const routes = {
      'contract_analysis': 'anthropic/claude-3.5-sonnet',
      'risk_assessment': 'openai/gpt-4-turbo',
      'complex_risk': 'openai/o1',
      'regulatory': 'cohere/command-r-plus',
      'client_comm': 'anthropic/claude-3.5-sonnet',
      'financial_analysis': 'bloomberg-gpt',  // or 'fin-gpt'
      'custom_underwriting': 'meta/llama-3.3-70b-fine-tuned'
    };
    
    return routes[task] || 'anthropic/claude-3.5-sonnet';
  }
}
```

---

## Required Integrations

### APIs & Data Sources

```yaml
data_sources:
  
  insurance_carriers:
    - iPipeline  # Carrier integrations (enterprise)
    - Firelight  # Life insurance data
    - NAIC  # Regulatory filings (free/paid)
    
  social_security:
    - SSA.gov  # Web scraping (no official API)
    - POMS Manual  # Build RAG system
    
  financial_data:
    - Bloomberg Terminal  # $24K/year (if accessible)
    - Alpha Vantage  # $50-600/mo
    - IEX Cloud  # $0-15K/mo
    
  regulatory:
    - Federal Register  # FREE
    - SEC EDGAR  # FREE
    - State insurance departments  # Varies
```

---

## RAG System Architecture

```
User Query: "What are the underwriting guidelines for diabetes?"
    ↓
Claude 3.5 Sonnet (understand query)
    ↓
RAG System retrieves:
  - Carrier underwriting guidelines
  - Internal policy documents
  - Recent regulatory updates
    ↓
GPT-4 (risk calculations if needed)
    ↓
Claude 3.5 Sonnet (synthesize answer)
    ↓
Return professional response
```

---

## Cost Estimates

### Small Agency (<100 cases/month)
- Claude 3.5 Sonnet: $50-100/month
- Simple RAG system: Infrastructure only
- **Total:** $50-150/month

### Medium Agency (100-500 cases/month)
- Claude 3.5 Sonnet: $200/month
- Cohere Command R+: $100/month
- GPT-4: $100/month
- RAG infrastructure: $50/month
- **Total:** $450-550/month

### Large Operation (500+ cases/month)
- Fine-tuned Llama 3.3 70B: Infrastructure
- Claude for client-facing: $300/month
- API integrations: $500-2000/month
- **Total:** $1500-5000/month

---

## Fine-Tuning Recommendations

### When to Fine-Tune
- You have 1000+ underwriting decisions
- Specific carrier guidelines to embed
- Need consistent output format
- Want to reduce API costs long-term

### What to Fine-Tune On
```yaml
training_data:
  - Carrier underwriting guidelines
  - Historical underwriting decisions
  - Product-specific rules
  - State-specific regulations
  - Internal policy documents
```

### Recommended Base Model
- **Llama 3.3 70B** - Best balance of quality and cost
- Deploy on-premise or private cloud
- Reduces per-query costs after initial investment

---

## Compliance & Security

### Data Handling
- ✅ Use BAA-compliant APIs (Azure OpenAI, AWS Bedrock)
- ✅ De-identify PII before sending to external APIs
- ✅ Consider local deployment for sensitive data
- ❌ Never send SSN, medical records to non-compliant APIs

### Audit Trail
- Log all LLM interactions
- Track which model made which decision
- Human review required for final underwriting

---

## Testing Protocol

1. **Baseline with Claude 3.5 Sonnet** (general capability)
2. **Add Cohere Command R+** (RAG for regulations)
3. **Add GPT-4** (complex risk calculations)
4. **Measure accuracy** against historical decisions
5. **Consider fine-tuning** if volume justifies it

---

## Success Metrics

- **Accuracy:** % of LLM recommendations matching human underwriter
- **Speed:** Time saved per case
- **Cost:** API costs vs. underwriter time saved
- **Compliance:** Zero regulatory violations

---

## Notes

- Always require human review for final decisions
- Keep RAG system updated quarterly
- Monitor for regulatory changes
- Consider fine-tuning after 6-12 months of data collection
