# No More Mondays Claude OS

A curated Claude Desktop skill library for the No More Mondays team. Built to turn casual Claude users into confident operators in one hour, with a personal knowledge base that grows, a skill library that compounds, and connections to the tools we actually use (Gmail, Google Calendar, Notion, Slack, Airtable).

## The model

Three shelves:

1. **Knowledge** — your Role Project in Claude Desktop. What Claude knows about you.
2. **Powers** — Connectors (live links to Gmail, Google Calendar, Notion, Slack, Airtable) + Skills (reusable recipes).
3. **Reflection** — the Wins Log. One line at end of day. How you get sharper every week.

Two vocabulary words: **Connector** and **Skill**. That is all you need.

## How to install a skill

Every skill in this repo is installed the same way. Learn this once, it works for everything.

1. Open the Notion page "No More Mondays Claude OS" and click the Install link for the skill you want.
2. GitHub opens the file view. Click the **Download raw file** icon at the top right of the file toolbar. The `SKILL.md` (or `.zip` for multi-file community skills) downloads to your Downloads folder.
3. In Claude Desktop: **Customize → Skills → + → Upload a skill**.
4. Drag the downloaded file from Downloads into the upload area.
5. Save. Done.

For the 7th starter skill (Skill Creator from Anthropic), the path is different: **Customize → Skills → + → Browse skills → Skill Creator → Install**. You learn this second install path during the training.

## Contents

```
claude-os/
├── onboarding/
│   └── nmm-os-setup/             start here: the guided setup coach
├── skills/
│   ├── morning-brief/            daily priorities from Slack + Notion
│   ├── student-reply/            FAQ-powered replies in your voice
│   ├── student-feedback/         marketing feedback via Corey Haynes patterns
│   ├── feedback-patterns/        bundled library used by student-feedback
│   ├── database-builder/         conversational Notion database create + edit
│   ├── airtable-query/           read-only Airtable search
│   ├── delegation-to-skill/      meta-skill that generates new skills from tasks
│   └── community/                forked open-source skills (Corey Haynes, etc.)
├── handbook/                     templates and checklists (mirrored to Notion)
│   ├── role-project-template.md  the 8-section questionnaire
│   ├── connectors-checklist.md   install path for all 5 connectors
│   ├── starter-skills-reference.md  one-pager on each of the 6 skills
│   ├── wins-log-template.md      the daily 1-line ritual
│   ├── house-voice-nmm.md        No More Mondays baseline voice profile
│   └── voice-samples/            raw reference messages (Albert's 10 samples)
├── facilitator/                  training session scripts
├── README.md                     this file
└── CHANGELOG.md                  every skill update, dated
```

## Who this is for

Built for the No More Mondays team first (VAs, coaches, Albert). Same framework will later power a training module for the UGC accelerator students. Same repo, different starter skills at that point.

## Updates

When a skill is updated, the `CHANGELOG.md` and the Notion page both reflect it. To pull an update, re-install the skill (steps above) overwriting your existing copy. Claude Desktop does not auto-sync skills.
