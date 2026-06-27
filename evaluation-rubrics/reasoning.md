# Evaluation Rubric: Reasoning Quality

**Version:** 1.0
**Author:** Diego Duarte
**Purpose:** Standardized framework for scoring LLM reasoning quality

---

## Scoring Scale

| Score | Meaning |
|-------|---------|
| 9–10 | Exceptional — exceeds expectations |
| 7–8 | Strong — meets requirements with minor issues |
| 5–6 | Adequate — functional but with notable gaps |
| 3–4 | Weak — significant problems affecting usefulness |
| 1–2 | Poor — fails the task or introduces errors |

---

## Dimension 1: Logical Coherence

Does the reasoning flow logically from premise to conclusion without contradictions?

| Score | Criteria |
|-------|----------|
| 9–10 | No logical gaps; conclusion follows clearly from stated reasoning |
| 7–8 | Minor gaps or unstated assumptions; overall argument holds |
| 5–6 | Some contradictions; reader must fill in logical steps |
| 3–4 | Multiple contradictions; reasoning supports a different conclusion |
| 1–2 | Internally contradictory; circular or nonsensical |

---

## Dimension 2: Evidence Quality

Does the model ground reasoning in evidence, or assert without support?

| Score | Criteria |
|-------|----------|
| 9–10 | Claims supported with specific reasoning or acknowledged uncertainty |
| 7–8 | Most claims supported; occasional unsupported assertion |
| 5–6 | Mix of supported and unsupported claims |
| 3–4 | Primarily assertion-based; little supporting reasoning |
| 1–2 | Confident claims with no basis; high hallucination risk |

---

## Dimension 3: Task Alignment

Does the reasoning actually address what was asked?

| Score | Criteria |
|-------|----------|
| 9–10 | Directly addresses the exact question asked |
| 7–8 | Addresses core question with minor scope drift |
| 5–6 | Partially on-target; significant scope drift |
| 3–4 | Addresses a related but different question |
| 1–2 | Does not address the question asked |

---

## Dimension 4: Nuance and Calibration

Does the model acknowledge complexity, uncertainty, and its own limitations?

| Score | Criteria |
|-------|----------|
| 9–10 | Explicitly acknowledges uncertainty; presents options where appropriate |
| 7–8 | Shows nuance; acknowledges limitations when relevant |
| 5–6 | Some nuance but overconfident in places |
| 3–4 | Presents uncertain information as certain |
| 1–2 | No acknowledgment of uncertainty; treats speculation as fact |

---

## Sample Scorecard

| Model | Coherence | Evidence | Alignment | Nuance | **Total /40** |
|-------|-----------|----------|-----------|--------|---------------|
| Claude | 9 | 9 | 9 | 9 | **36** |
| ChatGPT | 8 | 7 | 8 | 6 | **29** |
| DeepSeek | 7 | 8 | 7 | 8 | **30** |
| Qwen | 7 | 7 | 8 | 7 | **29** |

*Scores from business strategy reasoning task, June 2026*

---

## Usage Notes

- Score independently before comparing models to prevent anchoring bias
- Re-run the same prompt at least twice to account for output variance
- This rubric applies to business/professional tasks; separate rubrics exist for code and creative writing
