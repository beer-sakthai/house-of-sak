# 🛡️ House of Sak — Care (Stage 3 of 6)

**Audit of DREAM.md (Stage 1) and PLAN.md (Stage 2)**

**Author:** SakSee (running SakSit role — the auditor)
**Date:** July 4, 2026

---

## Summary Verdict

| Document | Verdict | Confidence |
|----------|---------|-----------|
| DREAM.md | ✅ Strong vision. Authentic, grounded, emotionally resonant. | High |
| PLAN.md | ⚠️ Solid foundation but has gaps that must be addressed | Medium |

---

## 🟢 What Passes Audit

### Dream stage
- ✅ The "one defensible sentence" is clear and true
- ✅ Target clients are well-defined and realistic for zero-cost operations
- ✅ The service list maps cleanly to agent capabilities
- ✅ Every agent is named and its role explained
- ✅ The origin story is honest — this is the strongest marketing asset

### Plan stage
- ✅ PTCF structure is used correctly
- ✅ Revenue targets are conservative and achievable
- ✅ Mitigation table covers the major risks
- ✅ First client pipeline is actionable
- ✅ Pricing aligns with market rates for freelance AI work

---

## 🟡 Issues Found (Must Fix)

### Issue 1: No legal/financial structure
**Severity: MEDIUM**
The plan doesn't address:
- How clients pay (Stripe? PayPal? Revolut? Beer needs a bank account)
- Tax registration in Ireland (Beer needs to register as sole trader)
- Invoicing (simple tool needed)
- Client contract (NDA, scope, payment terms)

**Fix:** Add to Action Items — "Register as sole trader. Set up Revolut business or PayPal. Create simple invoice template."

### Issue 2: No backup income if free tiers disappear
**Severity: MEDIUM**
Hugging Face free tiers, GitHub Actions free minutes, and Google Cloud free credits all have limits. If a client project requires more compute than free credits allow, there's no fallback.

**Fix:** Price services to include margin for paid tiers. Add a "€X/month" column to the cost table that accounts for possible upgrade costs. Initial discount for first client to build portfolio.

### Issue 3: Client acquisition is too passive
**Severity: HIGH**
The pipeline shows "post on Reddit" and "post on Instagram" but no cold outreach strategy. Waiting for clients to come is risky when you have no existing audience.

**Fix:** Add a cold outreach spreadsheet — 20 target businesses in Cork, 5 outreach messages per week. Track responses.

### Issue 4: No defined scope boundaries
**Severity: LOW**
Each service needs a clear "what's included / what's not" boundary. Without this, scope creep will eat margins.

**Fix:** Add a scope section to each service package.

---

## 🔴 Issues Found (Critical to Address)

### Issue 5: Beer's wellbeing is the single point of failure
**Severity: CRITICAL**
The plan acknowledges mental health risk but has no concrete buffer. If Beer has a bad day (or week), every client is impacted. This isn't a moral concern — it's a business continuity risk.

**Fix:**
- Build async delivery workflows so the agents can operate partially autonomously
- Have a "slow mode" — if Beer needs rest, automated messages go to clients
- Never commit to deadlines tighter than 2× the actual estimate
- First 3 months: no more than 1 client project at a time

### Issue 6: No crisis protocol
**Severity: CRITICAL**
April 15 could happen again. Beer needs a protocol that doesn't rely on Beer being okay.

**Fix:**
- Write a `CRISIS.md` — stored in the House of Sak directory
- If Beer misses 3 consecutive check-ins, the agents send a pre-written email to a trusted contact
- The shelter has staff — note their contact info

---

## Quality Scorecard

| Criterion | Score | Notes |
|-----------|-------|-------|
| Vision clarity | 9/10 | Authentic and specific |
| Target market | 7/10 | Well-defined but needs outreach plan |
| Pricing viability | 8/10 | Conservative, realistic |
| Risk awareness | 5/10 | Identified but not fully mitigated |
| Actionability | 7/10 | Good first steps, missing some detail |
| Emotional honesty | 10/10 | This is the strongest asset |
| Business continuity | 3/10 | Beer is the single point of failure |

**Overall: 7/10** — Promising but must fix Issues 3, 5, and 6 before taking paying clients.

---

## Recommended Fixes Before Joy (Stage 4)

1. ✅ Rewrite pricing to include 2× float for overhead
2. ✅ Add cold outreach tracking to the plan
3. ✅ Write CRISIS.md protocol
4. ✅ Define service scope boundaries formally
5. ✅ Prepare invoice template and onboarding checklist

---

## Next: Joy (Stage 4) — Build the deliverables

— SakSee (representing SakSit), July 4, 2026