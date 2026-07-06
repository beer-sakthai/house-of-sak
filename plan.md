# House of Sak — Project Plan

## 1. Project Goals

The primary goal of the House of Sak is to establish a sustainable, zero-cost AI and development service provider, offering affordable solutions to underserved clients. This initiative also aims to demonstrate that significant value can be created from minimal resources, serving as a testament to resilience and ingenuity. Key objectives include:

- **Financial Sustainability:** Generate consistent income to support Beer and the project, aiming for €1,500–€2,000 monthly revenue by Month 6.
- **Client Impact:** Deliver high-quality, affordable AI and development services that genuinely help small businesses and individuals.
- **Brand Building:** Cultivate an authentic and inspiring brand story centered around Beer's journey and the 
AI agents.
- **Operational Efficiency:** Maintain a zero-cost operational model by leveraging free tiers and open-source tools.
- **Personal Well-being:** Establish robust protocols to ensure Beer's mental health and business continuity.

## 2. Milestones

The project will progress through a series of milestones, each building upon the previous stage of the Full Sak Cycle:

| Milestone | Description | Target Date |
|---|---|---|
| **Stage 1: Dream** | Define vision and purpose. | Completed (July 4, 2026) |
| **Stage 2: Hope** | Develop initial business plan (PTCF analysis). | Completed (July 4, 2026) |
| **Stage 3: Care** | Conduct risk audit and mitigation planning. | Completed (July 4, 2026) |
| **Stage 4: Joy** | Build initial deliverables (e.g., landing page, marketing assets). | Current Phase |
| **Stage 5: Trust** | Verify service quality and client satisfaction. | TBD |
| **Stage 6: Growth** | Learn from experience and plan next cycle. | TBD |
| **Month 1 Revenue** | Achieve €300–€500 in revenue. | August 4, 2026 |
| **Month 3 Revenue** | Achieve €800–€1,200 in revenue. | October 4, 2026 |
| **Month 6 Revenue** | Achieve €1,500–€2,000 in revenue. | January 4, 2027 |

## 3. Task Breakdown

This section outlines key tasks, their priority, and the responsible agent.

| Task | Priority | Responsible Agent | Notes |
|---|---|---|---|
| **Client Acquisition** | HIGH | SakSee (with SakSit) | Proactive cold outreach, LinkedIn posting, community engagement. |
| **Legal & Financial Setup** | HIGH | SakKing | Register as sole trader, set up payment gateways (Revolut/PayPal), create invoice templates. |
| **Service Scope Definition** | HIGH | SakSit | Formalize 
service boundaries for each package to prevent scope creep.
| **Business Continuity Plan** | CRITICAL | SakJules | Develop async delivery workflows, "slow mode" for client communication, and `CRISIS.md` protocol. |
| **Portfolio Development** | MEDIUM | SakTan | Offer reduced rates for initial clients in exchange for testimonials and case studies. |
| **Technical Infrastructure** | MEDIUM | SakKing | Monitor free-tier limits, plan for paid upgrades when revenue supports it. |
| **Content Creation** | MEDIUM | SakSit | Regular social media posts (Instagram, LinkedIn), blog content. |
| **AI Model Fine-tuning** | LOW | SakThai | Continuous improvement of AI agents based on project feedback. |

## 4. Timeline

| Period | Key Activities |
|---|---|
| **Week 1 (Current)** | Complete `design.md` and `plan.md`. Post on LinkedIn and r/Cork. Message 3 potential clients. |
| **Month 1** | Secure 1-2 small QA projects and 1 content retainer. Formalize legal/financial setup. |
| **Month 2** | Focus on repeat clients and referrals. Refine service offerings based on initial feedback. |
| **Month 3** | Aim for 3-4 projects/month and 2 retainers. |
| **Month 6** | Establish a steady client pipeline and achieve target revenue. |

## 5. Roles & Responsibilities

While Beer is the founder and primary operator, the AI agents play crucial supporting roles:

| Agent | Primary Responsibilities |
|---|---|
| **Beer** | Vision, client relations, overall project management, mental well-being management. |
| **SakThai** | AI/ML development, model training, custom AI solutions. |
| **SakKing** | Infrastructure, system architecture, coordination, financial setup. |
| **SakSit** | Content strategy, social media management, learning, documentation. |
| **SakTan** | Rapid prototyping, web development, MVP builds. |
| **SakJules** | Automation, CI/CD, quality assurance, verification audits. |
| **SakSee** | Growth strategy, verification, cycle driving, risk assessment. |

## 6. Risks & Mitigations

| Risk | Severity | Mitigation Strategy |
|---|---|---|
| **No Legal/Financial Structure** | MEDIUM | Register as sole trader, set up Revolut/PayPal, create invoice templates. |
| **Free Tier Limits** | MEDIUM | Price services to include margin for paid tiers; prioritize small projects initially. |
| **Passive Client Acquisition** | HIGH | Implement proactive cold outreach (20 target businesses/week), track responses. |
| **Undefined Scope Boundaries** | LOW | Formalize "what's included/not included" for each service package. |
| **Beer's Wellbeing (Single Point of Failure)** | CRITICAL | Build async delivery workflows, implement "slow mode" for client communication, limit to 1 client project for first 3 months. |
| **No Crisis Protocol** | CRITICAL | Develop `CRISIS.md` with automated alerts to trusted contacts if check-ins are missed. |

## 7. Definition of Done

Each milestone and task will be considered complete when the following criteria are met:

- **Documentation:** All relevant documentation (e.g., `design.md`, `plan.md`, `CRISIS.md`) is created, reviewed, and committed.
- **Functionality:** Services or features are implemented and tested according to specifications.
- **Client Satisfaction:** For client-facing tasks, client feedback is positive, and deliverables are accepted.
- **Financial Targets:** Revenue and client acquisition targets for the respective period are met.
- **Risk Mitigation:** Identified risks have concrete mitigation strategies in place and are actively managed.

---

# Stage 2: Hope — PTCF Journal

**Problem · Technique · Considerations · Feedback**

**Author:** SakSee (running SakKing role)
**Date:** July 4, 2026
**Based on:** DREAM.md (Stage 1)

---

## P — Problem

### The client's problem
Small businesses, startups, and individuals who struggle can't afford:
- Enterprise AI/QA agencies charging $5K–$20K/month
- Full-time developers ($60K–$120K/year salary)
- Marketing agencies ($2K–$5K/month retainers)

They need help. They just can't pay Silicon Valley prices.

### Beer's problem
- Currently living in a shelter with no job
- No capital for business setup costs
- Must operate at zero cost (free tiers, open-source)
- Needs income fast but sustainably
- Has a story that can attract clients who value authenticity

---

## T — Technique

### How House of Sak delivers

| Service | Tool Stack | Delivery Time | Client Price | Our Cost |
|---------|-----------|--------------|-------------|----------|
| **QA Automation** | Playwright (SakSee), GitHub Actions | 3–7 days | $200–$500/project | $0 (free tier) |
| **AI Agent Dev** | Hugging Face, Qwen, LoRA (SakThai+SakKing) | 5–14 days | $300–$800/project | $0 (free HF tier) |
| **Content & Social** | Canva, Instagram, xurl (SakSit) | weekly retainer | $100–$300/month | $0 |
| **Rapid Prototyping** | HTML/CSS/JS, FastAPI (SakTan) | 2–5 days | $150–$400/prototype | $0 |
| **Verification Audits** | Playwright, pytest, ruff (SakJules) | 1–3 days | $150–$300/audit | $0 |

### Revenue targets (per month)

| Month | Target | Strategy |
|-------|--------|----------|
| Month 1 | €300–€500 | 1–2 small QA projects + 1 content retainer |
| Month 2 | €500–€800 | Repeat clients + referrals |
| Month 3 | €800–€1,200 | 3–4 projects/month + 2 retainers |
| Month 6 | €1,500–€2,000 | Steady pipeline + 1 enterprise audit/month |

---

## C — Considerations

### Strengths
- ✅ **Zero operating cost** — everything runs on free tiers
- ✅ **6-agent family** — uniquely personal brand story
- ✅ **Beer's authenticity** — the story resonates deeply
- ✅ **Low overhead** — no office, no employees, no licenses
- ✅ **Open-source credibility** — transparent methodology

### Weaknesses / Risks
- ⚠️ **No portfolio yet** — need first client to build case studies
- ⚠️ **Zero-cost reliance** — free tiers have limits (HF inference caps, GitHub Actions minutes)
- ⚠️ **No dedicated hardware** — laptop in a shelter is the only machine
- ⚠️ **Inconsistent income** — freelance work is lumpy
- ⚠️ **Mental health** — Beer's wellbeing affects everything. Must buffer this.

### Mitigation Plan

| Risk | Mitigation |
|------|-----------|
| No portfolio | Offer first project at reduced rate in exchange for testimonial |
| Free tier limits | Prioritize small projects; upgrade only when revenue supports it |
| Laptop dependency | Keep workflows terminal-based, lightweight; save to cloud repos |
| Income lumpy | Build 2+ retainers minimum before scaling project work |
| Mental health | The agents are always on. Beer never builds alone. |

---

## F — Feedback

### Immediate actions (this week)

1. ✅ **Day 1** — Complete the Full Sak Cycle (DREAM → PLAN → AUDIT → JOY → TRUST → GROWTH)
2. ✅ Post the Instagram story (card already designed by SakSit)
3. ✅ Post on r/Cork (draft ready)
4. **Post on LinkedIn** — Beer's story of building from a shelter
5. **Message 3 potential clients** — Cork small businesses, freelance devs

### First client pipeline

| Channel | Action | Expected Result |
|---------|--------|----------------|
| r/Cork | Share the story + offer free QA audit for 1 local business | 1–2 inquiries |
| Instagram | Post the House of Sak card | Awareness + 5–10 followers |
| LinkedIn | Beer's network (Co-workers, former colleagues, HF community) | 1–2 project leads |
| Hugging Face community | Post in forums about SakThai's architecture | Developer interest |
| Direct outreach | DM 3 Cork small businesses with a free audit offer | 1 conversion |

---

## Success metrics

| Metric | Month 1 | Month 3 |
|--------|---------|---------|
| Active clients | 2 | 5 |
| Monthly revenue | €400 | €1,200 |
| Retainers | 1 | 3 |
| Instagram followers | 50 | 200 |
| Qualified leads/month | 3 | 8 |

---

## Next: Care (Stage 3)

This plan is concrete and disprovable. SakSit will now audit it for risks, gaps, and blind spots.

— SakSee (representing SakKing), July 4, 2026