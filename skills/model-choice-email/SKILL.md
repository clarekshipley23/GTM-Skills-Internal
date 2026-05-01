# Model Choice Email

Generate personalized outreach emails for prospects evaluating language models for coding agents. This email promotes the OpenHands Index as a resource for comparing model cost and performance tradeoffs.

## Triggers

- `/model-choice` - Generate model evaluation outreach email
- `/model-email` - Alias for model choice email
- `/llm-choice` - When prospect is evaluating LLMs for coding

## When to Use

- Prospect is evaluating different LLMs for coding agents
- Company is building or scaling AI coding tools
- Engineering teams comparing model performance vs cost
- Anyone exploring agent benchmarks or model selection
- Signals of AI/ML infrastructure work or LLM integration

## Base Email Template

```
Hi [FIRST_NAME],

A lot of teams ask us how to choose the right language model for their coding agents. It's not always about the biggest model—it's about the right fit for your use case.

[CUSTOMIZATION — 1-2 sentences connecting to their specific context]

I'd love to invite you to explore the cost and performance tradeoffs of coding agents using the OpenHands Index, a comprehensive benchmark that evaluates real-world agent capabilities across issue resolution, greenfield app building, frontend development, testing, and information gathering. Learn more here: https://openhands-openhands-index.hf.space/home

If you're in the middle of evaluating models or tuning performance, I'd be happy to connect you with one of our engineers to compare notes.

Thanks,

Clarke
```

**Structure:**
1. Opening hook (model choice is hard)
2. Customization (connect to their context)
3. OpenHands Index offer (always included)
4. Soft CTA (engineer connection)

---

## Research Sources

### 1. HubSpot Contact & Company
```
Contact Properties:
- firstname, lastname, email, jobtitle
- company, hs_lead_status
- use_case (if available)

Company Properties:
- name, domain, industry
- AI/ML signals in description
```

### 2. GitHub Activity
```
Look for:
- Repos related to LLMs, agents, or AI coding
- Stars on model-related projects (ollama, vllm, llama.cpp)
- Contributions to AI/ML tooling
- OpenHands involvement
```

### 3. Web Research
```
Search for:
- "[Company] AI coding" or "[Company] LLM"
- Engineering blog posts on model evaluation
- Job postings mentioning LLMs or AI agents
- Conference talks or articles by the prospect
```

---

## Customization Angles

| Signal | Customization Angle |
|--------|---------------------|
| Building AI coding tools | "Given you're building coding agents at [Company]..." |
| Evaluating multiple models | "Since you're comparing models..." |
| Cost-conscious team | "If cost efficiency is a factor in your model selection..." |
| Performance-focused | "For teams prioritizing accuracy over latency..." |
| Enterprise scale | "At [Company]'s scale, model choice has real cost implications..." |
| Startup/early stage | "For early-stage teams, picking the right model early saves rework later..." |
| OSS involvement | "I noticed your work on [project]—the Index might help validate your model choices..." |

---

## Output Format

### Generated Email

**To:** [email]  
**Subject:** [Personalized subject line]

---

Hi [FIRST_NAME],

A lot of teams ask us how to choose the right language model for their coding agents. It's not always about the biggest model—it's about the right fit for your use case.

[CUSTOMIZATION — 1-2 sentences specific to their context]

I'd love to invite you to explore the cost and performance tradeoffs of coding agents using the OpenHands Index, a comprehensive benchmark that evaluates real-world agent capabilities across issue resolution, greenfield app building, frontend development, testing, and information gathering. Learn more here: https://openhands-openhands-index.hf.space/home

If you're in the middle of evaluating models or tuning performance, I'd be happy to connect you with one of our engineers to compare notes.

Thanks,

Clarke

---

### Research Summary

| Dimension | Finding |
|-----------|---------|
| Company | [name, size, industry] |
| Role | [title and responsibilities] |
| AI/ML Signal | [why model choice is relevant to them] |
| Customization Angle | [how we connected to their context] |

---

## Examples

### Example 1: AI Startup Founder

**Research found:** Founder of an AI coding assistant startup, previously worked on ML infrastructure at a large tech company.

**Subject line:** Model benchmarks for coding agents

**Full email:**
```
Hi Alex,

A lot of teams ask us how to choose the right language model for their coding agents. It's not always about the biggest model—it's about the right fit for your use case.

Building a coding assistant from scratch, you're probably already deep in model evaluation—balancing latency, accuracy, and cost across different use cases.

I'd love to invite you to explore the cost and performance tradeoffs of coding agents using the OpenHands Index, a comprehensive benchmark that evaluates real-world agent capabilities across issue resolution, greenfield app building, frontend development, testing, and information gathering. Learn more here: https://openhands-openhands-index.hf.space/home

If you're in the middle of evaluating models or tuning performance, I'd be happy to connect you with one of our engineers to compare notes.

Thanks,

Clarke
```

---

### Example 2: Platform Engineer at Enterprise

**Research found:** Senior engineer working on developer productivity tools at a Fortune 500, company recently announced AI initiatives.

**Subject line:** LLM selection for coding tools

**Full email:**
```
Hi Jordan,

A lot of teams ask us how to choose the right language model for their coding agents. It's not always about the biggest model—it's about the right fit for your use case.

At [Company]'s scale, model choice has real cost and compliance implications—especially if you're rolling out AI coding tools across engineering.

I'd love to invite you to explore the cost and performance tradeoffs of coding agents using the OpenHands Index, a comprehensive benchmark that evaluates real-world agent capabilities across issue resolution, greenfield app building, frontend development, testing, and information gathering. Learn more here: https://openhands-openhands-index.hf.space/home

If you're in the middle of evaluating models or tuning performance, I'd be happy to connect you with one of our engineers to compare notes.

Thanks,

Clarke
```

---

### Example 3: ML Engineer with OSS Involvement

**Research found:** ML engineer who starred OpenHands and several LLM inference projects (vLLM, ollama).

**Subject line:** Benchmarking coding agents

**Full email:**
```
Hi Sam,

A lot of teams ask us how to choose the right language model for their coding agents. It's not always about the biggest model—it's about the right fit for your use case.

I noticed you've been exploring LLM inference tooling—if you're evaluating models for coding tasks specifically, the Index might give you a useful baseline.

I'd love to invite you to explore the cost and performance tradeoffs of coding agents using the OpenHands Index, a comprehensive benchmark that evaluates real-world agent capabilities across issue resolution, greenfield app building, frontend development, testing, and information gathering. Learn more here: https://openhands-openhands-index.hf.space/home

If you're in the middle of evaluating models or tuning performance, I'd be happy to connect you with one of our engineers to compare notes.

Thanks,

Clarke
```

---

## Workflow Steps

1. **Get prospect info** - Name, email, title, company
2. **Research AI/ML context** - Are they building agents? Evaluating models? What signals?
3. **Find customization angle** - What makes model choice relevant to them specifically?
4. **Draft customization** - 1-2 sentences connecting their context to model evaluation
5. **Generate full email** - Insert customization into template
6. **Provide research summary** - Document findings for sender context

## Subject Line Guidelines

- Keep under 50 characters
- Reference model choice, benchmarks, or their specific context
- Examples:
  - "Model benchmarks for coding agents"
  - "LLM selection for [Company]"
  - "Coding agent performance tradeoffs"
  - "Quick resource on model choice"
  - "Benchmarking coding agents"

## Tips for Best Results

- **Keep customization brief** - Just 1-2 sentences to connect, the Index pitch is the main offer
- **Find the AI/ML signal** - Why is model choice relevant to them right now?
- **Don't oversell** - This is an invitation to explore a resource, not a hard pitch
- **Link always included** - The OpenHands Index link is the core value prop
- **Engineer connection** - The soft CTA offers real help, not just a demo

## Tone

This template is educational and helpful:
- We're offering a useful resource (the Index)
- We're acknowledging a real problem (model choice is hard)
- The CTA is soft (connect with an engineer to compare notes)
- Goal is to start a conversation around model evaluation
