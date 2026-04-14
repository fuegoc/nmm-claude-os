# Changelog

All notable changes to the No More Mondays Claude OS skills and handbook. Dates in YYYY-MM-DD.

## 2026-04-14

### Added
- Initial scaffold of the `claude-os` repository.
- Onboarding skill: `nmm-os-setup` (originally named `claude-os-setup`, renamed in v1.3 due to Anthropic's reserved-word filter).
- Starter skills: `morning-brief`, `student-reply`, `student-feedback`, `feedback-patterns`, `database-builder`, `airtable-query`, `delegation-to-skill`.
- Handbook templates: `role-project-template.md`, `connectors-checklist.md`, `starter-skills-reference.md`, `wins-log-template.md`.
- Facilitator documents: `agenda.md`, `prework.md`, `hook-demo-script.md`.
- House voice reference: `house-voice-nmm.md` extracted from 10 real Albert-authored student messages, plus raw `voice-samples/albert-responses.md`.
- Student Reply and Student Feedback skills now fall back to the house voice when a user's Role Project section 6 is thin.
- Corey Haines marketing skills forked into `skills/community/marketing-skills/` (cold-email, copywriting, copy-editing, ad-creative, marketing-psychology, customer-research, product-marketing-context) with attribution in `ATTRIBUTION.md`.
- Student Feedback skill routes pitch submissions to Corey Haines `cold-email` as the primary feedback lens.
- Added Skill Creator (Anthropic gallery skill) as the 7th starter skill, installed via the Browse path to teach a second install pattern.

## 2026-04-14 (v1.3)

### Fixed
- **Renamed onboarding skill from `claude-os-setup` to `nmm-os-setup`.** Anthropic's Claude Desktop Upload a skill flow rejects any skill whose `name:` field contains the reserved word "claude". Discovered when Albert tried to install the onboarding skill during a dry-run and got the error "Skill name in SKILL.md cannot contain the reserved word 'claude'." The skill folder was renamed via `git mv` to preserve history. All references across README, CHANGELOG, facilitator agenda, and the Notion handbook install link were updated. The user-facing trigger phrase ("setup my claude os") is unchanged because trigger phrases live in the description, not the name field.

## 2026-04-14 (v1.2)

### Changed
- **Replaced Google Drive with Google Calendar** as connector #2. NMM workflow does not currently use Drive. Calendar is more useful for coaches and momentum coaches who run scheduled meetings throughout the day.
- Updated handbook, README, prework, agenda, role project template, and onboarding skill to reflect the swap. Connector count stays at 5.

### Expanded
- **Morning Brief skill** is now significantly more powerful. New sources: Google Calendar (today and next 24 hours of meetings) and Gmail (priority senders, starred items, threads where the user owes a reply). Output now includes a "Today's calendar" section at the top and an "Email needing reply" section. New edge case for meetings starting in the next 30 minutes (flagged at the top of the brief). Pairs with all 4 read-write connectors (Gmail, Calendar, Slack, Notion). It is now the single most-used skill in the kit and touches every connector.
- Student Feedback skill no longer pairs with Drive (Notion only).
