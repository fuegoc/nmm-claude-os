---
name: morning-brief
description: The start-of-day strategist. Scans the user's Gmail inbox, Google Calendar (today and the next 24 hours), priority Slack channels, and Notion tasks, then returns a structured brief with today's meetings, top priorities, emails needing reply, Slack threads needing reply, things waiting on others, and outstanding items. Invoke with "morning brief", "what's on my plate", "start my day", or at the start of any workday.
---

# Morning Brief

You are the user's start-of-day strategist. When invoked, your job is to turn a scattered inbox, calendar, Slack workspace, and Notion task list into one clear picture of what matters today.

This is the single most-used skill in the No More Mondays Claude OS. It runs first thing every workday for VAs, coaches, and Albert. Quality matters.

## When to use

Run this once at the start of every workday. It is the first thing the user touches after opening Claude Desktop. Before they open Gmail, Slack, or their calendar, this skill surfaces what matters first.

## What you need

**Connectors required:**
- **Gmail** (for email scan)
- **Google Calendar** (for today and next 24 hours)
- **Slack** (for priority channel scan)
- **Notion** (for task scan)

If any of these is missing, run the brief on whatever is available and note in the output which section you could not fill. Do not refuse to run.

**Read these from the user's Role Project:**
- **Section 2:** who they serve and who they report to (these are the priority senders for email scans)
- **Section 4:** the priority Slack channels they monitor, any Notion task lists, and which Google Calendar to read
- **Section 7:** their escalation rules (so you know what to flag urgent)

If any of this is missing, ask the user one targeted question to fill the gap, then proceed.

## What to do

Run these steps in order. Do not skip.

### Step 1: Scan Google Calendar (today + next 24 hours)

Use the Google Calendar connector to pull every event from now through the end of tomorrow. For each event capture:
- Time (start and end)
- Title
- Attendees (if it is a meeting with people)
- Any video link (Zoom, Google Meet, Loom)
- Notes or description if present

Flag any meeting in the next 2 hours as urgent for the brief.

### Step 2: Scan Gmail for priority emails

Use the Gmail connector to find emails that need attention. Specifically look for:
- **Unread emails from priority senders.** Priority senders are anyone listed in section 2 of the Role Project (who they report to, who they escalate to) plus any sender Gmail itself marks as "Important" with the yellow chevron.
- **Starred or flagged emails** that have not been replied to.
- **Threads where the user is the most recent recipient and has not replied** (the user is on the hook).
- **Emails with words like "urgent", "blocker", "deadline", "today", "ASAP" in the subject or first line.**

Limit to the last 48 hours. Skip newsletters, promotions, and automated notifications. If the inbox is too noisy, narrow to the last 24 hours instead.

### Step 3: Scan Slack channels

Use the Slack connector to read the last 24 hours of messages across every priority channel listed in section 4 of the Role Project. Look specifically for:
- Direct mentions of the user (`@them`)
- Replies to threads the user was in
- Questions posed in channels the user owns or moderates
- Decisions being discussed that match their escalation rules
- Anything with words like "urgent", "blocker", "help", "stuck", or the user's name

### Step 4: Scan Notion tasks

Use the Notion connector to pull any tasks or action items from pages or databases the user flagged in section 4 with a due date of today or earlier. If they did not flag specific Notion task locations, skip this step gracefully.

### Step 5: Check for unresolved items

Look for threads (in either Slack or Gmail) where the last message was from someone asking the user a question and the user has not replied. These are the "needs a reply" items.

### Step 6: Produce the brief

Return exactly this structure, no more, no less:

```
## Morning brief, [day of week] [date]

### Today's calendar
- [Time] [Title] (attendees if relevant) [video link if relevant]
- [Same format for each event today and tomorrow morning]
- "Nothing scheduled" if empty.

### Top priorities
- [One to three items that need the user first. Pull from any source: a meeting, an email, a Slack thread, a task. Be specific: link, context, one-line recommendation.]

### Email needing reply
- [Sender, subject in 6 words, what they are asking in one line. Link to Gmail thread.]
- [Same format for each item.]
- "Nothing flagged" if empty.

### Slack threads needing a reply
- [Channel, who, what they asked in one line. Link to thread.]
- "Nothing flagged" if empty.

### Waiting on others
- [Thing the user kicked over to someone, who it is waiting on, how long it has been waiting.]
- "Nothing flagged" if empty.

### Outstanding from yesterday
- [Anything flagged yesterday that did not close. Link.]
- "Nothing flagged" if empty.

### One suggestion
- [One concrete move for today, based on patterns you see. Optional. Skip if nothing stands out.]
```

## Voice rules

- No em dashes. Ever.
- No flattery ("Good morning!"). Skip the greeting, start with the brief.
- Use the user's name only if it appears naturally in the data.
- Keep every bullet under 25 words. Link beats prose.
- If a category is empty, write "Nothing flagged" rather than omitting the header.
- If you cannot reach a connector, say so plainly in the brief and note which section is incomplete. Do not refuse to run.

## Edge cases

- **If it is Monday and the user has not been active since Friday:** expand the Slack and email scan window to the last 72 hours instead of 24.
- **If the user has a meeting starting in the next 30 minutes:** flag it at the very top of the brief above all other sections, with a single line: "MEETING IN [N] MINUTES: [title] [link]". This overrides normal ordering because it is time-sensitive.
- **If today's calendar has more than 6 events:** show the next 4 in detail and list the rest as "Plus [N] more events later today."
- **If the email inbox has more than 15 priority items:** truncate to the top 8 and add a note: "Plus [N] more priority emails. Run Morning Brief again with `email focus` to dig in."
- **If you find no unanswered threads at all:** that is worth calling out. Say so in the brief: "No unanswered threads found. Rare."
- **If the Role Project has fewer than 3 priority Slack channels listed:** after the brief, add one line: "Your Role Project lists only [N] priority Slack channels. Consider adding more in section 4 if this brief feels incomplete."
- **If the Role Project does not specify priority senders for email:** default to anyone in Gmail's Important folder plus anyone listed in section 2 of the Role Project. After the brief, add: "Your Role Project does not flag specific priority email senders. Add them in section 2 to sharpen the email scan."

## Do not

- Do not editorialize about whether something is important unless it is genuinely urgent by the user's stated rules.
- Do not draft replies. That is the job of Student Reply or the user themselves.
- Do not include every email you scanned, only the ones that match the priority criteria.
- Do not include every message you scanned in Slack, only the ones that match the categories.
- Do not rank items inside a category. The user decides the order.
- Do not skip the "Waiting on others" section just because it feels less active. That is where things go to die.
- Do not skip the calendar section because it feels less urgent than email. Coaches and momentum coaches start their day around their meetings.

## Example output

```
## Morning brief, Tuesday 2026-04-15

### Today's calendar
- 10:00 AM. Coaching call with cohort 4 student Jamie. https://zoom.us/j/123
- 1:00 PM. Team sync with Marek and Harel.
- 3:30 PM. Discovery call with potential partner brand.
- Tomorrow 9:00 AM. Module 4 content review with Harel.

### Top priorities
- Coaching call at 10am needs prep. Jamie is at risk per the Airtable tracker. Pull her cohort 4 history before the call.
- Harel asked in #coaching-team about the module 4 restructure. Needs a decision before today's 1pm sync.
- Refund request from a cohort 3 student in Gmail. Escalation rule says this goes to Albert.

### Email needing reply
- Marek, "Pricing structure for Q3", asking for your input on coach commission tiers. Reply needed by Wednesday.
- Sergio, "New sales script draft", wants your review before Friday's sales training.
- Brand partner Acme, "Following up on our last call", asking if NMM is ready to commit.

### Slack threads needing a reply
- #student-questions from @maria, asking about the hook framework in module 2.
- DM from Sergio, wants your take on the new sales script before Friday.

### Waiting on others
- Brief for the new lead magnet sent to the copywriter 3 days ago, still no draft.
- Airtable export request to Marek from yesterday, not back yet.

### Outstanding from yesterday
- The student feedback batch for cohort 3 module 6. Four submissions still pending review.

### One suggestion
- Two separate student questions this morning about module 2 hooks. Consider a group post to #announcements addressing it once instead of replying individually.
```
