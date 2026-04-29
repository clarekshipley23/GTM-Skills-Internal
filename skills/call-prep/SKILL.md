# AE → FDE / Exec Meeting Prep

Generate comprehensive pre-meeting intelligence briefs for executive re-introductions and strategic customer conversations by aggregating data from HubSpot (deals, companies, contacts, call transcripts), Slack discussions, and Notion documentation.

## When to Use

This skill should be invoked when:
- User asks to "prep for a call", "prepare for a meeting", "build a call brief"
- Preparing for an executive re-introduction or FDE support meeting
- Needing context on a deal's history before a strategic conversation
- Synthesizing information across multiple data sources for customer meetings

## Data Sources to Query

### 1. HubSpot Deal Record
Retrieve the deal record to get key commercial context:

```
Required Properties:
- dealname, amount, dealstage, pipeline, closedate
- hubspot_owner_id, assigned_technical_resource_fdese
- hs_manual_forecast_category, hs_priority
- use_case_description_for_openhands_deployment
- poc_use_case, fde_poc_notes, fde_poc_readiness
- hs_next_step, hs_is_stalled
- other_ai_coding_tools_in_use, ai_coding_tool_relativity
- deployment_type, first_oss_exposure, first_oss_use_notes, agent_maturity
- number_of_devs__users, notion_link
- mnda_signed, pocpilottrial_kickoff_date
```

### 2. HubSpot Company Record
Retrieve company details for organizational context:

```
Required Properties:
- name, domain, description, industry
- numberofemployees, hs_revenue_range, is_public
- country, city, state, address
- linkedin_company_page, website
- hs_num_decision_makers, hs_num_contacts_with_buying_roles
```

### 3. HubSpot Contacts
Retrieve all contacts associated with the company/deal:

```
Required Properties:
- firstname, lastname, email, jobtitle, phone, linkedin
- Identify roles: Economic Buyer, Technical Buyer, Champion, Blocker, Coach
```

### 4. HubSpot Call Transcripts
Retrieve all calls associated with the deal (sorted by date, newest first):

```
Required Properties:
- hs_call_title, hs_timestamp, hs_call_duration
- hs_call_summary (AI-generated summary)
- hs_call_has_transcript
```

### 5. Slack Discussions
Search Slack for relevant conversations:
- Search by company name and deal name
- Look in deal-specific channels if they exist
- Search for mentions of key contacts

### 6. Notion Documentation
If a `notion_link` exists in the deal record:
- Retrieve the linked page content
- Look for additional meeting prep notes or account documentation

---

## Output Format

**Choose format based on deal complexity:**
- **🟢 LIGHT VERSION** - SMB / Mid-Market deals, simpler stakeholder maps
- **🔵 HEAVY VERSION** - Enterprise / Complex deals, multiple stakeholders, political dynamics

---

# 🟢 LIGHT VERSION (SMB / Mid-Market)

## [COMPANY NAME] - AE/FDE Exec Meeting Prep

### 1️⃣ Deal Snapshot
| Field | Value |
|-------|-------|
| Stage | [dealstage] |
| Est. ACV | $[amount] |
| Target Close | [closedate] |
| Champion | [champion name & title] |

---

### 2️⃣ Why This Meeting Exists
- [ ] Use Case Validation
- [ ] Discovery  
- [ ] Move to Close

**Specific outcome required:**
> [What must happen for this meeting to be successful]

---

### 3️⃣ Biggest Blocker Right Now
> [The #1 thing preventing deal progress - from hs_next_step, fde_poc_notes, or call history]

---

### 4️⃣ Role of Exec / FDE
We need you to:
- **Reinforce:** [Key message to emphasize]
- **De-risk:** [Concern to address]
- **Apply Urgency Around:** [Time-sensitive element]

---

### 5️⃣ Likely Questions
1. [Anticipated question based on call history]
2. [Anticipated question based on competitive landscape]
3. [Anticipated question based on technical context]

---

### 6️⃣ Desired Next Step
- [Specific next action to secure in this meeting]

---

# 🔵 HEAVY VERSION (Enterprise / Complex)

## [COMPANY NAME] - AE/FDE Exec Meeting Prep

### 1️⃣ Deal Overview
| Field | Value |
|-------|-------|
| ACV / TCV | $[amount] |
| Stage | [dealstage] |
| Forecast Category | [hs_manual_forecast_category] |
| Close Plan | [timeline and key milestones] |
| Expansion Potential | [future growth opportunity] |
| Competitive Status | [who else is in the deal] |

---

### 2️⃣ Full Stakeholder Map

| Name | Title | Role | Power | Sentiment | LI Profile |
|------|-------|------|-------|-----------|------------|
| [name] | [title] | Champion | High/Med/Low | 👍/😐/👎 | [link] |
| [name] | [title] | Technical Buyer | High/Med/Low | 👍/😐/👎 | [link] |
| [name] | [title] | Economic Buyer | High/Med/Low | 👍/😐/👎 | [link] |

**Call out explicitly:**
- **Economic Buyer:** [name - the person who signs the check]
- **Technical Buyer:** [name - the person who validates technical fit]
- **Champion:** [name - internal advocate]
- **Blocker:** [name - if any, who is resistant]
- **Coach:** [name - if any, insider giving guidance]

---

### 3️⃣ Political Dynamics
> [Internal politics, org changes, competing priorities, or interpersonal dynamics affecting the deal]

---

### 4️⃣ Meeting Context
- **Context:** [Why is this meeting happening now? What triggered it?]
- **Background:** How has the OSS use gone for the team & why?
  > [first_oss_use_notes and relevant call history]

---

### 5️⃣ Strategic Narrative
> [The story we're telling - why OpenHands, why now, why this architecture]
> [Based on use_case_description and competitive positioning]

---

### 6️⃣ What We Need From FDE
- **Validate architecture for:** [specific technical concern]
- **Whiteboard integration path:** [system/workflow to diagram]
- **Identify technical landmines:** [risks to surface proactively]
- **Influence technical buyer:** [name and approach]

---

### 7️⃣ Competitive Strategy
- **Who we're up against:** [other_ai_coding_tools_in_use]
- **Our wedge:** [key differentiator for this account]
- **What must NOT happen in this meeting:** [worst-case scenario to avoid]

---

### 8️⃣ If This Meeting Goes Perfectly…
- **What changes in deal status?** [stage advancement, timeline acceleration]
- **What stakeholder unlocks?** [new access, champion empowerment, blocker neutralized]

---

### 🔗 Quick Links
- [HubSpot Deal Record](link)
- [HubSpot Company Record](link)
- [Notion Documentation](link if exists)
- [Recent Call Recordings](links)

---

## Workflow Steps

1. **Identify the target** - Get deal name or company name from user
2. **Query HubSpot** - Retrieve deal, company, contacts, and calls
3. **Assess complexity** - Determine LIGHT vs HEAVY format based on:
   - Deal size (>$50K typically HEAVY)
   - Number of stakeholders (>3 typically HEAVY)
   - Competitive presence
   - Political complexity
4. **Search Slack** - Find relevant discussions
5. **Check Notion** - If notion_link exists, retrieve page content
6. **Synthesize** - Generate the brief using appropriate template
7. **Identify the blocker** - Distill to the #1 issue
8. **Define FDE/Exec role** - Be specific about what support is needed

## Example Invocation

User: "Prep me for my call with Build One tomorrow"

Agent Response:
1. Search HubSpot for "Build One" deal
2. Assess: $38K deal, 3 stakeholders, competitive (Claude Code) → Use HEAVY format
3. Retrieve full deal record with all properties
4. Get associated company (Build.One)
5. Get all contacts and map roles
6. Retrieve all call transcripts (10 calls)
7. Search Slack for discussions
8. Generate HEAVY format brief with stakeholder map and competitive strategy

## Tips for Best Results

- **Focus on the blocker** - Every prep should crystallize the #1 obstacle
- **Be specific about FDE/Exec role** - Generic "support the deal" isn't helpful
- **Map stakeholder power accurately** - Who actually makes decisions?
- **Include competitive wedge** - What's our unfair advantage here?
- **Define success clearly** - What does "perfect meeting" look like?
- **Flag stalled deals** - hs_is_stalled = true needs urgent attention
- **Use call history for likely questions** - Past objections predict future ones
