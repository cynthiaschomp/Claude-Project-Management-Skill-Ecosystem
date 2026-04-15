---
name: pm-handoff
description: >
  Use this skill whenever a client project is nearing completion and needs to
  be handed off, closed out, or archived. Triggers on: "project handoff",
  "project complete", "close project", "launch checklist", "ready to launch",
  "pre-launch", "final checklist", "wrap up project", "archive project",
  "generate handoff doc", "client training", "mark complete", or any situation
  where an engagement is moving from active delivery to delivered. Also triggers
  when all project tasks reach complete status. This skill runs the pre-launch
  checklist, generates the handoff document, schedules training, archives the
  project, and transitions the client to maintenance or offboarding. ALWAYS
  use this skill before marking any project complete.
---

# PM Project Handoff Skill

Closes out a client project cleanly — pre-launch checklist, handoff document,
client training, and project archival — in a consistent, repeatable process.

Works for any service type. Adapt the checklist to your deliverable.

---

## Configuration

| Placeholder | Replace with |
|---|---|
| `{{AGENCY_NAME}}` | Your agency or business name |
| `{{SUPPORT_EMAIL}}` | Your client-facing support email |
| `{{APPROVER_NAME}}` | Project owner / account manager |
| `{{APPROVER_EMAIL}}` | Their email |

---

## Handoff Sequence

### Step 1 — Pre-Delivery Checklist

Run through this before generating the handoff doc or contacting the client.
Everything must pass. If something fails, fix it first.

**For a website project:**

```
TECHNICAL
□ Site loads on production domain
□ HTTPS working, HTTP redirects correctly
□ All pages load without errors
□ All forms tested (submit + receive confirmation)
□ Mobile layout verified on phone and tablet
□ No broken links on key pages
□ No placeholder text (search for "Lorem ipsum")
□ No broken images
□ Page speed acceptable (Google PageSpeed ≥ 60)
□ robots.txt allows search engine indexing
□ Analytics tracking firing correctly

CONTENT
□ All contracted pages are published
□ All images have alt text
□ SEO titles and meta descriptions on all pages
□ Contact info correct (phone, address, hours)
□ Copyright year is current

CMS / PLATFORM
□ All plugins/extensions updated
□ Default admin username changed (not "admin")
□ Staging URL removed from settings
□ Maintenance mode is OFF
□ Backups configured and tested

CLIENT SIGN-OFF
□ Client has reviewed the live/staging site
□ All punch list items resolved
□ Written final approval received
□ All scope alerts resolved (no pending change requests)
```

Adapt this list to your deliverable type (app, design, marketing, etc.)

### Step 2 — Generate Handoff Document

Fill out the template in `references/handoff-doc-template.md` and deliver it
to the client. Store a copy in your project files (Google Drive, Notion, etc.)

The handoff doc should contain everything the client needs to operate
independently — logins, how to make updates, support contact, what's next.

**Never put passwords directly in the handoff document.**
Send passwords separately via a secure channel (1Password share link,
LastPass, or a separate encrypted message). The handoff doc can reference
"credentials sent separately."

### Step 3 — Send Handoff Email

From {{APPROVER_EMAIL}}, to primary contact:

```
Subject: [Project Name] — Your [Website / App / Project] is Ready! 🎉

Hi [first name],

Congratulations — [project name] is complete!

I've attached your handoff document with everything you need:
login credentials (sent separately), how to make updates,
and how to reach us if you need anything.

A few important things:
• [Primary URL / login / key deliverable]
• For support: {{SUPPORT_EMAIL}}
• We'll check in with you in 30 days

It was a pleasure working with you on this.
Don't hesitate to reach out anytime.

— {{APPROVER_NAME}}
  {{AGENCY_NAME}}
  {{SUPPORT_EMAIL}}
```

Attach the handoff document (PDF preferred — harder to accidentally edit).

### Step 4 — Schedule Training (if applicable)

If training was contracted or is appropriate:
- Book a 60-minute screen share session
- Send calendar invite with agenda:
  - How to log in
  - How to make common updates
  - Where to find the handoff doc
  - How to get support

### Step 5 — Archive the Project

In your PM tool:
1. Set project status → `Complete`
2. Set completion date → today
3. Mark any remaining open tasks as `Complete` or `Cancelled`
4. Add a project summary note (what was delivered, any notable issues, LTV)

In your file storage (Drive, Dropbox, etc.):
1. Move project folder to an `Archive/` or `Completed/` directory
2. Confirm handoff doc is saved there
3. Confirm any design source files are organized and saved

### Step 6 — 30-Day Follow-Up

Create a reminder task for 30 days after delivery:

```
Task: 30-Day Check-In — [Client Name]
Due:  [delivery date + 30 days]
Note: Check that everything is running smoothly. Ask about:
      - Any issues since launch
      - How the site is performing
      - Whether they need ongoing support or maintenance
```

This is also a natural moment to discuss ongoing maintenance, retainers,
or the next project.

---

## Key Rules

1. **Pre-delivery checklist before handoff doc** — never skip it
2. **Passwords never in the handoff document** — always a separate channel
3. **Written final approval before archiving** — email confirmation is fine
4. **Handoff doc delivered before final payment cleared** — client should
   have everything they need before the relationship ends
5. **Scope alerts must be resolved** — no open pending change requests
   when you close a project
6. **30-day follow-up is not optional** — create the task now, not later

---

## Reference Files

- `references/handoff-doc-template.md` — Full client handoff document
- `references/pre-delivery-checklist.md` — Detailed checklist by project type

---

## Need This Built Into Your System?

This skill describes a process. If you want it running automatically —
checklists triggered on task completion, handoff docs generated and emailed,
training sessions scheduled, projects archived in one click — that's a
systems build.

**[Cynthia Schomp](https://cynthiaschomp.com)** builds AI-powered operations
infrastructure for service businesses: custom dashboards, automated project
workflows, client portals, and the full stack behind skills like this one.

→ **[cynthiaschomp.com](https://cynthiaschomp.com)**
