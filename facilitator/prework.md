# Pre-Session Homework

**Send to all attendees 48 hours before the live session.** Subject line: "Before our Claude training — 30 minutes of prep"

---

Hey [name],

Before our Claude training session on [date] at [time], you need to do about 30 minutes of prep. This is not optional. The session is tight and we cannot use our live time on account setup. If you skip the prep, you will fall behind in the first 10 minutes and you will not leave with a working Claude OS.

Here is the full checklist. Do it in order.

## 1. Download Claude Desktop and sign in (5 minutes)

- Download Claude Desktop: https://claude.ai/download
- Install and sign in with your personal Claude.ai account (not an API key — if you have a Pro or Max subscription, use that account).
- Open the app and make sure you can start a new chat. That's it for this step.

## 2. Confirm you can log in to all 5 tools in your browser (5 minutes)

Open one browser tab for each of these and make sure you are signed in:

- [ ] Gmail
- [ ] Google Drive
- [ ] Notion (the No More Mondays workspace)
- [ ] Slack (the No More Mondays internal workspace)
- [ ] Airtable (with access to the bases you use for work)

If you cannot log in to any of these, tell me now — before the session, not during it.

## 3. Create an Airtable Personal Access Token (10 minutes — the longest step)

This is the trickiest part of the whole setup. Do it now so we do not have to do it live.

1. Go to https://airtable.com/create/tokens
2. Click **Create new token**.
3. Name it: `Claude Desktop`
4. Under **Scopes**, add these four, exactly:
   - `data.records:read`
   - `data.records:write`
   - `schema.bases:read`
   - `schema.bases:write`
5. Under **Access**, choose "All current and future bases" (or pick specific bases if your IT rules require it).
6. Click **Create token**.
7. **Copy the token immediately and save it in your password manager.** You will not be able to see it again after you leave the page. If you lose it, you will have to generate a new one.
8. Keep the token accessible during the live session — you will paste it in around 35 minutes into the call.

## 4. Fill in your Role Project template (15-20 minutes — the most important step)

This is the single most valuable thing you will do this week. The Role Project is what makes Claude actually know *you*. Every skill you run during and after the training uses this as context. If you skip it or half-ass it, every skill you install will be weaker.

1. Open the Role Project template: [link to handbook/role-project-template.md on GitHub, or the Notion page version]
2. Duplicate it to a new Notion page titled "My Role Project — [Your Name]."
3. Fill in every section. Do not skip any.

**Sections that usually take the longest:**

- **Section 4 (Systems):** paste real links. We need the FAQ URL, your main Airtable base, your 3-6 priority Slack channels, your Discord channels, and your main Notion pages. Links, not descriptions.

- **Section 5 (Course):** list every module with a one-line description. This is what Student Reply uses to point students at the right module.

- **Section 6 (Voice):** this is the most important section. Paste **5 to 10 real messages you have written** — actual student replies, actual Slack messages, actual feedback notes. Mix of contexts. Also tell Claude which words you never use, your formality level, and how you usually open and close. Without this, Student Reply sounds like generic AI.

**Tip:** when pasting voice examples, do not curate. Use real, slightly messy examples. That is what your actual voice sounds like and that is what Claude needs to match.

## 5. Open the Notion handbook page in a browser tab and keep it open (1 minute)

Link: [Notion handbook URL]

This is your reference during the session. It has install buttons for every skill and every connector.

---

## That's it

When you're done with all 5 steps, you should have:

- Claude Desktop installed and signed in
- Logged-in browser tabs for Gmail, Drive, Notion, Slack, Airtable
- An Airtable Personal Access Token saved in your password manager
- A filled-in "My Role Project" Notion page with every section complete, especially section 6
- The handbook Notion page open in a browser tab

Show up to the Zoom call with all of that ready and you'll leave the hour with a working Claude OS. Miss the prep and you'll leave with homework for the weekend.

If anything breaks during prep, post in #claude-os (or wherever — [channel name]) and I'll help you unstick it before the call.

See you [day] at [time].

— Albert
