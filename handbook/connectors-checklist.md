# Connectors Checklist

Your Role Project knows who you are. Connectors give Claude hands to reach the tools you actually use. Install all five in order. After each one, run the test query to confirm it works before moving to the next. The onboarding skill walks you through this live, but this is your reference to repeat the process later or help a teammate.

A **Connector** is a live link between Claude Desktop and an external tool. Claude can read and, in some cases, write to the tool on your behalf. Every connector asks for your permission during install (an OAuth login or an access token).

---

## Install pattern

Claude Desktop → **Customize → Connectors → + → Browse connectors** → pick the connector → click Connect → log in when prompted → grant permissions → return to Claude Desktop.

For Airtable you will use **+ → Add custom connector** instead, because Airtable is installed by URL and token.

---

## The five connectors

### 1. Gmail
- [ ] Installed
- **Path:** Customize → Connectors → + → Browse → Gmail → Connect → sign in.
- **Test query:** *"How many unread emails are in my inbox right now?"*
- **Expected result:** Claude returns a number and optionally lists the latest unread senders.

### 2. Google Drive
- [ ] Installed
- **Path:** Customize → Connectors → + → Browse → Google Drive → Connect → sign in.
- **Test query:** *"List the 5 most recently edited Google Docs in my Drive."*
- **Expected result:** Claude returns a list with titles and edit dates.

### 3. Notion
- [ ] Installed
- **Path:** Customize → Connectors → + → Browse → Notion → Connect → sign in → select the workspace you want to expose (pick the No More Mondays workspace).
- **Test query:** *"Search my Notion workspace for 'FAQ' and show me the top 3 results."*
- **Expected result:** Claude returns titles with direct links.

### 4. Slack
- [ ] Installed
- **Path:** Customize → Connectors → + → Browse → Slack → Connect → pick your workspace → grant permissions.
- **Test query:** *"What are the 3 most recent messages in #general?"*
- **Expected result:** Claude returns the messages with senders and timestamps.
- **Note:** Slack is for internal team use only. Student support happens in Discord, which is handled via copy-paste, not a connector.

### 5. Airtable (custom connector — the trickiest one)
- [ ] Personal Access Token created in Airtable Builder Hub
- [ ] Connector installed

**Step 1: Create your Personal Access Token.** Before you install the connector, go to [airtable.com/create/tokens](https://airtable.com/create/tokens) and create a new token with these exact scopes:

- `data.records:read`
- `data.records:write`
- `schema.bases:read`
- `schema.bases:write`

Give the token access to the bases you want Claude to see (or all bases if you want flexibility). Save the token in your password manager. You will not be able to see it again after you leave the page.

**Step 2: Install the custom connector.**

- **Path:** Customize → Connectors → + → **Add custom connector**.
- **URL to paste:** `https://mcp.airtable.com/mcp`
- **Token:** paste your Personal Access Token when prompted.
- **Test query:** *"List the Airtable bases I have access to."*
- **Expected result:** Claude returns the names of your bases.

---

## Troubleshooting

- **OAuth loop or "something went wrong"** — usually a stale browser session. Log out of the tool in your browser, log back in, retry the connector install.
- **Airtable "invalid token"** — the PAT likely does not have the right scopes, or it was created for a different Airtable account than the one you are logged into in Claude. Recreate it with the scopes listed above.
- **Notion "no workspace found"** — you did not grant workspace access during OAuth. Reinstall and make sure to pick the workspace when prompted.
- **Connector shows installed but Claude says it cannot see the data** — end the current chat and start a fresh one. New connectors sometimes need a fresh session to register.

If a connector fails and you cannot unblock, mark it incomplete in this checklist, skip to the next one, and return to it after the session. The onboarding skill has "skip for now" branches for exactly this reason.
