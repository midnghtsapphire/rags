# Healthcare & Pharmaceuticals - Domain-Specific LLMs

**Source:** Claude analysis  
**Last Updated:** 2026-01-30

---

## Specialized Medical Models

### Clinical Reasoning

**1. Med-PaLM 2** (Google)
- **Cost:** Enterprise/API access
- **Best for:** Medical reasoning, clinical decision support
- **Why:** Best clinical accuracy, passed USMLE medical licensing exam
- **Access:** Enterprise only, contact Google Cloud

### Biomedical Research

**2. BioGPT** (Microsoft)
- **Cost:** FREE (open source)
- **Best for:** Biomedical literature search, PubMed analysis
- **Why:** Trained specifically on PubMed abstracts
- **Use when:** Research paper analysis, literature reviews

**3. PubMedBERT**
- **Cost:** FREE
- **Best for:** Research paper analysis, medical entity extraction
- **Why:** Better than general BERT for medical text
- **Use when:** Extracting medical entities, analyzing research

### Clinical Documentation

**4. GatorTron** (University of Florida)
- **Cost:** Research/Enterprise
- **Best for:** Clinical notes, EHR data, medical records
- **Why:** 90B parameters, trained on HIPAA-compliant data
- **Access:** Research partnerships or enterprise licensing

**5. ClinicalBERT**
- **Cost:** FREE
- **Best for:** Medical entity extraction from clinical notes
- **Why:** Specialized for clinical text understanding
- **Use when:** Processing EHR data, clinical documentation

### Patient Communication

**6. Anthropic Claude 3.5 Sonnet** - `anthropic/claude-3.5-sonnet`
- **Cost:** $3/M input, $15/M output
- **Best for:** Patient communication, medical writing, explaining concepts
- **Why:** Best at making complex medical information accessible
- **Use when:** Patient-facing content, medical education, care instructions

---

## Emerging Models

- **GPT-4 Medical** (OpenAI) - Rumored fine-tune, not public yet
- **Gemini Pro 1.5 Health** (Google) - Medical-specific variant
- **LLaMA 3 Medical** - Community fine-tunes on medical data

---

## Task-Specific Recommendations

| Task | Primary Model | Alternative |
|------|---------------|-------------|
| Clinical reasoning | Med-PaLM 2 | GPT-4 + medical RAG |
| Literature search | BioGPT | PubMedBERT |
| Patient communication | Claude 3.5 Sonnet | GPT-4 |
| EHR analysis | GatorTron | ClinicalBERT |
| Drug information | Claude 3.5 Sonnet + RAG | Med-PaLM 2 |
| Medical writing | Claude 3.5 Sonnet | GPT-4 |
| Research synthesis | BioGPT | Claude 3.5 Sonnet |

---

## Critical Gaps & Solutions

### What Medical LLMs CAN'T Do:
- ❌ Access current clinical trials (clinicaltrials.gov)
- ❌ Check latest FDA approvals in real-time
- ❌ Verify drug interactions (need DrugBank)
- ❌ Pull insurance formularies
- ❌ Access patient-specific EHR data (HIPAA)

### Recommended Architecture

```
User Query
    ↓
Claude 3.5 Sonnet (reasoning + understanding)
    ↓
PubMed API (latest research papers)
    ↓
FDA.gov Web Search (drug approvals, recalls)
    ↓
DrugBank API (drug interactions, contraindications)
    ↓
Med-PaLM 2 or BioGPT (medical synthesis)
    ↓
Claude 3.5 Sonnet (patient-friendly explanation)
```

---

## Required Integrations

### Free APIs
- **PubMed API:** Research papers, abstracts
- **FDA API:** Drug approvals, recalls, safety alerts
- **ClinicalTrials.gov API:** Clinical trial data
- **RxNorm:** Drug terminology

### Paid Services
- **DrugBank:** $1500-5000/year - Drug interactions, pharmacology
- **UpToDate API:** Medical reference (enterprise)
- **Epocrates:** Drug information (subscription)

---

## Use Cases

### Medical Research
1. **Search literature** → BioGPT (PubMed)
2. **Analyze papers** → PubMedBERT
3. **Synthesize findings** → Claude 3.5 Sonnet
4. **Check latest trials** → ClinicalTrials.gov API

### Patient Education
1. **Understand condition** → Med-PaLM 2 or Claude
2. **Explain treatment** → Claude 3.5 Sonnet
3. **Check drug info** → DrugBank API
4. **Create materials** → Claude 3.5 Sonnet

### Clinical Decision Support
1. **Analyze symptoms** → Med-PaLM 2
2. **Check guidelines** → RAG system with clinical guidelines
3. **Verify interactions** → DrugBank API
4. **Document reasoning** → Claude 3.5 Sonnet

---

## HIPAA Compliance

### For Sensitive Patient Data:

**Option 1: Local Deployment**
- Use Llama 3.3 70B (fine-tuned on medical data)
- Deploy on-premise or in BAA-compliant cloud
- No data leaves your infrastructure

**Option 2: BAA-Compliant APIs**
- Google Cloud (Med-PaLM 2) - Offers BAA
- Azure OpenAI - Offers BAA
- AWS Bedrock (Claude) - Offers BAA

**Option 3: De-identification**
- Remove all PHI before sending to LLMs
- Use de-identification tools (Microsoft Presidio, AWS Comprehend Medical)
- Only send anonymized data to APIs

---

## Cost Optimization

**For Medical Practice:**
- Use Claude 3.5 Sonnet for patient communication
- Use free BioGPT for research
- Build RAG with medical guidelines
- Estimated: $100-300/month

**For Research Institution:**
- Use Med-PaLM 2 (if accessible)
- Use BioGPT for literature mining
- Use Claude for synthesis and writing
- Estimated: $500-2000/month

**For Healthcare App:**
- Fine-tune Llama 3.3 70B on medical data
- Deploy locally for HIPAA compliance
- Use Claude for patient-facing features
- Estimated: Infrastructure + $200-500/month API costs

---

## Fine-Tuning Opportunities

**Consider fine-tuning Llama 3.3 70B on:**
- Your specialty's clinical guidelines
- Common patient questions in your domain
- Specific drug protocols
- Medical coding (ICD-10, CPT)

**Training Data Sources:**
- PubMed Central (open access papers)
- Clinical practice guidelines
- Medical textbooks (with licensing)
- De-identified clinical notes (with IRB approval)

---

## Tips

✅ **DO:**
- Use Med-PaLM 2 or Claude for clinical reasoning
- Always verify drug interactions via DrugBank
- Use RAG for current clinical guidelines
- Ensure HIPAA compliance for patient data
- Have human physician review AI outputs

❌ **DON'T:**
- Use general LLMs for clinical decisions without RAG
- Send PHI to non-BAA APIs
- Trust LLMs for drug dosing without verification
- Skip human review on patient-facing content
- Use outdated medical knowledge bases
