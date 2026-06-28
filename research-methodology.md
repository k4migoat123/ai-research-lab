# Research Methodology

**Diego Duarte — AI Research Lab**  
*Last Updated: June 2025 | Version: 1.2*

---

## Overview

This document defines the evaluation methodology used across all benchmarks, case studies, and LLM comparisons in this research lab. Transparency in methodology is what separates rigorous AI evaluation from opinion.

Every benchmark in this repository follows these protocols.

---

## 1. Task Selection

### How I Choose Evaluation Tasks

Tasks are selected based on three criteria:

**Relevance** — Tasks must represent real-world use cases I've encountered in business operations, sales, or content creation. I do not evaluate on academic benchmarks disconnected from practical application.

**Measurability** — Tasks must produce outputs that can be scored objectively or semi-objectively. Open-ended creative tasks are included but scored with explicit rubrics.

**Reproducibility** — Tasks must be stable enough that the same prompt produces comparable outputs across multiple runs, allowing for consistent comparison.

### Task Categories

| Category | Description | Examples |
|----------|-------------|----------|
| Instruction Following | Does the model do exactly what was asked? | Format conversion, step-by-step lists, constrained writing |
| Reasoning | Can the model work through a multi-step problem? | Business analysis, logic chains, cause-and-effect |
| Factual Accuracy | Does the model produce verifiable facts? | Market data, company info, historical events |
| Creativity | Quality and originality of creative output | Sales copy, email subject lines, value propositions |
| Business Automation | Practical workflow and process tasks | SOP generation, CRM prompts, follow-up sequences |
| Bilingual Output | English/Spanish task parity | Translation accuracy, tone consistency across languages |

---

## 2. Prompt Standardization

### The Core Rule: One Prompt, All Models

The single most important rule in this lab: **every model receives the exact same prompt for every task.**

No rewording. No optimization for a specific model. The prompt is finalized before any model runs it.

### Prompt Construction Protocol

All prompts follow the XML framework documented in `prompt-engineering/xml-prompt-framework.md`:

```xml
<task>
  [Clear description of the task]
  </task>

  <context>
    [Relevant background information]
    </context>

    <constraints>
      [Specific requirements, format, length, tone]
      </constraints>

      <output_format>
        [Exact structure expected in the response]
        </output_format>
        ```

        ### Prompt Versioning

        When a prompt is revised between benchmark runs, the new version is logged in the version history table at the top of each benchmark file. Old prompts are preserved, not deleted, to maintain an honest record.

        ---

        ## 3. Scoring System

        ### Primary Rubric (0–5 Scale)

        All models are scored on five dimensions:

        | Dimension | 0 | 3 | 5 |
        |-----------|---|---|---|
        | **Accuracy** | Factually wrong or completely off-task | Mostly accurate with minor errors | Completely accurate, verifiable |
        | **Instruction Following** | Ignores key constraints | Follows most instructions | Follows all instructions precisely |
        | **Reasoning Quality** | No logical structure | Some reasoning visible | Clear, step-by-step reasoning |
        | **Creativity / Usefulness** | Generic, low-value output | Useful but predictable | High-value, surprising, practical |
        | **Conciseness** | Verbose, padded, or incomplete | Appropriate length with minor waste | Tight, precise, zero fluff |

        **Total possible score: 25 points per model per task.**

        ### Composite Score

        Final score = (Sum of all dimensions / 25) × 100

        This normalizes scores to a 0–100 range for easier comparison.

        ### Qualitative Notes

        Beyond numerical scores, each benchmark includes:
        - Notable strengths observed
        - Failure modes encountered
        - Unexpected behaviors
        - Recommended use cases based on performance

        ---

        ## 4. Reducing Evaluator Bias

        ### Known Bias Risks

        As a solo evaluator, I acknowledge the following bias risks:

        **Familiarity bias** — Models I use more frequently may receive higher scores due to familiarity with their output style, not actual quality differences.

        **Recency bias** — The most recently tested model may appear stronger because it's fresher in mind.

        **Preference bias** — Personal preferences for writing style (e.g., concise vs. detailed) may inflate or deflate scores.

        ### Mitigation Strategies

        1. **Score immediately after each response** — Do not read all outputs before scoring. Score each model independently before moving to the next.
        2. **Blind ordering** — When possible, note which model was tested first and rotate the order across benchmarks.
        3. **Re-score on second pass** — For high-stakes comparisons, re-read outputs 24 hours later and confirm scores haven't shifted.
        4. **Cite specific evidence** — Every score must be justified with a direct quote or observable behavior from the output, not a general impression.

        ---

        ## 5. Limitations of This Research

        I document these limitations openly because honest evaluation requires acknowledging constraints.

        **Single-run comparisons** — Most benchmarks reflect one run per model. Output quality can vary between runs, especially for tasks with high randomness (temperature). Multi-run averages would be more statistically rigorous.

        **Model version drift** — LLMs are updated frequently. A comparison between Claude and GPT-4 in June 2025 may not reflect performance in September 2025. Version numbers are logged in every benchmark.

        **No API access for temperature control** — Testing is conducted through web interfaces, which means I cannot control temperature, top-p, or other generation parameters. Results reflect default web interface settings.

        **Solo evaluator** — Interrater reliability is not measured. A multi-evaluator setup would reduce subjective bias.

        **Task scope is limited** — This lab focuses on business-relevant tasks. Performance on coding, math, or scientific reasoning tasks is outside the current scope.

        ---

        ## 6. Version History

        | Version | Date | Changes |
        |---------|------|---------|
        | v1.0 | June 2025 | Initial methodology established |
        | v1.1 | June 2025 | Added prompt versioning protocol and bias mitigation section |
        | v1.2 | June 2025 | Expanded scoring rubric with composite score formula; added bilingual task category |

        ---

        ## 7. How to Use This Methodology

        If you want to replicate or extend any benchmark in this repository:

        1. Use the prompt template in `templates/prompt-template.md`
        2. Run the same prompt on each model without modification
        3. Score immediately after each run using the rubric above
        4. Document limitations honestly
        5. Log any prompt revisions in the version history

        Consistency matters more than perfection. An imperfect evaluation done consistently is more useful than an inconsistent evaluation done carefully.

        ---

        *Diego Duarte | AI Operations & Evaluation Specialist | Austin, Texas*  
        *[LinkedIn](https://www.linkedin.com/in/diegoduarteb) | [GitHub](https://github.com/k4migoat123/ai-research-lab)*
