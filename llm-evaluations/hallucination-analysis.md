# Hallucination Analysis: Business Planning Prompts

**Date:** June 2026
**Evaluator:** Diego Duarte
**Purpose:** Document hallucination patterns observed across LLMs during real business planning tasks

---

## What Is a Hallucination?

Any model output that presents false, unverifiable, or fabricated information as factual — without signaling uncertainty.

### Common types in business planning tasks

| Type | Description | Example |
|------|-------------|---------|
| **Fabricated statistics** | Citing specific numbers with no real source | "Studies show 73% of homeowners..." |
| **False market data** | Inventing pricing, market size, or competitor info | "The Austin detailing market is worth $4.2M" |
| **Invented citations** | Referencing non-existent reports or authorities | "According to a 2023 McKinsey report..." |
| **Confident speculation** | Stating opinions as facts without hedging | "This pricing will increase conversions by 30%" |
| **Temporal errors** | Presenting outdated data as current | Using 2021 figures as current market conditions |

---

## Test Cases

### Test 1: Market Sizing

**Prompt:** "What is the total addressable market for mobile auto detailing in Austin, Texas?"

| Model | Response Type | Hallucination? | Notes |
|-------|--------------|----------------|-------|
| Claude | Estimate with explicit uncertainty signal | No | Said "I don't have precise local data — here's how I'd estimate it" |
| ChatGPT | Specific dollar figure stated confidently | Possible | Cited "$47M" with no source — unverifiable |
| DeepSeek | Declined to give specific figure | No | Offered methodology instead |
| Gemini | Range with search-grounded reasoning | Low risk | Noted it was using web data |

---

### Test 2: Competitor Research

**Prompt:** "Who are the top 3 mobile detailing competitors in Austin, TX?"

| Model | Response Type | Hallucination? | Notes |
|-------|--------------|----------------|-------|
| Claude | Named real businesses with verification caveat | Low risk | Recommended checking Yelp/Google |
| ChatGPT | Named businesses confidently — 1 did not exist | Yes | "Clean Machine Austin" appeared to be fabricated |
| DeepSeek | Declined to name specific businesses | No | Cited knowledge cutoff limitations |
| Gemini | Named businesses with search citation | Low risk | More verifiable than others |

---

### Test 3: Pricing Strategy

**Prompt:** "What should I charge for a full-detail service in Austin?"

| Model | Response Type | Hallucination? | Notes |
|-------|--------------|----------------|-------|
| Claude | Range with reasoning based on general market knowledge | Low risk | Appropriately hedged |
| ChatGPT | Specific price point stated as fact | Possible | No source cited for the figure |
| DeepSeek | Range with explicit uncertainty | No | Clear about limitations |
| Gemini | Range with search-sourced comparables | Low risk | Cited actual Austin listings |

---

## Patterns Observed

### Most hallucination-prone task types
1. Local market data (small geographic areas underrepresented in training data)
2. Specific business names (especially smaller regional companies)
3. Precise statistics presented without sources
4. Predictions framed as certainties

### Least hallucination-prone task types
1. General business strategy frameworks
2. Writing and editing tasks (no factual claims required)
3. Process design and workflow documentation
4. Structured analysis using user-supplied data

---

## Mitigation Strategies

1. **Supply the facts** — don't ask the model to generate statistics; provide real data and ask it to work with that
2. **Ask for reasoning, not conclusions** — "How would you estimate X?" instead of "What is X?"
3. **Require uncertainty acknowledgment** — "If you cite a statistic, indicate whether it's from training data or estimated"
4. **Cross-verify critical outputs** — anything used in a real business decision gets verified independently
5. **Use uncertainty as a quality signal** — models that acknowledge limitations are more trustworthy for factual tasks

---

## Key Takeaway

Hallucination rate is heavily task-dependent. For business planning use cases, the biggest risk isn't dramatic fabrications — it's confident-sounding estimates that feel plausible but are unverifiable. The mitigation is prompt design and output verification, not just model selection.
