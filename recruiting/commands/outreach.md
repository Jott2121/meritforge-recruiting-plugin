---
description: Draft personalized candidate outreach messages — works standalone or directly from /source output
argument-hint: "<candidate info and role, or 'use sourced candidates'>"
---

# Draft Outreach

Craft personalized outreach messages that stand out in a candidate's inbox. Generates multi-touch sequences with tailored hooks based on the candidate's background and motivations. **Works in two modes: single-candidate deep personalization or batch outreach for an entire sourced candidate list.**

## Input

The user provides one or more of:
- Candidate name, current role, and company
- LinkedIn profile or resume
- Role being recruited for
- Why this candidate is a fit (specific reasons)
- Outreach channel (email, LinkedIn InMail, other)
- Any prior relationship or warm connection
- **A candidate list from `/claude-recruiting:source`** — if the user says "write outreach for the sourced candidates" or references candidates from a prior sourcing run, switch to **batch mode**

If minimal input, ask: "Who are you reaching out to and for what role? Share the candidate's background and the position — or if you've already sourced candidates, I can write outreach for the full list."

## Workflow

### Single Candidate Mode

1. **Research the candidate** — Parse provided info and use web search to understand their background, interests, recent activity, and likely motivations
2. **Identify hooks** — Find 2-3 personalized angles: recent project, company news, shared connection, career trajectory, technical interests
3. **Match to role** — Connect the candidate's likely motivations to what the role offers
4. **Draft the sequence** — Write a 3-touch outreach sequence (initial + 2 follow-ups) with different angles
5. **Optimize for channel** — Adjust length and tone for the outreach channel (LinkedIn InMail is shorter, email allows more detail)
6. **Add subject lines** — Write 2-3 subject line options for email outreach
7. **If data enrichment connected** — Pull verified contact info, mutual connections, and recent activity

### Batch Mode (from /source output)

When the user has a candidate list from `/claude-recruiting:source`:

1. **Identify the candidate list** — Pull the tiered candidate list from the current conversation or ask the user to paste it
2. **Group by outreach angle** — Cluster candidates by what's most likely to motivate them (career growth, mission alignment, comp/role upgrade, technical challenge, etc.)
3. **Generate per-candidate messages** — For each candidate in Tier A and Tier B, write a **ready-to-send initial outreach message** personalized with:
   - Their name and current title/company
   - A specific reason they were identified as a fit
   - The hook most likely to resonate based on their profile
   - A clear, low-friction call to action
4. **Produce a batch outreach table** — Organized for copy-paste-send efficiency
5. **Include follow-up templates** — 2 follow-up templates that can be lightly personalized per candidate
6. **For Tier C candidates** — Provide a single exploratory template that acknowledges the adjacent-profile angle

## Output Structure

```
## Outreach: [Candidate Name] → [Role Title]

### Candidate Research
- **Current**: [Role at Company]
- **Background**: [Key career highlights]
- **Likely motivations**: [What would make them move]
- **Personalization hooks**: [Specific details to reference]

### Message 1: Initial Outreach
**Channel**: [Email/LinkedIn] | **Tone**: [warm/direct/curious]
**Subject line options**:
1. [Option A]
2. [Option B]

---
[Message body — personalized, concise, specific about why them + why this role]
---

### Message 2: Follow-up (3-5 days later)
**Angle**: [Different hook than message 1]

---
[Follow-up message — adds new information, doesn't just "bump"]
---

### Message 3: Final Touch (5-7 days later)
**Angle**: [Lightest touch, easy call-to-action]

---
[Brief final message — respectful, offers a clear next step or graceful close]
---

### Outreach Tips
- **Best time to send**: [day/time recommendation]
- **If they respond positively**: [suggested next steps]
- **If no response after sequence**: [recommended waiting period and re-engagement strategy]
```

## With Connectors

- **If email connected**: Send the messages directly, schedule follow-ups
- **If data enrichment connected**: Pull verified email, phone, mutual connections, and recent social activity
- **If ATS connected**: Log the outreach, check for prior contact history, and avoid double-outreach
- **If chat connected**: Notify the hiring manager when a candidate responds

## Batch Output Structure

```
## Batch Outreach: [Role Title] — [X] Candidates

### Tier A Outreach

#### 1. [Candidate Name] — [Current Title] at [Company]
**Channel**: [Email/LinkedIn] | **Hook**: [What angle to use]
**Subject**: [Subject line]

---
[Ready-to-send message, fully personalized]
---

#### 2. [Candidate Name] — [Current Title] at [Company]
...

### Tier B Outreach

#### [X]. [Candidate Name] — [Current Title] at [Company]
...

### Tier C — Exploratory Template

---
[Single template with [CANDIDATE NAME], [COMPANY], and [SPECIFIC DETAIL] placeholders]
---

### Follow-up Templates

**Follow-up 1 (Day 4)**:
---
[Template with personalization placeholders]
---

**Follow-up 2 (Day 8)**:
---
[Template with personalization placeholders]
---

### Batch Summary
- Total messages drafted: [X]
- Tier A (fully personalized): [X]
- Tier B (personalized): [X]
- Tier C (template): [X]
- Estimated response rate: [X-Y%] based on personalization level
```

## Tips

- The more you know about the candidate, the better the personalization — LinkedIn profiles produce much better outreach than just a name
- Mention the specific reason you think they're a fit — generic "your background is impressive" messages get ignored
- For passive candidates, lead with what's in it for them, not what you need
- **Batch mode works best after `/claude-recruiting:source`** — the sourced candidate profiles give enough detail for meaningful personalization
- For cleared roles, mention the program's mission or impact rather than the clearance requirement — cleared candidates already know they're cleared
