---
description: Build a targeted sourcing strategy for a role and find real candidates
argument-hint: "<job title, team, or requirements>"
---

# Source Candidates

Build a comprehensive sourcing strategy for a specific role, then **execute the search to find real candidate profiles**. Produces a prioritized channel plan, Boolean search strings, target company lists, outreach angles, and a curated list of actual candidates sourced via web research.

## Input

The user provides one or more of:
- Job title or role description
- Team and hiring manager context
- Must-have and nice-to-have requirements
- Pasted job description
- Target seniority level or years of experience

If no input is provided, ask: "What role are you sourcing for? Share the title, key requirements, or paste the full JD."

## Workflow

### Phase 1: Strategy (steps 1-7)

1. **Parse the role** — Extract title, level, core skills, domain, and team context from `$ARGUMENTS`
2. **Define the ideal candidate profile** — Map must-haves vs. nice-to-haves, identify adjacent backgrounds that could transfer
3. **Build Boolean search strings** — Generate 3-5 search strings for LinkedIn, GitHub, Google X-ray, and niche platforms
4. **Identify target companies** — List 10-15 companies likely to employ this talent (competitors, adjacent industries, known talent hubs)
5. **Recommend sourcing channels** — Prioritize channels by expected yield: referrals, LinkedIn, communities, job boards, events, agencies
6. **Draft outreach angles** — Write 2-3 compelling hooks tailored to what would motivate this persona to explore
7. **If ATS connected** — Check for existing candidates in pipeline, silver medalists from past roles, and internal mobility candidates

### Phase 2: Candidate Finding (steps 8-11)

8. **Execute web searches** — Using the Boolean strings and target company list from Phase 1, run multiple web searches to find real candidate profiles. Search strategies include:
   - Google X-ray searches of LinkedIn (e.g., `site:linkedin.com/in "[title]" "[company]"`)
   - Searches combining target company names + role titles + relevant skills
   - Searches for professionals in relevant communities, conferences, or publications
   - Searches for people who have written or spoken about relevant topics
   - Run **at least 5-8 separate web searches** with varied queries to maximize coverage

9. **Compile candidate list** — For each candidate found, extract:
   - Full name
   - Current title and company
   - LinkedIn profile URL (if available)
   - Key qualifications that match the role (brief)
   - Fit assessment: Strong / Good / Exploratory
   - Any notable signals (open to work, recent career change, relevant content published, etc.)

10. **Deduplicate and rank** — Remove duplicates, rank candidates by apparent fit, and organize into tiers:
    - **Tier A**: Strong apparent match on must-have requirements
    - **Tier B**: Good match with some gaps or unknowns
    - **Tier C**: Exploratory — adjacent profile worth a conversation

11. **Produce the candidate list** — Target **10-20 real candidates** with enough detail to begin outreach. If fewer than 10 are found, note which searches yielded thin results and suggest additional angles to try.

## Output Structure

```
## Sourcing Strategy: [Role Title]

### Ideal Candidate Profile
- **Must-haves**: [skills, experience]
- **Nice-to-haves**: [bonus qualifications]
- **Adjacent backgrounds**: [transferable profiles]

### Boolean Search Strings
1. **LinkedIn**: `[string]`
2. **GitHub/Stack Overflow**: `[string]`
3. **Google X-ray**: `[string]`

### Target Companies (by tier)
| Tier | Companies | Why |
|------|-----------|-----|
| 1 - Direct competitors | ... | Same domain, likely skills match |
| 2 - Adjacent industry | ... | Transferable skills, different context |
| 3 - Talent hubs | ... | Known for developing this talent |

### Channel Priority
| Channel | Expected yield | Effort | Recommended actions |
|---------|---------------|--------|-------------------|
| Employee referrals | High | Low | [specific steps] |
| LinkedIn outreach | Medium | Medium | [specific steps] |
| ... | ... | ... | ... |

### Outreach Angles
**Angle 1**: [hook based on career growth]
**Angle 2**: [hook based on mission/impact]
**Angle 3**: [hook based on technical challenge]

### Pipeline Check
[If ATS connected: existing candidates, silver medalists, internal mobility]
[If standalone: "Connect your ATS to check for existing candidates"]

---

### Sourced Candidates

#### Tier A — Strong Matches
| # | Name | Current Title | Company | LinkedIn | Key Qualifications | Signals |
|---|------|--------------|---------|----------|-------------------|---------|
| 1 | [Name] | [Title] | [Co] | [URL] | [Why they match] | [Open to work, etc.] |
| ... | ... | ... | ... | ... | ... | ... |

#### Tier B — Good Matches
| # | Name | Current Title | Company | LinkedIn | Key Qualifications | Signals |
|---|------|--------------|---------|----------|-------------------|---------|
| ... | ... | ... | ... | ... | ... | ... |

#### Tier C — Exploratory
| # | Name | Current Title | Company | LinkedIn | Key Qualifications | Signals |
|---|------|--------------|---------|----------|-------------------|---------|
| ... | ... | ... | ... | ... | ... | ... |

### Search Coverage Summary
- Searches executed: [list of queries run]
- Total profiles reviewed: [number]
- Candidates surfaced: [number]
- Gaps: [areas where searches yielded thin results]
- Suggested next steps: [additional searches or channels to try]
```

## With Connectors

- **If ATS connected**: Search for past applicants, silver medalists, and internal candidates before external sourcing
- **If data enrichment connected**: Enrich target company lists with employee counts, growth signals, and funding data. Enrich found candidates with verified email addresses, phone numbers, and additional profile details.
- **If LinkedIn connected**: Search LinkedIn directly for candidate profiles matching the criteria, view full profiles, and check connection paths
- **If Apollo/Clay connected**: Use contact databases to find and enrich candidate profiles with verified contact information
- **If knowledge base connected**: Pull the team's sourcing playbooks, past strategies that worked, and hiring manager preferences

## Tips

- Include the hiring manager's LinkedIn profile or team page for better target company identification
- Mention any compensation constraints upfront so channel recommendations account for budget
- For niche roles, specify the exact technical stack or domain expertise needed
- The candidate finding step works best when the role is well-defined — provide a full JD for the best results
- Candidates found via web search represent publicly available information only; always verify details before outreach
- For deeper candidate finding with verified contact info, connect Apollo, Clay, or LinkedIn connectors
