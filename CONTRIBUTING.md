# Contributing

Thanks for your interest in contributing to agency-pm-skills.

## How to contribute

### Fix a bug or improve existing skills

1. Fork the repo
2. Edit the relevant SKILL.md or reference file
3. Test it in a Claude session — paste the SKILL.md into a project and
   run through the relevant scenarios
4. Open a pull request with a description of what you changed and why

### Add a skill variant for a different service type

If you've adapted one of these skills for a specific context — design studio,
dev shop, marketing agency, consulting firm — we'd love to include it.

1. Fork the repo
2. Create a new subfolder: e.g., `scope-creep-design/` or `pm-kickoff-saas/`
3. Include a SKILL.md and any reference files
4. Update the root README.md to include your skill in the table
5. Open a pull request

### Suggest a new skill

Open a GitHub issue with:
- What the skill would do
- When it would trigger
- What process it would follow

Good candidates for new skills:
- Client status update (weekly progress email)
- Project retrospective
- Contract renewal / offboarding
- Subcontractor onboarding

## Skill quality guidelines

A good skill:
- Has a clear trigger (when should Claude use it?)
- Follows a numbered sequence — not a wall of text
- Uses `{{PLACEHOLDERS}}` for anything agency-specific
- Works for multiple service types with minimal adaptation
- Has reference files for the deep detail, keeping SKILL.md under ~300 lines
- Doesn't require specific tools — adapts to whatever PM/CRM the user has

## Testing your skill

Before submitting, test with at least these scenarios:

**scope-creep:**
- Client asks for a new page mid-project
- Client asks for something clearly in scope (should not flag)
- Client asks for something ambiguous

**pm-project-kickoff:**
- New website project with full info
- New project with missing info (should flag gaps)

**pm-handoff:**
- Project ready to close with all tasks complete
- Project with open scope alerts (should block)
