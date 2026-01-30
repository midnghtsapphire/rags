# Social Security & Disability - Full Claude Analysis

**Source:** Claude (Anthropic)  
**Date:** 2026-01-30  
**Context:** Blue ocean opportunity identification

---

## Original Question

"What specialized LLMs exist for Social Security and disability benefits?"

---

## Claude's Key Finding

> **"No Specialized Models Exist - This is a major gap in the LLM ecosystem!"**

This was Claude's most emphatic statement in the entire domain analysis. Claude identified this as a **blue ocean opportunity**.

---

## Why Claude Thinks This is Significant

### Claude's Reasoning:

1. **Massive Underserved Market**
   - Disability attorneys need case law research
   - Advocates need up-to-date SSA rules
   - Claimants need benefit calculations
   - No AI tools exist for this domain

2. **High Complexity**
   - Program Operations Manual System (POMS) is 100,000+ pages
   - Constantly changing regulations
   - Circuit court precedents vary by region
   - Complex benefit calculations

3. **High Value**
   - Disability cases can take years
   - Attorneys bill hundreds of hours for research
   - Mistakes cost claimants their benefits
   - Time savings = significant ROI

4. **Defensible Moat**
   - Requires domain expertise + AI capability
   - High barrier to entry
   - Network effects (more users = better training data)
   - First-mover advantage in untapped market

---

## Claude's Recommended Approaches

### Option 1: RAG + General LLM

**Model:** Claude 3.5 Sonnet  
**Strategy:** Embed SSA.gov, POMS manual, update quarterly

**Claude's reasoning:**
- Fastest to market (3-6 months)
- Lower initial investment
- Easier to maintain
- Good for MVP validation

**Limitations:**
- Still requires general LLM (API costs)
- May not capture domain nuances
- Retrieval quality depends on chunking strategy

---

### Option 2: Fine-tuned Llama (Claude's Preferred Long-Term)

**Model:** Llama 3.3 70B  
**Strategy:** Fine-tune on disability case law, POMS, listings

**Claude's reasoning:**
- **Best long-term solution**
- Captures domain-specific reasoning
- Can run on-premise (privacy)
- Lower per-query costs after initial investment
- Competitive moat (hard to replicate)

**Why Claude prefers this:**
> "You could create the first SSA/Disability-specialized LLM by fine-tuning Llama 3.3 70B on POMS + case law. This would be extremely valuable for disability attorneys, advocates."

---

### Option 3: Hybrid System

**Model:** Claude + web_search  
**Strategy:** Real-time SSA.gov lookups

**Claude's reasoning:**
- Handles regulatory changes immediately
- No need to update knowledge base
- Good for current rules

**Limitations:**
- Slower (web scraping latency)
- Less reliable (website changes break scrapers)
- Can't access historical data easily

---

## What You'd Need to Build (Claude's Detailed Breakdown)

### 1. SSA Knowledge Base

Claude specified these exact sources:
- **Program Operations Manual System (POMS)** - The SSA's internal manual
- **Listing of Impairments (Blue Book)** - Medical criteria for disability
- **Social Security Rulings (SSRs)** - Policy interpretations
- **Federal Register updates** - New regulations

**Claude's note:** "These are publicly available but scattered across SSA.gov"

### 2. Case Law Database

Claude identified these legal sources:
- **Circuit court decisions on disability** - Precedents vary by region
- **HALLEX** (Hearings, Appeals, Litigation Law Manual) - ALJ procedures
- **Administrative Law Judge precedents** - Decision patterns

**Claude's insight:** "Circuit courts have different standards - 9th Circuit is most claimant-friendly, 5th Circuit is most restrictive. Your LLM needs to know which circuit applies."

### 3. Calculator Tools

Claude specified these calculations:
- **COLA adjustments** - Annual cost-of-living increases
- **Benefit calculators** - Primary Insurance Amount (PIA)
- **Earnings test computations** - Substantial Gainful Activity (SGA)
- **Windfall Elimination Provision (WEP)** - Pension offset calculations

**Claude's reasoning:** "These are mathematical, not language tasks. LLMs are bad at math. Build separate calculator tools and let the LLM call them."

---

## Claude's Opportunity Analysis

### Market Size (Claude's Estimate)

**Target Users:**
- ~14,000 disability attorneys in US
- ~5,000 non-attorney advocates
- ~2.5 million disability claims filed annually

**Willingness to Pay:**
- Attorneys: $200-500/month (saves 10-20 hours/month)
- Advocates: $50-100/month
- Claimants: $20-50/month (DIY research)

**Potential Revenue:**
- Conservative: $2-5M ARR (1000 attorney subscribers)
- Optimistic: $20-50M ARR (10,000 total subscribers)

---

## Claude's Implementation Roadmap

### Phase 1: RAG System (3-6 months)
1. Scrape and structure SSA.gov content
2. Embed POMS manual (100K+ pages)
3. Build retrieval system with Cohere Command R+ or similar
4. Test with Claude 3.5 Sonnet as synthesis layer
5. **MVP Goal:** Answer "What are the disability criteria for X condition?"

### Phase 2: Fine-Tuning (6-12 months)
1. Collect disability case law from Westlaw/LexisNexis
2. Structure training data (question-answer pairs)
3. Fine-tune Llama 3.3 70B on domain corpus
4. Validate against human disability attorneys
5. **Goal:** Match or exceed human attorney accuracy on case law research

### Phase 3: Production (12+ months)
1. Deploy as SaaS (web app + API)
2. Integrate with legal practice management tools (Clio, MyCase)
3. Build API for third-party integrations
4. Continuous learning from user feedback
5. **Goal:** 1000+ paying subscribers

---

## Why Claude is Uniquely Positioned to Analyze This

### Claude's Self-Awareness:

1. **Conservative by Design**
   - Claude acknowledged this is a high-stakes domain (people's livelihoods)
   - Recommended human oversight for final decisions
   - Emphasized accuracy over speed

2. **Legal Text Expertise**
   - Claude is trained on legal documents
   - Good at parsing complex regulatory language
   - Can identify contradictions in case law

3. **Honest About Limitations**
   - Admitted no specialized models exist
   - Didn't oversell current LLM capabilities
   - Recommended building domain-specific solution

---

## Claude's Unique Insights

### 1. "First-Mover Advantage is Massive"
Claude emphasized that whoever builds this first will be hard to displace:
- Network effects (more users = more training data)
- Integration lock-in (practice management tools)
- Brand recognition in niche market

### 2. "This is a 12-24 Month Project, Not 3 Months"
Claude was realistic about timeline:
- Data collection is hard (POMS is messy)
- Fine-tuning requires domain expertise
- Validation takes time (need attorney feedback)

### 3. "Partner with a Disability Attorney"
Claude strongly recommended:
> "You'll need domain expertise partnership. Don't try to build this alone - the SSA rules are too complex."

### 4. "Consider Licensing vs. Building"
Claude suggested an alternative:
> "This could be a licensing opportunity to existing legal tech companies (Clio, MyCase, Fastcase) rather than building a standalone product."

---

## Risks & Challenges (Claude's Warnings)

### 1. Regulatory Risk
**Claude's concern:** "SSA may not approve of AI-assisted claims. Check with SSA Office of General Counsel."

### 2. Liability Risk
**Claude's concern:** "If your AI gives wrong advice and someone loses their benefits, are you liable? Need legal review."

### 3. Data Access
**Claude's concern:** "POMS is public but messy. Case law requires expensive Westlaw/LexisNexis subscriptions."

### 4. Validation Difficulty
**Claude's concern:** "How do you know your AI is right? Need disability attorney experts to validate."

---

## Cost Estimates (Claude's Breakdown)

### RAG System (Initial)
- Embedding: $500-1000 one-time
- Vector DB: $150-500/month
- LLM API: $500-2000/month
- **Total:** $1150-3500/month

### Fine-Tuning (One-Time)
- Data collection: $5000-10000 (Westlaw access, scraping)
- Training: $2000-5000 (Together.ai or Anyscale)
- Validation: $2000-5000 (attorney expert review)
- **Total:** $9000-20000 one-time

### Production (Monthly)
- Infrastructure: $1000-3000/month (hosting, compute)
- Updates: $500-1000/month (quarterly POMS updates)
- Support: $1000-2000/month (customer support)
- **Total:** $2500-6000/month

**Claude's ROI calculation:**
- Break-even at ~50 attorney subscribers ($250/month each)
- Profitable at 100+ subscribers
- Highly profitable at 1000+ subscribers

---

## Meta-Analysis: Why This Recommendation Matters

### Claude's Approach vs. Other LLMs:

**Claude's strengths evident here:**
- **Opportunity identification** - Spotted the gap others missed
- **Realistic timeline** - Didn't oversell "build in 2 weeks"
- **Risk assessment** - Identified regulatory and liability concerns
- **Partnership thinking** - Suggested domain expert collaboration

**What makes this valuable:**
- This is **original insight**, not regurgitated knowledge
- Claude connected dots (no models + high value + defensible = opportunity)
- Provided actionable roadmap, not just "here are some models"

---

## Follow-Up Questions to Ask Claude

1. **Which circuit courts should be prioritized** for case law training data?
2. **How to structure training data** for fine-tuning on legal precedents?
3. **What's the best way to validate** AI accuracy against human attorneys?
4. **Should this be B2B (attorneys) or B2C (claimants)** first?
5. **How to handle conflicting precedents** across circuits?

---

## Next Steps (When Ready to Pursue)

1. ☐ Research market demand (survey 50 disability attorneys)
2. ☐ Assess data availability (can we access POMS easily?)
3. ☐ Prototype RAG system (3-month MVP, $10K budget)
4. ☐ Validate with 5 disability attorney experts
5. ☐ Decide: Build full product, license to legal tech, or shelve

---

## Why Save This Analysis

**This is Claude at its best:**
- Original thinking (identified gap)
- Detailed implementation plan
- Realistic about challenges
- Honest about timeline and costs

**Future you will thank present you for saving:**
- The full reasoning (not just "use Claude")
- The opportunity analysis (market size, ROI)
- The warnings (regulatory, liability risks)
- The roadmap (12-24 month timeline)

**When to revisit:**
- When you have 6-12 months to dedicate to a project
- When you have $20-50K to invest
- When you can partner with a disability attorney
- When you're ready for a blue ocean opportunity
