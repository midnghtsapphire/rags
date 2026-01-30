# Code Development - LLM Recommendations

**Use for:** Coding, debugging, architecture, code review, refactoring

---

## Recommended Models

### Premium Tier (Complex Coding)

**1. Google Gemini 2.5 Pro** - `google/gemini-2.5-pro`
- **Cost:** $1.25/M input, $5/M output
- **Best for:** Complex coding, architecture design, large codebase understanding
- **Why:** #1 on coding benchmarks, understands context across files
- **Use when:** Building new features, refactoring, system architecture

**2. Claude 3.5 Sonnet (Coding Mode)** - `anthropic/claude-3.5-sonnet:coding`
- **Cost:** $3/M input, $15/M output
- **Best for:** Code review, best practices, security analysis
- **Why:** Excellent at explaining code, identifying issues, suggesting improvements
- **Use when:** Code reviews, architecture analysis, documentation

**3. DeepSeek V3** - `deepseek/v3`
- **Cost:** $0.14-0.55/M tokens (extremely cheap)
- **Best for:** Reasoning-heavy coding tasks, algorithm design
- **Why:** Competitive with GPT-4, excellent reasoning, fraction of the cost
- **Use when:** Complex algorithms, optimization problems, cost-sensitive projects

### Specialized Coding Models

**4. DeepSeek Coder** - `deepseek/coder`
- **Cost:** Low
- **Best for:** Pure code generation, autocomplete-style tasks
- **Why:** Specialized for code, fast, accurate
- **Use when:** Writing boilerplate, generating functions, code completion

**5. Qwen 2.5 Coder 32B** - `qwen/qwen-2.5-coder-32b`
- **Cost:** Often free or very cheap
- **Best for:** Multilingual coding, specialized code tasks
- **Why:** Strong multilingual support, good code quality
- **Use when:** Non-English codebases, alternative to GLM 4.7 Flash

**6. MoonshotAI Kimi K2.5** - `moonshotai/kimi-k2.5`
- **Cost:** $0.50/M input, $2.80/M output
- **Best for:** Visual coding, agent development, tool-calling
- **Why:** State-of-the-art visual coding, understands UI → code
- **Use when:** Building automation, agents, converting designs to code

### Budget Tier (High-Volume Coding)

**7. Z.AI GLM 4.7 Flash** - `z-ai/glm-4.7-flash`
- **Cost:** $0.07/M input, $0.40/M output (cheapest)
- **Best for:** Code completion, simple fixes, documentation
- **Why:** Optimized for agentic coding, very fast
- **Use when:** High-volume tasks, simple bug fixes, doc generation

**8. Google Gemini 2.5 Flash** - `google/gemini-2.5-flash`
- **Cost:** $0.075/M input, $0.30/M output
- **Best for:** Quick coding tasks, prototyping
- **Why:** Fast, multimodal, good quality for the price
- **Use when:** Rapid prototyping, testing ideas

---

## Decision Matrix

| Task | Model | Why |
|------|-------|-----|
| New feature development | Gemini 2.5 Pro | Complex, needs context |
| Code review | Claude 3.5 Sonnet (Coding) | Best practices, security |
| Bug fixing | DeepSeek V3 | Reasoning + cheap |
| Algorithm design | DeepSeek V3 | Strong reasoning |
| Refactoring | Gemini 2.5 Pro | Understands large codebases |
| Code completion | GLM 4.7 Flash | Fast + cheap |
| Documentation | Claude 3.5 Sonnet (Coding) | Clear explanations |
| Agent development | Kimi K2.5 | Tool-calling expertise |
| UI → Code | Kimi K2.5 | Visual coding |
| Simple fixes | GLM 4.7 Flash | Volume + speed |

---

## Workflow Recommendations

### For New Features:
1. **Architecture** with Gemini 2.5 Pro (design)
2. **Implementation** with DeepSeek V3 (cost-effective quality)
3. **Review** with Claude 3.5 Sonnet (catch issues)

### For Debugging:
1. **Identify** with DeepSeek V3 (reasoning)
2. **Fix** with Gemini 2.5 Pro (complex fixes)
3. **Test** with GLM 4.7 Flash (generate test cases)

### For Refactoring:
1. **Analyze** with Claude 3.5 Sonnet (best practices)
2. **Plan** with Gemini 2.5 Pro (architecture)
3. **Execute** with DeepSeek V3 (cost-effective)

---

## Cost Optimization

**Monthly Budget: $50**
- Use DeepSeek V3 for 70% of coding (best value)
- Use GLM 4.7 Flash for 20% (simple tasks)
- Use Gemini 2.5 Pro for 10% (critical features)

**Monthly Budget: $200**
- Use Gemini 2.5 Pro for 50% (quality)
- Use DeepSeek V3 for 30% (reasoning)
- Use Claude 3.5 Sonnet for 20% (reviews)

**Monthly Budget: Unlimited**
- Use Gemini 2.5 Pro as default
- Use Claude 3.5 Sonnet for reviews
- Use specialized models for specific tasks

---

## Project-Specific Recommendations

### Mechatronopolis Hub
- **Primary:** Gemini 2.5 Pro
- **Secondary:** Claude 3.5 Sonnet (Coding)
- **Fallback:** DeepSeek V3
- **Reason:** Complex architecture, needs thorough reviews

### The Alt Text
- **Primary:** Gemini 2.5 Pro
- **Fallback:** DeepSeek V3
- **Reason:** Accessibility features require careful implementation

### Workflow Builder
- **Primary:** Kimi K2.5
- **Secondary:** Gemini 2.5 Pro
- **Reason:** Agent development + tool-calling focus

### Quick Prototypes
- **Primary:** DeepSeek V3
- **Fallback:** GLM 4.7 Flash
- **Reason:** Speed + cost for experimentation

---

## Special Use Cases

### Visual Coding (Screenshot → Code)
- **Use:** Kimi K2.5 or LLaVA
- **Why:** Specialized for UI understanding

### Multilingual Codebases
- **Use:** Qwen 2.5 Coder 32B
- **Why:** Strong multilingual support

### Security-Critical Code
- **Use:** Claude 3.5 Sonnet (Coding Mode)
- **Why:** Best at identifying security issues

### Performance Optimization
- **Use:** DeepSeek V3
- **Why:** Strong reasoning for algorithmic improvements

---

## Tips

✅ **DO:**
- Use Gemini 2.5 Pro for complex features
- Use DeepSeek V3 for cost-effective quality
- Use Claude for code reviews
- Use specialized models (DeepSeek Coder, Qwen Coder) for pure coding

❌ **DON'T:**
- Use content generation models for coding
- Use expensive models for simple tasks
- Skip code reviews to save money
- Use free models for production code
