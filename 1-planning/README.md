# Planning - Document Types & Templates

**Last Updated:** 2026-01-30  
**Purpose:** Store different types of planning documents for projects, grants, and business development

---

## Document Types Explained

### Quick Reference

| Document Type | Purpose | Audience | Detail Level | Update Frequency |
|---------------|---------|----------|--------------|------------------|
| **Roadmap** | Strategic vision | Executives, investors | High-level | Quarterly |
| **Blueprint** | Technical design | Developers | Very detailed | Once (then revise) |
| **Implementation Plan** | Execution strategy | Leadership, PMs | Detailed | Once (then track) |
| **Business Plan** | Business case | Investors, grants | Very detailed | Annually |
| **Grant Proposal** | Funding request | Grant committees | Very detailed | Per application |
| **Project Plan** | Task management | Team | Very detailed | Weekly |

---

## 1. Roadmaps

**What it is:** High-level strategic timeline showing major milestones and phases.

**When to use:**
- Communicating vision to stakeholders
- Board presentations
- Investor updates
- Strategic planning sessions

**What it contains:**
- Major milestones (not detailed tasks)
- Phases and timeline
- Goals and objectives
- Key deliverables

**Example:**
```
Q1 2026: MVP Development
Q2 2026: Beta Testing
Q3 2026: Commercial Launch
Q4 2026: Scale to 100 customers
```

**Folder:** `/planning/roadmaps/`

---

## 2. Blueprints

**What it is:** Technical architecture and system design documentation.

**When to use:**
- Before building a new system
- Technical decision-making
- Developer onboarding
- Architecture reviews

**What it contains:**
- System architecture diagrams
- Tech stack choices
- Data flow and APIs
- Infrastructure requirements
- Security considerations

**Example:**
```
User → Claude 3.5 Sonnet → RAG System → Vector DB → Response
```

**Folder:** `/planning/blueprints/`

---

## 3. Implementation Plans

**What it is:** Comprehensive execution strategy with phases, costs, timeline, and risks.

**When to use:**
- Starting a new major initiative
- Seeking leadership approval
- Resource planning
- Risk assessment

**What it contains:**
- Phased approach
- Detailed timeline
- Cost breakdowns
- Resource requirements
- Risk mitigation
- ROI projections
- Success metrics

**Example:** Claude's 40-page domain-specific LLM plan

**Folder:** `/planning/implementation-plans/`

---

## 4. Business Plans

**What it is:** Complete business case with market analysis, financials, and strategy.

**When to use:**
- Fundraising (investors, VCs)
- Major business decisions
- Board approval
- Strategic partnerships

**What it contains:**
- Executive summary
- Market analysis (TAM, SAM, SOM)
- Competitive landscape
- Business model
- Financial projections (5 years)
- Go-to-market strategy
- Team and advisors

**Example:**
```
TAM: $500M (disability legal services)
SAM: $50M (tech-forward law firms)
SOM: $5M (Year 1 target)
```

**Folder:** `/planning/business-plans/`

---

## 5. Grant Proposals

**What it is:** Formal funding request for grants, foundations, or government programs.

**When to use:**
- Applying for SBIR/STTR grants
- Foundation grants
- Research funding
- Non-profit funding

**What it contains:**
- Problem statement
- Proposed solution
- Timeline and milestones
- Detailed budget
- Impact and outcomes
- Team qualifications
- Letters of support

**Example:**
```
We request $50,000 to build the first SSA-specialized LLM
to help disability attorneys serve 2.5M annual claimants.
```

**Folder:** `/planning/grant-proposals/`

---

## 6. Project Plans

**What it is:** Detailed task-level project management documentation.

**When to use:**
- Day-to-day project execution
- Team coordination
- Sprint planning
- Progress tracking

**What it contains:**
- Task lists with assignments
- Dependencies
- Deadlines
- Status updates
- Blockers and risks
- Weekly progress

**Example:**
```
Week 1:
- [ ] Set up dev environment @john
- [ ] Scrape SSA.gov data @sarah
- [ ] Interview 5 attorneys @mike
```

**Folder:** `/planning/project-plans/`

---

## Naming Convention

### Format:
```
[llm]-[project]-[type]-YYYY-MM-DD.md
[llm]-[project]-[type]-YYYY-MM-DD-ABOUT.md
```

### Examples:
```
claude-ssa-llm-roadmap-2026-01-30.md
claude-ssa-llm-roadmap-2026-01-30-ABOUT.md

chatgpt-insurance-blueprint-2026-02-15.md
chatgpt-insurance-blueprint-2026-02-15-ABOUT.md

oz-mechatronopolis-business-plan-2026-03-01.md
oz-mechatronopolis-business-plan-2026-03-01-ABOUT.md
```

### When using OZ (multiple LLMs):
```
oz-[project]-[type]-YYYY-MM-DD.md
```

### When using single LLM:
```
claude-[project]-[type]-YYYY-MM-DD.md
chatgpt-[project]-[type]-YYYY-MM-DD.md
gemini-[project]-[type]-YYYY-MM-DD.md
```

---

## Current Documents

### Implementation Plans
- **[Claude's Domain-Specific LLM Plan](./implementation-plans/claude-domain-implementation-plan-2026-01-30.docx)** ⭐
  - 40+ page comprehensive plan
  - All domains covered
  - SSA/Disability identified as blue ocean
  - [Full context](./implementation-plans/claude-domain-implementation-plan-2026-01-30-ABOUT.md)

---

## For Grant Applications

### What Grant Committees Want:

1. **Problem Statement**
   - What problem are you solving?
   - Why does it matter?
   - Who is affected?

2. **Solution**
   - How will you solve it?
   - Why is your approach better?
   - What makes it innovative?

3. **Timeline**
   - When will you deliver?
   - What are the milestones?
   - What's the critical path?

4. **Budget**
   - How much do you need?
   - What will you spend it on?
   - Why is this amount justified?

5. **Impact**
   - What will change as a result?
   - How will you measure success?
   - Who will benefit?

6. **Team**
   - Who will execute?
   - What are their qualifications?
   - Do you have domain expertise?

7. **Sustainability**
   - What happens after the grant?
   - How will you sustain the project?
   - What's the long-term plan?

### Grant Folder Structure:

```
/planning/grant-proposals/
├── [grant-name]-proposal-YYYY-MM-DD.md
├── [grant-name]-budget-YYYY-MM-DD.xlsx
├── [grant-name]-timeline-YYYY-MM-DD.md
├── [grant-name]-status-reports/
│   ├── month-1-report.md
│   ├── month-2-report.md
│   └── final-report.md
└── [grant-name]-ABOUT.md
```

---

## Workflow

### Creating a New Planning Document:

1. **Choose document type** based on purpose and audience
2. **Name file** using convention: `[llm]-[project]-[type]-YYYY-MM-DD.md`
3. **Create ABOUT file** with full context and reasoning
4. **Save to appropriate folder**
5. **Link from this README**
6. **Commit to GitHub**

### Using Existing Documents:

1. **Check this README** for available documents
2. **Read ABOUT file first** for context
3. **Review main document** for details
4. **Update if needed** (save as new dated version)
5. **Track in project plan** if executing

---

## Related Folders

- **[/projects/oz/](../oz/)** - Active LLM stacks
- **[/projects/research/](../research/)** - Domain research and analysis
- **[/projects/rag/](../rag/)** - RAG implementation guides
- **[/projects/tasks/](../tasks/)** - To-do lists and task tracking
- **[/projects/braindump/](../braindump/)** - Daily idea capture

---

## Tips

### For ADHD-Friendly Planning:

✅ **DO:**
- Use templates (reduces decision fatigue)
- Save ABOUT files (context for future you)
- Date everything (know when it was created)
- Link related documents (easy navigation)
- Update this README (central index)

❌ **DON'T:**
- Create documents without clear purpose
- Skip ABOUT files (you'll forget context)
- Use vague names (be specific)
- Let documents get stale (archive old versions)
- Forget to commit to GitHub

---

## Next Steps

1. ☐ Review Claude's implementation plan
2. ☐ Decide which projects to pursue
3. ☐ Create roadmaps for chosen projects
4. ☐ Build blueprints for technical projects
5. ☐ Write grant proposals if seeking funding

---

## Notes

- All planning documents should have ABOUT files
- Date everything for easy reference
- Commit to GitHub regularly
- Link related documents
- Update this README when adding new documents
