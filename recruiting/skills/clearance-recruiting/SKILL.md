---
name: clearance-recruiting
description: "Source and evaluate candidates by security clearance level for defense, intelligence, and government roles. Trigger with \"cleared candidates\", \"security clearance\", \"TS/SCI\", \"Secret clearance\", \"Top Secret\", \"cleared engineers\", \"defense hiring\", \"government contractor\", \"SCIF\", \"polygraph\", \"cleared talent\", or when the user discusses hiring for roles requiring security clearances."
---

# Clearance Recruiting

Specialized sourcing and evaluation framework for roles requiring US security clearances. Covers clearance levels, polygraph types, adjudication timelines, and cleared talent sourcing channels.

## How It Works

- **Standalone**: Specify the clearance level and role, and get a targeted sourcing strategy for cleared talent including specialized channels, Boolean strings, and pipeline expectations.
- **With connectors**: Search cleared candidate databases, check ATS for existing cleared candidates, and enrich profiles with clearance verification signals.

## Clearance Levels

### Standard Hierarchy

| Level | Abbreviation | Access | Typical Roles | Talent Pool Size |
|-------|-------------|--------|--------------|-----------------|
| **Confidential** | C | Lowest classified | Entry-level government, some contractors | Large — easiest to source |
| **Secret** | S | Moderate classified | Most defense contractor roles, IT, logistics | Large — but active clearances are smaller pool |
| **Top Secret** | TS | Highly classified | Engineers, analysts, program managers | Moderate — significantly constrained |
| **Top Secret/SCI** | TS/SCI | Compartmented intel | Intelligence, cyber, signals, space systems | Small — highly competitive |
| **TS/SCI with CI Poly** | TS/SCI + CI | Counter-intelligence polygraph | Intelligence community roles | Very small — premium talent |
| **TS/SCI with Full Scope Poly** | TS/SCI + FSP | Most rigorous | NSA, CIA, some NRO/NGA roles | Extremely small — highest demand |

### Key Clearance Facts for Recruiters

- **Clearances are government-owned, not employer-owned.** A clearance transfers with the person when they move between cleared facilities.
- **Active vs. current**: An "active" clearance is currently sponsored. A "current" clearance may be in an inactive/debriefed status but can be reactivated (typically within 24 months) without full reinvestigation.
- **Investigation timelines** (approximate):
  - Secret: 2-6 months
  - Top Secret: 6-12 months
  - TS/SCI + Poly: 12-18+ months
- **Clearance sponsorship**: Only a government agency or cleared contractor with a facility clearance (FCL) can sponsor a clearance. Companies cannot "buy" clearances.
- **Reciprocity**: DoD clearances transfer across DoD agencies. IC clearances may require additional adjudication.
- **Continuous evaluation (CE)**: Replaces periodic reinvestigation for many clearance holders. Monitors financial, criminal, and foreign travel records continuously.

## Sourcing Cleared Talent

### Clearance-Specific Sourcing Channels

| Channel | Best for | Notes |
|---------|----------|-------|
| **ClearedJobs.net** | All clearance levels | Largest cleared job board; also hosts cleared job fairs nationwide |
| **ClearanceJobs.com** | TS and above | Candidates self-verify clearance status; premium talent pool |
| **Intelligence Careers (ic.gov)** | IC roles | Official IC job board — source from applicant pool intel |
| **USAJOBS** | Government direct-hire | Federal candidates with existing clearances |
| **Military transition programs** (Hire Heroes, ACP, MSSA) | Secret and above | Transitioning service members often hold active clearances |
| **LinkedIn** (with clearance filters) | All levels | Use "security clearance" in keywords; Recruiter has clearance filter |
| **Defense industry job fairs** | All levels | AFCEA, NDIA, ClearedJobs fairs, military base career events |
| **Veteran hiring events** | Secret and above | TAP/TAPS events, Hiring Our Heroes, military.com events |
| **Employee referrals** | Highest yield for TS+ | Cleared professionals know other cleared professionals — this is your #1 channel |

### Boolean Strings for Cleared Talent

**LinkedIn — TS/SCI Engineers:**
```
("TS/SCI" OR "Top Secret/SCI" OR "Top Secret" OR "TS SCI") AND ("software engineer" OR "systems engineer" OR "cyber" OR "cloud engineer") AND ("active clearance" OR "current clearance" OR "cleared")
```

**Google X-ray — Cleared professionals:**
```
site:linkedin.com/in ("TS/SCI" OR "Top Secret" OR "Secret clearance") ("software" OR "engineer" OR "cyber" OR "analyst") -jobs -posts
```

**Google X-ray — Military transition:**
```
site:linkedin.com/in ("transitioning" OR "separating" OR "veteran") ("Secret" OR "Top Secret" OR "TS/SCI") ("engineer" OR "analyst" OR "program manager") -jobs
```

**ClearanceJobs search:**
```
Use the platform's built-in clearance level filter + role title + location. ClearanceJobs allows filtering by active vs. current status.
```

### Target Company Tiers (Defense / IC)

| Tier | Companies | Why |
|------|-----------|-----|
| **Tier 1 — Prime defense contractors** | Lockheed Martin, Raytheon (RTX), Northrop Grumman, General Dynamics, L3Harris, BAE Systems | Largest cleared workforces; recruiters know the space |
| **Tier 2 — Mid-tier defense / IT** | Booz Allen Hamilton, Leidos, SAIC, CACI, Peraton, ManTech | Large cleared talent pools, especially IT and cyber |
| **Tier 3 — Cleared tech companies** | Palantir, Anduril, Shield AI, SpaceX (cleared programs), Microsoft (Azure Gov), AWS (GovCloud), Google (Public Sector) | Tech talent with clearances — high demand, high comp |
| **Tier 4 — Small cleared contractors** | Dozens of small/mid cleared contractors in major defense hubs | Often have talent that wants to move to larger or more innovative programs |

### Defense Hub Locations

Source candidates from these metropolitan areas for the deepest cleared talent pools:

- **Washington DC / Northern Virginia / Maryland** (DC Metro) — largest concentration globally
- **Colorado Springs, CO** — Space Command, Schriever, Peterson
- **Huntsville, AL** — Redstone Arsenal, missile defense, space
- **San Diego, CA** — Navy, SPAWAR/NAVWAR, cyber
- **San Antonio, TX** — Air Force cyber, NSA Texas
- **Omaha, NE** — STRATCOM
- **Tampa, FL** — SOCOM, CENTCOM
- **Augusta, GA** — Army Cyber Command, Fort Eisenhower
- **Dayton, OH** — Wright-Patterson AFB, Air Force research
- **Los Angeles, CA** — Space Systems Command, aerospace

## Clearance Evaluation in Screening

When screening cleared candidates, add these dimensions to the standard evaluation:

| Dimension | What to assess | How to verify |
|-----------|---------------|---------------|
| **Clearance level** | Does the level match the requirement? | Ask directly — candidates know their level |
| **Clearance status** | Active, current (within 24 months), or expired? | Ask when last briefed/debriefed |
| **Polygraph** | CI, Full Scope, or none? | Ask directly — poly type matters |
| **Sponsoring agency** | DoD vs. IC? | Affects reciprocity and transfer timeline |
| **Investigation date** | When was their last investigation? | Determines if CE or periodic reinvestigation applies |
| **Willingness to relocate** | Many cleared roles are location-locked to SCIFs | Critical for TS/SCI roles |

### Important Legal Notes

- **You cannot ask about the content of a candidate's clearance** — only the level, status, and type of investigation.
- **Clearance status is not a protected class** — you can legally require and filter by clearance level.
- **ITAR/EAR restrictions**: Some roles require US Person status (US citizen or permanent resident). This is a legal requirement, not a preference — document it as such in the JD.
- **Do not conflate clearance with citizenship in sourcing**: Not all US citizens have clearances, and clearance eligibility depends on adjudicative factors, not demographics.

## Pipeline Expectations for Cleared Roles

Cleared talent pipelines behave differently than commercial pipelines:

| Metric | Commercial benchmark | Cleared benchmark | Why |
|--------|---------------------|------------------|-----|
| Time-to-fill | 30-45 days | 45-90+ days | Smaller talent pool, clearance transfer/upgrade timelines |
| Sourced response rate | 15-25% | 20-35% | Cleared candidates are used to being recruited; respond well to relevant outreach |
| Offer acceptance rate | 70-85% | 60-75% | Counter-offers are aggressive in defense; candidates often have multiple offers |
| Top-of-funnel needed (per hire) | 50-75 | 75-150+ (TS/SCI) | Constrained pool requires more volume |

## Connectors

| Connector | Enhancement |
|-----------|------------|
| ATS | Search for existing cleared candidates, filter by clearance level, track clearance transfer status |
| Data enrichment | Verify current employer (cleared facility indicator), pull defense industry signals |
| ClearanceJobs/ClearedJobs | Direct access to cleared candidate databases |
| LinkedIn | Use clearance-level filters in Recruiter, search defense industry groups |
