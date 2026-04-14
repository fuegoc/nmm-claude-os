# Facilitator Agenda — Claude OS Training Session 1

**Duration:** 60 minutes live on Zoom
**Audience:** No More Mondays team — VAs and coaches together
**Goal:** everyone leaves with a live Claude OS: Role Project, 5 connectors, 6 skills, and a first Wins Log entry
**Recording:** yes, sharable with the handbook so attendees can rewatch

This is your script. Read it before the session. Do not read it verbatim during the session.

---

## Pre-flight checklist (10 minutes before the call)

- [ ] Confirm everyone completed pre-session homework. Anyone who didn't: send the homework link one more time and tell them to be 15 minutes early to catch up.
- [ ] Confirm the `claude-os` GitHub repo is pushed and the Notion page has working install links.
- [ ] Confirm you yourself have the onboarding skill installed and have done a full dry run (see `verification` in the plan file).
- [ ] Open in separate browser windows: the Notion page, the GitHub repo, your own Claude Desktop (ready to screen-share).
- [ ] Have the Airtable PAT template text ready to paste into Zoom chat at 0:34.
- [ ] Mute Slack and Discord desktop notifications.

---

## 0:00–0:05 — The mindset shift

**What to say (paraphrase, do not read):**

> Welcome. Before we touch anything, here is what we are doing today. You have all been using Claude like Google: ask a question, get an answer, forget about it. Today we are turning Claude into a teammate who remembers everything about your role, is connected to all your tools, and gets sharper every week. By the end of this hour your Claude Desktop will be connected to Gmail, Google Calendar, Notion, Slack, and Airtable, and it will have 6 skills installed — including a Morning Brief that scans your Slack and gives you your priorities every day, and a Student Reply skill trained on your voice that uses our FAQ. Live, in this session, not as homework.

**The hook demo.** Screen-share your Claude Desktop. Show two chats side by side:

- **Chat 1 (cold):** a fresh new chat, no project, no context. Type: *"Draft a reply to a student who says they're stuck on module 2 and don't understand what a pattern interrupt is."* Show the generic, no-voice, no-FAQ-reference response.
- **Chat 2 (in your Role Project with Notion connected):** same prompt, inside your own Claude Desktop Project, with the FAQ searchable. Show the tighter, voice-matched response that points to the actual module.

Let the difference speak. Say one line: *"That is the difference between how you have been using Claude and how you will be using Claude by the end of this hour."* Move on.

## 0:05–0:12 — The 3-shelf model

**What to say:**

> The whole system is three shelves. Remember three things, nothing else.
>
> **Shelf 1 is Knowledge.** That is your Role Project. What Claude knows about you.
>
> **Shelf 2 is Powers.** That is your Connectors and your Skills. What Claude can reach and what Claude can do.
>
> **Shelf 3 is Reflection.** That is your Wins Log. One line a day. That is how you get sharper.
>
> Two vocabulary words, and only two: a **Connector** is a live link to a tool like Gmail or Notion. A **Skill** is a reusable instruction recipe that teaches Claude to do a task consistently. You will hear the letters MCP floating around. That is the plumbing underneath Connectors. Ignore the acronym.
>
> By the end of this hour you will have all three shelves stocked.

Screen-share the Notion handbook page so they see it while you explain.

## 0:12–0:17 — Install your first skill: `nmm-os-setup`

**This is the pedagogically critical 5 minutes.** You are not teaching them the onboarding skill. You are teaching them *how to install a skill*, by having them install the skill that will install everything else.

**What to say:**

> We are about to install your first skill. Watch me once, then you do it. This is the exact same process you will use to install every skill ever, for the rest of your time on the team.

**Walk them through it on your screen:**

1. Open the Notion handbook page. Find the section "Onboarding skill." Click the Install link.
2. GitHub opens the file view. Click the **Download raw file** icon at the top right of the file toolbar (next to the "Raw" button). The `SKILL.md` downloads to your Downloads folder.
3. In Claude Desktop: *Customize → Skills → + → **Upload a skill** → drag the downloaded SKILL.md from Downloads into the upload area → Save.*

**Then say:**

> Your turn. You have 3 minutes. Go do it on your own screens. Unmute and tell me when you have saved it.

Wait until everyone confirms. If someone is stuck, walk them through it directly in chat or have them share their screen.

**Then say:**

> What you just installed is the most important skill in the universe of skills. It is going to teach Claude how to teach you everything else. Watch.

## 0:17–0:52 — Run the onboarding skill, together

**Your job here is to unblock, not to present.** The skill is the teacher. You are support.

**What to say:**

> Everyone, in Claude Desktop, start a new chat and type: `setup my claude os`. The skill will take over. It walks you through building your Role Project, installing the 5 connectors, installing the 6 starter skills, and running your first practice task. It paces you. Work through it on your own screens. I am here if you get stuck — just unmute and ask.

**During this block, your role is:**

- Monitor the Zoom chat and audio for "stuck" signals.
- When someone hits a failed OAuth flow, drop into a one-on-one screen share to diagnose.
- At 0:34, paste the Airtable PAT reference text into Zoom chat so everyone has the URL + scope list ready when the onboarding skill hits that phase.
- If someone's Role Project verification test (Phase 2 of the onboarding skill) fails because their template is thin, tell them to take 3 minutes to strengthen section 6 of their Role Project and then re-test.
- If the whole room is stuck on the same thing, pause the group, demo the fix on your screen, and unstick everyone at once.

**Things to keep in your head:**

- Airtable is the highest-risk connector. If someone's PAT is wrong, they create a new one in 2 minutes. If someone does not have a PAT at all (skipped homework), tell them to skip Airtable for now and return later.
- The onboarding skill has "skip for now" branches. Use them. Nobody leaves the session blocked on one thing.
- Target: everyone is at Phase 5 (practice task) by 0:47 at the latest. If a participant is still in Phase 3 at 0:47, they skip straight to Phase 5 and revisit connectors after the session.

## 0:52–0:57 — Wins Log + growth loop

**Pull everyone back to the main Zoom room.** Unshare your screen.

**What to say:**

> Everyone, take 30 seconds right now. Open a Notion page titled "My Wins Log" in your personal workspace. Write one line: `2026-04-14 — Set up my Claude OS. Installed 5 connectors and 6 skills. First Morning Brief was useful/off/mixed. Next I want to improve X.` Fill in the last part with something specific.
>
> Done? Good. Here is the rule: one line at the end of every workday. That is the whole ritual. For the first four weeks, share your daily line in the internal team Slack channel so we all see patterns. After that it can go personal.
>
> Every Friday afternoon, spend 10 minutes reading back your week. Three questions: what skill did I use most, what skill did I not use, and what did I wish Claude could do that it could not. The third question is the most important. Write a new skill for anything you wished Claude could do — run the Delegation-to-Skill skill on it, and it generates a SKILL.md for you.
>
> That is how your library grows. That is how the system gets sharper every week. Without this log, the whole thing plateaus.

## 0:57–1:00 — Homework and the next session

**What to say:**

> Your homework this week: use at least one skill per day on real work. Add at least one fact to your Role Project. Write one Wins Log line per day and share it in the team channel.
>
> Next session we are going to build your own skills from scratch with the skill-creator. You will be able to go from "I wish Claude could just do X" to "I have a working skill for X" in five minutes. Run with the Delegation-to-Skill move in the meantime and bring your candidate skills to the next session.
>
> If something breaks this week, post in the team channel with a screenshot. Do not suffer silently. The whole point of the first four weeks of public logging is that we fix things for everyone when one person hits a wall.
>
> That is it. Your Claude OS is live. Go use it.

End the session. Do not recap at length.

---

## Post-session (within 24 hours)

- [ ] Post the recording and a link to the Notion handbook in the internal team channel.
- [ ] Post a short message: "Three things for the week: one skill per day, one Role Project update, one Wins Log line per day. Share the log lines here."
- [ ] File a session summary to `daily/2026-04-14-session.md` in your life vault.
- [ ] File a decision file at `daily/decisions/2026-04-14-claude-os-framework.md` capturing what worked, what didn't, and what to change for the UGC accelerator version.
- [ ] Update the `CHANGELOG.md` in the repo if any skills were patched live during the session.

## Fallback plans

### If a connector fails for one person
Skip it. The onboarding skill allows skips. They revisit after the session with you one-on-one.

### If a connector fails for the whole group
This is an Anthropic-side issue. Tell everyone to skip that connector and move on. File a support ticket after the session.

### If the onboarding skill itself does not install for someone
Drop into a private Zoom breakout with them, walk them through the install live, rejoin main room when done. The rest of the group keeps moving.

### If Zoom or internet drops for you personally
The onboarding skill is self-paced. Tell attendees to keep running it and you'll rejoin. They will not be blocked by your absence for 5-10 minutes.

### If the whole session is running 15+ minutes behind at 0:45
Cut Phase 5 (practice task) and Phase 6 (wins log writing) from live execution. Push them to homework instead. Close with the 3-shelf model reminder and the homework. Session still worked; just trimmed.

## Zoom chat templates

Paste these into Zoom chat at the indicated times.

**At 0:12 (install your first skill):**
```
Install the onboarding skill:
1. Open Notion handbook: [your Notion page URL]
2. Find "Onboarding skill", click Install
3. On GitHub, click the "Download raw file" icon (top right of file toolbar)
4. Claude Desktop: Customize → Skills → + → Upload a skill → drag the SKILL.md in → Save
5. Start a new chat, type: setup my claude os
```

**At 0:34 (Airtable reference, when onboarding skill reaches Airtable phase):**
```
Airtable custom connector setup:
- URL: https://mcp.airtable.com/mcp
- Token: your Personal Access Token from homework
- Token scopes needed: data.records:read, data.records:write, schema.bases:read, schema.bases:write
- Path: Customize → Connectors → + → Add custom connector
- If you don't have a token yet: https://airtable.com/create/tokens
```

**At 0:52 (Wins Log):**
```
Your first Wins Log entry:
1. Create a Notion page in your personal workspace: "My Wins Log"
2. Write today's line:
   2026-04-14 — Set up Claude OS. Installed 5 connectors and 6 skills. First Morning Brief was [useful/off/mixed]. Next I want to improve [something specific].
3. Rule going forward: one line at the end of every workday. Share in team channel for the first 4 weeks.
```
