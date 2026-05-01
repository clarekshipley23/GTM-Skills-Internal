# SDK Outreach Email Customization

Generate personalized SDK adoption outreach emails by researching the prospect's company, technical stack, and use cases, then customizing the offer section with relevant value propositions.

## Triggers

Invoke this skill with any of these slash commands:
- `/sdk-email`
- `/sdk-outreach`
- `/sdk-template`

**Usage:** `/sdk-email [name], [title] at [company]`

**Examples:**
```
/sdk-email Robert Kim, Founder & CEO at Laminar
/sdk-email Jane Smith, VP Engineering at Acme Corp
/sdk-outreach sreenivas vemulapalli, Chief Architect at Bridgenext
```

## When to Use

This skill should be invoked when:
- User asks to "write an SDK email", "customize SDK outreach", "personalize SDK template"
- Preparing cold or warm outreach for SDK/developer platform adoption
- Needing to tailor the offer section based on prospect research
- Sending follow-up emails about OpenHands SDK capabilities

## Base Email Template

```
[FIRST_NAME],

Companies publish SDKs to make their products easier to adopt, extend, and integrate—turning them into scalable platforms that developers and customers can build on.

At OpenHands, automating large refactors using parallel agents is one of the top use cases for our SDK—developers coordinate multiple agents working across different modules, tests, and pull requests at the same time.

[OFFER_SECTION]

Thanks,

[SENDER_NAME]
```

**Note:** The offer section should end with a single question or call-to-action (e.g., "Worth a quick look?"). Do NOT add a second closing question like "Would that be useful?" after the offer section.

---

## Research Sources

### 1. HubSpot Contact & Company
Retrieve prospect context:

```
Contact Properties:
- firstname, lastname, email, jobtitle
- linkedin (for role context)

Company Properties:
- name, domain, industry, description
- numberofemployees, hs_revenue_range
- website
```

### 2. Web Research (Tavily)
Search for technical context:
- Company engineering blog posts
- GitHub organization/repositories
- Tech stack mentions (job postings, articles)
- Recent developer tooling initiatives
- AI/automation adoption signals

### 3. LinkedIn Profile
If available, check:
- Current role and responsibilities
- Technical background
- Recent posts about development practices

---

## Offer Section Customization Framework

The `[OFFER_SECTION]` should be **2-3 sentences** that:
1. Reference something specific about their company/role
2. Connect to a relevant SDK capability
3. Propose a concrete next step

### SDK Capabilities to Match

| Prospect Signal | SDK Capability to Highlight |
|-----------------|----------------------------|
| Large monorepo / many services | Parallel agents across modules |
| Active refactoring initiatives | Coordinated codebase modernization |
| Multiple teams / distributed dev | Multi-agent orchestration |
| CI/CD heavy, automation focus | Agent-driven PR workflows |
| Technical debt discussions | Automated large-scale fixes |
| Hiring for platform/devtools | SDK for internal tooling |
| Using other AI coding tools | Migration path / superior coordination |

---

## Output Format

### Generated Email

**To:** [email]  
**Subject:** [Personalized subject line]

---

[FIRST_NAME],

Companies publish SDKs to make their products easier to adopt, extend, and integrate—turning them into scalable platforms that developers and customers can build on.

At OpenHands, automating large refactors using parallel agents is one of the top use cases for our SDK—developers coordinate multiple agents working across different modules, tests, and pull requests at the same time.

[CUSTOMIZED_OFFER_SECTION — end with a single question/CTA]

Thanks,

[SENDER_NAME]

---

### Research Summary (for reference)

| Dimension | Finding |
|-----------|---------|
| Company | [name, size, industry] |
| Role | [title and inferred responsibilities] |
| Tech Signal | [relevant technical context discovered] |
| SDK Angle | [why this capability matters to them] |

---

## Offer Section Examples

### Example 1: Platform Engineering Leader

**Research found:** VP Platform at fintech, 200+ engineers, mentions "developer productivity" in LinkedIn bio

**Offer section:**
> I saw [Company] is scaling its platform engineering practice. One thing we've seen work well for teams your size is using the SDK to let developers self-serve agent-powered refactors—like dependency upgrades or API migrations—without waiting on a central team. Happy to show you how one platform team set this up in under a week.

---

### Example 2: Engineering Manager at Growth Startup

**Research found:** Series B startup, active GitHub org with 15+ repos, recent blog post about migrating to TypeScript

**Offer section:**
> Noticed [Company]'s been working through a TypeScript migration—that's exactly the kind of thing the SDK handles well. Teams use it to spin up parallel agents that handle different modules simultaneously, with coordinated PRs that don't step on each other. If you're interested, I can share how another team automated 80% of their migration in a few days.

---

### Example 3: Director of Engineering at Enterprise

**Research found:** Enterprise SaaS, 1000+ employees, job postings mention "modernization" and "technical debt"

**Offer section:**
> Based on what I've seen about [Company]'s engineering priorities, it seems like codebase modernization is a focus. The SDK is particularly useful for coordinating agents across large, complex codebases—running parallel refactors with full context sharing so nothing breaks. Would it be helpful to walk through how this works on a real example?

---

### Example 4: Founder with Active OSS Involvement (Warm Lead)

**Research found:** Robert Kim, Founder & CEO of Laminar (lmnr.ai) - YC S24 company building open-source AI agent observability. Already partnered with OpenHands to power trace visualizations for the OpenHands Index benchmark. 2.8K GitHub stars.

**Subject line:** SDK tracing for Laminar users

**Full email:**
```
Robert,

Companies publish SDKs to make their products easier to adopt, extend, and integrate—turning them into scalable platforms that developers and customers can build on.

At OpenHands, automating large refactors using parallel agents is one of the top use cases for our SDK—developers coordinate multiple agents working across different modules, tests, and pull requests at the same time.

Given the OpenHands Index traces you're already powering with Laminar, there's a natural fit: developers using the SDK could get native observability into their parallel agent runs—seeing how coordinated agents behave across modules in real time. Worth a quick call to explore what a tighter integration could look like?

Thanks,

Clarke
```

**Research summary:**

| Dimension | Finding |
|-----------|---------|
| Company | Laminar (lmnr.ai) - YC S24, 2.8K GitHub stars, open-source AI agent observability |
| Role | Founder & CEO |
| OSS Involvement | **Active partnership** - Laminar powers OpenHands Index eval traces (announced Feb 2026) |
| SDK Angle | Native SDK tracing → Laminar observability for parallel agent orchestration |

**Why this works:**
- References the existing partnership (they're *already* working together on the Index)
- Speaks to his core product value prop (agent observability)
- Proposes a concrete extension (SDK → Laminar integration for parallel agents)
- Low-pressure ask ("curious if users have asked") rather than hard sell

---

### Example 5: Senior Engineer at Polyglot Tech Company

**Research found:** Denys Rudchenko, Senior Software Engineer at EGYM (fitness technology, 24,500+ clubs worldwide). EGYM maintains repos across TypeScript, Swift, Kotlin, Rust, Java, Go. They have a public Tech Radar for tooling decisions. Denys has Kubernetes/Terraform experience.

**Subject line:** SDK for EGYM's multi-language stack

**Full email:**
```
Denys,

Companies publish SDKs to make their products easier to adopt, extend, and integrate—turning them into scalable platforms that developers and customers can build on.

At OpenHands, automating large refactors using parallel agents is one of the top use cases for our SDK—developers coordinate multiple agents working across different modules, tests, and pull requests at the same time.

I noticed you've starred OpenHands—glad it's on your radar. Looking at EGYM's GitHub, you're working across TypeScript, Swift, Kotlin, Rust, and Java—that's a lot of surface area for any codebase-wide change. Teams use the SDK to run parallel agents across language boundaries, so a dependency upgrade or API migration gets applied consistently without manually coordinating across repos. Given EGYM's tech radar approach to managing your stack, this might fit how you're already thinking about tooling decisions. Worth a quick look?

Thanks,

Clarke
```

**Research summary:**

| Dimension | Finding |
|-----------|---------|
| Company | EGYM - Global fitness technology leader, 24,500+ clubs, Munich-based |
| Role | Senior Software Engineer |
| Tech Stack | TypeScript (10 repos), Swift (3), Rust (2), Java, Kotlin, Go - maintains public Tech Radar |
| OSS Involvement | **Starred OpenHands** + professional-programming, kubernetes-in-action |
| SDK Angle | Multi-language parallel agents for consistent changes across diverse tech stack |

**Why this works:**
- References his OpenHands star directly
- Acknowledges EGYM's polyglot reality (5+ languages across repos)
- Mentions their Tech Radar—shows research into how they evaluate tooling
- Speaks to senior engineer concerns (coordinating changes across repos/languages)
- Single closing question ("Worth a quick look?")

---

## Workflow Steps

1. **Get prospect info** - Name, email, company from user or HubSpot
2. **Research company** - Tavily search for tech context, engineering blog, GitHub
3. **Research individual** - LinkedIn profile, role, recent activity
4. **Identify SDK angle** - Match signals to capabilities table
5. **Draft offer section** - 2-3 sentences, specific + actionable
6. **Generate full email** - Insert into template with subject line
7. **Provide research summary** - Document findings for sender context

## Subject Line Guidelines

- Keep under 50 characters
- Reference something specific (not generic "AI" or "automation")
- Examples:
  - "SDK for [Company]'s refactor workflow"
  - "Parallel agents for [specific initiative]"
  - "Quick question about [Company]'s dev tooling"
  - "Saw your [blog post/repo]—quick thought"

## Tips for Best Results

- **Be specific** - Generic offers get ignored; reference their actual context
- **One capability** - Don't list everything; pick the most relevant angle
- **Concrete next step** - "Show you how..." beats "Let me know if interested"
- **Keep it short** - Offer section should be 2-3 sentences max
- **Match their language** - If they say "developer productivity," use that phrase
- **Avoid hype** - Technical buyers respond to specifics, not buzzwords
