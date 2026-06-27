# XML Prompt Framework v1.0

## Overview

This is my personal framework for writing structured, reliable prompts for large language models.

XML-style tags create clear boundaries between context, instructions, and constraints. This reduces ambiguity, improves instruction following, and makes prompts easier to debug and iterate.

---

## Core Principle

Most prompt failures happen because the model doesn't know:
- What role it's playing
- What it's working with
- What format the output should take
- What constraints apply

XML tagging solves all four.

---

## Base Template

```xml
<role>
You are [specific role with relevant expertise].
</role>

<context>
[Background information the model needs to understand the task]
</context>

<task>
[Clear, specific instruction for what to produce]
</task>

<constraints>
- [Constraint 1]
- [Constraint 2]
- [Constraint 3]
</constraints>

<output_format>
[Exact format you want: headers, length, tone, structure]
</output_format>
```

---

## Real Example: Sales Outreach Email

```xml
<role>
You are an expert copywriter specializing in cold outreach for residential service businesses.
</role>

<context>
The business is DB Home Services, a mobile auto detailing and glass installation company
based in Austin, Texas. Target customers are homeowners aged 35-60 with household income
above $80K who value convenience and professional service.
</context>

<task>
Write a cold outreach email for a homeowner who left a 5-star review for a competitor
but has not used our service. Goal: introduce DB Home Services and offer a first-time discount.
</task>

<constraints>
- Maximum 150 words
- No generic phrases like "I hope this email finds you well"
- Must reference Austin specifically
- Must include a clear call to action
- Tone: conversational, professional, not salesy
</constraints>

<output_format>
Subject line
Email body
PS line
</output_format>
```

---

## Why This Works

| Element | Purpose |
|---------|--------|
| `<role>` | Anchors the model's persona and expertise level |
| `<context>` | Provides grounding to reduce hallucination |
| `<task>` | Single, clear instruction — not buried in paragraphs |
| `<constraints>` | Prevents common failure modes before they happen |
| `<output_format>` | Eliminates format ambiguity entirely |

---

## When to Use XML Tagging

**High value:**
- Multi-step tasks
- Tasks requiring a specific persona
- Tasks with strict output format requirements
- Tasks where consistency across runs matters

**Lower value:**
- Simple one-line queries
- Creative brainstorming (more freedom = better output)
- Casual conversational exchanges

---

## Iteration Protocol

1. Run the base prompt and capture output
2. Identify the specific failure (format, tone, accuracy, length)
3. Add a targeted constraint addressing only that failure
4. Re-run and compare outputs
5. Document the change and result

Never change more than one variable per iteration — otherwise you can't identify what fixed the problem.
