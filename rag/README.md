# RAG (Retrieval Augmented Generation) Systems

**Last Updated:** 2026-01-30

Your guide to building RAG systems for domain-specific knowledge bases.

---

## What is RAG?

**Retrieval Augmented Generation (RAG)** combines:
1. **Knowledge Base** - Your documents, data, regulations
2. **Retrieval System** - Finds relevant information
3. **LLM** - Generates answers grounded in your data

**Why RAG?**
- ✅ LLMs can't access your proprietary data
- ✅ LLMs don't have real-time information
- ✅ LLMs hallucinate without grounding
- ✅ RAG provides citations and sources

---

## RAG Systems by Domain

### 1. Insurance & Financial Services

**What to Include:**
- Insurance carrier underwriting guidelines
- Product rate sheets
- State-specific regulations
- Internal policy documents
- SSA.gov rules and POMS manual

**Best Model for RAG:**
- **Primary:** Cohere Command R+ (best at grounding)
- **Secondary:** Claude 3.5 Sonnet (synthesis)

**Update Frequency:** Quarterly or when carriers update rates

**See:** [insurance-financial-rag.md](./insurance-financial-rag.md)

---

### 2. Healthcare & Pharmaceuticals

**What to Include:**
- Clinical practice guidelines
- PubMed research papers
- FDA drug approvals
- Drug interaction databases
- Medical protocols

**Best Model for RAG:**
- **Primary:** Cohere Command R+ (retrieval)
- **Secondary:** Med-PaLM 2 or BioGPT (medical synthesis)

**Update Frequency:** Monthly (FDA updates, new research)

**See:** [healthcare-pharma-rag.md](./healthcare-pharma-rag.md)

---

### 3. Social Security & Disability

**What to Include:**
- Program Operations Manual System (POMS)
- Listing of Impairments (Blue Book)
- Social Security Rulings (SSRs)
- Federal Register updates
- Circuit court disability decisions
- HALLEX manual

**Best Model for RAG:**
- **Primary:** Claude 3.5 Sonnet + RAG
- **Alternative:** Fine-tuned Llama 3.3 70B

**Update Frequency:** Quarterly (SSA updates)

**Opportunity:** First SSA/Disability-specialized LLM!

**See:** [social-security-rag.md](./social-security-rag.md)

---

### 4. Policy Analysis

**What to Include:**
- Congressional bills
- Federal regulations
- GAO reports
- Supreme Court decisions
- Federal Register

**Best Model for RAG:**
- **Primary:** Cohere Command R+
- **Secondary:** Claude 3.5 Sonnet

**Update Frequency:** Weekly (legislative activity)

---

## RAG Architecture Patterns

### Pattern 1: Simple RAG (Most Common)

```
User Query
    ↓
Embed query
    ↓
Search vector database
    ↓
Retrieve top K documents
    ↓
LLM generates answer using retrieved docs
    ↓
Return answer + citations
```

**Best for:** Knowledge bases, documentation, FAQs

---

### Pattern 2: Hybrid RAG (Recommended)

```
User Query
    ↓
Parallel search:
  - Vector search (semantic)
  - Keyword search (exact matches)
  - Metadata filters (date, source, etc.)
    ↓
Rerank results
    ↓
LLM generates answer
    ↓
Return answer + citations
```

**Best for:** Complex domains (insurance, medical, legal)

---

### Pattern 3: Agentic RAG (Advanced)

```
User Query
    ↓
Agent decides:
  - Which knowledge bases to search
  - What APIs to call
  - What calculations to run
    ↓
Multi-step retrieval + reasoning
    ↓
Synthesize final answer
    ↓
Return with full audit trail
```

**Best for:** Multi-source systems (insurance + SSA + carrier APIs)

---

## Tech Stack Recommendations

### Embedding Models

| Model | Cost | Best For |
|-------|------|----------|
| **Voyage AI Embeddings** | $0.10/M tokens | General purpose, high quality |
| **OpenAI text-embedding-3** | $0.13/M tokens | Good quality, widely supported |
| **Cohere Embed v3** | $0.10/M tokens | Multilingual, good for RAG |
| **Open source (BGE, E5)** | FREE | Local deployment, privacy |

**Recommendation:** Voyage AI or Cohere Embed v3

---

### Vector Databases

| Database | Cost | Best For |
|----------|------|----------|
| **Pinecone** | $70-280/mo | Managed, easy to use |
| **Weaviate** | FREE (self-hosted) | Open source, flexible |
| **Qdrant** | FREE (self-hosted) | Fast, Rust-based |
| **Chroma** | FREE | Simple, embedded |
| **pgvector** | FREE | PostgreSQL extension |

**Recommendation:** 
- **Managed:** Pinecone (easiest)
- **Self-hosted:** Qdrant or Weaviate (best performance)
- **Simple:** Chroma (prototyping)

---

### RAG Frameworks

| Framework | Language | Best For |
|-----------|----------|----------|
| **LangChain** | Python | Full-featured, lots of integrations |
| **LlamaIndex** | Python | Document-focused, easy RAG |
| **Haystack** | Python | Production-ready, modular |
| **Semantic Kernel** | C#/Python | Microsoft ecosystem |
| **Custom** | Any | Full control, optimized |

**Recommendation:**
- **Beginners:** LlamaIndex (easiest)
- **Production:** Haystack or custom
- **Complex:** LangChain (most flexible)

---

## Building Your First RAG System

### Step 1: Collect Documents
```bash
# Example: Insurance guidelines
/data/
├── carrier_guidelines/
│   ├── carrier_a_underwriting.pdf
│   ├── carrier_b_rates.xlsx
│   └── carrier_c_products.docx
├── regulations/
│   ├── state_regulations.pdf
│   └── federal_guidelines.pdf
└── internal/
    └── company_policies.md
```

### Step 2: Process & Embed
```python
from llama_index import VectorStoreIndex, SimpleDirectoryReader

# Load documents
documents = SimpleDirectoryReader('/data/carrier_guidelines').load_data()

# Create embeddings & index
index = VectorStoreIndex.from_documents(documents)
```

### Step 3: Query
```python
# Query the RAG system
query_engine = index.as_query_engine()
response = query_engine.query(
    "What are the underwriting guidelines for diabetes?"
)

print(response)
print(response.source_nodes)  # Citations
```

### Step 4: Use with Specific LLM
```python
from llama_index.llms import Anthropic

# Use Claude for synthesis
llm = Anthropic(model="claude-3-5-sonnet")
query_engine = index.as_query_engine(llm=llm)
```

---

## Cost Estimates

### Small RAG System (10K documents)
- **Embedding:** $5-10 one-time
- **Vector DB:** $70/mo (Pinecone) or FREE (self-hosted)
- **Query costs:** $50-200/mo (LLM API calls)
- **Total:** $125-280/mo

### Medium RAG System (100K documents)
- **Embedding:** $50-100 one-time
- **Vector DB:** $150/mo (Pinecone) or FREE (self-hosted)
- **Query costs:** $200-500/mo
- **Total:** $350-650/mo

### Large RAG System (1M+ documents)
- **Embedding:** $500-1000 one-time
- **Vector DB:** $500+/mo or self-hosted infrastructure
- **Query costs:** $1000-5000/mo
- **Total:** $1500-6000/mo

---

## Best Practices

### Document Preparation
✅ **DO:**
- Clean and structure documents
- Add metadata (source, date, category)
- Chunk documents appropriately (500-1000 tokens)
- Remove duplicates

❌ **DON'T:**
- Embed raw PDFs without extraction
- Use huge chunks (>2000 tokens)
- Forget to update stale data

### Retrieval Optimization
✅ **DO:**
- Use hybrid search (vector + keyword)
- Implement reranking
- Add metadata filters
- Test different chunk sizes

❌ **DON'T:**
- Rely only on vector search
- Return too many results (>10)
- Ignore relevance scores

### LLM Integration
✅ **DO:**
- Use models good at grounding (Cohere Command R+, Claude)
- Include citations in prompts
- Validate answers against sources
- Log queries for improvement

❌ **DON'T:**
- Use models that hallucinate easily
- Skip citation requirements
- Trust LLM without verification

---

## Domain-Specific Guides

- **[Insurance & Financial RAG](./insurance-financial-rag.md)** - Carrier guidelines, SSA rules
- **[Healthcare & Pharma RAG](./healthcare-pharma-rag.md)** - Clinical guidelines, drug databases
- **[Social Security RAG](./social-security-rag.md)** - POMS, Blue Book, case law
- **[Policy Analysis RAG](./policy-analysis-rag.md)** - Congressional bills, regulations

---

## Next Steps

1. ✅ **Choose your domain** - Start with one knowledge base
2. ✅ **Collect documents** - Gather PDFs, docs, data
3. ✅ **Select tech stack** - Embedding model + vector DB + framework
4. ✅ **Build prototype** - Start simple with LlamaIndex
5. ✅ **Test and iterate** - Measure accuracy, improve chunks
6. ✅ **Deploy to production** - Scale up infrastructure
7. ✅ **Monitor and update** - Keep knowledge base current

---

## Resources

- **LlamaIndex Docs:** https://docs.llamaindex.ai
- **LangChain Docs:** https://python.langchain.com
- **Pinecone Guides:** https://docs.pinecone.io
- **Cohere RAG Guide:** https://docs.cohere.com/docs/retrieval-augmented-generation-rag

---

## Notes

- RAG is essential for domain-specific applications
- Start simple, add complexity as needed
- Update knowledge bases regularly
- Always include citations for trust
