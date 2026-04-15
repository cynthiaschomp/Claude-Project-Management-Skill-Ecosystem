# Agency PM Skills for Claude

A set of Claude skills for service agencies — web studios, dev shops, design
firms, consultancies — to manage client projects without scope creep eating
into profit.

Built and used in production by [Cynthia Schomp](https://cynthiaschomp.com), a web design agency
managing 100+ client websites.

---

## What's Included

| Skill | What it does |
|---|---|
| [scope-creep](./scope-creep/) | Detect scope creep, generate PRDs, create change orders, manage approval workflow |
| [pm-project-kickoff](./pm-project-kickoff/) | Scaffold new projects: phases, tasks, scope_doc, welcome email |
| [pm-handoff](./pm-handoff/) | Pre-launch checklist, handoff document, client training, archival |

---

## The Problem These Solve

Service agencies constantly lose money to three things:

1. **Scope creep** — clients ask for more, teams do it without charging, margins collapse
2. **Inconsistent onboarding** — each project starts differently, things get missed
3. **Sloppy handoffs** — clients don't have what they need, support tickets pile up

These skills give Claude the context and process to catch scope creep automatically,
kick off projects consistently, and close them cleanly every time.

---

## Quick Start

### 1. Install a skill

In [Claude.ai](https://claude.ai):
1. Go to **Settings → Skills** (or your project's knowledge section)
2. Upload the `SKILL.md` file from the skill folder
3. That's it — Claude will use the skill when relevant

Or install from the `.skill` package file if you have the Claude Skills CLI.

### 2. Configure placeholders

Each skill has a `## Configuration` section at the top with placeholders like
`{{AGENCY_NAME}}` and `{{HOURLY_RATE}}`. Either:

- Edit the SKILL.md files directly before uploading
- Or tell Claude your values once and it will remember them for the session

### 3. Use it

Just talk to Claude normally. The skills trigger automatically on relevant phrases:

> *"Our client is asking us to add a booking system — that wasn't in the proposal"*

Claude will run the scope-creep skill: check the scope_doc, flag it, generate
a PRD, and draft the client response.

> *"We just got a signed contract from a new client, let's set up the project"*

Claude will run the pm-project-kickoff skill: scaffold the phases, build the
scope_doc, and draft the welcome email.

---

## How Skills Work

A Claude skill is a Markdown file that gives Claude structured knowledge about
a process. When you upload it to a Claude project, Claude reads it and follows
the process automatically — no prompting required.

Skills use a three-layer system:
- **SKILL.md** — the main instructions Claude loads when the skill triggers
- **references/** — deeper documentation Claude reads when needed
- **Placeholders** — `{{LIKE_THIS}}` — swap for your own values

---

## Folder Structure

```
agency-pm-skills/
│
├── README.md                    ← you are here
│
├── scope-creep/
│   ├── SKILL.md                 ← main skill file
│   └── references/
│       ├── scope-detection-rules.md
│       ├── prd-template.md
│       ├── change-order-templates.md
│       └── scope-doc-template.md
│
├── pm-project-kickoff/
│   ├── SKILL.md
│   └── references/
│       ├── project-task-templates.md
│       ├── intake-questionnaire.md
│       └── scope-doc-template.md
│
└── pm-handoff/
    ├── SKILL.md
    └── references/
        └── handoff-doc-template.md
```

---

## Customizing for Your Agency

Every skill is designed to be adapted. Common customizations:

**scope-creep:**
- Add your specific feature types to `scope-detection-rules.md`
- Replace the email templates with your voice in `change-order-templates.md`
- Adjust the PRD sections you need in `prd-template.md`

**pm-project-kickoff:**
- Replace the 7-phase website structure with your service phases
- Add your intake questions to `intake-questionnaire.md`
- Adjust due date calculations to your actual workflow speed

**pm-handoff:**
- Replace the WordPress-specific checklist with your platform
- Adjust the handoff document to include your support terms

---

## The scope_doc Pattern

The single most important concept across all three skills is the **scope_doc** —
a plain-text document written at project kickoff that defines exactly what was
contracted. Every scope detection check runs against it.

A good scope_doc looks like:

```
Project: Acme Website 2026
Contracted: 5-page website (Home, About, Services, Portfolio, Contact)
            WordPress with Elementor
            Contact form
            Basic SEO (titles, meta, alt text)
            2 design revision rounds
NOT included: Blog, e-commerce, booking, extra pages, extra revision rounds
Revisions: 2 rounds
Assumptions: Client provides all written content and brand assets
```

If you write one of these for every project, scope creep becomes
detectable and documentable instead of invisible and free.

---

## Contributing

Pull requests welcome. If you've adapted these skills for a specific service
type (design, development, marketing, consulting) and want to share your
version, open a PR with your adapted files in a subfolder.

Issues and feedback: open a GitHub issue.

---

## License

MIT — use freely, adapt for your business, no attribution required.

---

---

## Want the Full System Built for Your Agency?

These skills describe the process. The full version runs automatically —
emails classified, scope checked, PRDs generated, tickets created, status
updates sent, projects closed — without you thinking about it.

**Cynthia Schomp** builds AI-powered operations infrastructure for service
businesses: custom dashboards, Gmail and PM integrations, automated workflows,
and production systems like the one these skills were built from.

**→ [cynthiaschomp.com](https://cynthiaschomp.com)**

---

Built by [Cynthia Schomp](https://cynthiaschomp.com) · Powered by [Claude](https://claude.ai)
