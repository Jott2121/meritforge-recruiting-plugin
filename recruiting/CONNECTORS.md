# Connectors

## How tool references work

Plugin files use `~~category` as a placeholder for whatever tool the user connects in that category. For example, `~~ats` might mean Greenhouse, Lever, Ashby, or any other applicant tracking system with an MCP server.

Plugins are **tool-agnostic** — they describe workflows in terms of categories (ATS, email, calendar, etc.) rather than specific products. The `.mcp.json` pre-configures specific MCP servers, but any MCP server in that category works.

Every command and skill works **fully standalone** with zero connectors using web search and user-provided context. Connectors supercharge the experience with live data and automation.

## Connectors for this plugin

| Category | Placeholder | Included servers | Other options |
|----------|-------------|-----------------|---------------|
| ATS | `~~ats` | Greenhouse, Lever | Ashby, Workday Recruiting, iCIMS, Jobvite, SmartRecruiters |
| Calendar | `~~calendar` | Google Calendar, Microsoft 365 | Calendly |
| Chat | `~~chat` | Slack | Microsoft Teams, Discord |
| Cloud storage | `~~cloud storage` | -- | Google Drive, Dropbox, SharePoint |
| CRM | `~~crm` | -- | HubSpot, Salesforce, Bullhorn |
| Data enrichment | `~~data enrichment` | Apollo, Clay, LinkedIn | Clearbit, ZoomInfo, Lusha, People Data Labs |
| Email | `~~email` | Gmail, Microsoft 365 | -- |
| HRIS | `~~hris` | -- | BambooHR, Workday, Rippling, Gusto |
| Knowledge base | `~~knowledge base` | Notion, Atlassian (Confluence) | Guru, Slite, Coda |
| Video conferencing | `~~video` | Zoom | Google Meet, Microsoft Teams |

## How connectors enhance workflows

### Without connectors (standalone mode)
- Paste or describe candidate information manually
- Copy in job descriptions and requirements
- Use web search for market research and company intel
- Get structured output you can paste into any system

### With connectors (supercharged mode)
- **~~ats**: Pull live candidate pipelines, update stages, add notes, check for duplicates
- **~~calendar**: Check interviewer availability, schedule loops, send invites
- **~~chat**: Post updates to hiring channels, notify hiring managers, share scorecards
- **~~data enrichment**: Enrich candidate profiles, find contact info, research companies
- **~~email**: Send personalized outreach, follow-ups, and offer letters
- **~~hris**: Check headcount approvals, verify compensation bands, pull org charts
- **~~knowledge base**: Access interview guides, rubrics, company values docs, and process wikis
- **~~video**: Schedule and configure interview rooms
