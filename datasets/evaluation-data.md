# Evaluation Data — Scored Results Archive

**Diego Duarte — AI Research Lab**
*Data Version: 1.0 | Last Updated: June 2025*

---

## Overview

This file archives the raw scoring data from all completed evaluations. Each row represents one model's performance on one task, scored on the 5-dimension rubric defined in research-methodology.md.

Scoring dimensions (0-5 each):
- A = Accuracy
- I = Instruction Following
- R = Reasoning Quality
- C = Creativity / Usefulness
- Co = Conciseness
- Total = Sum / 25 x 100

---

## Evaluation Results Table

### Task Group 1: Sales Outreach (PROMPT-001)
*3-email cold outreach sequence | Benchmark: llm-evaluations/claude-vs-chatgpt.md*

| Model | Version | A | I | R | C | Co | Total | Date |
|-------|---------|---|---|---|---|----|-------|------|
| Claude | 3.5 Sonnet | 5 | 5 | 4 | 5 | 4 | 92 | June 2025 |
| GPT-4o | June 2025 | 5 | 5 | 4 | 4 | 5 | 92 | June 2025 |
| DeepSeek | V3 | 4 | 4 | 3 | 4 | 4 | 76 | June 2025 |

**Winner:** Tie (Claude for tone, GPT-4o for structure)
**Notes:** Claude's emails felt more human. GPT-4o's subject lines were stronger.

---

### Task Group 2: Email Subject Lines (PROMPT-002)
*10 re-engagement subject lines | Benchmark: ai-case-studies/sales-outreach-benchmark.md*

| Model | Version | A | I | R | C | Co | Total | Date |
|-------|---------|---|---|---|---|----|-------|------|
| Claude | 3.5 Sonnet | 5 | 5 | 4 | 5 | 5 | 96 | June 2025 |
| GPT-4o | June 2025 | 5 | 5 | 4 | 4 | 5 | 92 | June 2025 |

**Winner:** Claude
**Notes:** Claude produced more variety across curiosity/urgency/value categories. GPT-4o's options were usable but more similar to each other.

---

### Task Group 3: Market Research (PROMPT-003)
*Competitive landscape analysis | Benchmark: ai-case-studies/market-research-benchmark.md*

| Model | Version | A | I | R | C | Co | Total | Date |
|-------|---------|---|---|---|---|----|-------|------|
| Claude | 3.5 Sonnet | 4 | 5 | 5 | 4 | 4 | 88 | June 2025 |
| Gemini | 1.5 Pro | 4 | 4 | 4 | 3 | 3 | 72 | June 2025 |

**Winner:** Claude
**Notes:** Gemini tried to cite specific local businesses but made unverifiable claims. Claude's framework was more reliable even if less specific.

---

### Task Group 4: Business Automation SOP (PROMPT-004)
*Customer follow-up SOP | Benchmark: business-automation/db-home-services.md*

| Model | Version | A | I | R | C | Co | Total | Date |
|-------|---------|---|---|---|---|----|-------|------|
| Claude | 3.5 Sonnet | 5 | 5 | 5 | 5 | 4 | 96 | June 2025 |
| GPT-4o | June 2025 | 5 | 5 | 4 | 4 | 5 | 92 | June 2025 |

**Winner:** Claude
**Notes:** Claude's SOP was implementable same-day. GPT-4o was clean and well-formatted but slightly more generic.

---

## Aggregate Performance Summary

| Model | Tasks Evaluated | Avg Score | Best Category | Weakness |
|-------|----------------|-----------|---------------|----------|
| Claude 3.5 Sonnet | 4 | 93.0 | Business SOPs, Tone | Can be verbose |
| GPT-4o | 3 | 92.0 | Structure, Subject lines | Can be generic |
| DeepSeek V3 | 1 | 76.0 | Speed | Instruction following |
| Gemini 1.5 Pro | 1 | 72.0 | Local specificity attempts | Hallucination risk |

---

## Data Integrity Notes

- All evaluations conducted through web interfaces (not API)
- Temperature settings: default (not controlled)
- Single-run results unless noted otherwise
- Scoring done immediately after each output (not batch scored)
- Evaluator: Diego Duarte (solo — see research-methodology.md for bias mitigation)

---

## Pending Evaluations

| Task | Models | Status | Target Date |
|------|--------|--------|-------------|
| DeepSeek vs Qwen (reasoning task) | DeepSeek V3, Qwen 2.5 | In progress | July 2025 |
| Gemini vs Claude (creative task) | Gemini 1.5 Pro, Claude 3.5 | Planned | July 2025 |
| Hallucination stress test | All 4 models | Planned | July 2025 |
| Bilingual output parity | Claude, GPT-4o | Planned | July 2025 |

---

*Diego Duarte | AI Research Lab | Austin, Texas*
