# OSS Activity Outreach Email

Generate personalized outreach emails for prospects whose company has shown activity on the OpenHands repository. This is a warmer touch than cold SDK outreach—there's already usage signal.

## Triggers

- `/oss-activity` - Generate email based on company repo activity
- `/activity-email` - Alias for OSS activity outreach
- `/warm-outreach` - When there's existing engagement signal

## When to Use

- Company developers have starred, forked, or contributed to OpenHands
- Spike in activity from a company domain (commits, issues, PRs)
- Individual prospect has direct OSS involvement
- Following up on community engagement

## Base Email Template

```
[FIRST_NAME],

I'm Clarke from OpenHands—we recently noticed a spike in developer activity from [COMPANY] using OpenHands, so I figured I'd reach out.

[OFFER_SECTION]

Thanks for being part of the OH community, let me know if you need anything.

Thanks,

Clarke
```

**Note:** The offer section should be personalized based on:
1. What kind of activity was detected (stars, forks, contributions, usage patterns)
2. The prospect's role and likely use case
3. Any specific repos, issues, or features they've engaged with

---

## Research Sources

### 1. GitHub Activity Analysis
Check for company involvement:

```
Activity Signals:
- Stars from @company email domains
- Forks by employees
- Issues opened/commented
- PRs submitted
- Discussions participation

Search queries:
- "org:[company]" in OpenHands contributors
- Employee GitHub profiles → starred repos
- Company GitHub org → forks of OpenHands
```

### 2. HubSpot Contact & Company
```
Contact Properties:
- firstname, lastname, email, jobtitle
- company, hs_lead_status
- reo_contact_github (if available)

Company Properties:
- name, domain, industry, numberofemployees
```

### 3. Web Research
```
Search for:
- "[Company] OpenHands" or "[Company] AI coding"
- Company engineering blog
- Tech stack and dev tooling
- Recent initiatives (modernization, platform, AI adoption)
```

---

## Activity-Based Angle Selection

| Activity Signal | Offer Angle |
|-----------------|-------------|
| Multiple stars from company | "Looks like several folks on your team are exploring OpenHands..." |
| Fork of repo | "I noticed someone from [Company] forked the repo—if you're evaluating..." |
| Issue/PR submitted | "Saw the [issue/PR] from your team—happy to help with that use case..." |
| Spike in usage | "We've seen a spike in activity from [Company]—wanted to check in..." |
| Contributions | "Thanks for the contribution to [feature]—curious what you're building..." |

---

## Output Format

### Generated Email

**To:** [email]  
**Subject:** [Personalized subject line]

---

[FIRST_NAME],

I'm Clarke from OpenHands—we recently noticed a spike in developer activity from [COMPANY] using OpenHands, so I figured I'd reach out.

[CUSTOMIZED_OFFER_SECTION — reference specific activity + offer help]

Thanks for being part of the OH community, let me know if you need anything.

Thanks,

Clarke

---

### Research Summary

| Dimension | Finding |
|-----------|---------|
| Company | [name, size, industry] |
| Role | [title and responsibilities] |
| Activity Signal | [what triggered the outreach] |
| Offer Angle | [specific help or resource offered] |

---

## Offer Section Examples

### Example 1: Multiple Team Members Starring

**Activity found:** 5 developers from Acme Corp starred OpenHands in the past month

**Offer section:**
> Looks like several folks on your engineering team have been exploring OpenHands recently. If there's a specific use case you're evaluating—large refactors, test generation, codebase migrations—happy to do a quick walkthrough of how other teams are using it at scale. Or if you're already running experiments, I can connect you with our solutions team.

---

### Example 2: Fork Detected

**Activity found:** Engineering team forked the repo, likely evaluating for internal use

**Offer section:**
> I noticed someone from [Company] forked the repo recently—if you're evaluating OpenHands for internal workflows, I can share how similar teams have set up enterprise deployments, including self-hosted options and SSO integration. Happy to jump on a quick call if that'd be useful.

---

### Example 3: Issue or PR Submitted

**Activity found:** Developer opened an issue about parallel agent coordination

**Offer section:**
> Saw the issue your team opened about [specific topic]—that's actually a common pattern we see with teams running large-scale refactors. I can share some examples of how others have approached it, or connect you with someone on our team who works on that area directly.

---

### Example 4: General Usage Spike

**Activity found:** Increased API calls or cloud usage from company domain

**Offer section:**
> We've noticed increased activity from [Company] on OpenHands recently—looks like you're putting it to work. If you're scaling up usage or running into any friction, I'd be happy to help. We also have enterprise options if you're thinking about broader team rollout.

---

## Workflow Steps

1. **Identify activity signal** - What triggered this outreach? (stars, forks, issues, usage)
2. **Get prospect info** - Name, email, title, company from HubSpot or provided
3. **Research company** - Size, industry, tech stack, likely use cases
4. **Research individual** - Role, GitHub activity, relevant context
5. **Match activity to offer** - What specific help makes sense?
6. **Draft offer section** - Reference the activity + concrete offer
7. **Generate full email** - Insert into template with subject line
8. **Provide research summary** - Document findings for sender context

## Subject Line Guidelines

- Reference the activity or community connection
- Keep under 50 characters
- Examples:
  - "OpenHands at [Company]"
  - "Noticed your team on OpenHands"
  - "Following up from the OH community"
  - "Quick note from OpenHands"
  - "RE: [Company] + OpenHands"

## Tips for Best Results

- **Be specific about activity** - "5 of your engineers starred the repo" beats "noticed some activity"
- **Offer concrete help** - Walkthrough, connection, resources—not just "let me know"
- **Keep it brief** - This is a warm touch, not a sales pitch
- **Match their level** - IC gets technical offer, manager gets team-level offer
- **Don't overstate** - If it's just stars, don't imply they're power users
- **Genuine appreciation** - They're part of the community, acknowledge that

## Tone

This template is warmer and more casual than cold SDK outreach:
- We're thanking them for being part of the community
- We're offering help, not pitching
- The activity signal gives us a legitimate reason to reach out
- Goal is to start a conversation, not close a deal
