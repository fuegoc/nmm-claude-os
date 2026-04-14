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

## 2026-04-14 (v1.4)

### Added
- **`handbook/voice-samples-nmm-team.md`** — the team voice baseline. Coach Albert's 10 reference messages with a friendly header explaining when to use it and when to layer on personal voice. This is the file every team member uploads to Project Knowledge in week 1.
- **`handbook/voice-samples-template.md`** — the personal voice template. Empty slots for 10 messages plus a voice rules section. Team members fill this in (or duplicate the matching Notion sub-page) when they want their drafts to sound like them specifically instead of the team baseline. Recommended starting point for week 2 or later.
- **`handbook/course-modules-nmm.md`** — the Inner Circle UGC Accelerator module list (Month 1 through Month 3, 29 modules total) extracted into a standalone file. Lives in Project Knowledge so the Student Reply skill can search it via retrieval instead of bloating Project Instructions.

### Changed
- **Student Reply and Student Feedback skills** updated with a 4-tier voice fallback chain: personal voice file in Project Knowledge first, then team baseline file in Project Knowledge, then Role Project section 6, then the repo `house-voice-nmm.md` as last resort. When both personal and team files are present, the personal file is weighted at roughly 70% and the team file at roughly 30% (team file as safety net). Both skills also now look for `course-modules-nmm.md` in Project Knowledge.
- **Onboarding skill (`nmm-os-setup`) Phase 2** rewritten. New flow: paste sections 1-8 of Role Project into Project Instructions, then download `voice-samples-nmm-team.md` and `course-modules-nmm.md` from the handbook and drag both into Project Knowledge. Mentions the personal voice upgrade path for week 2 without making it a day-1 task.
- **`handbook/role-project-template.md`** sections 5 and 6 updated. Section 5 no longer asks users to inline the module list (it lives in `course-modules-nmm.md`). Section 6 is now structural rules only, not message samples (the samples live in `voice-samples-nmm-team.md` for week 1, and in `voice-samples-[name].md` for week 2+).

### Rationale
- Project Instructions has a character cap and gets loaded into every chat. Stuffing 10 voice samples plus the full course module list into Instructions hits the cap and bloats every chat with content that is only relevant to ~30% of skill invocations. Project Knowledge is the right home for reference content because Claude retrieves it when relevant instead of loading it on every turn.
- Phased rollout: week 1 every team member uses the team voice baseline file (zero friction setup, drafts in Albert voice). Week 2+ team members can add their personal voice file using the template, and the skill fallback chain automatically prefers the personal file when present. This avoids asking VAs to gather 5-10 of their own messages on day 1 (too much homework) while keeping all the plumbing ready for the day they want to upgrade.

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
