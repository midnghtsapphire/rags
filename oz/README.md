# OZ - LLM Stack Management System

**Last Updated:** 2026-01-30  
**Purpose:** Active LLM stacks for current projects

---

## What's in This Folder

This folder contains **only the LLM stacks you're actively using**. Research and future projects are in `/projects/research/`.

---

## Active Stacks

### Universal Stacks (Choose One)

**[ChatGPT Stack](./stacks/universal-oz-chatgpt-stack.md)**
- ChatGPT's "research-lab level" recommendations
- Includes Perplexity for SEO/web-aware content
- Best for: Quality-first approach

**[Claude Stack](./stacks/universal-oz-claude-stack.md)**
- Claude's cost-optimized recommendations
- 3-tier system (quality/cost/speed)
- Best for: Cost-conscious approach

**Next Step:** Test both stacks and choose one for general work

---

### Domain-Specific Stacks

**[Insurance & Financial](./stacks/insurance-financial-stack.md)**
- For your active insurance/financial business
- Models: Claude 3.5 Sonnet, GPT-4, Cohere Command R+
- Includes RAG architecture for carrier guidelines

---

## Quick Decision Guide

### "Which universal stack should I use?"

**Choose ChatGPT Stack if:**
- ✅ Quality is top priority
- ✅ SEO and affiliate content is important
- ✅ You want Perplexity for web-aware content
- ✅ Cost is not the primary concern

**Choose Claude Stack if:**
- ✅ Cost optimization is important
- ✅ You want flexibility (quality/cost/speed tiers)
- ✅ You might need multilingual support
- ✅ Local deployment might be needed later

**Recommendation:** Test both for 1-2 weeks, then pick one.

---

## File Structure

```
/projects/oz/
├── README.md (this file)
├── universal_oz.md (master list of all 45 models)
└── stacks/
    ├── universal-oz-chatgpt-stack.md
    ├── universal-oz-claude-stack.md
    └── insurance-financial-stack.md
```

---

## Related Folders

- **[/projects/research/](../research/)** - Future domain research (healthcare, social security, etc.)
- **[/projects/rag/](../rag/)** - RAG implementation guides
- **[/projects/tasks/](../tasks/)** - Your to-do list with LLM tasks
- **[/projects/braindump/](../braindump/)** - Daily idea capture

---

## Next Steps

1. ☐ **Test both universal stacks** (see tasks in `/projects/tasks/todo.md`)
2. ☐ **Choose your primary stack** for general work
3. ☐ **Implement insurance/financial stack** for your business
4. ☐ **Build RAG system** for carrier guidelines (when ready)
5. ☐ **Explore future domains** in `/projects/research/` (later)

---

## Notes

- Keep this folder simple - only active stacks
- Move completed research to `/projects/research/`
- Don't create new stacks until you're actively working on that domain
- Update this README when you add/remove stacks
