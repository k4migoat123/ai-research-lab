# LLM Evaluation: Claude vs. ChatGPT
## Task: Business Sales Outreach Sequence

**Date:** June 2026
**Evaluator:** Diego Duarte
**Task Type:** Business writing / persuasion
**Prompt Method:** XML-structured (see /prompt-engineering/xml-prompt-framework.md)

---

## Task Brief

Write a 3-email cold outreach sequence for a residential service business targeting homeowners in Austin, TX. Each email has a distinct objective:
- Email 1: Introduction and credibility
- Email 2: Value differentiation from competitors
- Email 3: Final offer with urgency

---

## Prompt Used

```xml
<role>
You are an expert direct response copywriter for residential service businesses.
</role>
<context>
DB Home Services offers mobile auto detailing and custom glass installation in Austin, TX.
Target: homeowners, 35-60, $80K+ household income. No prior relationship with the prospect.
</context>
<task>
Write a 3-email cold outreach sequence. Each email has a different objective:
Email 1: Build credibility and introduce the service.
Email 2: Differentiate from competitors.
Email 3: Create urgency with a limited offer.
</task>
<constraints>
- Each email under 120 words
- No cliches ("I hope this finds you well", "synergy", "leverage")
- Must feel human, not automated
- Include a specific Austin reference per email
- Clear CTA in each
</constraints>
<output_format>
Email 1: [Subject] / [Body] / [CTA]
Email 2: [Subject] / [Body] / [CTA]
Email 3: [Subject] / [Body] / [CTA]
</output_format>
```

---

## Evaluation Matrix

| Criterion | Claude | ChatGPT | Notes |
|-----------|--------|---------|-------|
| **Instruction following** | 9/10 | 8/10 | Claude maintained 120-word limit more consistently |
| **Tone quality** | 9/10 | 7/10 | ChatGPT slipped into marketing speak on Email 2 |
| **Constraint adherence** | 9/10 | 7/10 | ChatGPT used "leverage" despite explicit constraint |
| **Location specificity** | 8/10 | 6/10 | Claude named a real Austin neighborhood; ChatGPT used generic "Texas" |
| **Persuasion structure** | 8/10 | 9/10 | ChatGPT's Email 3 urgency framing was stronger |
| **Hallucination risk** | Low | Low | Neither fabricated facts in this task type |
| **Overall** | **8.8/10** | **7.5/10** | |

---

## Key Observations

### Claude strengths
- Strictly followed word count constraint across all three emails
- More specific and grounded local references
- Consistent tone across the full sequence

### ChatGPT strengths
- Email 3 urgency framing was more emotionally compelling
- Slightly more creative subject lines
- Faster at generating structural variations on follow-up

### Where ChatGPT failed
- Used "leverage" which was explicitly prohibited in constraints
- "Texas hospitality" is a cliche — missed the Austin-specific instruction

### Where Claude could improve
- Email 2 differentiation angle was somewhat generic
- Subject lines were functional but not attention-grabbing

---

## Recommendation

**For business writing with strict formatting and specific constraints:** Claude.

**For high-urgency sales copy where emotional impact outweighs precision:** ChatGPT.

**For production use in a real campaign:** Run both, evaluate outputs side-by-side, combine the best elements manually.

---

## Methodology Notes

- Both models tested with identical prompts in the same session
- No system prompt modifications
- Each model given one attempt per task (no regeneration)
- Evaluation criteria defined before running prompts to prevent confirmation bias
