# Prompts Used — Master Collection

**Diego Duarte — AI Research Lab**
*Dataset Version: 1.0 | Last Updated: June 2025*

---

## Overview

This file catalogs every prompt used across benchmarks, case studies, and evaluations in this research lab. Each prompt is documented with its task category, models tested, version number, and notes on effectiveness.

This collection serves two purposes:
1. Reproducibility — anyone can run the same prompts on any model
2. Pattern analysis — tracking which prompt structures produce consistent results

---

## Prompt Catalog

### Category: Sales & Outreach

---

**PROMPT-001**
- **Task:** Write a 3-email cold outreach sequence for a mobile detailing business
- **Category:** Sales copywriting
- **Models Tested:** Claude 3.5 Sonnet, GPT-4o, DeepSeek V3
- **Benchmark:** llm-evaluations/claude-vs-chatgpt.md
- **Version:** v1.0
- **Notes:** Best performer for tone: Claude. Best performer for structure: GPT-4o.

```xml
<task>
  Write a 3-email cold outreach sequence for a mobile auto detailing business.
  </task>
  <context>
    Business name: DB Home Services. Target customer: residential homeowners in Austin, TX with 2+ vehicles. Service: premium mobile detailing, we come to you.
    </context>
    <constraints>
      - Email 1: Introduction and value prop (max 150 words)
        - Email 2: Social proof / follow-up (max 120 words)
          - Email 3: Final follow-up with offer (max 100 words)
            - Tone: Professional but conversational
              - No aggressive sales language
              </constraints>
              <output_format>
                Three separate emails with Subject line and Body for each.
                </output_format>
                ```

                ---

                **PROMPT-002**
                - **Task:** Generate 10 subject lines for a re-engagement email campaign
                - **Category:** Email marketing
                - **Models Tested:** Claude 3.5 Sonnet, GPT-4o
                - **Benchmark:** ai-case-studies/sales-outreach-benchmark.md
                - **Version:** v1.0
                - **Notes:** Claude produced more varied options; GPT-4o was more formulaic but used stronger action verbs.

                ```xml
                <task>
                  Generate 10 email subject lines for a re-engagement campaign targeting customers who haven't booked in 60+ days.
                  </task>
                  <context>
                    Business: mobile auto detailing. Customer last booked: 60-90 days ago. Goal: get them to rebook.
                    </context>
                    <constraints>
                      - Mix of curiosity, urgency, and value-based subject lines
                        - Max 50 characters each
                          - No spam trigger words (FREE, URGENT, ACT NOW)
                            - A/B testable pairs preferred
                            </constraints>
                            <output_format>
                              Numbered list of 10 subject lines, grouped by type (curiosity / urgency / value).
                              </output_format>
                              ```

                              ---

                              ### Category: Business Analysis & Research

                              ---

                              **PROMPT-003**
                              - **Task:** Analyze competitive landscape for mobile detailing in Austin, TX
                              - **Category:** Market research
                              - **Models Tested:** Claude 3.5 Sonnet, Gemini 1.5 Pro
                              - **Benchmark:** ai-case-studies/market-research-benchmark.md
                              - **Version:** v1.0
                              - **Notes:** Gemini cited specific local competitors; Claude produced more structured analysis framework.

                              ```xml
                              <task>
                                Analyze the competitive landscape for mobile auto detailing services in Austin, Texas.
                                </task>
                                <context>
                                  I am launching/growing a mobile detailing business called DB Home Services. Target market: residential customers in Austin suburbs (Cedar Park, Round Rock, Pflugerville).
                                  </context>
                                  <constraints>
                                    - Identify 3 competitive tiers (budget, mid-range, premium)
                                      - Note pricing patterns if available
                                        - Identify market gaps or underserved segments
                                          - Keep analysis grounded in verifiable information
                                          </constraints>
                                          <output_format>
                                            Structured report with: Overview, Competitive Tiers table, Market Gaps section, Recommendations.
                                            </output_format>
                                            ```

                                            ---

                                            ### Category: Workflow & Operations

                                            ---

                                            **PROMPT-004**
                                            - **Task:** Build a customer follow-up SOP for a service business
                                            - **Category:** Business automation
                                            - **Models Tested:** Claude 3.5 Sonnet, GPT-4o
                                            - **Benchmark:** business-automation/db-home-services.md
                                            - **Version:** v1.1
                                            - **Notes:** v1.0 produced generic output; v1.1 added GoHighLevel CRM context and got significantly more specific results.

                                            ```xml
                                            <task>
                                              Create a standard operating procedure (SOP) for following up with customers after a service appointment.
                                              </task>
                                              <context>
                                                Business: mobile auto detailing. CRM: GoHighLevel. Customer completes appointment, pays on-site. Goal: get review + rebook.
                                                </context>
                                                <constraints>
                                                  - Must work within GoHighLevel automation capabilities
                                                    - Timeline: Day 0 (day of service), Day 1, Day 3, Day 7
                                                      - Include SMS and email touchpoints
                                                        - Review request must comply with Google's terms (no incentivized reviews)
                                                        </constraints>
                                                        <output_format>
                                                          Timeline table with: Day, Channel (SMS/Email), Message goal, Template message.
                                                          </output_format>
                                                          ```

                                                          ---

                                                          **PROMPT-005**
                                                          - **Task:** Write a job application cover letter optimized for AI trainer roles
                                                          - **Category:** Professional writing
                                                          - **Models Tested:** Claude 3.5 Sonnet, GPT-4o, DeepSeek V3
                                                          - **Benchmark:** ai-case-studies/resume-optimization.md
                                                          - **Version:** v1.0
                                                          - **Notes:** All three models produced usable output. Claude's was the most authentic-sounding; GPT-4o's was the most structured.

                                                          ```xml
                                                          <task>
                                                            Write a cover letter for an AI trainer / data annotation specialist role at a remote AI company.
                                                            </task>
                                                            <context>
                                                              Applicant: Diego Duarte, 17 (turning 18 July 2025), Austin TX. Background: mobile business owner, sales, CRM, AI tools user. No college degree. Fluent English and Spanish.
                                                              </context>
                                                              <constraints>
                                                                - Max 250 words
                                                                  - No fabricated experience
                                                                    - Emphasize practical AI usage, bilingual capability, self-direction
                                                                      - Tone: confident, direct, not desperate
                                                                      </constraints>
                                                                      <output_format>
                                                                        Single cover letter with opening hook, 2 body paragraphs, closing CTA.
                                                                        </output_format>
                                                                        ```

                                                                        ---

                                                                        ## Prompt Effectiveness Patterns

                                                                        Based on testing PROMPT-001 through PROMPT-005, these structural choices consistently improve output quality:

                                                                        | Pattern | Effect | Confidence |
                                                                        |---------|--------|------------|
                                                                        | Specifying word/character limits in constraints | Reduces verbosity | High |
                                                                        | Naming the CRM or tool in context | Gets tool-specific output | High |
                                                                        | Requesting grouped output (e.g., "by type") | Improves organization | Medium |
                                                                        | Adding tone descriptors | Reduces generic language | Medium |
                                                                        | Specifying what NOT to do | Reduces common failure modes | High |

                                                                        ---

                                                                        ## Prompts in Development

                                                                        | ID | Task | Status |
                                                                        |----|------|--------|
                                                                        | PROMPT-006 | Spanish-language outreach sequence | Planned |
                                                                        | PROMPT-007 | LLM hallucination stress-test battery | In progress |
                                                                        | PROMPT-008 | GoHighLevel automation workflow design | Planned |
                                                                        | PROMPT-009 | Resume bullet point optimization across models | Planned |
                                                                        | PROMPT-010 | Bilingual customer service response templates | Planned |

                                                                        ---

                                                                        *Diego Duarte | AI Research Lab | Austin, Texas*
