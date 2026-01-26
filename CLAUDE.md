# CLAUDE.md

This is an **agentic development planning template**. Use it to transform any app idea into a structured plan ready for AI-assisted development.

## What This Template Does

Given an app description, this template generates:
- Architecture and technical decisions
- Phased development plan with user stories
- Task backlog organized by phase
- Skills (domain-specific knowledge) for the AI agent
- UI/UX design specs
- Progress tracking

The output is a fully planned project that an AI agent (Claude Code) can build iteratively.

## Template Structure

```
template/
├── CLAUDE.md              # (You are here) Meta instructions
├── template-CLAUDE.md     # Template for project system prompt
├── TASKS.md               # Template for task tracker
├── docs/
│   ├── PRD.md             # Template for product requirements
│   ├── design.md          # Template for UI design specs
│   └── development-progress.yaml  # Template for phase tracking
├── prompts/
│   └── phase-1.md         # Template for Ralph Loop prompts
└── .claude/
    ├── settings.json      # Hooks configuration
    ├── hooks/             # Session/prompt hooks
    └── skills/
        └── create-skill/  # Guide for creating new skills
```

## Placeholder Syntax

All template files use `{{PLACEHOLDER}}` syntax. Replace these with actual values:

```
{{APP_NAME}}           → "TaskFlow"
{{APP_DESCRIPTION}}    → "A project management app for remote teams"
{{TECH_STACK_LIST}}    → "- Next.js 14\n- Prisma + PostgreSQL\n- Clerk Auth"
```

Placeholders are UPPERCASE with underscores. Comments (`<!-- -->`) provide examples.

## How to Use This Template

### Step 1: Gather App Requirements

Start with a description of the app. Ask clarifying questions to understand:
- **Problem**: What problem does this solve?
- **Users**: Who uses it? What are their roles?
- **Core Features**: What can users do? (Prioritize: must/should/could)
- **Auth**: Login needed? Methods? Roles/permissions?
- **Data**: What data is stored? Real-time needs?
- **Integrations**: External APIs, payments, email, etc.
- **Tech Preferences**: Framework, database, hosting constraints

### Step 2: Fill In Templates

For the new app, replace placeholders in each file:

1. **template-CLAUDE.md** → rename to **CLAUDE.md**
   - `{{APP_DESCRIPTION_ONE_LINE}}` - One sentence summary
   - `{{TECH_STACK_LIST}}` - Bullet list of technologies
   - `{{COMMANDS}}` - npm/yarn commands
   - `{{PHASES_TABLE}}` - Development phases
   - `{{SKILLS_LIST}}` - Skills to create
   - `{{ENV_VARS}}` - Environment variables

2. **docs/PRD.md**
   - `{{APP_NAME}}`, `{{APP_DESCRIPTION}}`
   - `{{TARGET_USERS}}`, `{{VALUE_PROPOSITION}}`
   - `{{GOAL_N}}` - Project goals
   - User stories with `{{USER_STORY_TITLE}}`, `{{ACTION}}`, `{{BENEFIT}}`
   - `{{CRITERION_N}}` - Acceptance criteria
   - `{{DATA_SCHEMA}}` - TypeScript interfaces

3. **docs/design.md**
   - `{{USER_FLOW_DIAGRAM}}` - Page flow
   - `{{PAGE_N_NAME}}`, `{{ASCII_WIREFRAME}}` - Page layouts
   - Component hierarchy
   - Color tokens and styling approach

4. **docs/development-progress.yaml**
   - `{{PHASE_N_NAME}}`, `{{PHASE_N_DESCRIPTION}}`
   - `{{DELIVERABLE_N}}` - Key outputs per phase
   - `{{CRITERION_N}}` - Completion criteria

5. **TASKS.md**
   - `{{APP_NAME}}`
   - `{{PHASE_N_NAME}}` - Phase headings
   - `{{TASK}}` - Individual tasks

6. **prompts/phase-1.md** (copy for each phase)
   - `{{N}}` - Phase number
   - `{{PHASE_NAME}}` - Phase name
   - `{{USER_STORIES}}` - User story IDs
   - `{{RELEVANT_SKILLS}}` - Skills for this phase

7. **.claude/skills/** - Create skills as needed
   - Use `/create-skill` or copy from `create-skill/SKILL.md` template

### Step 3: Validate the Plan

Before finalizing:
- [ ] All user stories have acceptance criteria
- [ ] Phases are ordered by dependency
- [ ] TASKS.md aligns with PRD user stories
- [ ] Skills cover all technical domains
- [ ] Design covers all pages in user flow
- [ ] Progress tracker matches phases

## File Purposes

| File | Purpose | When Updated |
|------|---------|--------------|
| `CLAUDE.md` | Agent system prompt | Once at start |
| `TASKS.md` | Track work | Every task start/complete |
| `docs/PRD.md` | Requirements source of truth | When requirements change |
| `docs/design.md` | UI reference | When UI changes |
| `docs/development-progress.yaml` | Phase status | Phase transitions |
| `prompts/phase-N.md` | Ralph Loop prompts | Once per phase |
| `.claude/skills/` | Domain knowledge | As domains added |

## Development Workflow (Ralph Loop)

Each phase runs as a loop:

1. **Read**: PRD acceptance criteria, relevant skills, design specs
2. **Build**: Implement feature
3. **Test**: Use agent-browser for E2E testing
4. **Commit**: Only if tests pass
5. **Repeat**: Until phase complete

Phase completion:
- Check off `[x]` in PRD acceptance criteria
- Move tasks to Complete in TASKS.md
- Update `development-progress.yaml`

## Boundaries

**Always:**
- Keep documents concise (sacrifice grammar for brevity)
- Use checkboxes for acceptance criteria
- Organize tasks by phase
- Create skills for each technical domain

**Never:**
- Generate code in planning phase
- Skip acceptance criteria
- Mix phases in tasks
- Create skills for non-technical domains
