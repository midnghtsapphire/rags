# Complete Project Lifecycle Guide

**Purpose:** End-to-end guide from idea to operational business  
**Last Updated:** 2026-01-30

---

## Overview

This system covers the complete lifecycle of a business and product from initial idea through ongoing operations. Perfect for grant applications, investor pitches, and systematic project execution.

---

## 8 Phases

| Phase | Name | Duration | Cost | When |
|-------|------|----------|------|------|
| **0** | [Inception](#phase-0-inception) | 2-4 weeks | $2K-10K | Before anything |
| **1** | [Planning](#phase-1-planning) | 2-4 weeks | $0-5K | After legal entity |
| **2** | [Design](#phase-2-design) | 2-6 weeks | $5K-20K | Before coding |
| **3** | [Development](#phase-3-development) | 3-6 months | $20K-100K | After design |
| **4** | [Testing](#phase-4-testing) | 2-4 weeks | $5K-15K | During/after dev |
| **5** | [Deployment](#phase-5-deployment) | 1-2 weeks | $2K-10K | After testing |
| **6** | [Compliance](#phase-6-compliance) | Ongoing | $5K-50K/year | Before launch + ongoing |
| **7** | [Maintenance](#phase-7-maintenance) | Continuous | $5K-20K/month | After launch |

**Total Initial Investment:** $39K-160K  
**Ongoing Monthly:** $5K-20K

---

## Phase 0: Inception

**Goal:** Transform idea into legal business entity

### Subphases:
1. **Idea Validation** - Customer interviews, market research
2. **Branding** - Name, logo, domain
3. **Legal Entity** - LLC/Corp registration, EIN
4. **Tax Setup** - W-4, W-9, payroll
5. **Intellectual Property** - Patents, trademarks
6. **Banking** - Business account, accounting

### Key Deliverables:
- [ ] 10-20 customer interviews completed
- [ ] Business name and logo finalized
- [ ] Registered with Secretary of State
- [ ] EIN obtained from IRS
- [ ] Patent search completed
- [ ] Business bank account opened

### Templates:
- [Legal Entity Checklist](./0-inception/legal-entity/legal-entity-checklist.md)
- [Patent Search Template](./0-inception/intellectual-property/patent-search-template.md)

**[Full Phase 0 Guide →](./0-inception/README.md)**

---

## Phase 1: Planning

**Goal:** Create strategic plans and technical blueprints

### Document Types:
1. **Roadmap** - Strategic timeline (quarterly updates)
2. **Blueprint** - Technical architecture
3. **Implementation Plan** - Execution strategy
4. **Business Plan** - Full business case (for investors)
5. **Grant Proposal** - Funding requests
6. **Project Plan** - Task management (weekly)

### Key Deliverables:
- [ ] Product roadmap (12-month)
- [ ] Technical architecture diagram
- [ ] Implementation plan with phases
- [ ] Business plan (if seeking funding)
- [ ] Grant proposal (if applicable)

### Current Plans:
- [Claude's Domain Implementation Plan](./1-planning/implementation-plans/claude-domain-implementation-plan-2026-01-30.docx) ⭐

**[Full Phase 1 Guide →](./1-planning/README.md)**

---

## Phase 2: Design

**Goal:** Create visual and technical designs

### Deliverables:
1. **Wireframes** - Low-fidelity UI sketches
2. **Mockups** - High-fidelity visual designs
3. **Prototypes** - Interactive demos
4. **User Flows** - Navigation diagrams
5. **UML Diagrams** - Technical class/sequence diagrams
6. **ERD** - Database schema
7. **Architecture** - System design

### Key Deliverables:
- [ ] Wireframes for all screens
- [ ] High-fidelity mockups
- [ ] Clickable prototype
- [ ] Database schema (ERD)
- [ ] System architecture diagram

### Tools:
- Figma (UI/UX)
- Lucidchart (diagrams)
- dbdiagram.io (database)

**[Full Phase 2 Guide →](./2-design/README.md)**

---

## Phase 3: Development

**Goal:** Build the product

### Methodologies:
- **Kanban** - Continuous flow, small teams
- **Scrum** - 2-week sprints, larger teams
- **Agile** - Fast iteration, changing requirements

### Key Deliverables:
- [ ] Working MVP
- [ ] Code in version control (GitHub)
- [ ] CI/CD pipeline configured
- [ ] Documentation written
- [ ] Code reviews completed

### Tools:
- GitHub (version control)
- Jira/Linear (project management)
- GitHub Actions (CI/CD)

**[Full Phase 3 Guide →](./3-development/README.md)**

---

## Phase 4: Testing

**Goal:** Find and fix bugs before launch

### Test Types:
- **Unit Tests** - Individual functions
- **Integration Tests** - Component interactions
- **E2E Tests** - Full user flows
- **Performance Tests** - Load/stress testing
- **Security Tests** - Vulnerability scans

### Key Deliverables:
- [ ] Test plan documented
- [ ] 80%+ code coverage
- [ ] All critical bugs fixed
- [ ] Performance benchmarks met
- [ ] Security scan passed

### Tools:
- Jest, Pytest (unit tests)
- Playwright (E2E)
- Sentry (error tracking)

**[Full Phase 4 Guide →](./4-testing/README.md)**

---

## Phase 5: Deployment

**Goal:** Launch to production safely

### Deliverables:
- **Deployment Checklist** - Pre-launch verification
- **Rollout Plan** - Phased deployment
- **Rollback Plan** - Revert if needed
- **Release Notes** - What's new
- **Monitoring** - Uptime and errors

### Key Deliverables:
- [ ] Deployment checklist completed
- [ ] Rollback plan tested
- [ ] Monitoring configured
- [ ] Release notes published
- [ ] Successfully deployed to production

### Tools:
- GitHub Actions (CI/CD)
- Vercel, Railway, AWS (hosting)
- Datadog, New Relic (monitoring)

**[Full Phase 5 Guide →](./5-deployment/README.md)**

---

## Phase 6: Compliance

**Goal:** Meet regulatory and legal requirements

### Compliance Types:
- **SOX** - Financial controls (public companies)
- **Six Sigma** - Quality management
- **HIPAA** - Healthcare data
- **GDPR** - EU privacy
- **SOC 2** - Security controls (SaaS)
- **AI Ethics** - Responsible AI use

### Key Deliverables:
- [ ] Privacy policy published
- [ ] Terms of service published
- [ ] Security policy documented
- [ ] Compliance certifications (if needed)
- [ ] Regular audits scheduled

### When You Need Each:
- **SOX** - If public company or planning IPO
- **HIPAA** - If handling healthcare data
- **GDPR** - If serving EU customers
- **SOC 2** - If B2B SaaS company
- **AI Ethics** - If using AI/ML models

**[Full Phase 6 Guide →](./6-compliance/README.md)**

---

## Phase 7: Maintenance

**Goal:** Keep product running and improving

### Activities:
- **Monitoring** - Uptime, errors, performance
- **Patches** - Security updates
- **Updates** - Dependency upgrades
- **Bug Fixes** - User-reported issues
- **Features** - New functionality
- **Support** - Customer help

### Key Deliverables:
- [ ] 99.9% uptime maintained
- [ ] Security patches applied within 24 hours
- [ ] Dependencies updated monthly
- [ ] Bug backlog < 50 items
- [ ] Customer support SLA met

### Tools:
- Datadog (monitoring)
- Sentry (errors)
- PagerDuty (alerts)
- Dependabot (updates)

**[Full Phase 7 Guide →](./7-maintenance/README.md)**

---

## When to Use Each Methodology

### Kanban
**Use when:**
- Continuous flow of work
- No fixed deadlines
- Support/maintenance work
- Small team (1-3 people)

**Don't use when:**
- Need predictable velocity
- Large team coordination
- Fixed sprint commitments

---

### Scrum
**Use when:**
- Fixed 2-week sprints
- Clear deliverables
- Larger team (5-9 people)
- Need predictable velocity

**Don't use when:**
- Requirements change constantly
- Very small team
- Continuous deployment

---

### Agile
**Use when:**
- Requirements change frequently
- Need fast iteration
- Customer feedback is critical
- Startup/product development

**Don't use when:**
- Fixed scope contracts
- Regulatory requirements need waterfall
- Team unfamiliar with agile

---

### Six Sigma
**Use when:**
- Manufacturing or operations
- Need to reduce defects
- Process optimization
- Large-scale operations

**Don't use when:**
- Software development (use Agile instead)
- Creative work
- Rapid prototyping

---

### SOX Compliance
**Use when:**
- Public company
- Planning IPO
- Financial reporting
- Audit requirements

**Don't use when:**
- Private company with no IPO plans
- Pre-revenue startup

---

## Cost Summary

### Initial Investment (Phases 0-5):
| Phase | Low | High |
|-------|-----|------|
| 0. Inception | $2,000 | $10,000 |
| 1. Planning | $0 | $5,000 |
| 2. Design | $5,000 | $20,000 |
| 3. Development | $20,000 | $100,000 |
| 4. Testing | $5,000 | $15,000 |
| 5. Deployment | $2,000 | $10,000 |
| **TOTAL** | **$34,000** | **$160,000** |

### Ongoing Costs (Phases 6-7):
| Item | Monthly |
|------|---------|
| Compliance | $400-4,000 |
| Maintenance | $5,000-20,000 |
| **TOTAL** | **$5,400-24,000** |

---

## Timeline

### Typical Startup Timeline:
- **Weeks 1-4:** Phase 0 (Inception)
- **Weeks 5-8:** Phase 1 (Planning)
- **Weeks 9-14:** Phase 2 (Design)
- **Weeks 15-38:** Phase 3 (Development) - 6 months
- **Weeks 39-42:** Phase 4 (Testing)
- **Weeks 43-44:** Phase 5 (Deployment)
- **Ongoing:** Phases 6-7 (Compliance & Maintenance)

**Total Time to Launch:** 10-11 months

---

## For Grant Applications

### What Grant Committees Want to See:

1. **Completed Phase 0** - Proof of legal entity
   - EIN confirmation
   - Secretary of State registration
   - Operating agreement

2. **Detailed Phase 1** - Clear plan
   - Implementation plan
   - Timeline with milestones
   - Budget breakdown

3. **Phase 2 Designs** (if applicable) - Visual proof
   - Mockups or prototypes
   - Technical architecture

4. **Compliance Plan** - Risk mitigation
   - IP protection strategy
   - Regulatory compliance plan
   - Security measures

### Grant-Ready Checklist:
- [ ] Legal entity registered
- [ ] EIN obtained
- [ ] Patent search completed
- [ ] Implementation plan written
- [ ] Budget detailed by phase
- [ ] Timeline with milestones
- [ ] Team qualifications documented
- [ ] Impact metrics defined

---

## Example: SSA/Disability LLM Project

### Phase 0: Inception (Weeks 1-4)
- [ ] Interview 20 disability attorneys
- [ ] Register "DisabilityAI" LLC in Delaware
- [ ] Get EIN
- [ ] Patent search: "AI for legal research"
- [ ] Trademark "DisabilityAI"

### Phase 1: Planning (Weeks 5-8)
- [ ] Use Claude's implementation plan ✅
- [ ] Write SBIR grant proposal
- [ ] Create 12-month roadmap

### Phase 2: Design (Weeks 9-14)
- [ ] Wireframes for attorney dashboard
- [ ] Database schema for POMS data
- [ ] RAG architecture diagram

### Phase 3: Development (Weeks 15-38)
- [ ] Scrape SSA.gov data
- [ ] Build RAG system
- [ ] Fine-tune Llama 3.3 70B
- [ ] Build web interface

### Phase 4: Testing (Weeks 39-42)
- [ ] Beta test with 5 attorneys
- [ ] Validate accuracy vs. human
- [ ] Performance testing

### Phase 5: Deployment (Weeks 43-44)
- [ ] Deploy to production
- [ ] Launch to 50 beta users

### Phase 6-7: Ongoing
- [ ] HIPAA compliance (if storing client data)
- [ ] SOC 2 certification (for enterprise sales)
- [ ] Quarterly POMS updates
- [ ] Customer support

---

## Folder Structure

```
/projects/
├── 0-inception/
│   ├── idea-validation/
│   ├── branding/
│   ├── legal-entity/
│   ├── tax-setup/
│   ├── intellectual-property/
│   └── banking/
├── 1-planning/
│   ├── roadmaps/
│   ├── blueprints/
│   ├── implementation-plans/
│   ├── business-plans/
│   ├── grant-proposals/
│   └── project-plans/
├── 2-design/
├── 3-development/
├── 4-testing/
├── 5-deployment/
├── 6-compliance/
└── 7-maintenance/
```

---

## Quick Start

### Starting a New Project:

1. **Create project folder:** `/projects/0-inception/[project-name]/`
2. **Complete Phase 0 checklist**
3. **Move to Phase 1 when legal entity is formed**
4. **Progress through phases sequentially**
5. **Don't skip phases** (especially 0 and 1)

### For Grant Applications:

1. **Complete Phase 0 first** (grants require legal entity)
2. **Create detailed Phase 1 plan**
3. **Use templates** in `/1-planning/grant-proposals/`
4. **Show you understand full lifecycle** (reference this guide)

---

## Related Folders

- **[/oz/](./oz/)** - LLM stacks for AI projects
- **[/research/](./research/)** - Domain research
- **[/rag/](./rag/)** - RAG implementation guides
- **[/tasks/](./tasks/)** - To-do lists
- **[/braindump/](./braindump/)** - Idea capture

---

## Notes

- This is a comprehensive system - not every project needs every phase
- Grants and investors want to see you understand the full lifecycle
- Phase 0 (Inception) is often skipped but is CRITICAL for legal/funding
- Compliance (Phase 6) requirements vary by industry
- Maintenance (Phase 7) costs are often underestimated

---

**Last Updated:** 2026-01-30  
**Version:** 1.0
