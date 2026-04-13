# Starter Skills Reference

Seven skills, paired to the connectors you just installed. Six are custom-built for No More Mondays and ship in the `claude-os` repo. The seventh (Skill Creator) is a free skill from Anthropic that you install from the built-in gallery. Together they cover your daily work and give you the tools to build new skills as you need them.

---

## 1. Morning Brief *(universal, daily)*

**Pairs with:** Slack + Notion (Gmail optional)
**Trigger:** `morning brief` or `what's on my plate today`
**What it does:** scans your priority Slack channels, flags unanswered threads and mentions, surfaces anything urgent, pulls today's Notion tasks, and returns a structured brief with four sections:
- **Top priorities** — what needs you first
- **Needs a reply** — threads waiting on your response
- **Waiting on others** — things you kicked over, watch for returns
- **Outstanding items** — anything from yesterday still open

**When to use:** once, at the start of every workday. Turns Slack from a reactive mess into a managed queue.

**Example:** run it with no arguments. Claude uses the priority channels listed in section 4 of your Role Project automatically.

---

## 2. Student Reply *(VAs, high-frequency)*

**Pairs with:** Notion (FAQ) + copy-paste from Discord
**Trigger:** paste a student question and say `student reply`
**What it does:** searches the FAQ in Notion, drafts a reply in your voice (calibrated against section 6 of your Role Project), points to the right course module, and matches your typical length.

**When to use:** every time a student asks a question in Discord that you need to answer.

**Do not:** post the draft blindly. Always read and lightly edit before sending. The skill is a speed multiplier, not a replacement.

---

## 3. Student Feedback *(coaches + VAs, on submissions)*

**Pairs with:** Drive + Notion (and requires the Corey Haynes marketing skills to also be installed)
**Trigger:** paste a student submission and say `feedback`
**What it does:** structured marketing feedback on hooks, CTAs, positioning, audience fit — delivered in your team's voice. Calls into the forked Corey Haynes skills under `skills/community/corey-haynes-marketing/` for the actual marketing patterns.

**When to use:** whenever you need to give a student structured feedback on written or recorded work.

**Dependency:** install the `feedback-patterns` skill and the Corey Haynes marketing skills before using this one. The onboarding skill handles this for you.

---

## 4. Database Builder *(backend ops)*

**Pairs with:** Notion
**Trigger:** `build a database` or `edit the [name] database`
**What it does:** creates a new Notion database from a plain-English description, or edits an existing one (add fields, rename options, change views). Pure conversational database management.

**Examples:**
- *"Build a database to track student progress by cohort with module completion dates and a status field."*
- *"Add a field called 'coach assigned' to the student tracker."*
- *"Change the status options on the onboarding tracker to include 'paused'."*

**When to use:** whenever you would otherwise spend 20 minutes clicking around Notion to set up or modify a tracker.

---

## 5. Airtable Query *(read-only)*

**Pairs with:** Airtable
**Trigger:** ask a natural-language question about an Airtable base
**What it does:** translates your question into an Airtable query and returns the matching records. Read-only by design — this skill does not create or edit anything in Airtable, only finds information that is already there.

**Examples:**
- *"Find all students in cohort 4 who haven't completed module 3."*
- *"Which students paid with Stripe and signed up in the last 30 days?"*
- *"Show me every student tagged 'at risk' with their last activity date."*

**When to use:** whenever you need to find something in Airtable and would otherwise open the base and filter by hand.

---

## 6. Skill Creator *(Anthropic gallery — installed via Browse)*

**Source:** Anthropic + partners (gallery skill, 16.5k installs at time of build)
**Install path:** *Customize → Skills → + → Browse skills → Skill Creator → Install*
**Trigger:** `create a skill` or invoke it from any chat
**What it does:** Anthropic's official skill for building new skills. Interviews you about a task, walks through structure, and produces a SKILL.md you can save to your library. Free, maintained by Anthropic, trusted.

**When to use:** when you want a generic, no-context skill built quickly — Claude's take on the task without NMM voice or Role Project calibration.

**How it differs from Delegation-to-Skill (skill #7):** Skill Creator is generic. Delegation-to-Skill uses your NMM house voice and references your Role Project so the generated skill feels like it belongs to the team. Use Skill Creator as a fast backup or when the task is generic and doesn't need team voice.

**Why it's in the starter kit:** it also teaches you the **Browse skills** install path, which is how you'll install any future Anthropic or partner skill without us. One install, two lessons learned.

---

## 7. Delegation-to-Skill *(the meta skill)*

**Pairs with:** Notion (optional, for saving generated skills)
**Trigger:** `delegate this` or `turn this into a skill`
**What it does:** interviews you about a task you do repeatedly — what triggers it, what inputs it needs, what outputs it should produce, what voice, what edge cases — then generates a new `SKILL.md` file tailored to that task. You review, save it to your library, and share the best ones back with Albert so they can be merged into the canonical repo for everyone.

**When to use:** the third or fourth time you catch yourself doing the same task manually. That is the signal.

**Why this skill matters most for the long run:** this is how your skill library grows from the frontline instead of plateauing. Every skill generated here is a permanent leverage gain.

---

## How to install each skill

See [connectors-checklist.md](./connectors-checklist.md) for the connector install pattern. For skills, two paths exist:

### Path A: Upload (for skills from the `claude-os` repo, items 1 through 5 and 7)

1. Open the Notion page ("No More Mondays Claude OS") and click the Install link for the skill.
2. GitHub opens the file view. Click the **Download raw file** icon in the file toolbar (top right of the file header). The file downloads to your Downloads folder. Single-file skills download as `SKILL.md`. Multi-file community skills (the Corey Haines marketing skills) download as a `.zip`.
3. In Claude Desktop: **Customize → Skills → + → Upload a skill**.
4. Drag the downloaded file or zip from Downloads into the upload area.
5. Save.
6. Test with the example prompt above.

### Path B: Browse gallery (for Skill Creator, item 6)

1. In Claude Desktop: **Customize → Skills → + → Browse skills**.
2. Find **Skill Creator** near the top of the directory (it has around 16k installs).
3. Click Install.
4. Done — no download, no drag-and-drop.

Same two patterns cover every skill you will ever install. Path A for anything from our repo or third-party zips. Path B for anything from the Anthropic gallery or directory.
