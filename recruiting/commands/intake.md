---
description: Run a structured intake for a new search — generates JD, sourcing strategy, and interview plan in one shot
argument-hint: "<role title or hiring manager brief>"
---

# Intake

Run a full structured intake for a new hiring search. Asks the right questions, then auto-generates three deliverables: a job description, a sourcing strategy with real candidates, and an interview plan — all from a single conversation.

## Input

The user provides one or more of:
- Role title and level
- Hiring manager name and team
- Brief description of what the role does
- Urgency and timeline
- Compensation range
- Location / remote policy
- Security clearance requirement (if applicable)
- Any existing JD to start from

If minimal input, ask: "What role are you opening? Give me the title and a sentence or two about what this person will do."

## Workflow

### Phase 1: Intake Questions (interactive)

Ask the user these questions in a structured, conversational flow. Group them to avoid overwhelming — 3-4 questions at a time. Skip any the user has already answered.

**Role definition:**
1. What's the role title and level? (e.g., Senior Software Engineer, L5)
2. What team is this on and who does it report to?
3. Is this a backfill or a new headcount? If backfill, what happened?
4. In one sentence, what will this person's biggest impact be in their first 6 months?

**Requirements:**
5. What are the 3-4 absolute must-haves? (skills, experience, credentials)
6. What are the nice-to-haves that would make someone a standout?
7. Any dealbreakers? (things that are an automatic no)
8. Is a security clearance required? If so, what level and type?

**Logistics:**
9. What's the compensation range? (base, bonus, equity)
10. Location — remote, hybrid, or on-site? Any location restrictions?
11. What's the urgency? When do you need this person to start?
12. Is this full-time permanent, contract, or temp?

**Interview and process:**
13. Who will be on the interview panel?
14. How many interview stages do you want?
15. Any specific competencies or traits that matter most to you?
16. What's the typical candidate experience you want to deliver?

**Sourcing direction:**
17. Where have you found great people for similar roles before?
18. Any target companies or competitors you'd want to pull from?
19. Any companies or sources to avoid?
20. Is there an internal candidate or referral already in play?

### Phase 2: Generate Deliverables

Once the intake is complete, generate all three deliverables automatically:

1. **Job description** — Using the intake answers, run the full `/claude-recruiting:write-jd` workflow to produce a polished, optimized JD
2. **Sourcing strategy + candidates** — Using the intake answers, run the full `/claude-recruiting:source` workflow including Phase 2 candidate finding to produce a strategy and 10-20 real candidate profiles
3. **Interview plan** — Using the intake answers, run the full `/claude-recruiting:interview-prep` workflow for a complete multi-stage interview loop with scorecards

Save all three as a combined document for the hiring manager.

## Output Structure

```
# Search Kickoff: [Role Title]
**Hiring Manager**: [Name] | **Team**: [Team] | **Target Start**: [Date]
**Status**: Intake complete — deliverables ready

---

## 1. Job Description
[Full JD output from write-jd workflow]

---

## 2. Sourcing Strategy & Candidates

### Strategy
[Full strategy output from source workflow — ideal profile, Boolean strings, target companies, channels, outreach angles]

### Sourced Candidates
[Full candidate list from source Phase 2 — tiered, with profiles and LinkedIn URLs]

---

## 3. Interview Plan
[Full interview loop from interview-prep workflow — stages, questions, scorecards, interviewer guidance]

---

## Next Steps
- [ ] Hiring manager reviews and approves JD
- [ ] Post JD to job boards and careers page
- [ ] Begin outreach to Tier A candidates
- [ ] Schedule calibration call with interview panel
- [ ] Set up weekly pipeline check-in cadence
```

## With Connectors

- **If ATS connected**: Create the job requisition, upload the JD, configure the interview plan, and submit for approval
- **If calendar connected**: Schedule the calibration call and first pipeline check-in
- **If email/chat connected**: Send the intake summary to the hiring manager for sign-off, notify the interview panel
- **If knowledge base connected**: Pull the team's hiring playbook, comp bands, and approved headcount

## Tips

- This command works best when you have 5-10 minutes to go through the intake questions — it's a conversation, not a form
- If the hiring manager is in a rush, provide minimal info (title + 1 sentence) and the plugin will make reasonable assumptions and flag them for review
- For cleared roles, mention the clearance level early so the sourcing strategy targets the right channels from the start
- After intake, use `/claude-recruiting:outreach` in batch mode to immediately generate personalized messages for the sourced candidates
