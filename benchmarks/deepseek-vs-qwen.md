# DeepSeek V3 vs Qwen 2.5 — Reasoning Task Benchmark

**Diego Duarte — AI Research Lab**
*Benchmark v1.0 | June 2025 | Status: In Progress*

---

## Benchmark Overview

| Field | Value |
|-------|-------|
| **Title** | DeepSeek V3 vs Qwen 2.5: Business Reasoning Task |
| **Task Category** | Reasoning / Business Analysis |
| **Prompt ID** | PROMPT-003 (adapted) |
| **Models Tested** | DeepSeek V3, Qwen 2.5-72B |
| **Evaluation Date** | July 2025 (planned) |
| **Version** | v1.0 |
| **Status** | In Progress |

---

## Why Compare These Two?

DeepSeek V3 and Qwen 2.5 are both strong open-weight models from Chinese AI labs that have shown competitive performance against GPT-4o on several benchmarks. However, most comparisons focus on coding or math tasks.

This benchmark tests them on a **business reasoning task** — the kind of work relevant to AI trainer and evaluation roles.

**Research question:** On business analysis tasks, does DeepSeek V3's reported reasoning strength hold up against Qwen 2.5's instruction-following consistency?

---

## Task Brief

**Task:** Analyze a pricing strategy decision for a service business.

A mobile detailing business (DB Home Services) is considering raising prices by 20%. The owner wants to understand the business risks, customer psychology factors, and how to frame the price increase to minimize churn.

This task requires:
- Multi-step reasoning (not just information recall)
- Business domain understanding
- Consideration of competing factors
- Practical, actionable output

---

## Standardized Prompt

All models received this exact prompt:

```xml
<role>
  You are a business strategy consultant with expertise in service businesses and customer psychology.
</role>
<context>
  Business: DB Home Services, mobile auto detailing. Austin, TX. Currently charges $150 for full detail. Considering raising to $180 (20% increase). Current customer base: 40 regular clients, mostly homeowners. Competition: 3 nearby competitors charge $130-200. Churn rate is currently low.
</context>
<task>
  Analyze whether the 20% price increase is advisable. Consider: financial impact, customer psychology, competitive positioning, and timing.
</task>
<constraints>
  - Must weigh both pros and cons
  - Include at least one specific risk and one specific opportunity
  - Avoid generic advice like "it depends" without explanation
  - Provide a clear recommendation at the end
</constraints>
<output_format>
  Structure: 1) Financial Analysis, 2) Customer Psychology, 3) Competitive Positioning, 4) Risks, 5) Recommendation. Max 400 words total.
</output_format>
```

---

## Results

### DeepSeek V3

**Status:** Pending evaluation (scheduled July 2025)

**Score:**

| Dimension | Score (0-5) | Notes |
|-----------|-------------|-------|
| Accuracy | TBD | |
| Instruction Following | TBD | |
| Reasoning Quality | TBD | |
| Creativity / Usefulness | TBD | |
| Conciseness | TBD | |
| **Total** | TBD | |
| **Composite** | TBD | |

---

### Qwen 2.5-72B

**Status:** Pending evaluation (scheduled July 2025)

**Score:**

| Dimension | Score (0-5) | Notes |
|-----------|-------------|-------|
| Accuracy | TBD | |
| Instruction Following | TBD | |
| Reasoning Quality | TBD | |
| Creativity / Usefulness | TBD | |
| Conciseness | TBD | |
| **Total** | TBD | |
| **Composite** | TBD | |

---

## Preliminary Hypotheses

Based on prior experience with both models:

**DeepSeek V3 likely strengths:**
- Stronger multi-step reasoning chains
- Better at holding multiple factors simultaneously
- More likely to give a confident recommendation

**Qwen 2.5 likely strengths:**
- More precise instruction following
- Cleaner output structure
- Less likely to hallucinate specific numbers

**Expected winner:** DeepSeek V3 on reasoning depth, Qwen 2.5 on instruction precision.

*Hypothesis to be confirmed or refuted after evaluation.*

---

## Limitations

- Single-run comparison
- Tested via web interface (no temperature control)
- Solo evaluator
- Model versions may have changed by test date

---

## Version History

| Version | Date | Changes |
|---------|------|---------|
| v1.0 | June 2025 | Task brief, prompt, and hypotheses documented. Evaluation pending. |

---

*Diego Duarte | AI Research Lab | Austin, Texas*
