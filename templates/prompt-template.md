# Prompt Template

Copy this template for any new prompt. Fill in all XML blocks before testing.

---

```xml
<role>
You are [specific role with expertise level].
</role>

<context>
[Background the model needs. Include: who you are, what the business does, relevant constraints, target audience.]
</context>

<task>
[One clear, specific instruction. Avoid compound tasks. If multiple steps needed, use numbered list.]
</task>

<constraints>
- [Specific constraint 1 — measurable]
- [Specific constraint 2 — format]
- [Specific constraint 3 — tone/style]
- [Things to avoid]
</constraints>

<output_format>
[Exact structure you want: headers, sections, length, list vs prose, code blocks if needed.]
</output_format>
```

---

## Checklist Before Running

- [ ] Role is specific, not generic (not just "assistant")
- [ ] Context includes enough background to prevent hallucination
- [ ] Task is one instruction, not three bundled together
- [ ] At least 3 constraints defined
- [ ] Output format specifies length and structure
- [ ] Criteria for success defined before running

---

## After Running

- [ ] Document the output
- [ ] Score against criteria
- [ ] Identify the specific failure if output was suboptimal
- [ ] Change one variable and re-run
- [ ] Record in `/datasets/prompts-used.md`
