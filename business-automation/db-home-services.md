# Case Study: AI-Driven Operations at DB Home Services

**Business:** DB Home Services — Mobile auto detailing & custom glass installation
**Location:** Austin, Texas | **Period:** 2024–Present | **Role:** Founder & Operations Lead

---

## Overview

DB Home Services was built using AI tools as a core part of the business infrastructure — not as a supplement, but as a foundational layer from day one. This document covers how AI was applied across every major business function and what was learned in the process.

---

## AI Integration Map

| Business Function | Tools Used | Application |
|------------------|-----------|-------------|
| Branding & Positioning | ChatGPT, Claude | Business name, tagline, brand voice |
| Marketing Copy | Claude, ChatGPT | Email templates, social posts, service descriptions |
| Pricing Strategy | ChatGPT | Competitive analysis, pricing tiers |
| Customer Communication | Claude | Response templates, follow-up sequences |
| SOPs | Claude | Step-by-step operational procedures |
| Sales Scripts | Claude, ChatGPT | Discovery call scripts, objection handling |
| CRM Automation | GoHighLevel + ChatGPT | Workflow design, automation logic |
| Market Research | Gemini, Claude | Local competitor analysis, customer personas |
| Business Documentation | Claude | Contracts, policies, service agreements |

---

## Prompt Engineering Applied

### Challenge: Inconsistent customer messaging

**Problem:** Different response styles depending on which AI was used, causing brand voice inconsistency.

**Solution:** Built a master brand voice document prepended to every customer-facing prompt:

```xml
<context>
DB Home Services brand voice:
- Professional but conversational
- Confident, never pushy
- Specific about Austin — use local references
- Response length: match the customer's message length
- Never use: "synergy," "leverage," "circle back," corporate jargon
</context>
```

**Result:** Consistent tone across all communications regardless of which model generated the first draft.

---

## Workflow Example: Customer Follow-Up Sequence

**Objective:** 3-message follow-up for leads who requested a quote but didn't respond.

**Process:**
1. Defined sequence structure manually (timing, tone, objective per message)
2. Generated drafts using XML-structured prompts with brand voice context
3. Evaluated outputs from Claude and ChatGPT side-by-side
4. Selected Claude for messages 1–2 (better constraint adherence)
5. Selected ChatGPT for message 3 (stronger urgency framing)
6. Edited both for final voice consistency
7. Loaded into GoHighLevel automation

**Result:** ~2 hours of manual writing reduced to ~25 minutes including evaluation and editing.

---

## Key Learnings

**1. AI is a first-draft tool, not a final output tool**
Every AI-generated document required human review. The value is speed of generating a usable draft — not automatic publication-ready output.

**2. Prompt quality determines output quality**
Vague prompts produce generic outputs. Specific, constrained XML-structured prompts produce immediately usable results.

**3. Model selection matters per task type**
Claude excelled at nuanced, constraint-heavy writing. ChatGPT excelled at structured templates and iterative brainstorming.

**4. Evaluation skills are the real differentiator**
Effective AI use requires evaluating whether output is actually good — not just whether it looks good. That is what separates high-value AI users from average ones.
