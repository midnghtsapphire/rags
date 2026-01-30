# Automation & Agents - LLM Recommendations

**Use for:** Workflow automation, multi-agent systems, tool-calling, RAG, agent loops

---

## Recommended Models

### Premium Tier (Complex Automation)

**1. Mistral Large 2** - `mistral/mistral-large-2`
- **Cost:** $2-4/M tokens
- **Best for:** Tool-calling, structured outputs, agent loops
- **Why:** Best-in-class tool-calling, reliable JSON workflows
- **Use when:** Building production agents, complex workflows, API orchestration

**2. OpenAI GPT-5** - `openai/gpt-5`
- **Cost:** Premium
- **Best for:** Multi-agent planning, system orchestration
- **Why:** Deep thinking, complex reasoning over constraints
- **Use when:** Designing agent architectures, complex automation strategy

**3. MoonshotAI Kimi K2.5** - `moonshotai/kimi-k2.5`
- **Cost:** $0.50/M input, $2.80/M output
- **Best for:** Agentic tool-calling, automation frameworks
- **Why:** State-of-the-art agentic behavior, visual coding
- **Use when:** Agent development, workflow builder, tool integration

### Reasoning & Planning

**4. OpenAI o1** - `openai/o1`
- **Cost:** $15/M input, $60/M output
- **Best for:** Complex reasoning, multi-step planning
- **Why:** Chain-of-thought reasoning, problem-solving
- **Use when:** Workflow optimization, complex automation logic

**5. LiquidAI LFM2.5-1.2B-Thinking** - `liquid/lfm2.5-1.2b-thinking:free`
- **Cost:** FREE
- **Best for:** Lightweight reasoning, edge devices
- **Why:** Small footprint, optimized for agentic tasks
- **Use when:** On-device reasoning, RAG applications, data extraction

### RAG & Knowledge Base

**6. Cohere Command R+** - `cohere/command-r-plus`
- **Cost:** Mid-range
- **Best for:** RAG, knowledge bases, document Q&A
- **Why:** Insanely good at grounding answers in your data
- **Use when:** Building knowledge bases, document search, compliance docs

**7. Writer Palmyra X5** - `writer/palmyra-x5`
- **Cost:** $0.60/M input, $6/M output
- **Best for:** Long context processing (1M tokens)
- **Why:** Fast inference, enterprise-grade, massive context window
- **Use when:** Processing entire websites, large documents, workflow automation

---

## Decision Matrix

| Task | Model | Why |
|------|-------|-----|
| API orchestration | Mistral Large 2 | Best tool-calling |
| Multi-agent system | GPT-5 | System-level thinking |
| Workflow builder | Kimi K2.5 | Agentic expertise |
| Complex planning | OpenAI o1 | Chain-of-thought |
| RAG pipeline | Cohere Command R+ | Best at grounding |
| Document processing | Palmyra X5 | 1M token context |
| Edge reasoning | LiquidAI LFM2.5 | Lightweight |
| JSON workflows | Mistral Large 2 | Structured outputs |
| Tool integration | Kimi K2.5 | Visual + tool-calling |
| Agent loops | Mistral Large 2 | Reliable iteration |

---

## Workflow Recommendations

### For Building Agents:
1. **Design architecture** with GPT-5 (strategy)
2. **Implement tool-calling** with Mistral Large 2 (execution)
3. **Test reasoning** with o1 (validation)

### For RAG Systems:
1. **Design pipeline** with Cohere Command R+ (RAG expert)
2. **Process documents** with Palmyra X5 (long context)
3. **Implement retrieval** with Cohere Command R+ (grounding)

### For Workflow Automation:
1. **Plan workflow** with o1 (reasoning)
2. **Build automation** with Mistral Large 2 (tool-calling)
3. **Optimize** with Kimi K2.5 (agentic improvements)

---

## Cost Optimization

**Monthly Budget: $50**
- Use LiquidAI LFM2.5 for 60% (free reasoning)
- Use Kimi K2.5 for 30% (mid-range agentic)
- Use Mistral Large 2 for 10% (critical tool-calling)

**Monthly Budget: $200**
- Use Mistral Large 2 for 50% (tool-calling)
- Use Cohere Command R+ for 30% (RAG)
- Use o1 for 20% (complex planning)

**Monthly Budget: Unlimited**
- Use GPT-5 for strategy
- Use Mistral Large 2 for execution
- Use o1 for complex reasoning
- Use Cohere Command R+ for RAG

---

## Project-Specific Recommendations

### OZ Marketing Suite Automation
- **Primary:** Mistral Large 2
- **Secondary:** Kimi K2.5
- **Reason:** Tool-calling for API integration, workflow automation

### Workflow Builder
- **Primary:** Kimi K2.5
- **Secondary:** Mistral Large 2
- **Fallback:** LiquidAI LFM2.5
- **Reason:** Agentic development focus

### Affiliate Automation
- **Primary:** Mistral Large 2
- **Fallback:** Kimi K2.5
- **Reason:** API orchestration, data extraction

### Knowledge Base Apps
- **Primary:** Cohere Command R+
- **Secondary:** Palmyra X5
- **Reason:** RAG + long document processing

---

## Special Use Cases

### Tool-Calling Pattern
```
"Call API → parse → reason → call another tool → format output"
```
**Best Model:** Mistral Large 2  
**Why:** Most reliable at multi-step tool chains

### Multi-Agent Orchestration
**Best Model:** GPT-5  
**Why:** System-level thinking, agent coordination

### RAG Pipeline
**Best Model:** Cohere Command R+  
**Why:** Best at grounding answers in provided data

### Edge Deployment
**Best Model:** LiquidAI LFM2.5-1.2B-Thinking  
**Why:** Small footprint, runs on device

### Long Document Analysis
**Best Model:** Palmyra X5  
**Why:** 1M token context window

---

## Architecture Patterns

### Agent Loop Pattern
1. **Planner:** o1 (reasoning)
2. **Executor:** Mistral Large 2 (tool-calling)
3. **Validator:** Cohere Command R+ (grounding)

### RAG Pattern
1. **Retrieval:** Cohere Command R+ (semantic search)
2. **Context:** Palmyra X5 (long context)
3. **Generation:** Mistral Large 2 (structured output)

### Multi-Agent Pattern
1. **Orchestrator:** GPT-5 (coordination)
2. **Specialists:** Mistral Large 2 (execution)
3. **Memory:** Cohere Command R+ (knowledge base)

---

## Tips

✅ **DO:**
- Use Mistral Large 2 for production tool-calling
- Use Cohere Command R+ for RAG systems
- Use o1 for complex planning
- Test with LiquidAI LFM2.5 (free) first

❌ **DON'T:**
- Use content models for tool-calling
- Use expensive models for simple automation
- Skip planning phase (use o1 or GPT-5)
- Ignore context window limits
