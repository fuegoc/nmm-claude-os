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

## 2026-04-14 (v1.5)

### Changed (repo sync with Notion handbook page)
- **`handbook/role-project-template.md` section 5** simplified to match the Notion handbook. Removed the "What is the accelerator" prompt, the modules note, and the FAQ bullet. Replaced with a pre-filled paragraph about the Inner Circle UGC Accelerator and one fill-in bullet for common student journeys. The full module list stays in `course-modules-nmm.md`.
- **`handbook/role-project-template.md` section 6** renamed from "Your voice (the structural rules)" to "Your voice rules". Removed the verbose preamble about team baseline vs. personal voice. Now reads just "Fill in the rules below." above the existing bullet list. Matches the Notion handbook.
- **`onboarding/nmm-os-setup/SKILL.md` Phase 2 step 2** removed the stale parenthetical "(skip section 9, that goes somewhere else)". Section 9 no longer exists in the template.
- **`onboarding/nmm-os-setup/SKILL.md` Phase 2 step 4** rewritten. Previously told users to download the two Knowledge files live during the session. Now tells users to drag the pre-downloaded files from their Claude OS folder into Project Knowledge. Aligns with the new Step 2 pre-work timing in the Notion handbook (files are downloaded as pre-work, dragged into the Project during live training).
- **`onboarding/nmm-os-setup/SKILL.md` Phase 2 failure branch** updated. Previously told users to "add 3 more voice examples" if the Role Project was thin. Voice examples are no longer in the Role Project template (they live in the `voice-samples-nmm-team.md` Knowledge file). Failure branch now points at section 6 voice rules and section 7 principles.
- **`onboarding/nmm-os-setup/SKILL.md` Phase 4 heading** updated from "Install the six starter skills" to "Install the seven starter skills plus Skill Creator". The actual count is 7 Upload skills + Skill Creator (Browse) = 8 total.
- **`onboarding/nmm-os-setup/SKILL.md` Phase 4 body** updated from "The first six follow the same Upload pattern. The seventh (Skill Creator)..." to "The first seven follow the same Upload pattern. The eighth (Skill Creator)..." to match the corrected count.

### Not changed (intentional)
- Em dashes in SKILL.md and handbook files are not cleaned up in this pass. They violate the house voice rule but are in model-facing instructions, not user-facing output. Planned for a dedicated follow-up pass.

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
